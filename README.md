<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wedding Services Finder</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            background-color: #fffaf0;
            font-family: 'Playfair Display', serif;
        }
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.8s ease-out;
        }
        .fade-in.show {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const elements = document.querySelectorAll(".fade-in");
            const observer = new IntersectionObserver(entries => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("show");
                    }
                });
            });
            elements.forEach(el => observer.observe(el));
        });
    </script>
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="bg-white shadow-md fixed w-full top-0 z-50 flex justify-between px-8 py-4 items-center">
        <h1 class="text-3xl font-bold text-pink-600">✨ Wedding Bliss ✨</h1>
        <ul class="hidden md:flex space-x-8 text-gray-700 font-semibold">
            <li><a href="#home" class="hover:text-pink-600">Home</a></li>
            <li><a href="#services" class="hover:text-pink-600">Services</a></li>
            <li><a href="#contact" class="hover:text-pink-600">Contact</a></li>
            <li><a href="#login" class="hover:text-pink-600">Sign In</a></li>
        </ul>
    </nav>

    <!-- Hero Section with Social Media Links -->
    <header id="home" class="relative h-screen flex flex-col items-center justify-center bg-cover bg-center text-center text-white" style="background-image: url('https://source.unsplash.com/1600x900/?wedding,elegant');">
        <div class="bg-black bg-opacity-50 absolute inset-0"></div>
        <div class="z-10 fade-in">
            <h1 class="text-6xl font-bold">Find the Perfect Wedding Services</h1>
            <p class="mt-4 text-lg">Elegant bridal stylists, top-tier performers, and dreamy decorations.</p>
            <button onclick="document.querySelector('#services').scrollIntoView({ behavior: 'smooth' })" class="start-planning mt-6 px-8 py-3 bg-gradient-to-r from-pink-500 to-red-500 text-white rounded-full text-lg font-semibold hover:scale-105 transition">Start Planning</button>
        </div>
    </header>

    <!-- Service Selection Section -->
    <section id="services" class="h-screen flex flex-col justify-center items-center text-center">
        <h2 class="text-4xl font-bold text-gray-800">Choose Your Wedding Service</h2>
        <div class="mt-6 flex items-center space-x-4">
            <select class="p-3 border rounded-md">
                <option>Select Category</option>
                <option>Bridal Hairstylists (Hajjema)</option>
                <option>Wedding Performers (Salat Afrah)</option>
                <option>Photographers</option>
                <option>Decor Services</option>
            </select>
            <button class="px-6 py-3 bg-pink-500 text-white rounded-md hover:bg-pink-700 transition">Find</button>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 bg-gradient-to-r from-pink-200 to-pink-500 text-center fade-in">
        <h2 class="text-4xl font-bold text-white">Contact Us</h2>
        <p class="mt-4 text-white">Have questions? Let’s talk!</p>
        <div class="mt-6 max-w-lg mx-auto">
            <input type="text" placeholder="Your Name" class="w-full p-4 border border-gray-300 rounded-md mb-4">
            <input type="email" placeholder="Your Email" class="w-full p-4 border border-gray-300 rounded-md mb-4">
            <textarea placeholder="Your Message" class="w-full p-4 border border-gray-300 rounded-md mb-4"></textarea>
            <button class="px-6 py-4 bg-white text-pink-600 rounded-md hover:bg-gray-100 transition">Send Message</button>
        </div>
    </section>

    <!-- Login/Signup Section -->
    <section id="login" class="py-20 bg-gray-100 fade-in text-center">
        <h2 class="text-4xl font-bold text-gray-800">Create an Account</h2>
        <p class="mt-4 text-gray-600">Sign up to save your favorite vendors and manage bookings.</p>
        <div class="mt-6 max-w-md mx-auto">
            <input type="text" placeholder="Full Name" class="w-full p-3 border rounded-md mb-4">
            <input type="email" placeholder="Email" class="w-full p-3 border rounded-md mb-4">
            <input type="password" placeholder="Password" class="w-full p-3 border rounded-md mb-4">
            <button class="px-6 py-3 bg-pink-500 text-white rounded-md hover:bg-pink-700 transition">Sign Up</button>
            <p class="mt-4">Already have an account? <a href="#" class="text-pink-600">Sign In</a></p>
        </div>
    </section>
</body>
</html>
