---
permalink: /
title: "Satria Adhi Pradana academic personal websites"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

"I am a Newbie Coder"

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio Virtual Assistant - Satria Adhi Pradana</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        stone: {
                            50: '#fafaf9',
                            100: '#f5f5f4',
                            200: '#e7e5e4',
                            300: '#d6d3d1',
                            700: '#44403c',
                            800: '#292524',
                            900: '#1c1917',
                        },
                        teal: {
                            600: '#0d9488',
                            700: '#0f766e',
                        }
                    },
                    fontFamily: {
                        sans: ['Segoe UI', 'Roboto', 'Helvetica Neue', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

    <style>
        /* CSS Wajib untuk Chart Container agar responsif dan terkontrol */
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 40vh;
            max-height: 400px;
            min-height: 300px;
        }

        /* Animasi transisi konten */
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Styling kustom untuk tab aktif */
        .tab-active {
            background-color: #0d9488;
            color: white;
            border-color: #0d9488;
        }
        .tab-inactive {
            background-color: transparent;
            color: #44403c;
            border-color: #d6d3d1;
        }
        .tab-inactive:hover {
            background-color: #f5f5f4;
        }
    </style>
</head>
<body class="bg-stone-50 text-stone-800 font-sans antialiased leading-relaxed">

    <!-- Chosen Palette: Warm Neutrals (Stone) with Teal accents -->
    <!-- Application Structure Plan: The SPA is structured as an interactive landing page for a Virtual Assistant. Instead of statically listing the 3 cover options from the source report, it implements an "Interactive Persona Switcher". This allows the user (or prospective clients) to view Satria's profile through different professional lenses (Corporate, Creative, Results-driven), fulfilling the source report's options dynamically. It also extracts the core skills into an interactive data visualization (Chart.js) and turns the "Tips" section into an interactive accordion, ensuring all source data is presented interactively and effectively. -->
    <!-- Visualization & Content Choices: 
         1. Persona Switcher (Interactive Text Blocks) -> Goal: Compare different cover styles -> Viz: Dynamic DOM updates via buttons -> Library: Vanilla JS. 
         2. Core Skills Chart (Doughnut Chart) -> Goal: Inform on skill distribution extracted from Option 2 -> Viz: Chart.js -> Interaction: Hover tooltips -> Library: Chart.js (NO SVG/Mermaid). 
         3. Tips Accordion -> Goal: Organize actionable advice -> Viz: Expandable HTML sections -> Library: Vanilla JS. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <div class="max-w-5xl mx-auto px-4 py-8 md:py-12">
        
        <!-- Header Section -->
        <header class="text-center mb-16 fade-in">
            <div class="inline-block p-4 rounded-full bg-teal-100 text-teal-700 text-4xl mb-4">
                💼
            </div>
            <h1 class="text-4xl md:text-5xl font-bold tracking-tight text-stone-900 mb-3">Satria Adhi Pradana</h1>
            <p class="text-xl text-stone-600 max-w-2xl mx-auto">Portofolio Virtual Assistant</p>
        </header>

        <!-- Section 1: Interactive Cover Letter (Persona Switcher) -->
        <section class="mb-20 bg-white rounded-2xl shadow-sm border border-stone-200 p-6 md:p-10 fade-in" style="animation-delay: 0.1s;">
            <div class="mb-8 border-b border-stone-200 pb-6">
                <h2 class="text-2xl font-bold text-stone-800 mb-2">🎯 Hello...</h2>
                <p class="text-stone-600">
                    Welcome to the professional portfolio of Satria Adhi Pradana, a dedicated and detail-oriented Virtual Assistant committed to helping businesses, entrepreneurs, and professionals manage their digital tasks more efficiently. With a strong passion for productivity, organization, and digital support, I provide reliable assistance designed to simplify workflows, improve time management, and support business growth in today’s fast-paced digital environment. As a Virtual Assistant, I specialize in administrative support, content management, data entry, scheduling, research, communication handling, and various digital operations tailored to client needs. I believe that behind every successful business is a well-organized system, clear communication, and consistent execution. Through professionalism, adaptability, and a results-driven mindset, I aim to become a trusted remote partner who helps clients focus on what matters most. This portfolio showcases my skills, experiences, services, and selected projects that reflect my commitment to quality work and continuous learning. Whether working independently or collaborating with teams, I strive to deliver efficient solutions, maintain high standards, and create positive working relationships with every client I support.
                </p>
            </div>

            <!-- Tab Controls -->
            <div class="flex flex-col sm:flex-row gap-3 mb-8 justify-center">
                <button onclick="switchPersona('opsi1')" id="btn-opsi1" class="px-6 py-3 rounded-lg font-medium border transition-colors duration-200 tab-active">
                    🏢 Virtual Assistant
                </button>
                <button onclick="switchPersona('opsi2')" id="btn-opsi2" class="px-6 py-3 rounded-lg font-medium border transition-colors duration-200 tab-inactive">
                    🚀 Media Management
                </button>
                <button onclick="switchPersona('opsi3')" id="btn-opsi3" class="px-6 py-3 rounded-lg font-medium border transition-colors duration-200 tab-inactive">
                    📈 Office or Data Centre Management
                </button>
            </div>

            <!-- Dynamic Content Area -->
            <div id="dynamic-cover-content" class="min-h-[250px] flex items-center justify-center p-8 bg-stone-50 rounded-xl border border-stone-200 transition-all duration-300">
                <!-- Content injected via JS -->
            </div>
        </section>

        <!-- Section 2: Visualisasi Keahlian (Chart.js) -->
        <section class="mb-20 fade-in" style="animation-delay: 0.2s;">
            <div class="bg-white rounded-2xl shadow-sm border border-stone-200 p-6 md:p-10">
                <div class="mb-8 text-center md:text-left">
                    <h2 class="text-2xl font-bold text-stone-800 mb-2">📊 Core Skills Distribution</h2>
                    <p class="text-stone-600 max-w-3xl">
                        This visualization highlights the core competencies presented in my professional profile, including Email Management, Data Entry, Customer Support, and Project Management. The interactive chart below represents an estimated distribution of my working focus, service capacity, and operational expertise as a Virtual Assistant. Each category reflects the areas where I consistently provide support to clients, helping businesses maintain organization, improve communication flow, manage administrative workloads, and increase overall productivity. By strategically balancing these responsibilities, I ensure efficient task execution and reliable remote assistance tailored to different business needs. Hover over the chart to explore detailed insights into each skill area and understand how my expertise contributes to building smoother, more effective business operations.
                    </p>
                </div>

                <!-- REQUIRED: Chart Container styling applied here -->
                <div class="chart-container">
                    <canvas id="skillsChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Section 3: Tips Pembuatan Portofolio (Interactive Accordion) -->
        <section class="mb-16 fade-in" style="animation-delay: 0.3s;">
            <div class="mb-8">
                <h2 class="text-2xl font-bold text-stone-800 mb-2">💡 Main Responsibilities of Satria Adhi Pradana as a Virtual Assistant</h2>
                <p class="text-stone-600">
                     As a professional Virtual Assistant, Satria Adhi Pradana specializes in four core areas that support business productivity, operational efficiency, and client communication. These responsibilities reflect the essential services provided to help individuals, entrepreneurs, and businesses manage their daily digital activities more effectively.
                </p>
            </div>

            <div class="space-y-3">
                <!-- Accordion Item 1 -->
                <div class="border border-stone-200 rounded-xl bg-white overflow-hidden">
                    <button class="w-full px-6 py-4 text-left font-semibold text-stone-800 bg-white hover:bg-stone-50 flex justify-between items-center focus:outline-none" onclick="toggleAccordion('tip1')">
                        <span>1. Email Management</span>
                        <span id="icon-tip1" class="text-teal-600 transition-transform duration-200 text-xl">➕</span>
                    </button>
                    <div id="content-tip1" class="px-6 py-0 max-h-0 overflow-hidden transition-all duration-300 bg-stone-50 text-stone-600">
                        <p class="py-4 border-t border-stone-200"> Managing and organizing emails professionally to ensure smooth communication, timely responses, inbox organization, spam filtering, scheduling follow-ups, and maintaining efficient correspondence with clients or business partners.</p>
                    </div>
                </div>

                <!-- Accordion Item 2 -->
                <div class="border border-stone-200 rounded-xl bg-white overflow-hidden">
                    <button class="w-full px-6 py-4 text-left font-semibold text-stone-800 bg-white hover:bg-stone-50 flex justify-between items-center focus:outline-none" onclick="toggleAccordion('tip2')">
                        <span>2. Data Entry & Administrative Support</span>
                        <span id="icon-tip2" class="text-teal-600 transition-transform duration-200 text-xl">➕</span>
                    </button>
                    <div id="content-tip2" class="px-6 py-0 max-h-0 overflow-hidden transition-all duration-300 bg-stone-50 text-stone-600">
                        <p class="py-4 border-t border-stone-200"> Handling data input, document organization, spreadsheet management, file maintenance, and other administrative tasks with accuracy and attention to detail to help businesses maintain structured and reliable information systems.</p>
                    </div>
                </div>

                <!-- Accordion Item 3 -->
                <div class="border border-stone-200 rounded-xl bg-white overflow-hidden">
                    <button class="w-full px-6 py-4 text-left font-semibold text-stone-800 bg-white hover:bg-stone-50 flex justify-between items-center focus:outline-none" onclick="toggleAccordion('tip3')">
                        <span>3. Customer Support</span>
                        <span id="icon-tip3" class="text-teal-600 transition-transform duration-200 text-xl">➕</span>
                    </button>
                    <div id="content-tip3" class="px-6 py-0 max-h-0 overflow-hidden transition-all duration-300 bg-stone-50 text-stone-600">
                        <p class="py-4 border-t border-stone-200"> Providing responsive and professional customer assistance through email, chat, or social media platforms. This includes answering inquiries, resolving basic issues, maintaining customer satisfaction, and supporting positive client relationships.</p>
                    </div>
                </div>

                <!-- Accordion Item 4 -->
                <div class="border border-stone-200 rounded-xl bg-white overflow-hidden">
                    <button class="w-full px-6 py-4 text-left font-semibold text-stone-800 bg-white hover:bg-stone-50 flex justify-between items-center focus:outline-none" onclick="toggleAccordion('tip4')">
                        <span>4. Project Management</span>
                        <span id="icon-tip4" class="text-teal-600 transition-transform duration-200 text-xl">➕</span>
                    </button>
                    <div id="content-tip4" class="px-6 py-0 max-h-0 overflow-hidden transition-all duration-300 bg-stone-50 text-stone-600">
                        <p class="py-4 border-t border-stone-200">Assisting in task coordination, deadline tracking, workflow organization, and team communication to ensure projects run efficiently and remain aligned with business goals and timelines.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer / Contact Info Aggregated -->
        <footer class="bg-stone-800 text-stone-300 py-10 px-6 rounded-2xl text-center fade-in" style="animation-delay: 0.4s;">
            <h3 class="text-xl font-bold text-white mb-6">Lets Connect</h3>
            <div class="flex flex-col md:flex-row justify-center items-center gap-6 md:gap-12 text-sm md:text-base">
                <div class="flex items-center gap-2">
                    <span class="text-xl">📧</span> satriaadhipradana2701@gmail.com
                </div>
                <div class="flex items-center gap-2">
                    <span class="text-xl">📞</span> +62 8xx 7539 XXXX
                </div>
                <div class="flex items-center gap-2">
                    <span class="text-xl">🌐</span> LinkedIn & Portofolio Online
                </div>
                <div class="flex items-center gap-2">
                    <span class="text-xl">📍</span> Jakarta, Indonesia
                </div>
            </div>
            <div class="mt-8 pt-6 border-t border-stone-700 text-sm text-stone-500">
                Portofolio "Satria Adhi Pradana"
            </div>
        </footer>

    </div>

    <!-- Application Logic -->
    <script>
        // --- 1. State Management & Data Storage ---
        const portfolioData = {
            opsi1: `
                <div class="text-center fade-in w-full">
                    <h2 class="text-3xl font-extrabold text-stone-900 tracking-wide mb-2">SATRIA ADHI PRADANA</h2>
                    <p class="text-lg text-teal-700 font-semibold mb-6 uppercase tracking-widest">Virtual Assistant Profesional</p>
                    <div class="w-16 h-1 bg-teal-600 mx-auto mb-6"></div>
                    <p class="text-stone-600 text-lg max-w-2xl mx-auto leading-relaxed">
                        Helping you manage administrative and operational tasks efficiently, so you can focus on growing your business and achieving your goals. In addition to Virtual Assistant services, I also provide support in Cyber Security awareness, digital safety practices, basic security analysis, and technology-related assistance to help individuals and businesses maintain secure and well-organized digital operations in today’s connected world.
                    </p>
                </div>
            `,
            opsi2: `
                <div class="text-left fade-in w-full md:px-8">
                    <h1 class="text-4xl font-bold text-stone-900 mb-2">Hello, Im <span class="text-teal-600">Satria.</span></h1>
                    <h3 class="text-xl text-stone-600 mb-6 border-b border-stone-200 pb-4">I am your reliable Virtual Assistant.</h3>
                    <p class="font-semibold text-stone-800 mb-3">Keahlian Inti:</p>
                    <ul class="grid grid-cols-1 sm:grid-cols-2 gap-3 mb-6 text-stone-600">
                        <li class="flex items-center gap-2"><span>✔️</span> Email & Schedule Management</li>
                        <li class="flex items-center gap-2"><span>✔️</span> Data Entry & Research</li>
                        <li class="flex items-center gap-2"><span>✔️</span> Customer Support</li>
                        <li class="flex items-center gap-2"><span>✔️</span> Project Management</li>
                    </ul>
                    <p class="text-teal-700 font-medium italic">"I am ready to provide practical and reliable solutions to improve your business efficiency, streamline daily operations, and support your productivity in the digital world."</p>
                </div>
            `,
            opsi3: `
                <div class="text-center fade-in w-full">
                    <h2 class="text-3xl md:text-4xl font-black text-stone-900 mb-2 leading-tight">
                        Boost Your Productivity.<br>
                        <span class="text-teal-600">Reduce Your Workload.</span>
                    </h2>
                    <div class="my-6 inline-block bg-stone-200 text-stone-800 px-4 py-1 rounded-full text-sm font-semibold">
                        Satria Adhi Pradana | Your Trusted Virtual Assistant
                    </div>
                    <p class="text-stone-600 text-lg max-w-2xl mx-auto border-l-4 border-teal-500 pl-4 text-left">
                        I manage the details, so you can lead the business. This portfolio showcases my experience and commitment to delivering exceptional administrative and digital support with professionalism, efficiency, and attention to detail.
                    </p>
                </div>
            `
        };

        // --- 2. Interactive Logic: Persona Switcher ---
        function switchPersona(opsi) {
            // Update Content
            const contentContainer = document.getElementById('dynamic-cover-content');
            contentContainer.innerHTML = portfolioData[opsi];

            // Update Button Styles
            const buttons = ['btn-opsi1', 'btn-opsi2', 'btn-opsi3'];
            buttons.forEach(id => {
                const btn = document.getElementById(id);
                if (id === 'btn-' + opsi) {
                    btn.classList.remove('tab-inactive');
                    btn.classList.add('tab-active');
                } else {
                    btn.classList.remove('tab-active');
                    btn.classList.add('tab-inactive');
                }
            });
        }

        // Initialize default view
        switchPersona('opsi1');


        // --- 3. Interactive Logic: Tips Accordion ---
        function toggleAccordion(id) {
            const content = document.getElementById('content-' + id);
            const icon = document.getElementById('icon-' + id);
            
            if (content.style.maxHeight) {
                // Close it
                content.style.maxHeight = null;
                icon.textContent = '➕';
                icon.style.transform = 'rotate(0deg)';
            } else {
                // Open it
                content.style.maxHeight = content.scrollHeight + "px";
                icon.textContent = '➖';
                icon.style.transform = 'rotate(180deg)';
            }
        }


        // --- 4. Chart.js Implementation (Keahlian Inti) ---
        document.addEventListener('DOMContentLoaded', function() {
            const ctx = document.getElementById('skillsChart').getContext('2d');
            
            // Konfigurasi Chart
            new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: [
                        'Manajemen Email & Jadwal', 
                        'Entri Data & Riset', 
                        'Dukungan Pelanggan', 
                        'Manajemen Proyek Ringan'
                    ],
                    datasets: [{
                        label: 'Persentase Fokus Layanan',
                        data: [35, 25, 25, 15], // Estimasi data berdasarkan peran VA
                        backgroundColor: [
                            '#0d9488', // Teal 600
                            '#2dd4bf', // Teal 400
                            '#44403c', // Stone 700
                            '#a8a29e'  // Stone 400
                        ],
                        borderWidth: 0,
                        hoverOffset: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false, // Wajib agar mengikuti chart-container
                    cutout: '65%',
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                padding: 20,
                                font: {
                                    family: "'Segoe UI', 'Roboto', sans-serif",
                                    size: 13
                                },
                                color: '#44403c'
                            }
                        },
                        tooltip: {
                            backgroundColor: 'rgba(41, 37, 36, 0.9)',
                            padding: 12,
                            titleFont: { size: 14 },
                            bodyFont: { size: 13 },
                            callbacks: {
                                label: function(context) {
                                    return ' ' + context.label + ': ' + context.raw + '% Fokus';
                                }
                            }
                        }
                    },
                    animation: {
                        animateScale: true,
                        animateRotate: true
                    }
                }
            });
        });
    </script>
</body>
</html>

## Expertise and Experience

### Technical Project Management
As a seasoned Technical Project Manager, He is excels in orchestrating complex projects from inception to completion. His meticulous approach ensures seamless execution and timely delivery, making him a reliable partner in any technological endeavor.

### UI/UX Design
His possesses a keen eye for detail and a user-centric mindset in UI/UX Design. He creates intuitive and visually captivating designs that engage users and enhance their overall experience. From wireframes to prototypes and usability testing, his work resonates with elegance and functionality.

### Web Development
In the realm of Web Development, He is an architect of digital solutions. He transforms ideas into robust, scalable web applications, leveraging a diverse range of technologies and frameworks to create tailor made solutions that meet various business needs.

### Cyber Security
Understanding the critical importance of safeguarding digital assets, He is deeply committed to Cyber Security. He employs cutting-edge security practices and methodologies to protect systems against cyber threats, ensuring data integrity and confidentiality.

### Virtual Assistant
As a Virtual Assistant, He is offers comprehensive support to streamline your operations and enhance productivity. From managing schedules and communications to handling administrative tasks and project coordination, he is dedicated to helping you focus on what matters most. His organizational skills and attention to detail ensure that your projects run smoothly and efficiently.


![Editing a markdown file](/images/editing-talk.png)


# Follow Me on Social Media

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/satriaadhipradana)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/DFIRgeek)
[![Instagram](https://img.shields.io/badge/Instagram-E1306C?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/satriaadhipradana_)
[![Medium](https://img.shields.io/badge/Medium-00AB6C?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@satriaadhipradana)



