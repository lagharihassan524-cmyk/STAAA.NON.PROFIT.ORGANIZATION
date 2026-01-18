# STAAA.NON.PROFIT.ORGANIZATION[index.html.html](https://github.com/user-attachments/files/24695189/index.html.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sindh Tail Agriculture Abadgar Association</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Lora:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Poppins', sans-serif; background-color: #fafaf9; }
        h1, h2, h3, h4, .font-serif { font-family: 'Lora', serif; }
        
        /* Animations */
        .fade-in { animation: fadeIn 0.8s cubic-bezier(0.16, 1, 0.3, 1); }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        
        .glass-nav { background: rgba(15, 23, 42, 0.85); backdrop-filter: blur(16px); border-bottom: 1px solid rgba(255,255,255,0.1); }
        .glass-card { background: rgba(255, 255, 255, 0.95); backdrop-filter: blur(10px); border: 1px solid rgba(226, 232, 240, 0.8); }
        
        /* Ticker Animation */
        .animate-marquee { display: inline-block; padding-left: 100%; animation: marquee 30s linear infinite; }
        @keyframes marquee { 0% { transform: translate(0, 0); } 100% { transform: translate(-100%, 0); } }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #0f766e; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #0d9488; }
    </style>
</head>
<body class="bg-gray-50 text-gray-800 flex flex-col min-h-screen">

    <!-- Navigation -->
    <nav class="bg-emerald-950 text-white shadow-2xl sticky top-0 z-50 transition-all duration-300 border-b border-emerald-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <div class="flex items-center space-x-3 cursor-pointer group" onclick="showSection('home')">
                    <div class="bg-amber-500 p-1.5 rounded-lg shadow-lg group-hover:scale-105 transition duration-300 rotate-3 group-hover:rotate-0">
                        <img id="display-logo-img" src="" class="h-9 w-9 object-contain hidden" alt="Logo">
                        <span id="display-logo-icon" class="text-3xl block h-9 w-9 text-center leading-9">🌾</span>
                    </div>
                    <div>
                        <div class="font-serif font-bold text-xl tracking-wide leading-none text-amber-50 group-hover:text-white transition">STAAA</div>
                        <div class="text-[0.6rem] text-amber-200/80 uppercase tracking-widest font-bold">Sindh Tail Agriculture</div>
                    </div>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-2">
                        <button onclick="showSection('home')" class="text-emerald-100 hover:text-white hover:bg-emerald-800/50 px-5 py-2.5 rounded-md text-sm font-medium transition-all duration-300 border border-transparent hover:border-emerald-700">Home</button>
                        <button onclick="showSection('about')" class="text-emerald-100 hover:text-white hover:bg-emerald-800/50 px-5 py-2.5 rounded-md text-sm font-medium transition-all duration-300 border border-transparent hover:border-emerald-700">About Us</button>
                        <button onclick="showSection('updates')" class="text-emerald-100 hover:text-white hover:bg-emerald-800/50 px-5 py-2.5 rounded-md text-sm font-medium transition-all duration-300 border border-transparent hover:border-emerald-700">Updates</button>
                        <button onclick="showSection('contact')" class="text-emerald-100 hover:text-white hover:bg-emerald-800/50 px-5 py-2.5 rounded-md text-sm font-medium transition-all duration-300 border border-transparent hover:border-emerald-700">Contact</button>
                    </div>
                </div>
                <div>
                    <button onclick="toggleAdmin()" id="adminBtn" class="bg-amber-500 hover:bg-amber-400 text-emerald-950 border-none px-6 py-2.5 rounded-lg text-sm font-bold transition-all shadow-lg hover:shadow-amber-500/50 transform hover:-translate-y-1">Admin Panel</button>
                </div>
            </div>
            <!-- Mobile menu button -->
            <div class="-mr-2 flex md:hidden absolute right-4 top-5">
                <button type="button" onclick="document.getElementById('mobile-menu').classList.toggle('hidden')" class="bg-emerald-800/50 inline-flex items-center justify-center p-2 rounded-md text-emerald-100 hover:text-white hover:bg-emerald-700 focus:outline-none backdrop-blur-sm">
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div class="hidden md:hidden bg-emerald-900 border-t border-emerald-800" id="mobile-menu">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <button onclick="showSection('home')" class="block hover:bg-emerald-800 px-3 py-3 rounded-md text-base font-medium w-full text-left text-white border-b border-emerald-800/50">Home</button>
                <button onclick="showSection('about')" class="block hover:bg-emerald-800 px-3 py-3 rounded-md text-base font-medium w-full text-left text-white border-b border-emerald-800/50">About Us</button>
                <button onclick="showSection('updates')" class="block hover:bg-emerald-800 px-3 py-3 rounded-md text-base font-medium w-full text-left text-white border-b border-emerald-800/50">Updates</button>
                <button onclick="showSection('contact')" class="block hover:bg-emerald-800 px-3 py-3 rounded-md text-base font-medium w-full text-left text-white">Contact</button>
            </div>
        </div>
    </nav>



    <!-- Main Content Area -->
    <main id="mainContent" class="flex-grow">
        
        <!-- Home Section -->
        <section id="home" class="fade-in">
            <!-- Hero -->
            <div class="relative bg-emerald-900 text-white overflow-hidden min-h-[70vh] flex items-center py-20">
                <div class="absolute inset-0">
                    <img src="https://images.unsplash.com/photo-1625246333195-f8196ba00803?ixlib=rb-1.2.1&auto=format&fit=crop&w=1920&q=80" class="w-full h-full object-cover opacity-50" alt="Agriculture Field">
                    <div class="absolute inset-0 bg-gradient-to-br from-emerald-950/90 via-emerald-900/80 to-stone-900/70"></div>
                    <div class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/wood-pattern.png')] opacity-10"></div>
                </div>
                <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center z-10">
                    <div class="inline-block mb-6 px-6 py-2 rounded-full bg-amber-500/20 backdrop-blur-md border border-amber-500/30 text-amber-300 text-xs font-bold tracking-widest uppercase shadow-lg">
                        Sindh, Pakistan
                    </div>
                    <h1 id="display-hero-title" class="font-serif text-5xl md:text-7xl font-bold tracking-tight mb-8 drop-shadow-2xl text-white leading-tight">
                        Sindh Tail Agriculture Abadgar Association
                    </h1>
                    <p id="display-hero-text" class="mt-4 text-lg md:text-2xl max-w-4xl mx-auto text-emerald-50 drop-shadow-lg leading-relaxed font-normal opacity-90 font-light">
                        Empowering farmers, advocating for water rights, and building a sustainable agricultural future.
                    </p>
                    
                    <div class="mt-12 flex flex-col md:flex-row items-center justify-center gap-8">
                        <button onclick="showSection('about')" class="bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-400 hover:to-amber-500 text-white font-bold py-4 px-10 rounded-lg shadow-[0_10px_25px_rgba(245,158,11,0.4)] transition-all transform hover:-translate-y-1 hover:scale-105 text-lg border-b-4 border-amber-700">
                            Explore Our Mission
                        </button>
                        
                        <div class="flex flex-col sm:flex-row gap-4">
                            <!-- Water Status Widget -->
                            <div class="bg-emerald-950/60 backdrop-blur-md border border-amber-500/30 rounded-xl p-4 flex items-center space-x-4 min-w-[200px] shadow-2xl hover:bg-emerald-900/60 transition">
                                <div class="relative">
                                    <div id="water-status-indicator" class="w-4 h-4 rounded-full bg-emerald-500 shadow-[0_0_15px_rgba(16,185,129,0.8)]"></div>
                                    <div id="water-status-ping" class="absolute top-0 left-0 w-4 h-4 rounded-full bg-emerald-500 animate-ping opacity-75"></div>
                                </div>
                                <div class="text-left">
                                    <p class="text-[10px] text-emerald-200 uppercase font-bold tracking-widest">Water Status</p>
                                    <p id="display-water-status" class="text-lg font-bold text-white font-serif">Full Flow</p>
                                </div>
                            </div>

                             <!-- Weather Widget -->
                             <div class="bg-emerald-950/60 backdrop-blur-md border border-amber-500/30 rounded-xl p-4 flex items-center space-x-4 min-w-[200px] shadow-2xl hover:bg-emerald-900/60 transition">
                                <div class="text-3xl drop-shadow-md">☀️</div>
                                <div class="text-left">
                                    <p class="text-[10px] text-amber-200 uppercase font-bold tracking-widest">Sindh Forecast</p>
                                    <p class="text-lg font-bold text-white font-serif">38°C Sunny</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Features -->
            <div class="max-w-7xl mx-auto py-20 px-4 sm:px-6 lg:px-8 -mt-24 relative z-10">
                <div id="features-container" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 text-center">
                    <!-- Features injected via JS -->
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="hidden fade-in max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-extrabold text-green-800 sm:text-4xl">About Our Association</h2>
                <div class="mt-4 max-w-2xl mx-auto h-1 bg-green-500 rounded"></div>
            </div>
            
            <div class="bg-white rounded-2xl shadow-lg overflow-hidden flex flex-col md:flex-row">
                <div class="md:w-1/3 bg-green-100 flex items-center justify-center p-8">
                    <span class="text-9xl">🌱</span>
                </div>
                <div class="md:w-2/3 p-8 md:p-12">
                    <h3 class="text-2xl font-bold text-gray-800 mb-4">Who We Are</h3>
                    <p id="display-about-text" class="text-gray-600 text-lg leading-relaxed mb-6">
                        Loading content...
                    </p>
                    
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mt-8">
                        <div class="flex items-start">
                            <div class="flex-shrink-0">
                                <span class="flex items-center justify-center h-10 w-10 rounded-md bg-green-500 text-white">✓</span>
                            </div>
                            <div class="ml-4">
                                <h4 class="text-lg leading-6 font-medium text-gray-900">Unity</h4>
                                <p class="mt-2 text-base text-gray-500">Uniting farmers under one platform.</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0">
                                <span class="flex items-center justify-center h-10 w-10 rounded-md bg-green-500 text-white">✓</span>
                            </div>
                            <div class="ml-4">
                                <h4 class="text-lg leading-6 font-medium text-gray-900">Advocacy</h4>
                                <p class="mt-2 text-base text-gray-500">Direct representation to government.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Updates Section -->
        <section id="updates" class="hidden fade-in max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-extrabold text-green-800 sm:text-4xl">News & Announcements</h2>
                <p class="mt-4 text-xl text-gray-500">Stay informed about the latest developments.</p>
            </div>
            <div id="news-container" class="grid grid-cols-1 gap-8 max-w-4xl mx-auto">
                <!-- News items injected via JS -->
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="hidden fade-in max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:px-8">
            <h2 class="text-3xl font-extrabold text-green-800 text-center mb-12">Contact Us</h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                
                <!-- Contact Form -->
                <div class="bg-white p-8 rounded-2xl shadow-lg">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Send a Message</h3>
                    <form onsubmit="event.preventDefault(); alert('Message sent successfully!');">
                        <div class="space-y-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Full Name</label>
                                <input type="text" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-green-500 focus:border-green-500" required>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Contact Number</label>
                                <input type="text" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-green-500 focus:border-green-500" required>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700">Message</label>
                                <textarea rows="4" class="mt-1 block w-full border border-gray-300 rounded-md shadow-sm py-2 px-3 focus:outline-none focus:ring-green-500 focus:border-green-500" required></textarea>
                            </div>
                            <button type="submit" class="w-full flex justify-center py-3 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-green-700 hover:bg-green-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-green-500 transition">
                                Send Message
                            </button>
                        </div>
                    </form>
                </div>

                <!-- Contact Info -->
                <div class="bg-gradient-to-br from-green-800 to-green-600 text-white p-8 rounded-2xl shadow-lg flex flex-col justify-center">
                    <h3 class="text-2xl font-bold mb-6">Contact Information</h3>
                    <p class="mb-8 text-green-100">Visit our office or call us for any queries regarding membership or water schedules.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start">
                            <span class="text-2xl mr-4">📍</span>
                            <div>
                                <h4 class="font-bold">Head Office</h4>
                                <p class="text-green-100 display-address">Loading Address...</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <span class="text-2xl mr-4">📞</span>
                            <div>
                                <h4 class="font-bold">Phone</h4>
                                <p class="text-green-100 display-phone">Loading...</p>
                            </div>
                        </div>
                        <div class="flex items-center">
                            <span class="text-2xl mr-4">✉️</span>
                            <div>
                                <h4 class="font-bold">Email</h4>
                                <p class="text-green-100 display-email">Loading...</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Admin Login Section -->
        <section id="admin-login" class="hidden fade-in min-h-[60vh] flex items-center justify-center px-4">
            <div class="bg-white p-10 rounded-2xl shadow-2xl max-w-md w-full border-t-8 border-green-600">
                <div class="text-center mb-8">
                    <span class="text-4xl">🔒</span>
                    <h2 class="text-2xl font-bold text-gray-800 mt-4">Admin Access</h2>
                    <p class="text-gray-500 text-sm">Secure area for officials only</p>
                </div>
                <form onsubmit="handleLogin(event)">
                    <div class="mb-4">
                        <label class="block text-gray-700 text-sm font-bold mb-2">Username</label>
                        <input id="username" type="text" class="w-full border rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-green-500" required>
                    </div>
                    <div class="mb-6">
                        <label class="block text-gray-700 text-sm font-bold mb-2">Password</label>
                        <input id="password" type="password" class="w-full border rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-green-500" required>
                    </div>
                    <button class="w-full bg-green-700 hover:bg-green-800 text-white font-bold py-3 rounded-lg transition shadow-md" type="submit">
                        Login
                    </button>
                </form>
            </div>
        </section>

        <!-- Admin Dashboard Section -->
        <section id="admin-dashboard" class="hidden fade-in max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center mb-8 bg-white p-6 rounded-lg shadow">
                <div>
                    <h2 class="text-3xl font-bold text-gray-800">Admin Dashboard</h2>
                    <p class="text-gray-500">Welcome, Sajjad</p>
                </div>
                <button onclick="logout()" class="bg-red-500 hover:bg-red-600 text-white px-6 py-2 rounded shadow transition">Logout</button>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                
                <!-- Left Column: Site Content Settings -->
                <div class="space-y-8">
                    <div class="bg-white p-6 rounded-lg shadow-md border-l-4 border-blue-500">
                        <h3 class="text-xl font-bold text-gray-700 mb-4 flex items-center">
                            <span class="mr-2">⚙️</span> Site Content Settings
                        </h3>
                        <form onsubmit="saveSiteSettings(event)">
                            <div class="mb-6">
                                <label class="block text-sm font-bold text-gray-700 uppercase mb-2">Website Logo</label>
                                <div class="border-2 border-dashed border-blue-300 rounded-lg p-4 bg-blue-50 text-center hover:bg-blue-100 transition">
                                    <div id="logo-preview-container" class="hidden mb-3">
                                        <img id="admin-logo-preview" class="h-20 w-auto mx-auto object-contain bg-white rounded shadow-sm" />
                                        <p class="text-xs text-green-600 font-bold mt-1">Logo Selected</p>
                                    </div>
                                    <label class="cursor-pointer block">
                                        <span class="text-blue-600 font-semibold text-lg">Click to Upload Logo</span>
                                        <p class="text-xs text-gray-500 mt-1">PNG, JPG, SVG (Max 2MB)</p>
                                        <input id="edit-logo" type="file" accept="image/*" class="hidden" onchange="previewLogo()" />
                                    </label>
                                </div>
                            </div>
                            <div class="mb-4">
                                <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Hero Title</label>
                                <input id="edit-hero-title" type="text" class="w-full border border-gray-300 rounded px-3 py-2 text-sm focus:ring-blue-500 focus:border-blue-500">
                            </div>
                            <div class="mb-4">
                                <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Hero Description</label>
                                <textarea id="edit-hero-text" rows="3" class="w-full border border-gray-300 rounded px-3 py-2 text-sm focus:ring-blue-500 focus:border-blue-500"></textarea>
                            </div>
                            <div class="mb-4">
                                <label class="block text-xs font-bold text-gray-500 uppercase mb-1">About Us Text</label>
                                <textarea id="edit-about-text" rows="4" class="w-full border border-gray-300 rounded px-3 py-2 text-sm focus:ring-blue-500 focus:border-blue-500"></textarea>
                            </div>
                            
                            <div class="grid grid-cols-2 gap-4">
                                <div class="mb-4">
                                    <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Phone</label>
                                    <input id="edit-phone" type="text" class="w-full border border-gray-300 rounded px-3 py-2 text-sm">
                                </div>
                                <div class="mb-4">
                                    <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Email</label>
                                    <input id="edit-email" type="text" class="w-full border border-gray-300 rounded px-3 py-2 text-sm">
                                </div>
                            </div>
                             <div class="mb-4">
                                <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Address</label>
                                <input id="edit-address" type="text" class="w-full border border-gray-300 rounded px-3 py-2 text-sm">
                            </div>

                            <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded transition">
                                Save Content Changes
                            </button>
                        </form>
                    </div>

                    <!-- Live Data Settings -->
                    <div class="bg-white p-6 rounded-lg shadow-md border-l-4 border-yellow-500">
                        <h3 class="text-xl font-bold text-gray-700 mb-4 flex items-center">
                            <span class="mr-2">⚡</span> Live Updates
                        </h3>
                        <form onsubmit="saveLiveSettings(event)">

                            <div class="mb-4">
                                <label class="block text-xs font-bold text-gray-500 uppercase mb-1">Water Availability Status</label>
                                <select id="edit-water-status-type" class="w-full border border-gray-300 rounded px-3 py-2 text-sm mb-2" onchange="updateWaterStatusLabel()">
                                    <option value="green">Full Flow (Green)</option>
                                    <option value="yellow">Rotation (Yellow)</option>
                                    <option value="red">Shortage (Red)</option>
                                </select>
                                <input id="edit-water-status-text" type="text" class="w-full border border-gray-300 rounded px-3 py-2 text-sm" placeholder="Custom Label (e.g. Full Flow)">
                            </div>
                            <button type="submit" class="w-full bg-yellow-600 hover:bg-yellow-700 text-white font-bold py-2 px-4 rounded transition">
                                Update Live Data
                            </button>
                        </form>
                    </div>
                </div>

                <!-- Right Column: News Management -->
                <div class="space-y-8">
                    <!-- Post News -->
                    <div class="bg-white p-6 rounded-lg shadow-md border-l-4 border-green-500">
                        <h3 class="text-xl font-bold text-gray-700 mb-4 flex items-center">
                            <span class="mr-2">📢</span> Post New Update
                        </h3>
                        <form onsubmit="addNews(event)">
                            <div class="mb-3">
                                <label class="block text-gray-700 text-sm font-bold mb-1">Title</label>
                                <input id="newsTitle" type="text" class="w-full border rounded px-3 py-2 focus:ring-green-500 focus:border-green-500" required>
                            </div>
                            <div class="mb-3">
                                <label class="block text-gray-700 text-sm font-bold mb-1">Date</label>
                                <input id="newsDate" type="date" class="w-full border rounded px-3 py-2 focus:ring-green-500 focus:border-green-500" required>
                            </div>
                            <div class="mb-4">
                                <label class="block text-gray-700 text-sm font-bold mb-2">Attachment (Image or PDF)</label>
                                <div class="flex items-center justify-center w-full">
                                    <label for="newsImage" class="flex flex-col items-center justify-center w-full h-32 border-2 border-green-300 border-dashed rounded-lg cursor-pointer bg-green-50 hover:bg-green-100 transition">
                                        <div class="flex flex-col items-center justify-center pt-5 pb-6">
                                            <span class="text-3xl mb-2">📁</span>
                                            <p class="mb-2 text-sm text-gray-500"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                                            <p class="text-xs text-gray-500">PNG, JPG or PDF (MAX. 5MB)</p>
                                            <p id="fileName" class="mt-2 text-sm text-green-600 font-bold hidden"></p>
                                        </div>
                                        <input id="newsImage" type="file" class="hidden" accept="image/*,application/pdf" onchange="updateFileName()" />
                                    </label>
                                </div>
                            </div>
                            <div class="mb-4">
                                <label class="block text-gray-700 text-sm font-bold mb-1">Content</label>
                                <textarea id="newsContent" rows="3" class="w-full border rounded px-3 py-2 focus:ring-green-500 focus:border-green-500" required></textarea>
                            </div>
                            <button type="submit" class="w-full bg-green-600 hover:bg-green-700 text-white font-bold py-2 px-4 rounded transition">
                                Publish Update
                            </button>
                        </form>
                    </div>

                    <!-- List News -->
                    <div class="bg-white p-6 rounded-lg shadow-md">
                        <h3 class="text-xl font-bold text-gray-700 mb-4">Manage Recent Updates</h3>
                        <div class="overflow-x-auto">
                            <table class="min-w-full leading-normal">
                                <thead>
                                    <tr>
                                        <th class="px-3 py-2 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase">Title</th>
                                        <th class="px-3 py-2 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase">Date</th>
                                        <th class="px-3 py-2 border-b-2 border-gray-200 bg-gray-100 text-right text-xs font-semibold text-gray-600 uppercase">Action</th>
                                    </tr>
                                </thead>
                                <tbody id="admin-news-list">
                                    <!-- Injected -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Manage Features Section -->
            <div class="mt-8 bg-white p-6 rounded-lg shadow-md border-l-4 border-purple-500">
                <h3 class="text-xl font-bold text-gray-700 mb-6 flex items-center">
                    <span class="mr-2">✨</span> Manage Home Features
                </h3>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Add Feature Form -->
                    <div class="md:col-span-1 bg-purple-50 p-6 rounded-lg border border-purple-100">
                        <h4 class="font-bold text-gray-700 mb-4">Add New Feature</h4>
                        <form onsubmit="addFeature(event)">
                            <div class="mb-3">
                                <label class="block text-gray-700 text-xs font-bold mb-1 uppercase">Title</label>
                                <input id="featureTitle" type="text" class="w-full border rounded px-3 py-2 text-sm focus:ring-purple-500 focus:border-purple-500" placeholder="e.g. Soil Testing" required>
                            </div>
                            <div class="mb-3 grid grid-cols-2 gap-3">
                                <div>
                                    <label class="block text-gray-700 text-xs font-bold mb-1 uppercase">Icon (Emoji)</label>
                                    <input id="featureIcon" type="text" class="w-full border rounded px-3 py-2 text-center text-lg focus:ring-purple-500 focus:border-purple-500" value="🌟" required>
                                </div>
                                <div>
                                    <label class="block text-gray-700 text-xs font-bold mb-1 uppercase">Color Theme</label>
                                    <select id="featureColor" class="w-full border rounded px-3 py-2 text-sm focus:ring-purple-500 focus:border-purple-500">
                                        <option value="emerald">Green</option>
                                        <option value="amber">Gold</option>
                                        <option value="red">Red</option>
                                        <option value="blue">Blue</option>
                                    </select>
                                </div>
                            </div>
                            <div class="mb-4">
                                <label class="block text-gray-700 text-xs font-bold mb-1 uppercase">Description</label>
                                <textarea id="featureText" rows="3" class="w-full border rounded px-3 py-2 text-sm focus:ring-purple-500 focus:border-purple-500" placeholder="Short description..." required></textarea>
                            </div>
                            <button type="submit" class="w-full bg-purple-600 hover:bg-purple-700 text-white font-bold py-2 px-4 rounded transition shadow-md">
                                Add Feature
                            </button>
                        </form>
                    </div>

                    <!-- List Features -->
                    <div class="md:col-span-2">
                        <div class="overflow-x-auto bg-white rounded-lg border border-gray-200">
                            <table class="min-w-full leading-normal">
                                <thead class="bg-gray-50">
                                    <tr>
                                        <th class="px-3 py-3 border-b-2 border-gray-200 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider">Feature Title</th>
                                        <th class="px-3 py-3 border-b-2 border-gray-200 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider">Color</th>
                                        <th class="px-3 py-3 border-b-2 border-gray-200 text-right text-xs font-semibold text-gray-600 uppercase tracking-wider">Action</th>
                                    </tr>
                                </thead>
                                <tbody id="admin-features-list">
                                    <!-- Injected via JS -->
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-emerald-950 text-white pt-16 pb-8 mt-auto border-t border-emerald-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <span class="text-3xl">🌾</span>
                        <h3 class="text-2xl font-serif font-bold text-amber-500">STAAA</h3>
                    </div>
                    <p class="text-emerald-200/70 text-sm leading-relaxed">Serving the tail-end farmers of Sindh. Dedicated to water rights, fair crop prices, and agricultural prosperity for every grower.</p>
                </div>
                <div>
                    <h3 class="text-lg font-serif font-bold mb-6 text-white border-b border-emerald-800 pb-2 inline-block">Quick Links</h3>
                    <ul class="space-y-3 text-emerald-200/70 text-sm">
                        <li><button onclick="showSection('home')" class="hover:text-amber-400 transition flex items-center"><span class="mr-2">›</span> Home</button></li>
                        <li><button onclick="showSection('about')" class="hover:text-amber-400 transition flex items-center"><span class="mr-2">›</span> About Us</button></li>
                        <li><button onclick="showSection('updates')" class="hover:text-amber-400 transition flex items-center"><span class="mr-2">›</span> Latest Updates</button></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-serif font-bold mb-6 text-white border-b border-emerald-800 pb-2 inline-block">Connect</h3>
                    <div class="flex space-x-4">
                        <a href="#" class="bg-emerald-900 hover:bg-amber-600 text-white w-12 h-12 rounded-lg flex items-center justify-center transition shadow-lg border border-emerald-800">F</a>
                        <a href="#" class="bg-emerald-900 hover:bg-amber-600 text-white w-12 h-12 rounded-lg flex items-center justify-center transition shadow-lg border border-emerald-800">T</a>
                        <a href="#" class="bg-emerald-900 hover:bg-amber-600 text-white w-12 h-12 rounded-lg flex items-center justify-center transition shadow-lg border border-emerald-800">W</a>
                    </div>
                </div>
            </div>
            <div class="border-t border-emerald-900 mt-12 pt-8 text-center text-sm text-emerald-400/50">
                &copy; 2023 Sindh Tail Agriculture Abadgar Association. All rights reserved.
            </div>
        </div>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // --- State Management ---
        
        // Default Site Configuration
        let siteConfig = {
            logoImage: null,
            heroTitle: "Sindh Tail Agriculture Abadgar Association",
            heroText: "Empowering farmers, advocating for water rights, and building a sustainable agricultural future for Sindh's tail-end growers.",
            aboutText: "The Sindh Tail Agriculture Abadgar Association is dedicated to the welfare of farmers located at the tail-end of the irrigation system in Sindh. We understand the unique challenges faced by these growers, primarily water scarcity and delayed distribution. Our mission is to unite farmers, represent their grievances to government authorities, and ensure that every acre of fertile land gets its due share of water and resources.",
            contactPhone: "+92 300 1234567",
            contactEmail: "info@staaa.org",
            contactAddress: "Main Office, Hyderabad Road, Sindh, Pakistan",
            marketRates: "🌾 Wheat: 4000/40kg  •  ☁️ Cotton: 8500/40kg  •  🍬 Sugar Cane: 450/40kg  •  🍚 Rice: 3500/40kg",
            waterStatus: "Full Flow", // Options: Full Flow, Rotation, Shortage
            waterStatusColor: "green" // green, yellow, red
        };

        // Features Data
        let featuresData = [
            {
                id: 1,
                title: "Water Security",
                icon: "💧",
                text: "Fighting tirelessly for fair and equal water distribution for every tail-end grower.",
                color: "emerald" // emerald, amber, red, blue
            },
            {
                id: 2,
                title: "Crop Support",
                icon: "🌾",
                text: "Access to high-quality seeds, fertilizers, and expert advice for maximum yield.",
                color: "amber"
            },
            {
                id: 3,
                title: "Human Rights",
                icon: "✊",
                text: "Protecting fundamental rights, fighting oppression, and ensuring dignity for farmers.",
                color: "red"
            },
            {
                id: 4,
                title: "Legal Aid",
                icon: "⚖️",
                text: "Standing united against injustice, resolving land disputes, and court representation.",
                color: "blue"
            }
        ];

        // News Data
        let newsData = [
            {
                id: 1,
                title: "Upcoming Water Distribution Schedule",
                date: "2023-10-15",
                content: "The new water rotation schedule for the tail-end distributaries has been released. Please visit the office or check the notice board for details regarding your specific minor.",
                image: "https://images.unsplash.com/photo-1586771107445-d3ca888129ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80"
            },
            {
                id: 2,
                title: "General Body Meeting",
                date: "2023-09-20",
                content: "All members are requested to attend the annual general meeting on Sunday at the Community Hall to elect new representatives. Lunch will be served.",
                image: null
            },
            {
                id: 3,
                title: "Subsidized Fertilizer Availability",
                date: "2023-08-05",
                content: "Government subsidized urea is now available for registered members. Bring your membership card and original CNIC to claim your quota.",
                image: null
            }
        ];

        let isAdmin = false;

        // --- Navigation ---
        function showSection(sectionId) {
            const sections = ['home', 'about', 'updates', 'contact', 'admin-login', 'admin-dashboard'];
            
            // Hide all
            sections.forEach(id => {
                const el = document.getElementById(id);
                if (el) el.classList.add('hidden');
            });

            // Show selected
            document.getElementById(sectionId).classList.remove('hidden');

            // Mobile menu close
            const mobileMenu = document.getElementById('mobile-menu');
            if(mobileMenu) mobileMenu.classList.add('hidden');

            // Scroll top
            window.scrollTo(0,0);

            // Context specific rendering
            if (sectionId === 'updates') {
                renderNews();
            }
            if (sectionId === 'admin-dashboard') {
                if (!isAdmin) {
                    showSection('admin-login');
                } else {
                    renderAdminDashboard();
                }
            }
        }

        function toggleAdmin() {
            if (isAdmin) {
                showSection('admin-dashboard');
            } else {
                showSection('admin-login');
            }
        }

        // --- Authentication ---
        function handleLogin(e) {
            e.preventDefault();
            const user = document.getElementById('username').value;
            const pass = document.getElementById('password').value;

            // Updated Secure Credentials
            if (user === 'sajjad' && pass === 'sajjad1985') {
                isAdmin = true;
                // Clear fields
                document.getElementById('username').value = '';
                document.getElementById('password').value = '';
                
                // Update UI
                const adminBtn = document.getElementById('adminBtn');
                adminBtn.innerText = "Dashboard";
                adminBtn.classList.remove('bg-green-800');
                adminBtn.classList.add('bg-blue-600');
                
                showSection('admin-dashboard');
            } else {
                alert('Invalid Username or Password. Access Denied.');
            }
        }

        function logout() {
            isAdmin = false;
            
            // Reset UI
            const adminBtn = document.getElementById('adminBtn');
            adminBtn.innerText = "Admin Panel";
            adminBtn.classList.remove('bg-blue-600');
            adminBtn.classList.add('bg-green-800');
            
            showSection('home');
            alert('Logged out successfully');
        }

        // --- Content Rendering & Logic ---
        function renderSiteContent() {
            // Apply config to DOM elements
            const logoImg = document.getElementById('display-logo-img');
            const logoIcon = document.getElementById('display-logo-icon');
            const adminLogoPreview = document.getElementById('admin-logo-preview');

            const logoPreviewContainer = document.getElementById('logo-preview-container');

            if (siteConfig.logoImage) {
                if(logoImg) {
                    logoImg.src = siteConfig.logoImage;
                    logoImg.classList.remove('hidden');
                }
                if(logoIcon) logoIcon.classList.add('hidden');
                
                if(adminLogoPreview) {
                    adminLogoPreview.src = siteConfig.logoImage;
                }
                if(logoPreviewContainer) logoPreviewContainer.classList.remove('hidden');
            } else {
                if(logoImg) logoImg.classList.add('hidden');
                if(logoIcon) logoIcon.classList.remove('hidden');
                if(logoPreviewContainer) logoPreviewContainer.classList.add('hidden');
            }

            const heroTitle = document.getElementById('display-hero-title');
            const heroText = document.getElementById('display-hero-text');
            const aboutText = document.getElementById('display-about-text');
            
            if(heroTitle) heroTitle.innerText = siteConfig.heroTitle;
            if(heroText) heroText.innerText = siteConfig.heroText;
            if(aboutText) aboutText.innerText = siteConfig.aboutText;
            
            // Class based updates for multiple instances
            document.querySelectorAll('.display-phone').forEach(el => el.innerText = siteConfig.contactPhone);
            document.querySelectorAll('.display-email').forEach(el => el.innerText = siteConfig.contactEmail);
            document.querySelectorAll('.display-address').forEach(el => el.innerText = siteConfig.contactAddress);

            // Render Live Data
            const ticker = document.getElementById('display-ticker');
            if(ticker) ticker.innerText = siteConfig.marketRates;

            const waterStatusText = document.getElementById('display-water-status');
            const waterIndicator = document.getElementById('water-status-indicator');
            const waterPing = document.getElementById('water-status-ping');
            
            if(waterStatusText) {
                waterStatusText.innerText = siteConfig.waterStatus;
                
                // Reset classes
                waterIndicator.className = "w-4 h-4 rounded-full shadow-[0_0_15px_rgba(0,0,0,0.5)]";
                waterPing.className = "absolute top-0 left-0 w-4 h-4 rounded-full animate-ping opacity-75";

                if(siteConfig.waterStatusColor === 'green') {
                    waterIndicator.classList.add('bg-green-500', 'shadow-[0_0_15px_rgba(34,197,94,0.8)]');
                    waterPing.classList.add('bg-green-500');
                } else if (siteConfig.waterStatusColor === 'yellow') {
                    waterIndicator.classList.add('bg-yellow-500', 'shadow-[0_0_15px_rgba(234,179,8,0.8)]');
                    waterPing.classList.add('bg-yellow-500');
                } else {
                    waterIndicator.classList.add('bg-red-500', 'shadow-[0_0_15px_rgba(239,68,68,0.8)]');
                    waterPing.classList.add('bg-red-500');
                }
            }
        }

        function renderFeatures() {
            const container = document.getElementById('features-container');
            if(!container) return;
            container.innerHTML = '';
            
            featuresData.forEach(feature => {
                // Determine styling based on color
                let colorClass = "border-emerald-500";
                let bgClass = "bg-emerald-50 group-hover:bg-emerald-100";
                let shadowClass = "hover:shadow-[0_20px_40px_rgba(16,185,129,0.2)]";
                
                if(feature.color === 'amber') {
                    colorClass = "border-amber-500";
                    bgClass = "bg-amber-50 group-hover:bg-amber-100";
                    shadowClass = "hover:shadow-[0_20px_40px_rgba(245,158,11,0.2)]";
                } else if(feature.color === 'red') {
                    colorClass = "border-red-600";
                    bgClass = "bg-red-50 group-hover:bg-red-100";
                    shadowClass = "hover:shadow-[0_20px_40px_rgba(220,38,38,0.2)]";
                } else if(feature.color === 'blue') {
                    colorClass = "border-blue-500";
                    bgClass = "bg-blue-50 group-hover:bg-blue-100";
                    shadowClass = "hover:shadow-[0_20px_40px_rgba(59,130,246,0.2)]";
                }

                const card = `
                    <div class="p-6 glass-card bg-white/95 rounded-2xl shadow-2xl ${shadowClass} transition-all duration-500 transform hover:-translate-y-3 group border-t-4 ${colorClass}">
                        <div class="text-5xl mb-6 ${bgClass} w-20 h-20 mx-auto rounded-full flex items-center justify-center transition">${feature.icon}</div>
                        <h3 class="text-xl font-bold mb-3 text-emerald-900 font-serif">${feature.title}</h3>
                        <p class="text-gray-600 text-sm leading-relaxed">${feature.text}</p>
                    </div>
                `;
                container.innerHTML += card;
            });
        }

        function renderNews() {
            const container = document.getElementById('news-container');
            container.innerHTML = '';

            if (newsData.length === 0) {
                container.innerHTML = '<div class="text-center py-10 text-gray-500">No updates currently available.</div>';
                return;
            }

            const sortedNews = [...newsData].sort((a, b) => new Date(b.date) - new Date(a.date));

            sortedNews.forEach(news => {
                let attachmentHtml = '';
                if (news.image) {
                    if (news.image.startsWith('data:application/pdf')) {
                        attachmentHtml = `
                            <div class="bg-green-50 p-6 flex items-center justify-center border-b border-green-100">
                                <div class="text-center">
                                    <span class="text-4xl block mb-2">📄</span>
                                    <a href="${news.image}" download="${news.title}.pdf" class="text-green-700 font-bold hover:underline hover:text-green-900 transition">Download PDF Document</a>
                                </div>
                            </div>`;
                    } else {
                        attachmentHtml = `<img src="${news.image}" class="w-full h-48 object-cover" alt="${news.title}">`;
                    }
                }
                
                const newsCard = `
                    <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition duration-300 border-l-4 border-green-600">
                        ${attachmentHtml}
                        <div class="p-6">
                            <div class="flex items-center justify-between mb-4">
                                <h3 class="text-xl font-bold text-gray-800">${news.title}</h3>
                                <div class="text-sm font-semibold text-green-800 bg-green-100 px-3 py-1 rounded-full">
                                    ${news.date}
                                </div>
                            </div>
                            <p class="text-gray-600 leading-relaxed">${news.content}</p>
                        </div>
                    </div>
                `;
                container.innerHTML += newsCard;
            });
        }

        // --- Admin Functions ---
        function renderAdminDashboard() {
            // Render News List
            renderAdminNewsList();
            renderAdminFeaturesList();
            
            // Populate Content Forms with current data
            document.getElementById('edit-hero-title').value = siteConfig.heroTitle;
            document.getElementById('edit-hero-text').value = siteConfig.heroText;
            document.getElementById('edit-about-text').value = siteConfig.aboutText;
            document.getElementById('edit-phone').value = siteConfig.contactPhone;
            document.getElementById('edit-email').value = siteConfig.contactEmail;
            document.getElementById('edit-address').value = siteConfig.contactAddress;
            
            // Populate Live Data
            document.getElementById('edit-market-rates').value = siteConfig.marketRates;
            document.getElementById('edit-water-status-text').value = siteConfig.waterStatus;
            document.getElementById('edit-water-status-type').value = siteConfig.waterStatusColor;
        }

        function updateWaterStatusLabel() {
            const type = document.getElementById('edit-water-status-type').value;
            const textInput = document.getElementById('edit-water-status-text');
            if(type === 'green') textInput.value = "Full Flow";
            if(type === 'yellow') textInput.value = "Rotation";
            if(type === 'red') textInput.value = "Shortage";
        }

        function saveLiveSettings(e) {
            e.preventDefault();
            siteConfig.marketRates = document.getElementById('edit-market-rates').value;
            siteConfig.waterStatus = document.getElementById('edit-water-status-text').value;
            siteConfig.waterStatusColor = document.getElementById('edit-water-status-type').value;

            renderSiteContent();
            alert('Live data updated successfully!');
        }

        function saveSiteSettings(e) {
            e.preventDefault();
            
            const logoInput = document.getElementById('edit-logo');
            
            const finishSave = () => {
                // Update config object
                siteConfig.heroTitle = document.getElementById('edit-hero-title').value;
                siteConfig.heroText = document.getElementById('edit-hero-text').value;
                siteConfig.aboutText = document.getElementById('edit-about-text').value;
                siteConfig.contactPhone = document.getElementById('edit-phone').value;
                siteConfig.contactEmail = document.getElementById('edit-email').value;
                siteConfig.contactAddress = document.getElementById('edit-address').value;
                
                // Re-render public views
                renderSiteContent();
                
                alert('Website settings updated successfully! Changes are live in this session.');
            };

            if (logoInput.files && logoInput.files[0]) {
                const reader = new FileReader();
                reader.onload = function(evt) {
                    siteConfig.logoImage = evt.target.result;
                    finishSave();
                };
                reader.readAsDataURL(logoInput.files[0]);
            } else {
                finishSave();
            }
        }

        function renderAdminNewsList() {
            const tbody = document.getElementById('admin-news-list');
            tbody.innerHTML = '';

            const sortedNews = [...newsData].sort((a, b) => new Date(b.date) - new Date(a.date));

            sortedNews.forEach(news => {
                const row = `
                    <tr class="hover:bg-gray-50 transition">
                        <td class="px-3 py-3 border-b border-gray-200 text-sm font-medium text-gray-900">
                            <div class="flex items-center">
                                <span>${news.title}</span>
                                ${news.image ? '<span class="ml-2 text-green-600" title="Has Attachment">📎</span>' : ''}
                            </div>
                        </td>
                        <td class="px-3 py-3 border-b border-gray-200 text-sm text-gray-500">
                            ${news.date}
                        </td>
                        <td class="px-3 py-3 border-b border-gray-200 text-sm text-right">
                            <button onclick="deleteNews(${news.id})" class="text-red-600 hover:text-red-900 bg-red-50 hover:bg-red-100 px-3 py-1 rounded-md transition">Delete</button>
                        </td>
                    </tr>
                `;
                tbody.innerHTML += row;
            });
        }

        function updateFileName() {
            const input = document.getElementById('newsImage');
            const fileNameDisplay = document.getElementById('fileName');
            if (input.files && input.files[0]) {
                fileNameDisplay.textContent = "Selected: " + input.files[0].name;
                fileNameDisplay.classList.remove('hidden');
            } else {
                fileNameDisplay.classList.add('hidden');
            }
        }

        function previewLogo() {
            const input = document.getElementById('edit-logo');
            const preview = document.getElementById('admin-logo-preview');
            const container = document.getElementById('logo-preview-container');
            
            if (input.files && input.files[0]) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    preview.src = e.target.result;
                    container.classList.remove('hidden');
                };
                reader.readAsDataURL(input.files[0]);
            }
        }

        function addNews(e) {
            e.preventDefault();
            const title = document.getElementById('newsTitle').value;
            const date = document.getElementById('newsDate').value;
            const content = document.getElementById('newsContent').value;
            const imageInput = document.getElementById('newsImage');
            const file = imageInput.files[0];

            if(!title || !date || !content) {
                alert("Please fill in all required fields (Title, Date, Content)");
                return;
            }

            const processNews = (imgSrc) => {
                const newPost = {
                    id: Date.now(),
                    title,
                    date,
                    content,
                    image: imgSrc || null
                };

                newsData.push(newPost);
                
                // Clear inputs
                document.getElementById('newsTitle').value = '';
                document.getElementById('newsDate').value = '';
                document.getElementById('newsContent').value = '';
                document.getElementById('newsImage').value = ''; // Reset file input
                document.getElementById('fileName').textContent = '';
                document.getElementById('fileName').classList.add('hidden');

                alert('Update Published Successfully!');
                renderAdminNewsList();
                renderNews(); // Update public view immediately
            };

            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    processNews(e.target.result);
                };
                reader.readAsDataURL(file);
            } else {
                processNews(null);
            }
        }

        function deleteNews(id) {
            if(confirm('Are you sure you want to delete this update?')) {
                newsData = newsData.filter(news => news.id !== id);
                renderAdminNewsList();
            }
        }

        function renderAdminFeaturesList() {
            const tbody = document.getElementById('admin-features-list');
            if(!tbody) return;
            tbody.innerHTML = '';

            featuresData.forEach(feature => {
                const row = `
                    <tr class="hover:bg-gray-50 transition">
                        <td class="px-3 py-3 border-b border-gray-200 text-sm font-medium text-gray-900 text-left">
                            <span class="text-xl mr-2">${feature.icon}</span> ${feature.title}
                        </td>
                        <td class="px-3 py-3 border-b border-gray-200 text-sm text-gray-500 text-left">
                            <span class="inline-block w-3 h-3 rounded-full bg-${feature.color === 'emerald' ? 'emerald-500' : feature.color === 'amber' ? 'amber-500' : feature.color === 'red' ? 'red-600' : 'blue-500'}"></span>
                        </td>
                        <td class="px-3 py-3 border-b border-gray-200 text-sm text-right">
                            <button onclick="deleteFeature(${feature.id})" class="text-red-600 hover:text-red-900 bg-red-50 hover:bg-red-100 px-3 py-1 rounded-md transition">Delete</button>
                        </td>
                    </tr>
                `;
                tbody.innerHTML += row;
            });
        }

        function addFeature(e) {
            e.preventDefault();
            const title = document.getElementById('featureTitle').value;
            const icon = document.getElementById('featureIcon').value;
            const text = document.getElementById('featureText').value;
            const color = document.getElementById('featureColor').value;

            if(!title || !icon || !text) {
                alert("Please fill in all fields");
                return;
            }

            const newFeature = {
                id: Date.now(),
                title,
                icon,
                text,
                color
            };

            featuresData.push(newFeature);
            
            // Clear inputs
            document.getElementById('featureTitle').value = '';
            document.getElementById('featureIcon').value = '🌟';
            document.getElementById('featureText').value = '';
            
            alert('Feature Added Successfully!');
            renderAdminFeaturesList();
            renderFeatures();
        }

        function deleteFeature(id) {
            if(confirm('Are you sure you want to delete this feature?')) {
                featuresData = featuresData.filter(f => f.id !== id);
                renderAdminFeaturesList();
                renderFeatures();
            }
        }

        // --- Initialization ---
        window.onload = function() {
            renderSiteContent();
            renderFeatures();
            showSection('home');
        };

    </script>
</body>
</html>
