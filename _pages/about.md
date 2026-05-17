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

        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

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

    <div class="max-w-5xl mx-auto px-4 py-8 md:py-12">
        
        <header class="text-center mb-16 fade-in">
            <div class="inline-block p-4 rounded-full bg-teal-100 text-teal-700 text-4xl mb-4">
                💼
            </div>
            <h1 class="text-4xl md:text-5xl font-bold tracking-tight text-stone-900 mb-3">Satria Adhi Pradana</h1>
            <p class="text-xl text-stone-600 max-w-2xl mx-auto">Portofolio Virtual Assistant</p>
        </header>

        <section class="mb-20 bg-white rounded-2xl shadow-sm border border-stone-200 p-6 md:p-10 fade-in" style="animation-delay: 0.1s;">
            <div class="mb-8 border-b border-stone-200 pb-6">
                <h2 class="text-2xl font-bold text-stone-800 mb-2">🎯 Hello...</h2>
                <p class="text-stone-600">
                    Welcome to the professional portfolio of Satria Adhi Pradana, a dedicated and detail-oriented Virtual Assistant committed to helping businesses, entrepreneurs, and professionals manage their digital tasks more efficiently.
                </p>
            </div>

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

            <div id="dynamic-cover-content" class="min-h-[250px] flex items-center justify-center p-8 bg-stone-50 rounded-xl border border-stone-200 transition-all duration-300">
            </div>
        </section>

        <section class="mb-20 fade-in" style="animation-delay: 0.2s;">
            <div class="bg-white rounded-2xl shadow-sm border border-stone-200 p-6 md:p-10">
                <div class="mb-8 text-center md:text-left">
                    <h2 class="text-2xl font-bold text-stone-800 mb-2">📊 Core Skills Distribution</h2>
                </div>
                <div class="chart-container">
                    <canvas id="skillsChart"></canvas>
                </div>
            </div>
        </section>

        <section class="mb-16 fade-in" style="animation-delay: 0.3s;">
            <div class="mb-8">
                <h2 class="text-2xl font-bold text-stone-800 mb-2">💡 Main Responsibilities</h2>
            </div>
            <div class="space-y-3">
                <div class="border border-stone-200 rounded-xl bg-white overflow-hidden">
                    <button class="w-full px-6 py-4 text-left font-semibold text-stone-800 bg-white hover:bg-stone-50 flex justify-between items-center focus:outline-none" onclick="toggleAccordion('tip1')">
                        <span>1. Email Management</span>
                        <span id="icon-tip1" class="text-teal-600 transition-transform duration-200 text-xl">➕</span>
                    </button>
                    <div id="content-tip1" class="px-6 py-0 max-h-0 overflow-hidden transition-all duration-300 bg-stone-50 text-stone-600">
                        <p class="py-4 border-t border-stone-200"> Managing and organizing emails professionally to ensure smooth communication.</p>
                    </div>
                </div>
            </div>
        </section>

        <footer class="bg-stone-800 text-stone-300 py-10 px-6 rounded-2xl text-center fade-in" style="animation-delay: 0.4s;">
            <h3 class="text-xl font-bold text-white mb-6">Lets Connect</h3>
            <div class="mt-8 pt-6 border-t border-stone-700 text-sm text-stone-500">
                Portofolio "Satria Adhi Pradana"
            </div>
        </footer>
    </div>

    <script>
        const portfolioData = {
            opsi1: `<div class="text-center fade-in w-full"><h2>SATRIA ADHI PRADANA</h2><p>Virtual Assistant Profesional</p></div>`,
            opsi2: `<div class="text-left fade-in w-full"><h2>Hello, Im Satria.</h2><p>I am your reliable Virtual Assistant.</p></div>`,
            opsi3: `<div class="text-center fade-in w-full"><h2>Boost Your Productivity.</h2></div>`
        };

        function switchPersona(opsi) {
            const contentContainer = document.getElementById('dynamic-cover-content');
            contentContainer.innerHTML = portfolioData[opsi];
            const buttons = ['btn-opsi1', 'btn-opsi2', 'btn-opsi3'];
            buttons.forEach(id => {
                const btn = document.getElementById(id);
                btn.className = id === 'btn-' + opsi ? 'px-6 py-3 rounded-lg font-medium border transition-colors duration-200 tab-active' : 'px-6 py-3 rounded-lg font-medium border transition-colors duration-200 tab-inactive';
            });
        }
        switchPersona('opsi1');

        function toggleAccordion(id) {
            const content = document.getElementById('content-' + id);
            const icon = document.getElementById('icon-' + id);
            if (content.style.maxHeight) {
                content.style.maxHeight = null;
                icon.textContent = '➕';
            } else {
                content.style.maxHeight = content.scrollHeight + "px";
                icon.textContent = '➖';
            }
        }

        document.addEventListener('DOMContentLoaded', function() {
            const ctx = document.getElementById('skillsChart').getContext('2d');
            new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: ['Email', 'Data Entry', 'Support', 'Project'],
                    datasets: [{
                        data: [35, 25, 25, 15],
                        backgroundColor: ['#0d9488', '#2dd4bf', '#44403c', '#a8a29e']
                    }]
                },
                options: { responsive: true, maintainAspectRatio: false }
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



