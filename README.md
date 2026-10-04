<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Creative Digital Services | Portfolio</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Poppins', 'sans-serif'],
                    },
                    colors: {
                        dark: '#0a0a0f',
                        card: '#13131f',
                        accent1: '#00f2fe',
                        accent2: '#4facfe',
                        accent3: '#a855f7',
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #0a0a0f;
            color: #ffffff;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0a0a0f;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #00f2fe, #a855f7);
            border-radius: 4px;
        }

        /* Glassmorphism utilities */
        .glass {
            background: rgba(19, 19, 31, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .glass-card:hover {
            transform: translateY(-10px);
            border-color: rgba(168, 85, 247, 0.5);
            box-shadow: 0 10px 30px -10px rgba(168, 85, 247, 0.4), inset 0 0 20px rgba(0, 242, 254, 0.1);
        }

        /* Text Gradients */
        .text-gradient {
            background: linear-gradient(135deg, #00f2fe 0%, #a855f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Glow effects */
        .glow-button {
            position: relative;
            z-index: 1;
        }
        .glow-button::before {
            content: '';
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            background: linear-gradient(135deg, #00f2fe, #a855f7);
            z-index: -1;
            border-radius: inherit;
            transition: opacity 0.3s ease;
            opacity: 0;
            filter: blur(15px);
        }
        .glow-button:hover::before {
            opacity: 0.7;
        }

        /* Input styling overrides for dark mode select */
        select option {
            background-color: #13131f;
            color: white;
        }
    </style>
</head>
<body class="antialiased selection:bg-accent3 selection:text-white">

    <nav class="fixed w-full z-50 glass transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 flex items-center cursor-pointer" onclick="window.scrollTo(0,0)">
                    <span class="text-2xl font-bold tracking-tighter">VFX<span class="text-gradient">Pro</span></span>
                </div>
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#home" class="text-gray-300 hover:text-white transition-colors text-sm font-medium">Home</a>
                    <a href="#services" class="text-gray-300 hover:text-white transition-colors text-sm font-medium">Services</a>
                    <a href="#contact" class="px-5 py-2.5 rounded-full bg-white/10 hover:bg-white/20 border border-white/10 transition-all text-sm font-medium">Get in Touch</a>
                </div>
                <!-- Mobile menu button (visual only for simplicity) -->
                <div class="md:hidden flex items-center">
                    <button class="text-gray-300 hover:text-white p-2">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <section id="home" class="relative min-h-screen flex items-center justify-center pt-20 overflow-hidden">
        <!-- Background decorative elements -->
        <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-accent3/20 rounded-full blur-[100px] pointer-events-none"></div>
        <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-accent1/20 rounded-full blur-[100px] pointer-events-none"></div>
        
        <div class="relative z-10 text-center px-4 max-w-4xl mx-auto">
            <div class="inline-block mb-4 px-4 py-1.5 rounded-full border border-accent1/30 bg-accent1/10 text-accent1 text-xs font-semibold tracking-wide uppercase">
                Available for Freelance Work
            </div>
            <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight mb-6 leading-tight">
                Elevate Your Content with <br class="hidden md:block" />
                <span class="text-gradient">Premium Visuals</span>
            </h1>
            <p class="mt-4 text-xl text-gray-400 mb-10 max-w-2xl mx-auto font-light">
                Professional video editing, stunning graphic design, and captivating presentations tailored to make your brand stand out in the digital landscape.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#contact" class="glow-button relative px-8 py-4 bg-gradient-to-r from-accent1 to-accent3 rounded-full text-white font-semibold shadow-lg hover:shadow-accent3/50 transition-all duration-300 transform hover:-translate-y-1">
                    Hire Me Today
                </a>
                <a href="#services" class="px-8 py-4 bg-card rounded-full text-white font-semibold border border-white/10 hover:bg-white/5 transition-all duration-300">
                    Explore Services
                </a>
            </div>
        </div>
    </section>

    <section id="services" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-5xl font-bold mb-4">My <span class="text-gradient">Services</span></h2>
                <p class="text-gray-400 max-w-2xl mx-auto">Delivering high-quality digital assets across multiple disciplines to meet your exact project requirements.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                
                <!-- Service 1: Video Editing -->
                <div class="glass-card rounded-2xl p-8 group cursor-pointer">
                    <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-accent1/20 to-accent3/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-7 h-7 text-accent1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 10l4.553-2.276A1 1 0 0121 8.618v6.764a1 1 0 01-1.447.894L15 14M5 18h8a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v8a2 2 0 002 2z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Video Editing</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Cinematic cuts, color grading, motion graphics, and engaging transitions for YouTube, TikTok, and corporate videos.</p>
                </div>

                <!-- Service 2: Photo Editing -->
                <div class="glass-card rounded-2xl p-8 group cursor-pointer">
                    <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-accent1/20 to-accent3/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-7 h-7 text-accent3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Photo Editing</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">High-end retouching, background removal, color correction, and creative manipulations for products and portraits.</p>
                </div>

                <!-- Service 3: Poster Making -->
                <div class="glass-card rounded-2xl p-8 group cursor-pointer">
                    <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-accent1/20 to-accent3/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-7 h-7 text-accent1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Poster Design</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Eye-catching digital and print-ready posters for events, marketing campaigns, movies, and social media promotions.</p>
                </div>

                <!-- Service 4: PPT Presentation -->
                <div class="glass-card rounded-2xl p-8 group cursor-pointer">
                    <div class="w-14 h-14 rounded-xl bg-gradient-to-br from-accent1/20 to-accent3/20 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform duration-300">
                        <svg class="w-7 h-7 text-accent3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 12l3-3 3 3 4-4M8 21l4-4 4 4M3 4h18M4 4h16v12a1 1 0 01-1 1H5a1 1 0 01-1-1V4z"></path>
                        </svg>
                    </div>
                    <h3 class="text-xl font-semibold mb-3 text-white">Presentations</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">Modern, sleek, and impactful PowerPoint/Keynote pitch decks and corporate presentations that tell your story.</p>
                </div>

            </div>
        </div>
    </section>

    <section id="contact" class="py-24 relative bg-card/50 border-t border-white/5">
        <div class="absolute top-0 right-0 w-1/2 h-full bg-gradient-to-l from-accent3/5 to-transparent pointer-events-none"></div>
        
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="text-center mb-12">
                <h2 class="text-3xl md:text-5xl font-bold mb-4">Request a <span class="text-gradient">Project</span></h2>
                <p class="text-gray-400">Ready to start? Fill out the form below and I'll get back to you within 24 hours.</p>
            </div>

            <div class="glass-card p-8 md:p-12 rounded-3xl relative overflow-hidden">
                
                <!-- Success Message (Hidden by default) -->
                <div id="success-message" class="hidden absolute inset-0 bg-card z-20 flex flex-col items-center justify-center p-8 text-center rounded-3xl">
                    <div class="w-20 h-20 bg-green-500/20 rounded-full flex items-center justify-center mb-6">
                        <svg class="w-10 h-10 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                        </svg>
                    </div>
                    <h3 class="text-3xl font-bold mb-2">Request Sent!</h3>
                    <p class="text-gray-400 mb-6">Thank you for reaching out. I've received your project details and will review them shortly.</p>
                    <button onclick="resetForm()" class="px-6 py-2 border border-white/20 rounded-full hover:bg-white/10 transition-colors">
                        Send Another Request
                    </button>
                </div>

                <!-- Form -->
                <form id="project-form" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="space-y-2">
                            <label class="text-sm font-medium text-gray-300">Your Name</label>
                            <input type="text" required class="w-full bg-dark/50 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-accent1 focus:ring-1 focus:ring-accent1 transition-colors" placeholder="John Doe">
                        </div>
                        <div class="space-y-2">
                            <label class="text-sm font-medium text-gray-300">Email Address</label>
                            <input type="email" required class="w-full bg-dark/50 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-accent1 focus:ring-1 focus:ring-accent1 transition-colors" placeholder="john@example.com">
                        </div>
                    </div>

                    <div class="space-y-2">
                        <label class="text-sm font-medium text-gray-300">Service Required</label>
                        <select required class="w-full bg-dark/50 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-accent3 focus:ring-1 focus:ring-accent3 transition-colors appearance-none">
                            <option value="" disabled selected>Select a service...</option>
                            <option value="video">Video Editing</option>
                            <option value="photo">Photo Editing</option>
                            <option value="poster">Poster Making</option>
                            <option value="ppt">PPT Presentation</option>
                            <option value="other">Multiple / Other</option>
                        </select>
                    </div>

                    <div class="space-y-2">
                        <label class="text-sm font-medium text-gray-300">Project Details</label>
                        <textarea required rows="4" class="w-full bg-dark/50 border border-white/10 rounded-xl px-4 py-3 text-white focus:outline-none focus:border-accent3 focus:ring-1 focus:ring-accent3 transition-colors resize-none" placeholder="Tell me about your project, timeline, and any specific requirements..."></textarea>
                    </div>

                    <button type="submit" class="w-full glow-button relative px-8 py-4 bg-gradient-to-r from-accent3 to-accent1 rounded-xl text-white font-bold text-lg shadow-lg hover:shadow-accent1/50 transition-all duration-300">
                        Submit Project Request
                    </button>
                </form>
            </div>
        </div>
    </section>

    <footer class="border-t border-white/5 py-8 text-center">
        <p class="text-gray-500 text-sm">
            &copy; <span id="year"></span> VFXPro Portfolio. All rights reserved. Designed for excellence.
        </p>
    </footer>

    <script>
        // Set current year in footer
        document.getElementById('year').textContent = new Date().getFullYear();

        // Navbar blur effect on scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 20) {
                navbar.classList.add('shadow-lg', 'bg-card/90');
                navbar.classList.remove('bg-transparent');
            } else {
                navbar.classList.remove('shadow-lg', 'bg-card/90');
                navbar.classList.add('bg-transparent');
            }
        });

        // Form submission handling
        const form = document.getElementById('project-form');
        const successMessage = document.getElementById('success-message');

        form.addEventListener('submit', (e) => {
            e.preventDefault(); // Prevent page reload
            
            // Simulate network request/processing
            const btn = form.querySelector('button[type="submit"]');
            const originalText = btn.innerText;
            btn.innerText = "Sending...";
            btn.disabled = true;

            setTimeout(() => {
                // Hide form, show success ui smoothly
                form.style.opacity = '0';
                setTimeout(() => {
                    form.classList.add('hidden');
                    successMessage.classList.remove('hidden');
                    successMessage.classList.add('animate-fade-in'); // simple visual cue
                }, 300);
                
                // Reset button for next time
                btn.innerText = originalText;
                btn.disabled = false;
            }, 800);
        });

        // Function to reset form and show it again
        window.resetForm = function() {
            form.reset();
            successMessage.classList.add('hidden');
            form.classList.remove('hidden');
            form.style.opacity = '1';
        }
    </script>
</body>
</html>
