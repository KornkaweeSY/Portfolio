<template>
    <div>
        <div id="space-background"></div>
        <!-- <TheExperience /> -->
    </div>
</template>

<script>
import * as THREE from 'three';

export default {
    mounted() {
        this.initThreeJS();
    },
    methods: {
        initThreeJS() {
            // Scene setup
            const scene = new THREE.Scene();
            const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            const renderer = new THREE.WebGLRenderer();
            
            renderer.setSize(window.innerWidth, window.innerHeight);
            document.getElementById('space-background').appendChild(renderer.domElement);
            
            // Create stars
            const starsGeometry = new THREE.BufferGeometry();
            const starsMaterial = new THREE.PointsMaterial({
                color: 0xFFFFFF,
                size: 0.1
            });

            const starsVertices = [];
            for(let i = 0; i < 10000; i++) {
                const x = (Math.random() - 0.5) * 2000;
                const y = (Math.random() - 0.5) * 2000;
                const z = (Math.random() - 0.5) * 2000;
                starsVertices.push(x, y, z);
            }

            starsGeometry.setAttribute('position', new THREE.Float32BufferAttribute(starsVertices, 3));
            const stars = new THREE.Points(starsGeometry, starsMaterial);
            scene.add(stars);

            // Create Milky Way galaxy
            const textureLoader = new THREE.TextureLoader();
            const galaxyTexture = textureLoader.load('/images/Milky_way_top.png', (texture) => {
                texture.encoding = THREE.sRGBEncoding;
            });

            const galaxyGeometry = new THREE.PlaneGeometry(30, 30);
            const galaxyMaterial = new THREE.MeshBasicMaterial({
                map: galaxyTexture,
                transparent: true,
                opacity: 0.8,
                side: THREE.DoubleSide,
                blending: THREE.AdditiveBlending,
            });

            const galaxy = new THREE.Mesh(galaxyGeometry, galaxyMaterial);
            galaxy.rotation.x = Math.PI / 10; // Tilt the galaxy
            scene.add(galaxy);

            camera.position.z = 20;

            // Animation
            const animate = () => {
                requestAnimationFrame(animate);
                stars.rotation.y += 0.0009;
                
                // Rotate galaxy
                galaxy.rotation.z += 0.0005;
                
                // Add subtle floating motion to galaxy
                galaxy.position.y = Math.sin(Date.now() * 0.0005) * 0.2;
                
                renderer.render(scene, camera);
            };

            animate();

            // Handle window resize
            window.addEventListener('resize', () => {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            });
        }
    },
    beforeDestroy() {
        // Cleanup
        window.removeEventListener('resize');
    }
}
</script>

<style lang="scss" scoped>
#space-background {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
}
</style>