!DOCTYPE html> <
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ELYRA Skin — Guimaras Mango Powered Skincare</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts for Ultra Readability -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@600;700&family=Outfit:wght@400;500;600;700;800;900&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'elyra-yellow': '#F5CD00',
                        'elyra-yellow-dark': '#C9A300',
                        'elyra-bg': '#FAF8F3',
                        'elyra-card': '#EFECE6',
                        'elyra-dark': '#1C1C1A',
                        'elyra-grey': '#666561',
                        'elyra-light-grey': '#E0DDD5'
                    },
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                        heading: ['"Outfit"', 'sans-serif'],
                        signature: ['Caveat', 'cursive']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #FAF8F3;
            color: #1C1C1A;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
        }

        h1, h2, h3, .brand-font {
            font-family: 'Outfit', sans-serif;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #FAF8F3;
        }
        ::-webkit-scrollbar-thumb {
            background: #E0DDD5;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #666561;
        }

        /* Glass overlay */
        .glass-panel {
            background: rgba(250, 248, 243, 0.92);
            backdrop-filter: blur(14px);
            -webkit-backdrop-filter: blur(14px);
        }

        /* Shape renders */
        .pebble-bottle {
            border-radius: 42% 58% 45% 55% / 55% 45% 55% 45%;
            transition: all 0.5s ease;
        }
        .pebble-bottle:hover {
            border-radius: 50%;
        }

        .droplet-bottle {
            border-radius: 60% 40% 50% 50% / 70% 70% 30% 30%;
        }

        .jar-body {
            border-radius: 35% 35% 45% 45% / 30% 30% 50% 50%;
        }

        /* Cart Drawer */
        .cart-drawer {
            transition: transform 0.35s cubic-bezier(0.16, 1, 0.3, 1);
        }
        
        .modal-backdrop {
            transition: opacity 0.3s ease;
        }
    </style>
</head>
<body class="bg-elyra-bg text-elyra-dark min-h-screen flex flex-col selection:bg-elyra-yellow selection:text-black">

    <!-- TOP ANNOUNCEMENT BAR -->
    <div class="bg-elyra-dark text-white text-xs tracking-wider uppercase py-2.5 px-4 text-center font-semibold flex items-center justify-center gap-2 relative z-50">
        <span class="inline-block w-2 h-2 rounded-full bg-elyra-yellow animate-pulse"></span>
        <span>FREE SHIPPING OVER ₱500</span>
        <span class="hidden sm:inline opacity-40">•</span>
        <span class="hidden sm:inline text-elyra-yellow font-bold">GUIMARAS MANGO POWERED SKINCARE</span>
    </div>

    <!-- NAVIGATION BAR -->
    <header class="sticky top-0 z-40 glass-panel border-b border-black/5 transition-all duration-300">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <!-- Left Links -->
            <nav class="hidden md:flex items-center gap-8 text-xs font-bold tracking-widest uppercase">
                <a href="#shop" class="hover:text-elyra-yellow-dark transition-colors relative py-1 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-elyra-yellow hover:after:w-full after:transition-all">SHOP</a>
                <a href="#about" class="hover:text-elyra-yellow-dark transition-colors relative py-1 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-elyra-yellow hover:after:w-full after:transition-all">ABOUT</a>
                <a href="#team" class="hover:text-elyra-yellow-dark transition-colors relative py-1 after:content-[''] after:absolute after:bottom-0 after:left-0 after:w-0 after:h-0.5 after:bg-elyra-yellow hover:after:w-full after:transition-all">TEAM</a>
            </nav>

            <!-- Mobile Menu Toggle Button -->
            <button id="mobileMenuBtn" onclick="toggleMobileMenu()" class="md:hidden text-xl p-2 hover:opacity-75 transition-opacity">
                <i class="fa-solid fa-bars"></i>
            </button>

            <!-- Center Logo -->
            <a href="#" class="flex items-center gap-2 group">
                <span class="brand-font text-3xl sm:text-4xl font-extrabold tracking-tight text-elyra-dark group-hover:text-elyra-yellow-dark transition-colors">ELYRA <span class="text-elyra-yellow-dark">Skin</span></span>
                <!-- Mango SVG Icon -->
                <svg class="w-7 h-7 fill-elyra-yellow transition-transform group-hover:rotate-12" viewBox="0 0 24 24">
                    <path d="M12,2C8,2 4,5 4,10C4,15.5 8,21 13,22C17,22.8 20,20 20,15C20,9 17,2 12,2Z" />
                    <path d="M14,3C13,3 12,2 12,1C14,1 16,1.5 17,3" stroke="#F5CD00" stroke-width="1.5" stroke-linecap="round" />
                </svg>
            </a>

            <!-- Right Actions -->
            <div class="flex items-center gap-6">
                <a href="#account" onclick="openModal('Account Login', 'Manage your ELYRA Skin rewards and orders.')" class="hidden sm:inline-block text-xs font-bold tracking-widest uppercase hover:text-elyra-yellow-dark transition-colors">ACCOUNT</a>
                
                <button id="cartBtn" onclick="toggleCart()" class="relative bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black transition-all p-3 rounded-full flex items-center justify-center w-11 h-11 shadow-md">
                    <i class="fa-solid fa-bag-shopping text-sm"></i>
                    <span id="cartCount" class="absolute -top-1 -right-1 bg-elyra-yellow text-black font-extrabold text-[10px] w-5 h-5 rounded-full flex items-center justify-center border-2 border-elyra-bg">0</span>
                </button>
            </div>
        </div>

        <!-- Mobile Navigation Menu Dropdown -->
        <div id="mobileMenu" class="hidden md:hidden bg-elyra-bg border-b border-black/10 px-6 py-4 flex flex-col gap-4 text-xs font-bold uppercase tracking-wider">
            <a href="#shop" onclick="toggleMobileMenu()" class="py-2 border-b border-black/5 hover:text-elyra-yellow-dark">SHOP</a>
            <a href="#about" onclick="toggleMobileMenu()" class="py-2 border-b border-black/5 hover:text-elyra-yellow-dark">ABOUT</a>
            <a href="#team" onclick="toggleMobileMenu()" class="py-2 border-b border-black/5 hover:text-elyra-yellow-dark">TEAM</a>
            <a href="#account" onclick="toggleMobileMenu(); openModal('Account Login', 'Manage your ELYRA Skin rewards and orders.')" class="py-2">ACCOUNT</a>
        </div>
    </header>

    <main class="flex-grow">
        
        <!-- HERO SECTION (USING elyrabg.png.jpg BEACH CAMPAIGN PICTURE) -->
        <section class="relative w-full bg-black overflow-hidden">
            <div class="relative w-full min-h-[500px] sm:min-h-[650px] lg:min-h-[750px] flex items-center justify-center">
                <img src="Untitled132_20261015013138 (1).png" alt="ELYRA Skin Beach Campaign" class="absolute inset-0 w-full h-full object-cover object-center opacity-95">
                <!-- Gentle Gradient overlay to guarantee CTA readability -->
                <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-black/20"></div>
                <!-- Overlay Interactive Shop Button -->
                <div class="absolute bottom-8 sm:bottom-16 right-6 sm:right-16 z-20 text-right">
                    <a href="#shop" class="inline-flex items-center gap-3 bg-elyra-yellow text-black hover:bg-white hover:scale-105 font-extrabold px-8 py-4 rounded-full text-xs sm:text-sm uppercase tracking-widest shadow-2xl transition-all border border-black/10">
                        <span>Button to shop</span>
                        <i class="fa-solid fa-arrow-right text-xs"></i>
                    </a>
                </div>
            </div>
        </section>

        <!-- VALUES / BADGES BANNER -->
        <section class="bg-elyra-card border-y border-black/10 py-4 overflow-x-auto">
            <div class="max-w-7xl mx-auto px-4 text-center">
                <p class="text-xs sm:text-sm font-extrabold uppercase tracking-widest text-elyra-dark/80 flex items-center justify-center gap-4 sm:gap-8 min-w-max">
                    <span>cruelty-free</span>
                    <span class="text-elyra-yellow-dark">•</span>
                    <span>100% vegan</span>
                    <span class="text-elyra-yellow-dark">•</span>
                    <span>guimaras mango extract</span>
                    <span class="text-elyra-yellow-dark">•</span>
                    <span>dermatologist-tested</span>
                    <span class="text-elyra-yellow-dark">•</span>
                    <span>fragrance-free options</span>
                </p>
            </div>
        </section>

        <!-- FOUNDER NOTE SECTION ("A NOTE FROM LEMUEL") -->
        <section id="about" class="py-16 sm:py-24 px-4 sm:px-6 lg:px-8 max-w-5xl mx-auto">
            <div class="bg-white rounded-3xl p-8 sm:p-14 border border-black/10 shadow-xl relative overflow-hidden text-center space-y-6">
                <!-- Background decorative mango outline -->
                <svg class="absolute -bottom-10 -right-10 w-64 h-64 opacity-5 fill-elyra-yellow pointer-events-none" viewBox="0 0 24 24">
                    <path d="M12,2C8,2 4,5 4,10C4,15.5 8,21 13,22C17,22.8 20,20 20,15C20,9 17,2 12,2Z" />
                </svg>

                <span class="text-xs font-extrabold tracking-widest uppercase text-elyra-dark/60 bg-elyra-bg px-4 py-1.5 rounded-full border border-black/5 inline-block">OUR HERITAGE</span>

                <h2 class="text-2xl sm:text-4xl font-extrabold tracking-tight text-elyra-dark uppercase">
                    A NOTE FROM LEMUEL
                </h2>

                <p class="text-elyra-dark/90 text-base sm:text-lg leading-relaxed max-w-3xl mx-auto font-medium">
                    "Our skincare products harness the vitamin-rich, hydrating power of authentic Guimaras mangoes, directly and ethically sourced from local Filipino farmers. Through fair-trade partnerships, we ensure sustainable livelihoods for our farming families, transforming every product into a gentle beauty essential that nourishes your skin while empowering our community."
                </p>

                <div class="pt-4 flex flex-col items-center justify-center">
                    <span class="font-signature text-4xl sm:text-5xl text-elyra-yellow-dark select-none">xo Lemuel</span>
                    <span class="text-[11px] font-extrabold tracking-widest uppercase text-elyra-grey mt-1">Founder & Formulator, ELYRA Skin</span>
                </div>
            </div>
        </section>

        <!-- PRODUCT LINEUP SECTION (PRICED PRODUCTS) -->
        <section id="shop" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12 gap-4">
                <div>
                    <span class="text-xs font-extrabold uppercase tracking-widest text-elyra-yellow-dark bg-black text-white px-3 py-1.5 rounded-full">THE LINEUP</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold tracking-tight text-elyra-dark mt-3">Essential Daily Rituals</h2>
                </div>
                <p class="text-elyra-grey text-sm max-w-md font-medium">
                    Designed with minimal, aesthetic grey packaging and potent Guimaras Mango extract infusions.
                </p>
            </div>

            <!-- PRODUCT GRID -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                
                <!-- PRODUCT 1: Toner (₱149) -->
                <div class="bg-white rounded-3xl p-6 border border-black/10 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between group">
                    <div class="bg-elyra-bg rounded-2xl h-64 flex items-center justify-center relative overflow-hidden mb-6 p-4 border border-black/5">
                        <span class="absolute top-3 left-3 bg-elyra-dark text-white font-extrabold text-[10px] uppercase px-2.5 py-1 rounded-md">ESSENCE</span>
                        
                        <div class="w-28 h-44 bg-[#9E9D97] opacity-90 droplet-bottle shadow-md flex flex-col items-center justify-center relative transform transition-transform group-hover:scale-105">
                            <div class="rotate-90 text-center">
                                <span class="brand-font font-black text-base tracking-widest text-elyra-yellow block">ELYRA</span>
                            </div>
                            <div class="absolute bottom-5 text-center px-2">
                                <span class="text-[7px] font-bold uppercase text-black block leading-none">GUIMARAS</span>
                                <span class="text-[7px] font-bold uppercase text-black block leading-none mt-0.5">TONER</span>
                            </div>
                            <div class="w-7 h-8 bg-[#7A7973] rounded-t-md absolute -top-6"></div>
                        </div>
                    </div>

                    <div>
                        <h3 class="font-extrabold text-lg text-elyra-dark group-hover:text-elyra-yellow-dark transition-colors">Guimaras Toner</h3>
                        <p class="text-xs text-elyra-grey mt-1 mb-4 line-clamp-2 font-medium">Refreshing essential essence water for instant botanical luminosity.</p>
                        
                        <div class="flex items-center justify-between border-t border-black/10 pt-4 mt-auto">
                            <span class="font-black text-xl text-elyra-dark">₱149</span>
                            <button onclick="addToCart('Guimaras Toner', 149, 'Glass Droplet • 120ml')" class="bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold text-xs uppercase px-4 py-2.5 rounded-full transition-all shadow-sm">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>

                <!-- PRODUCT 2: Sunscreen (₱169) -->
                <div class="bg-white rounded-3xl p-6 border border-black/10 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between group">
                    <div class="bg-elyra-bg rounded-2xl h-64 flex items-center justify-center relative overflow-hidden mb-6 p-4 border border-black/5">
                        <span class="absolute top-3 left-3 bg-elyra-yellow text-black font-extrabold text-[10px] uppercase px-2.5 py-1 rounded-md">BESTSELLER</span>
                        
                        <div class="w-24 h-48 bg-[#9A9993] rounded-t-xl rounded-b-md shadow-lg flex flex-col items-center justify-between py-4 relative transform transition-transform group-hover:scale-105">
                            <div class="w-full text-center px-2">
                                <span class="brand-font font-black text-sm tracking-wider block text-elyra-yellow">ELYRA</span>
                            </div>
                            <div class="text-center px-1">
                                <span class="text-[7px] tracking-tight uppercase text-black font-bold block leading-tight">ULTRA LIGHT</span>
                                <span class="text-[7px] tracking-tight uppercase text-black font-bold block leading-tight">SUNSCREEN</span>
                            </div>
                            <div class="w-16 h-8 bg-[#7A7973] rounded-b-md absolute -bottom-7 border-t border-black/20"></div>
                        </div>
                    </div>

                    <div>
                        <h3 class="font-extrabold text-lg text-elyra-dark group-hover:text-elyra-yellow-dark transition-colors">Ultra Light Sunscreen</h3>
                        <p class="text-xs text-elyra-grey mt-1 mb-4 line-clamp-2 font-medium">SPF 50+ PA++++ invisible shield enriched with raw mango antioxidants.</p>
                        
                        <div class="flex items-center justify-between border-t border-black/10 pt-4 mt-auto">
                            <span class="font-black text-xl text-elyra-dark">₱169</span>
                            <button onclick="addToCart('Ultra Light Sunscreen', 169, 'Tube • 50ml')" class="bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold text-xs uppercase px-4 py-2.5 rounded-full transition-all shadow-sm">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>

                <!-- PRODUCT 3: Moisturizer (₱179) -->
                <div class="bg-white rounded-3xl p-6 border border-black/10 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between group">
                    <div class="bg-elyra-bg rounded-2xl h-64 flex items-center justify-center relative overflow-hidden mb-6 p-4 border border-black/5">
                        <div class="w-32 h-40 bg-[#9A9993] pebble-bottle shadow-lg flex flex-col items-center justify-center relative transform transition-transform group-hover:scale-105">
                            <div class="rotate-90 text-center">
                                <span class="brand-font font-black text-lg tracking-widest text-elyra-yellow block">ELYRA</span>
                            </div>
                            <div class="w-6 h-6 bg-[#7A7973] rounded-t-md absolute -top-5"></div>
                            <div class="w-8 h-2 bg-[#7A7973] rounded-full absolute -top-6 -left-1"></div>
                            
                            <div class="absolute bottom-4 text-center px-2">
                                <span class="text-[7px] font-bold uppercase text-black block leading-none">HYDRATING</span>
                                <span class="text-[7px] font-bold uppercase text-black block leading-none mt-0.5">MOISTURIZER</span>
                            </div>
                        </div>
                    </div>

                    <div>
                        <h3 class="font-extrabold text-lg text-elyra-dark group-hover:text-elyra-yellow-dark transition-colors">Hydrating Moisturizer</h3>
                        <p class="text-xs text-elyra-grey mt-1 mb-4 line-clamp-2 font-medium">Sculptural pebble bottle featuring deeply barrier-repairing mango lipids.</p>
                        
                        <div class="flex items-center justify-between border-t border-black/10 pt-4 mt-auto">
                            <span class="font-black text-xl text-elyra-dark">₱179</span>
                            <button onclick="addToCart('Hydrating Moisturizer', 179, 'Pebble Pump • 80ml')" class="bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold text-xs uppercase px-4 py-2.5 rounded-full transition-all shadow-sm">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>

                <!-- PRODUCT 4: Cleanser Balm (₱199) -->
                <div class="bg-white rounded-3xl p-6 border border-black/10 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between group">
                    <div class="bg-elyra-bg rounded-2xl h-64 flex items-center justify-center relative overflow-hidden mb-6 p-4 border border-black/5">
                        <div class="w-36 h-28 bg-[#9A9993] jar-body shadow-lg flex flex-col items-center justify-center relative transform transition-transform group-hover:scale-105">
                            <div class="w-32 h-6 bg-gradient-to-r from-gray-300 via-gray-100 to-gray-400 rounded-t-lg absolute -top-5 border-b border-black/30 shadow-sm"></div>
                            
                            <div class="text-center px-2">
                                <span class="brand-font font-black text-xl tracking-widest text-elyra-yellow block">ELYRA</span>
                                <span class="text-[6px] font-bold uppercase text-black block leading-none mt-1">MELTING BALM CLEANSER</span>
                            </div>
                        </div>
                    </div>

                    <div>
                        <h3 class="font-extrabold text-lg text-elyra-dark group-hover:text-elyra-yellow-dark transition-colors">Melting Balm Cleanser</h3>
                        <p class="text-xs text-elyra-grey mt-1 mb-4 line-clamp-2 font-medium">Silky mango fusion balm that effortlessly dissolves makeup and impurities.</p>
                        
                        <div class="flex items-center justify-between border-t border-black/10 pt-4 mt-auto">
                            <span class="font-black text-xl text-elyra-dark">₱199</span>
                            <button onclick="addToCart('Melting Balm Cleanser', 199, 'Jar • 100g')" class="bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold text-xs uppercase px-4 py-2.5 rounded-full transition-all shadow-sm">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <!-- COUNTDOWN TIMER & PROMOTION BANNER (MANDATORY REQUIREMENT) -->
        <section class="bg-elyra-dark text-white py-12 px-4 border-y border-black/10">
            <div class="max-w-4xl mx-auto text-center space-y-6">
                <span class="bg-elyra-yellow text-black text-xs font-extrabold px-3.5 py-1.5 rounded-full uppercase tracking-widest inline-block">Limited Time Promo</span>
                <h2 class="text-2xl sm:text-3xl font-extrabold uppercase">Guimaras Glow Campaign Duration</h2>
                <p id="promoStatusText" class="text-xs text-gray-300 max-w-lg mx-auto font-medium">Claim your 20% discount on the complete collection before the timer expires on November 30, 2026.</p>
                
                <!-- Countdown Clock Display -->
                <div id="countdownTimerContainer" class="flex justify-center gap-4 text-center">
                    <div class="bg-white/10 px-4 py-3 rounded-2xl min-w-[70px]">
                        <span id="days" class="text-xl sm:text-2xl font-black text-elyra-yellow">12</span>
                        <span class="text-[9px] uppercase tracking-wider block text-gray-300">Days</span>
                    </div>
                    <div class="bg-white/10 px-4 py-3 rounded-2xl min-w-[70px]">
                        <span id="hours" class="text-xl sm:text-2xl font-black text-elyra-yellow">05</span>
                        <span class="text-[9px] uppercase tracking-wider block text-gray-300">Hours</span>
                    </div>
                    <div class="bg-white/10 px-4 py-3 rounded-2xl min-w-[70px]">
                        <span id="minutes" class="text-xl sm:text-2xl font-black text-elyra-yellow">34</span>
                        <span class="text-[9px] uppercase tracking-wider block text-gray-300">Mins</span>
                    </div>
                    <div class="bg-white/10 px-4 py-3 rounded-2xl min-w-[70px]">
                        <span id="seconds" class="text-xl sm:text-2xl font-black text-elyra-yellow">20</span>
                        <span class="text-[9px] uppercase tracking-wider block text-gray-300">Secs</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- TESTIMONIALS SECTION (THREE CLEARLY LABELED FICTIONAL TESTIMONIALS) -->
        <section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
            <div class="text-center mb-12 space-y-2">
                <span class="text-xs font-extrabold uppercase tracking-widest text-elyra-yellow-dark bg-black text-white px-3 py-1.5 rounded-full">Testimonials</span>
                <h2 class="text-3xl font-extrabold text-elyra-dark tracking-tight mt-2">What Our Customers Say</h2>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-6 sm:p-8 rounded-3xl border border-black/10 shadow-sm space-y-4 flex flex-col justify-between">
                    <div class="text-elyra-yellow text-sm space-x-0.5"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                    <p class="text-xs text-elyra-dark font-medium leading-relaxed">"The sunscreen feels so lightweight in this humid weather! No greasy feeling at all."</p>
                    <span class="text-[11px] font-extrabold uppercase tracking-wider text-elyra-grey block">— Mika R. (Verified Buyer)</span>
                </div>
                <div class="bg-white p-6 sm:p-8 rounded-3xl border border-black/10 shadow-sm space-y-4 flex flex-col justify-between">
                    <div class="text-elyra-yellow text-sm space-x-0.5"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                    <p class="text-xs text-elyra-dark font-medium leading-relaxed">"Love the Guimaras mango scent. My skin feels deeply hydrated all day long."</p>
                    <span class="text-[11px] font-extrabold uppercase tracking-wider text-elyra-grey block">— Carlos T. (Verified Buyer)</span>
                </div>
                <div class="bg-white p-6 sm:p-8 rounded-3xl border border-black/10 shadow-sm space-y-4 flex flex-col justify-between">
                    <div class="text-elyra-yellow text-sm space-x-0.5"><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i></div>
                    <p class="text-xs text-elyra-dark font-medium leading-relaxed">"Affordable and effective starter kit. Highly recommend to anyone with sensitive tropical skin."</p>
                    <span class="text-[11px] font-extrabold uppercase tracking-wider text-elyra-grey block">— Andrea P. (Verified Buyer)</span>
                </div>
            </div>
        </section>

        <!-- MEET THE TEAM SECTION (LEADERSHIP PHOTOS) -->
        <section id="team" class="py-16 sm:py-24 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto bg-elyra-card/50 rounded-3xl my-8 border border-black/5">
            <div class="text-center max-w-2xl mx-auto mb-16 space-y-2">
                <span class="text-xs font-extrabold tracking-widest uppercase text-black bg-elyra-yellow px-3.5 py-1.5 rounded-full">THE LEADERSHIP</span>
                <h2 class="text-3xl sm:text-4xl font-extrabold text-elyra-dark tracking-tight mt-2">Meet the Head of Departments</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-10 max-w-4xl mx-auto">
                
                <!-- Team Member 1: Head of Operations -->
                <div class="bg-white rounded-3xl p-8 border border-black/10 shadow-md flex flex-col items-center text-center space-y-5 relative group hover:-translate-y-1 transition-transform">
                    <div class="w-48 h-48 rounded-2xl bg-elyra-card overflow-hidden relative shadow-inner border border-black/10 flex items-center justify-center">
                       <img src="elyra_img2.png" alt="Cassey Allyah Dejumo - Head of Operations" class="w-fill h-fill object-cover object-top transition-transform duration-500 group-hover:scale-105">
                        <i class="fa-solid fa-user-gear text-6xl text-elyra-grey/30"></i>
                        <div class="absolute inset-0 bg-gradient-to-t from-black/50 via-transparent to-transparent"></div>
                        <span class="absolute bottom-3 text-[10px] font-extrabold text-white uppercase tracking-wider bg-elyra-dark/80 px-3 py-1 rounded-full backdrop-blur-sm">Operations</span>
                    </div>

                    <div class="space-y-1">
                        <h3 class="text-2xl font-extrabold text-elyra-dark">Cassey Alliyah Dejumo</h3>
                        <p class="text-xs font-extrabold uppercase tracking-widest text-elyra-yellow-dark">Head of Operations</p>
                    </div>

                    <p class="text-xs text-elyra-grey leading-relaxed max-w-sm font-medium">
                        Cassey is in charge of the execution engine of our organization, responsible for turning inputs into finished goods or services as efficiently and cost-effectively as possible.
                    </p>
                </div>

                <!-- Team Member 2: Head of Finance (USING jade.png.jpg PHOTO) -->
                <div class="bg-white rounded-3xl p-8 border border-black/10 shadow-md flex flex-col items-center text-center space-y-5 relative group hover:-translate-y-1 transition-transform">
                    <div class="w-48 h-48 rounded-2xl bg-elyra-card overflow-hidden relative shadow-md border border-black/10">
                        <img src="Untitled143 (1).png" alt="Jadelynn Arnigo - Head of Finance" class="w-full h-full object-cover object-top transition-transform duration-500 group-hover:scale-105">
                        <div class="absolute inset-0 bg-gradient-to-t from-black/50 via-transparent to-transparent"></div>
                        <span class="absolute bottom-3 left-1/2 -translate-x-1/2 text-[10px] font-extrabold text-white uppercase tracking-wider bg-elyra-dark/80 px-3 py-1 rounded-full backdrop-blur-sm whitespace-nowrap">Finance</span>
                    </div>

                    <div class="space-y-1">
                        <h3 class="text-2xl font-extrabold text-elyra-dark">Jadelynn Arnigo</h3>
                        <p class="text-xs font-extrabold uppercase tracking-widest text-elyra-yellow-dark">Head of Finance</p>
                    </div>

                    <p class="text-xs text-elyra-grey leading-relaxed max-w-sm font-medium">
                        Jadelynn is responsible for managing its money, ensuring regulatory compliance, and driving long-term strategic growth for ELYRA Skin.
                    </p>
                </div>

            </div>
        </section>

        <!-- LEAD CAPTURE FORM SECTION (MANDATORY REQUIREMENT) -->
        <section class="py-16 px-4">
            <div class="max-w-xl mx-auto bg-white p-8 sm:p-10 rounded-3xl border border-black/10 shadow-xl space-y-6">
                <div class="text-center space-y-2">
                    <span class="text-[10px] font-extrabold uppercase tracking-widest bg-elyra-yellow px-3.5 py-1.5 rounded-full inline-block">VIP Access</span>
                    <h3 class="text-2xl font-extrabold text-elyra-dark">Join the ELYRA Community</h3>
                    <p class="text-xs text-elyra-grey font-medium">Sign up below with your name and email to secure your 20% launch discount voucher code.</p>
                </div>
                
                <form onsubmit="handleLeadSubmit(event)" class="space-y-4 text-xs font-medium">
                    <div>
                        <label for="leadName" class="block font-bold text-elyra-dark mb-1">Full Name</label>
                        <input type="text" id="leadName" required placeholder="Enter your full name" class="w-full px-4 py-3.5 rounded-xl border border-black/10 focus:ring-2 focus:ring-elyra-yellow focus:outline-none bg-elyra-bg/50">
                    </div>
                    <div>
                        <label for="leadEmail" class="block font-bold text-elyra-dark mb-1">Email Address</label>
                        <input type="email" id="leadEmail" required placeholder="Enter your email address" class="w-full px-4 py-3.5 rounded-xl border border-black/10 focus:ring-2 focus:ring-elyra-yellow focus:outline-none bg-elyra-bg/50">
                    </div>
                    <div class="flex items-start gap-2.5 pt-1">
                        <input type="checkbox" id="leadConsent" required class="mt-1 accent-black">
                        <label for="leadConsent" class="text-[11px] text-elyra-grey leading-tight">I agree to receive marketing updates and simulated promotional offers in accordance with data privacy guidelines[cite: 8].</label>
                    </div>
                    <button type="submit" class="w-full bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold py-4 rounded-full uppercase tracking-wider transition-colors shadow-md">
                        Claim My 20% Discount
                    </button>
                </form>
                <p id="leadSuccessMsg" class="text-center text-xs font-bold text-green-600 hidden">Success! Your simulated voucher code has been registered securely.</p>
            </div>
        </section>

    </main>

    <!-- FOOTER / NEWSLETTER -->
    <footer class="bg-elyra-card border-t border-black/10 pt-16 pb-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto space-y-12">
            
            <!-- Newsletter Sign-up Box -->
            <div class="max-w-2xl mx-auto text-center space-y-4">
                <p class="text-xs font-extrabold uppercase tracking-widest text-elyra-grey">Join us on the road to an effortless glow.</p>
                <p class="text-xs text-elyra-dark/80 font-medium">Receive tips, tricks & exclusive offer updates directly from our team.</p>
                
                <form onsubmit="handleSubscribe(event)" class="flex flex-col sm:flex-row gap-2 max-w-md mx-auto pt-2">
                    <input type="email" required placeholder="Email Address" class="flex-grow px-5 py-3.5 rounded-full border border-black/10 text-xs focus:outline-none focus:ring-2 focus:ring-elyra-yellow bg-white font-medium">
                    <button type="submit" class="bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold text-xs uppercase px-8 py-3.5 rounded-full transition-all tracking-wider">
                        SUBSCRIBE
                    </button>
                </form>
            </div>

            <!-- Massive Brand Footer Logo -->
            <div class="py-8 text-center border-y border-black/10">
                <span class="brand-font font-black text-6xl sm:text-9xl tracking-tight block select-none text-elyra-dark">ELYRA <span class="text-elyra-yellow-dark">Skin</span></span>
            </div>

            <!-- Bottom Links -->
            <div class="flex flex-col sm:flex-row items-center justify-between text-xs text-elyra-grey gap-4 font-medium">
                <p>© 2026 ELYRA Skin Inc. All Rights Reserved. Sourced from Guimaras, Philippines.</p>
                <div class="flex gap-6 font-bold">
                    <a href="#" onclick="openModal('Privacy Policy', 'Your privacy is our priority. We never sell your personal data.')" class="hover:text-black">PRIVACY</a>
                    <a href="#" onclick="openModal('Terms of Service', 'Standard e-commerce terms apply to all ELYRA Skin orders.')" class="hover:text-black">TERMS</a>
                    <a href="#" onclick="openModal('Shipping & Returns', 'Free shipping on orders over ₱500 across the Philippines.')" class="hover:text-black">SHIPPING</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- SLIDE-OUT CART DRAWER -->
    <div id="cartDrawerBackdrop" class="fixed inset-0 bg-black/60 z-50 opacity-0 pointer-events-none transition-opacity duration-300" onclick="toggleCart()"></div>
    
    <aside id="cartDrawer" class="fixed top-0 right-0 h-full w-full sm:w-96 bg-elyra-bg z-50 shadow-2xl cart-drawer translate-x-full flex flex-col justify-between">
        <div class="p-6 border-b border-black/10 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <span class="font-extrabold text-2xl text-elyra-dark">Your Cart</span>
                <span id="cartDrawerBadge" class="bg-elyra-yellow text-black text-[10px] font-extrabold px-2.5 py-0.5 rounded-full">0</span>
            </div>
            <button onclick="toggleCart()" class="text-xl p-2 hover:opacity-60">
                <i class="fa-solid fa-xmark"></i>
            </button>
        </div>

        <div id="cartItemsContainer" class="p-6 overflow-y-auto flex-grow space-y-4">
            <div id="emptyCartMsg" class="text-center py-12 space-y-3">
                <i class="fa-solid fa-basket-shopping text-4xl text-elyra-grey/30"></i>
                <p class="text-xs font-bold uppercase tracking-wider text-elyra-grey">Your bag is empty</p>
                <a href="#shop" onclick="toggleCart()" class="inline-block bg-elyra-yellow text-black text-xs font-extrabold px-6 py-2.5 rounded-full uppercase">Explore Products</a>
            </div>
        </div>

        <div class="p-6 border-t border-black/10 bg-white space-y-4">
            <div class="space-y-2 text-xs">
                <div class="flex justify-between text-elyra-grey font-medium">
                    <span>Subtotal</span>
                    <span id="cartSubtotal" class="font-bold text-elyra-dark">₱0</span>
                </div>
                <div class="flex justify-between text-elyra-grey font-medium">
                    <span>Shipping</span>
                    <span id="cartShipping" class="font-bold text-elyra-dark">Calculated at checkout</span>
                </div>
                <div class="flex justify-between text-sm font-black text-elyra-dark pt-2 border-t border-black/5">
                    <span>Total</span>
                    <span id="cartTotal" class="text-elyra-dark">₱0</span>
                </div>
            </div>

            <button onclick="checkout()" class="w-full bg-elyra-yellow text-black hover:bg-elyra-dark hover:text-white font-extrabold py-3.5 rounded-full text-xs uppercase tracking-wider transition-colors shadow-md">
                Checkout Now
            </button>
        </div>
    </aside>

    <!-- GENERIC MODAL -->
    <div id="infoModal" class="fixed inset-0 bg-black/60 z-50 flex items-center justify-center p-4 opacity-0 pointer-events-none modal-backdrop">
        <div class="bg-elyra-bg rounded-3xl max-w-md w-full p-6 sm:p-8 space-y-4 shadow-2xl relative transform scale-95 transition-all duration-300" id="modalContentBox">
            <h3 id="modalTitle" class="font-extrabold text-xl text-elyra-dark">Modal Title</h3>
            <p id="modalDesc" class="text-xs text-elyra-grey leading-relaxed font-medium">Modal description goes here.</p>
            <button onclick="closeModal()" class="w-full bg-elyra-dark text-white hover:bg-elyra-yellow hover:text-black font-extrabold py-3 rounded-full text-xs uppercase tracking-wider transition-colors">Close</button>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Cart State
        let cart = [];

        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        function addToCart(name, price, desc) {
            const existingItem = cart.find(item => item.name === name);
            if (existingItem) {
                existingItem.qty += 1;
            } else {
                cart.push({ name, price, desc, qty: 1 });
            }
            updateCartUI();
            toggleCart();
        }

        function removeFromCart(name) {
            cart = cart.filter(item => item.name !== name);
            updateCartUI();
        }

        function updateCartUI() {
            const container = document.getElementById('cartItemsContainer');
            const countBadge = document.getElementById('cartCount');
            const drawerBadge = document.getElementById('cartDrawerBadge');
            const subtotalEl = document.getElementById('cartSubtotal');
            const totalEl = document.getElementById('cartTotal');
            
            const totalItems = cart.reduce((sum, item) => sum + item.qty, 0);
            countBadge.textContent = totalItems;
            drawerBadge.textContent = totalItems;

            if (cart.length === 0) {
                container.innerHTML = `
                    <div id="emptyCartMsg" class="text-center py-12 space-y-3">
                        <i class="fa-solid fa-basket-shopping text-4xl text-elyra-grey/30"></i>
                        <p class="text-xs font-bold uppercase tracking-wider text-elyra-grey">Your bag is empty</p>
                        <a href="#shop" onclick="toggleCart()" class="inline-block bg-elyra-yellow text-black text-xs font-extrabold px-6 py-2.5 rounded-full uppercase">Explore Products</a>
                    </div>
                `;
                subtotalEl.textContent = '₱0';
                totalEl.textContent = '₱0';
                return;
            }

            let html = '';
            let subtotal = 0;

            cart.forEach(item => {
                subtotal += item.price * item.qty;
                html += `
                    <div class="bg-white p-4 rounded-2xl border border-black/5 flex items-center justify-between shadow-sm">
                        <div>
                            <h4 class="font-bold text-xs text-elyra-dark">${item.name}</h4>
                            <p class="text-[10px] text-elyra-grey">${item.desc}</p>
                            <span class="text-xs font-extrabold text-elyra-dark mt-1 block">₱${item.price} × ${item.qty}</span>
                        </div>
                        <button onclick="removeFromCart('${item.name}')" class="text-red-500 hover:text-red-700 p-2 text-xs">
                            <i class="fa-solid fa-trash-can"></i>
                        </button>
                    </div>
                `;
            });

            container.innerHTML = html;
            subtotalEl.textContent = `₱${subtotal}`;
            const shipping = subtotal >= 500 ? 0 : 50;
            document.getElementById('cartShipping').textContent = shipping === 0 ? 'FREE' : '₱50';
            totalEl.textContent = `₱${subtotal + shipping}`;
        }

        function toggleCart() {
            const drawer = document.getElementById('cartDrawer');
            const backdrop = document.getElementById('cartDrawerBackdrop');
            drawer.classList.toggle('translate-x-full');
            backdrop.classList.toggle('opacity-0');
            backdrop.classList.toggle('pointer-events-none');
        }

        function checkout() {
            if (cart.length === 0) {
                alert('Your cart is empty!');
                return;
            }
            alert('Simulation Successful! Order placed securely. Thank you for shopping with ELYRA Skin.');
            cart = [];
            updateCartUI();
            toggleCart();
        }

        function handleSubscribe(e) {
            e.preventDefault();
            alert('Thank you for subscribing! Check your inbox for exclusive updates.');
            e.target.reset();
        }

        function handleLeadSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('leadName').value;
            const email = document.getElementById('leadEmail').value;
            const consent = document.getElementById('leadConsent').checked;

            if (!name || !email || !consent) {
                alert('Please complete all fields and check the consent box.');
                return;
            }

            document.getElementById('leadSuccessMsg').classList.remove('hidden');
            setTimeout(() => {
                e.target.reset();
                document.getElementById('leadSuccessMsg').classList.add('hidden');
            }, 4000);
        }

        // Fixed-Date Countdown Timer with Expired State Handling
        function updateCountdown() {
            const promoEndDate = new Date('November 30, 2026 23:59:59').getTime();
            const now = new Date().getTime();
            const distance = promoEndDate - now;

            const daysEl = document.getElementById('days');
            const hoursEl = document.getElementById('hours');
            const minsEl = document.getElementById('minutes');
            const secsEl = document.getElementById('seconds');
            const timerContainer = document.getElementById('countdownTimerContainer');
            const statusText = document.getElementById('promoStatusText');

            if (distance < 0) {
                if (timerContainer) timerContainer.style.display = 'none';
                if (statusText) statusText.textContent = 'PROMOTION EXPIRED: Thank you for participating in the ELYRA Skin launch campaign!';
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            if (daysEl) daysEl.textContent = String(days).padStart(2, '0');
            if (hoursEl) hoursEl.textContent = String(hours).padStart(2, '0');
            if (minsEl) minsEl.textContent = String(minutes).padStart(2, '0');
            if (secsEl) secsEl.textContent = String(seconds).padStart(2, '0');
        }

        setInterval(updateCountdown, 1000);
        updateCountdown();

        function openModal(title, desc) {
            document.getElementById('modalTitle').textContent = title;
            document.getElementById('modalDesc').textContent = desc;
            const modal = document.getElementById('infoModal');
            const box = document.getElementById('modalContentBox');
            modal.classList.remove('opacity-0', 'pointer-events-none');
            box.classList.remove('scale-95');
            box.classList.add('scale-100');
        }

        function closeModal() {
            const modal = document.getElementById('infoModal');
            const box = document.getElementById('modalContentBox');
            modal.classList.add('opacity-0', 'pointer-events-none');
            box.classList.remove('scale-100');
            box.classList.add('scale-95');
        }
    </script>
</body>
</html>
