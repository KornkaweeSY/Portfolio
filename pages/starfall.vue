<template>
    <div>
        <div id="starfall-container"></div>
    </div>
</template>

<script>
import * as THREE from 'three';
import { onMounted, onBeforeUnmount } from 'vue';

export default {
    setup() {
        let scene, camera, renderer;
        let shootingStars = [];

        const initThreeJS = () => {
            scene = new THREE.Scene();
            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            renderer = new THREE.WebGLRenderer({ antialias: true });
            
            renderer.setSize(window.innerWidth, window.innerHeight);
            document.getElementById('starfall-container').appendChild(renderer.domElement);
            
            camera.position.z = 50;

            // Create shooting star material
            const shootingStarMaterial = new THREE.MeshBasicMaterial({
                color: 0xffffff,
                transparent: true,
                opacity: 0.8,
            });

            // Function to create a shooting star
            const createShootingStar = () => {
                const length = Math.random() * 3 + 1; // Random length between 1 and 4
                const geometry = new THREE.BoxGeometry(length, 0.1, 0.1);
                const star = new THREE.Mesh(geometry, shootingStarMaterial);

                // Random starting position
                star.position.set(
                    Math.random() * 100 - 50, // x between -50 and 50
                    Math.random() * 30 + 20,  // y between 20 and 50
                    Math.random() * 20 - 10   // z between -10 and 10
                );

                // Random direction (diagonal, downward)
                const speed = Math.random() * 0.3 + 0.2;
                star.userData = {
                    velocity: new THREE.Vector3(
                        (Math.random() - 0.5) * speed,
                        -speed,
                        0
                    ),
                    life: 1.0 // Life counter for fade out
                };

                scene.add(star);
                shootingStars.push(star);
            };

            // Animation loop
            const animate = () => {
                requestAnimationFrame(animate);

                // Update shooting stars
                shootingStars.forEach((star, index) => {
                    star.position.add(star.userData.velocity);
                    star.userData.life -= 0.01;
                    star.material.opacity = star.userData.life;

                    // Remove stars that are out of view or faded out
                    if (star.position.y < -30 || star.userData.life <= 0) {
                        scene.remove(star);
                        shootingStars.splice(index, 1);
                    }
                });

                // Randomly create new shooting stars
                if (Math.random() < 0.03 && shootingStars.length < 20) {
                    createShootingStar();
                }

                renderer.render(scene, camera);
            };

            // Start animation
            animate();

            // Handle window resize
            const handleResize = () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            };

            window.addEventListener('resize', handleResize);

            // Return cleanup function
            return () => {
                window.removeEventListener('resize', handleResize);
                shootingStars.forEach(star => scene.remove(star));
                renderer.dispose();
            };
        };

        onMounted(() => {
            const cleanup = initThreeJS();
            onBeforeUnmount(cleanup);
        });

        return {};
    }
}
</script>

<style lang="scss" scoped>
#starfall-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    background: linear-gradient(to bottom, #0a0a2a, #1a1a3a);
}
</style>