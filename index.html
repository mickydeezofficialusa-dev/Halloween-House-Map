<!DOCTYPE html>
<html lang="en" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <title>SpookyMap | Mudon & DAMAC Hills 1 Trick-or-Treat Tracker</title>
  
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Creepster&family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  
  <!-- Leaflet CSS & JS -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    body {
      font-family: 'Plus Jakarta Sans', sans-serif;
      background-color: #0f0a19;
      color: #f8fafc;
      overflow: hidden;
    }
    .spooky-font {
      font-family: 'Creepster', cursive;
      letter-spacing: 0.05em;
    }
    /* Custom Map Marker Styling */
    .custom-pin {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 44px;
      height: 44px;
      background: linear-gradient(135deg, #f97316 0%, #ea580c 100%);
      border: 3px solid #fef08a;
      border-radius: 50% 50% 50% 0;
      transform: rotate(-45deg);
      box-shadow: 0 8px 20px -2px rgba(249, 115, 22, 0.7);
      transition: all 0.2s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    .custom-pin:hover {
      transform: rotate(-45deg) scale(1.18);
      z-index: 999 !important;
    }
    .custom-pin span {
      transform: rotate(45deg);
      font-size: 22px;
      line-height: 1;
    }
    .pin-out-of-candy {
      background: linear-gradient(135deg, #475569 0%, #1e293b 100%);
      border-color: #94a3b8;
      box-shadow: 0 4px 10px rgba(0,0,0,0.5);
      opacity: 0.75;
    }
    /* Leaflet Popup Overrides */
    .leaflet-popup-content-wrapper {
      background: #1a1228 !important;
      color: #f8fafc !important;
      border: 1px solid rgba(249, 115, 22, 0.35);
      border-radius: 16px !important;
      padding: 0 !important;
      overflow: hidden;
      box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.7) !important;
    }
    .leaflet-popup-content {
      margin: 0 !important;
      width: 290px !important;
    }
    .leaflet-popup-tip {
      background: #1a1228 !important;
    }
    .leaflet-container a.leaflet-popup-close-button {
      color: #fff !important;
      background: rgba(0,0,0,0.6) !important;
      border-radius: 50%;
      width: 26px !important;
      height: 26px !important;
      top: 10px !important;
      right: 10px !important;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 10;
    }
    /* Scrollbar */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #130d1e; }
    ::-webkit-scrollbar-thumb { background: #3b2854; border-radius: 9999px; }
    ::-webkit-scrollbar-thumb:hover { background: #f97316; }
  </style>
</head>
<body class="h-screen w-screen flex flex-col select-none">

  <!-- TOP NAVIGATION BAR -->
  <header class="h-16 bg-[#160f24]/95 backdrop-blur-md border-b border-orange-500/20 px-4 lg:px-6 flex items-center justify-between z-30 shrink-0">
    <div class="flex items-center gap-3">
      <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-orange-500 to-amber-600 flex items-center justify-center shadow-lg shadow-orange-500/30 text-2xl">
        🎃
      </div>
      <div>
        <h1 class="text-2xl spooky-font text-orange-400 tracking-wider leading-none">SPOOKYMAP DUBAI</h1>
        <p class="text-[11px] text-purple-300/80 font-medium">Mudon & DAMAC Hills 1 Trick-or-Treat Tracker</p>
      </div>
    </div>

    <!-- Quick Community Jump Pills -->
    <div class="hidden md:flex items-center bg-[#231836] p-1 rounded-xl border border-purple-500/20 gap-1">
      <button onclick="flyToArea('both')" id="tab-both" class="area-tab px-3 py-1.5 rounded-lg text-xs font-semibold bg-orange-500 text-white shadow transition">
        All (Mudon + DH1)
      </button>
      <button onclick="flyToArea('mudon')" id="tab-mudon" class="area-tab px-3 py-1.5 rounded-lg text-xs font-semibold text-purple-200 hover:text-white transition">
        📍 Mudon
      </button>
      <button onclick="flyToArea('dh1')" id="tab-dh1" class="area-tab px-3 py-1.5 rounded-lg text-xs font-semibold text-purple-200 hover:text-white transition">
        📍 DAMAC Hills 1
      </button>
    </div>

    <!-- Action Buttons -->
    <div class="flex items-center gap-2.5">
      <button onclick="locateUser()" title="Find My Location" class="p-2.5 rounded-xl bg-[#231836] hover:bg-[#2e2046] text-purple-200 border border-purple-500/20 transition flex items-center gap-1.5 text-xs font-semibold">
        <i data-lucide="locate-fixed" class="w-4 h-4 text-orange-400"></i>
        <span class="hidden sm:inline">Near Me</span>
      </button>

      <button onclick="startAddHouseMode()" id="addHouseBtn" class="px-4 py-2.5 rounded-xl bg-gradient-to-r from-orange-500 to-amber-500 hover:from-orange-600 hover:to-amber-600 text-slate-950 font-bold text-xs sm:text-sm shadow-lg shadow-orange-500/25 transition flex items-center gap-2">
        <i data-lucide="plus-circle" class="w-4 h-4 stroke-[2.5]"></i>
        <span>Add My House</span>
      </button>
    </div>
  </header>

  <!-- MOBILE COMMUNITY SWITCHER -->
  <div class="md:hidden bg-[#1a1228] border-b border-purple-500/20 px-3 py-2 flex items-center justify-between gap-2 z-20 shrink-0">
    <div class="flex gap-1 flex-1">
      <button onclick="flyToArea('both')" class="flex-1 py-1.5 rounded-lg text-xs font-bold bg-[#281c3d] text-orange-400 border border-orange-500/30">Both</button>
      <button onclick="flyToArea('mudon')" class="flex-1 py-1.5 rounded-lg text-xs font-semibold bg-[#231836] text-purple-200">Mudon</button>
      <button onclick="flyToArea('dh1')" class="flex-1 py-1.5 rounded-lg text-xs font-semibold bg-[#231836] text-purple-200">DAMAC Hills 1</button>
    </div>
    <button onclick="toggleMobileDrawer()" class="px-3 py-1.5 rounded-lg bg-purple-900/50 border border-purple-400/30 text-xs font-semibold text-purple-200 flex items-center gap-1">
      <i data-lucide="list" class="w-3.5 h-3.5"></i> List (<span id="mobileCount">0</span>)
    </button>
  </div>

  <!-- MAIN WORKSPACE -->
  <div class="flex-1 flex relative overflow-hidden">
    
    <!-- LEFT SIDEBAR: HOUSE DIRECTORY & FILTERS -->
    <aside id="sidebar" class="w-full sm:w-96 bg-[#140e21] border-r border-purple-500/20 flex flex-col z-20 absolute sm:relative inset-0 transform -translate-x-full sm:translate-x-0 transition-transform duration-300">
      
      <!-- Search & Filters -->
      <div class="p-4 border-b border-purple-500/20 space-y-3 bg-[#191129]">
        <div class="flex items-center justify-between sm:hidden mb-1">
          <span class="text-sm font-bold text-orange-400">Participating Houses</span>
          <button onclick="toggleMobileDrawer()" class="text-purple-300 p-1"><i data-lucide="x" class="w-5 h-5"></i></button>
        </div>

        <div class="relative">
          <i data-lucide="search" class="w-4 h-4 text-purple-400 absolute left-3.5 top-1/2 -translate-y-1/2"></i>
          <input id="searchInput" oninput="renderHouseList()" type="text" placeholder="Search cluster, villa #, or theme..." 
            class="w-full pl-10 pr-4 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white placeholder-purple-400/60 focus:outline-none focus:border-orange-500 transition" />
        </div>

        <!-- Filter Pills -->
        <div class="flex items-center gap-1.5 overflow-x-auto pb-1 no-scrollbar text-[11px]">
          <button onclick="setFilter('all')" id="filter-all" class="filter-pill px-2.5 py-1 rounded-lg bg-orange-500/20 text-orange-300 border border-orange-500/40 font-semibold shrink-0">
            All Houses
          </button>
          <button onclick="setFilter('candy')" id="filter-candy" class="filter-pill px-2.5 py-1 rounded-lg bg-[#231836] text-purple-300 border border-transparent hover:border-purple-500/40 shrink-0">
            🍬 Has Candy
          </button>
          <button onclick="setFilter('allergy')" id="filter-allergy" class="filter-pill px-2.5 py-1 rounded-lg bg-[#231836] text-purple-300 border border-transparent hover:border-purple-500/40 shrink-0">
            🥜 Allergy-Friendly
          </button>
          <button onclick="setFilter('scary')" id="filter-scary" class="filter-pill px-2.5 py-1 rounded-lg bg-[#231836] text-purple-300 border border-transparent hover:border-purple-500/40 shrink-0">
            👻 Extreme Haunt
          </button>
        </div>
      </div>

      <!-- Stats Bar -->
      <div class="px-4 py-2 bg-[#110b1c] border-b border-purple-500/10 flex items-center justify-between text-[11px] text-purple-300/80">
        <span>Showing <strong id="houseCount" class="text-orange-400">0</strong> spooky stops</span>
        <button onclick="exportImportModal()" class="hover:text-orange-400 underline flex items-center gap-1">
          <i data-lucide="share-2" class="w-3 h-3"></i> Share / Backup Map
        </button>
      </div>

      <!-- Scrollable List of Houses -->
      <div id="houseList" class="flex-1 overflow-y-auto p-3 space-y-2.5">
        <!-- Populated dynamically via JS -->
      </div>
    </aside>

    <!-- MAP CONTAINER -->
    <main class="flex-1 relative">
      <!-- Placement Instruction Banner (Hidden by default) -->
      <div id="placementBanner" class="hidden absolute top-4 left-1/2 -translate-x-1/2 z-[1000] bg-gradient-to-r from-orange-600 to-amber-600 text-slate-950 px-5 py-3 rounded-2xl shadow-2xl border-2 border-yellow-200 flex items-center gap-3 animate-bounce">
        <span class="text-xl">📍</span>
        <div class="text-xs sm:text-sm font-extrabold">
          Tap anywhere on the map to place your Villa pin!
        </div>
        <button onclick="cancelAddHouseMode()" class="ml-2 px-2.5 py-1 bg-slate-950/20 hover:bg-slate-950/30 rounded-lg text-xs font-bold">
          Cancel
        </button>
      </div>

      <!-- Map Layer Switcher (Google Hybrid / Satellite / Dark Street) -->
      <div class="absolute bottom-6 right-4 z-[900] flex flex-col gap-2">
        <div class="bg-[#160f24]/90 backdrop-blur-md p-1.5 rounded-xl border border-purple-500/30 shadow-xl flex flex-col gap-1 text-xs">
          <button onclick="setMapLayer('hybrid')" id="layer-hybrid" class="px-3 py-1.5 rounded-lg bg-orange-500 text-slate-950 font-bold text-left flex items-center gap-2">
            🛰️ Google Hybrid
          </button>
          <button onclick="setMapLayer('streets')" id="layer-streets" class="px-3 py-1.5 rounded-lg text-purple-200 hover:bg-white/5 font-medium text-left flex items-center gap-2">
            🗺️ Google Streets
          </button>
        </div>
      </div>

      <!-- Interactive Map Div -->
      <div id="map" class="w-full h-full z-10"></div>
    </main>
  </div>

  <!-- MODAL: ADD / EDIT HOUSE -->
  <div id="houseModal" class="hidden fixed inset-0 z-50 bg-black/75 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto">
    <div class="bg-[#191129] border border-orange-500/40 rounded-2xl max-w-lg w-full overflow-hidden shadow-2xl my-8">
      <div class="px-6 py-4 bg-gradient-to-r from-orange-500/20 to-purple-600/20 border-b border-purple-500/20 flex items-center justify-between">
        <div class="flex items-center gap-2.5">
          <span class="text-2xl">🎃</span>
          <h2 class="text-lg font-bold text-white">Register Your Trick-or-Treat Villa</h2>
        </div>
        <button onclick="closeHouseModal()" class="text-purple-300 hover:text-white p-1">
          <i data-lucide="x" class="w-5 h-5"></i>
        </button>
      </div>

      <form id="houseForm" onsubmit="saveHouse(event)" class="p-6 space-y-4 max-h-[80vh] overflow-y-auto">
        <input type="hidden" id="formLat" />
        <input type="hidden" id="formLng" />

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-semibold text-purple-200 mb-1">Community *</label>
            <select id="formCommunity" required class="w-full px-3.5 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white focus:border-orange-500 focus:outline-none">
              <option value="Mudon">Mudon</option>
              <option value="DAMAC Hills 1">DAMAC Hills 1</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-semibold text-purple-200 mb-1">Sub-Cluster & Villa # *</label>
            <input id="formTitle" type="text" required placeholder="e.g., Rahat Villa 42 / Silver Springs 18" 
              class="w-full px-3.5 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white placeholder-purple-400/40 focus:border-orange-500 focus:outline-none" />
          </div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-semibold text-purple-200 mb-1">Pin Icon Theme</label>
            <select id="formIcon" class="w-full px-3.5 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white focus:border-orange-500 focus:outline-none">
              <option value="🎃">🎃 Classic Pumpkin</option>
              <option value="👻">👻 Friendly Ghost</option>
              <option value="💀">💀 Skeleton / Scary Haunt</option>
              <option value="🧙‍♀️">🧙‍♀️ Witch's Brew</option>
              <option value="🍬">🍬 Candy Paradise</option>
              <option value="🕸️">🕸️ Haunted Mansion</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-semibold text-purple-200 mb-1">Candy Status</label>
            <select id="formStatus" class="w-full px-3.5 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white focus:border-orange-500 focus:outline-none">
              <option value="plenty">🍬 Plenty of Candy!</option>
              <option value="low">⚡ Running Low</option>
              <option value="out">💤 Out of Candy</option>
            </select>
          </div>
        </div>

        <div>
          <label class="block text-xs font-semibold text-purple-200 mb-1">Description & Instructions *</label>
          <textarea id="formDesc" required rows="3" placeholder="Tell trick-or-treaters about your decorations, active hours (e.g. 5:30 PM - 9:00 PM), or gate code tips!"
            class="w-full px-3.5 py-2.5 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white placeholder-purple-400/40 focus:border-orange-500 focus:outline-none"></textarea>
        </div>

        <!-- Special Tags -->
        <div>
          <label class="block text-xs font-semibold text-purple-200 mb-2">Special Highlights</label>
          <div class="grid grid-cols-2 gap-2 text-xs">
            <label class="flex items-center gap-2 p-2.5 rounded-xl bg-[#0f0a19] border border-purple-500/20 cursor-pointer hover:border-orange-500/40">
              <input type="checkbox" id="tagAllergy" class="accent-orange-500 rounded" />
              <span>🥜 Nut-Free / Allergy Safe</span>
            </label>
            <label class="flex items-center gap-2 p-2.5 rounded-xl bg-[#0f0a19] border border-purple-500/20 cursor-pointer hover:border-orange-500/40">
              <input type="checkbox" id="tagScary" class="accent-orange-500 rounded" />
              <span>👻 Jump Scares / Animatronics</span>
            </label>
            <label class="flex items-center gap-2 p-2.5 rounded-xl bg-[#0f0a19] border border-purple-500/20 cursor-pointer hover:border-orange-500/40">
              <input type="checkbox" id="tagToddler" class="accent-orange-500 rounded" />
              <span>👶 Toddler Friendly</span>
            </label>
            <label class="flex items-center gap-2 p-2.5 rounded-xl bg-[#0f0a19] border border-purple-500/20 cursor-pointer hover:border-orange-500/40">
              <input type="checkbox" id="tagPhoto" class="accent-orange-500 rounded" />
              <span>📸 Photo Booth / Props</span>
            </label>
          </div>
        </div>

        <!-- Picture Upload OR Image URL -->
        <div class="space-y-2">
          <label class="block text-xs font-semibold text-purple-200">House Photo (Upload from phone or paste link)</label>
          <div class="flex items-center gap-3">
            <label class="flex-1 flex flex-col items-center justify-center px-4 py-3 bg-[#0f0a19] border-2 border-dashed border-purple-500/40 rounded-xl cursor-pointer hover:border-orange-500 transition text-center">
              <i data-lucide="camera" class="w-5 h-5 text-orange-400 mb-1"></i>
              <span class="text-xs text-purple-200 font-medium">Upload Photo</span>
              <span class="text-[10px] text-purple-400">Auto-compressed for fast loading</span>
              <input type="file" id="formImageFile" accept="image/*" class="hidden" onchange="handleImageUpload(event)" />
            </label>
            <div id="imagePreviewContainer" class="hidden w-20 h-20 rounded-xl overflow-hidden border border-orange-500 relative shrink-0">
              <img id="imagePreview" src="" class="w-full h-full object-cover" />
              <button type="button" onclick="clearUploadedImage()" class="absolute top-1 right-1 bg-black/70 text-white rounded-full p-0.5">
                <i data-lucide="x" class="w-3 h-3"></i>
              </button>
            </div>
          </div>
          <input id="formImageUrl" type="url" placeholder="Or paste an image URL (optional)" 
            class="w-full px-3.5 py-2 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-xs text-white placeholder-purple-400/40 focus:border-orange-500 focus:outline-none" />
        </div>

        <div class="pt-3 border-t border-purple-500/20 flex items-center justify-end gap-3">
          <button type="button" onclick="closeHouseModal()" class="px-4 py-2.5 rounded-xl bg-[#231836] text-purple-200 text-xs font-semibold hover:bg-[#2e2046]">
            Cancel
          </button>
          <button type="submit" class="px-5 py-2.5 rounded-xl bg-gradient-to-r from-orange-500 to-amber-500 text-slate-950 font-bold text-xs shadow-lg shadow-orange-500/25 hover:from-orange-600 hover:to-amber-600">
            🎃 Publish House to Map
          </button>
        </div>
      </form>
    </div>
  </div>

  <!-- MODAL: SHARE / EXPORT JSON -->
  <div id="shareModal" class="hidden fixed inset-0 z-50 bg-black/75 backdrop-blur-sm flex items-center justify-center p-4">
    <div class="bg-[#191129] border border-purple-500/40 rounded-2xl max-w-md w-full p-6 space-y-4 shadow-2xl">
      <div class="flex items-center justify-between">
        <h3 class="text-base font-bold text-white flex items-center gap-2">
          <i data-lucide="share-2" class="w-4 h-4 text-orange-400"></i> Share or Sync Community Data
        </h3>
        <button onclick="document.getElementById('shareModal').classList.add('hidden')" class="text-purple-300 hover:text-white">
          <i data-lucide="x" class="w-5 h-5"></i>
        </button>
      </div>
      <p class="text-xs text-purple-200/80 leading-relaxed">
        Copy the JSON below to share your marked villas on WhatsApp groups for Mudon & DAMAC Hills 1, or paste a neighbor's code to merge their pins!
      </p>
      <textarea id="jsonExportArea" rows="5" class="w-full p-3 bg-[#0f0a19] border border-purple-500/30 rounded-xl text-[11px] font-mono text-orange-300 focus:outline-none"></textarea>
      <div class="flex gap-2 justify-end">
        <button onclick="copyExportJson()" class="px-4 py-2 rounded-xl bg-orange-500 text-slate-950 font-bold text-xs">
          Copy Code
        </button>
        <button onclick="importJsonData()" class="px-4 py-2 rounded-xl bg-purple-600 text-white font-bold text-xs">
          Import & Merge
        </button>
      </div>
    </div>
  </div>

  <script>
    // --- 1. COORDINATES FOR MUDON & DAMAC HILLS 1 ---
    const COORDS = {
      both:  { center: [25.0235, 55.2605], zoom: 14 },
      mudon: { center: [25.0225, 55.2690], zoom: 15 },
      dh1:   { center: [25.0246, 55.2520], zoom: 15 }
    };

    // --- 2. DEFAULT SAMPLE HOUSES (Mudon & DAMAC Hills 1) ---
    const DEFAULT_HOUSES = [
      {
        id: 'sample-1',
        community: 'Mudon',
        title: 'Al Ranim 2 - Villa 114',
        lat: 25.0195,
        lng: 55.2678,
        icon: '🎃',
        status: 'plenty',
        desc: 'Giant 12ft animated skeleton out front! Full-size chocolate bars and glow sticks for everyone. Active 5:30 PM - 9:30 PM.',
        tags: ['allergy', 'photo', 'toddler'],
        likes: 24,
        image: 'https://images.unsplash.com/photo-1509557965875-b88c97052f0e?auto=format&fit=crop&w=600&q=80'
      },
      {
        id: 'sample-2',
        community: 'Mudon',
        title: 'Rahat - Villa 48 (Near Central Park)',
        lat: 25.0262,
        lng: 55.2685,
        icon: '🕸️',
        status: 'plenty',
        desc: 'Walk-through haunted graveyard in the front courtyard with fog machines and spooky sound effects!',
        tags: ['scary', 'photo'],
        likes: 39,
        image: 'https://images.unsplash.com/photo-1604005950576-87fcb62705e1?auto=format&fit=crop&w=600&q=80'
      },
      {
        id: 'sample-3',
        community: 'DAMAC Hills 1',
        title: 'Silver Springs - Villa 82',
        lat: 25.0278,
        lng: 55.2495,
        icon: '🧙‍♀️',
        status: 'plenty',
        desc: 'Witches Cauldron station! Nut-free Haribo bags, Pokemon Halloween packs, and cold juice boxes for tired parents.',
        tags: ['allergy', 'toddler'],
        likes: 31,
        image: 'https://images.unsplash.com/photo-1508361001413-7a9dca21d08a?auto=format&fit=crop&w=600&q=80'
      },
      {
        id: 'sample-4',
        community: 'DAMAC Hills 1',
        title: 'The Park Villas - Villa 19',
        lat: 25.0220,
        lng: 55.2548,
        icon: '💀',
        status: 'low',
        desc: 'Pirate Shipwreck theme right by Trump Golf Club! Come grab gold chocolate coins before the ghost captain wakes up.',
        tags: ['scary', 'photo'],
        likes: 18,
        image: 'https://images.unsplash.com/photo-1572061486732-b528a9b293a3?auto=format&fit=crop&w=600&q=80'
      }
    ];

    let houses = JSON.parse(localStorage.getItem('spookymap_dubai_v1')) || DEFAULT_HOUSES;
    let currentFilter = 'all';
    let isAddingHouse = false;
    let uploadedBase64Image = '';
    let markersLayer = L.layerGroup();

    // --- 3. INITIALIZE MAP WITH GOOGLE MAPS TILES ---
    const map = L.map('map', {
      center: COORDS.both.center,
      zoom: COORDS.both.zoom,
      zoomControl: false
    });

    L.control.zoom({ position: 'topright' }).addTo(map);

    // Google Maps Hybrid & Street Tile Layers (Works out-of-the-box with zero billing)
    const googleHybrid = L.tileLayer('https://{s}.google.com/vt/lyrs=s,h&x={x}&y={y}&z={z}', {
      maxZoom: 20,
      subdomains: ['mt0', 'mt1', 'mt2', 'mt3'],
      attribution: '&copy; Google Maps — Mudon & DAMAC Hills 1 Halloween Map'
    });

    const googleStreets = L.tileLayer('https://{s}.google.com/vt/lyrs=m&x={x}&y={y}&z={z}', {
      maxZoom: 20,
      subdomains: ['mt0', 'mt1', 'mt2', 'mt3'],
      attribution: '&copy; Google Maps'
    });

    googleHybrid.addTo(map);
    markersLayer.addTo(map);

    // Community Boundary Labels
    const addAreaLabel = (coords, text) => {
      L.marker(coords, {
        interactive: false,
        icon: L.divIcon({
          className: 'pointer-events-none',
          html: `<div class="px-3 py-1 rounded-full bg-black/70 border border-orange-500/50 text-orange-300 font-extrabold text-xs whitespace-nowrap shadow-lg backdrop-blur-sm">${text}</div>`,
          iconSize: [140, 28],
          iconAnchor: [70, 14]
        })
      }).addTo(map);
    };
    addAreaLabel([25.0273, 55.2675], '🎃 MUDON');
    addAreaLabel([25.0246, 55.2539], '👻 DAMAC HILLS 1');

    // --- 4. RENDER MARKERS & SIDEBAR ---
    function renderAll() {
      localStorage.setItem('spookymap_dubai_v1', JSON.stringify(houses));
      renderMarkers();
      renderHouseList();
      lucide.createIcons();
    }

    function renderMarkers() {
      markersLayer.clearLayers();
      const query = document.getElementById('searchInput').value.toLowerCase();

      houses.forEach(house => {
        if (!passesFilter(house, query)) return;

        const isOut = house.status === 'out';
        const markerHtml = `
          <div class="custom-pin ${isOut ? 'pin-out-of-candy' : ''}">
            <span>${isOut ? '💤' : house.icon}</span>
          </div>
        `;

        const icon = L.divIcon({
          className: '',
          html: markerHtml,
          iconSize: [44, 44],
          iconAnchor: [22, 44],
          popupAnchor: [0, -42]
        });

        const statusBadge = {
          plenty: `<span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-emerald-500/20 text-emerald-300 border border-emerald-500/30">🍬 Plenty of Candy</span>`,
          low: `<span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-amber-500/20 text-amber-300 border border-amber-500/30">⚡ Running Low</span>`,
          out: `<span class="px-2 py-0.5 rounded-full text-[10px] font-bold bg-slate-600/30 text-slate-300 border border-slate-500/30">💤 Out of Candy</span>`
        }[house.status];

        const popupHtml = `
          <div class="text-left">
            ${house.image ? `<img src="${house.image}" class="w-full h-36 object-cover border-b border-purple-500/20" alt="${house.title}" />` : ''}
            <div class="p-3.5 space-y-2">
              <div class="flex items-center justify-between gap-1">
                <span class="text-[10px] font-extrabold uppercase tracking-wider px-2 py-0.5 rounded bg-orange-500/20 text-orange-300">${house.community}</span>
                ${statusBadge}
              </div>
              <h3 class="font-bold text-sm text-white leading-snug">${house.icon} ${house.title}</h3>
              <p class="text-xs text-purple-200/90 leading-relaxed">${house.desc}</p>
              
              <div class="flex flex-wrap gap-1 pt-1">
                ${house.tags.includes('allergy') ? '<span class="text-[10px] bg-purple-900/60 px-2 py-0.5 rounded text-purple-200">🥜 Allergy Safe</span>' : ''}
                ${house.tags.includes('scary') ? '<span class="text-[10px] bg-red-900/60 px-2 py-0.5 rounded text-red-200">👻 Scary</span>' : ''}
                ${house.tags.includes('toddler') ? '<span class="text-[10px] bg-blue-900/60 px-2 py-0.5 rounded text-blue-200">👶 Toddler Friendly</span>' : ''}
                ${house.tags.includes('photo') ? '<span class="text-[10px] bg-amber-900/60 px-2 py-0.5 rounded text-amber-200">📸 Photo Op</span>' : ''}
              </div>

              <div class="pt-2.5 border-t border-purple-500/20 flex items-center justify-between gap-2">
                <button onclick="upvoteHouse('${house.id}')" class="px-2.5 py-1.5 rounded-lg bg-[#251a3a] hover:bg-orange-500/20 text-orange-300 text-xs font-bold flex items-center gap-1 transition">
                  🎃 Spooky! (<span>${house.likes || 0}</span>)
                </button>
                <div class="flex items-center gap-1">
                  <button onclick="cycleCandyStatus('${house.id}')" title="Update Candy Status" class="px-2 py-1.5 rounded-lg bg-[#251a3a] hover:bg-purple-700/40 text-purple-200 text-[11px] font-semibold">
                    Status 🔄
                  </button>
                  <a href="https://www.google.com/maps/dir/?api=1&destination=${house.lat},${house.lng}" target="_blank" 
                    class="px-2.5 py-1.5 rounded-lg bg-orange-500 hover:bg-orange-600 text-slate-950 font-bold text-xs flex items-center gap-1">
                    Navigate ↗
                  </a>
                </div>
              </div>
            </div>
          </div>
        `;

        const marker = L.marker([house.lat, house.lng], { icon }).bindPopup(popupHtml);
        markersLayer.addLayer(marker);
      });
    }

    function renderHouseList() {
      const listEl = document.getElementById('houseList');
      const query = document.getElementById('searchInput').value.toLowerCase();
      const filtered = houses.filter(h => passesFilter(h, query));

      document.getElementById('houseCount').textContent = filtered.length;
      document.getElementById('mobileCount').textContent = filtered.length;

      if (filtered.length === 0) {
        listEl.innerHTML = `
          <div class="text-center py-12 px-4 text-purple-300/60 space-y-2">
            <div class="text-4xl">🕸️</div>
            <p class="text-xs font-semibold">No spooky villas match your filter yet.</p>
            <button onclick="startAddHouseMode()" class="text-xs text-orange-400 underline">Be the first to add one!</button>
          </div>
        `;
        return;
      }

      listEl.innerHTML = filtered.map(house => `
        <div onclick="focusHouse('${house.id}')" class="group bg-[#1c132e] hover:bg-[#25193d] border border-purple-500/20 hover:border-orange-500/50 rounded-2xl p-3 transition cursor-pointer flex gap-3 items-start">
          ${house.image ? `
            <img src="${house.image}" class="w-20 h-20 rounded-xl object-cover shrink-0 border border-purple-500/30" alt="${house.title}" />
          ` : `
            <div class="w-20 h-20 rounded-xl bg-[#110b1c] border border-purple-500/20 flex items-center justify-center text-3xl shrink-0">
              ${house.icon}
            </div>
          `}
          <div class="flex-1 min-w-0">
            <div class="flex items-center justify-between gap-1 mb-0.5">
              <span class="text-[10px] font-bold text-orange-400 uppercase tracking-wider">${house.community}</span>
              <span class="text-[10px] text-purple-300 font-semibold">🎃 ${house.likes || 0}</span>
            </div>
            <h4 class="text-xs font-bold text-white truncate group-hover:text-orange-300 transition">${house.icon} ${house.title}</h4>
            <p class="text-[11px] text-purple-300/80 line-clamp-2 mt-1 leading-relaxed">${house.desc}</p>
          </div>
        </div>
      `).join('');
    }

    function passesFilter(house, query) {
      const matchesSearch = house.title.toLowerCase().includes(query) ||
                            house.community.toLowerCase().includes(query) ||
                            house.desc.toLowerCase().includes(query);
      if (!matchesSearch) return false;
      if (currentFilter === 'candy') return house.status !== 'out';
      if (currentFilter === 'allergy') return house.tags.includes('allergy');
      if (currentFilter === 'scary') return house.tags.includes('scary');
      return true;
    }

    // --- 5. MAP INTERACTIONS & ADDING A HOUSE ---
    function startAddHouseMode() {
      isAddingHouse = true;
      document.getElementById('placementBanner').classList.remove('hidden');
      document.getElementById('map').style.cursor = 'crosshair';
      if (window.innerWidth < 640) {
        document.getElementById('sidebar').classList.add('-translate-x-full');
      }
    }

    function cancelAddHouseMode() {
      isAddingHouse = false;
      document.getElementById('placementBanner').classList.add('hidden');
      document.getElementById('map').style.cursor = '';
    }

    map.on('click', function(e) {
      if (!isAddingHouse) return;
      cancelAddHouseMode();

      const { lat, lng } = e.latlng;
      document.getElementById('formLat').value = lat.toFixed(6);
      document.getElementById('formLng').value = lng.toFixed(6);

      // Auto-detect Mudon vs DAMAC Hills 1 by longitude boundary (~55.261)
      const guessedCommunity = lng > 55.261 ? 'Mudon' : 'DAMAC Hills 1';
      document.getElementById('formCommunity').value = guessedCommunity;

      document.getElementById('houseModal').classList.remove('hidden');
    });

    // Compress uploaded photo on client so it fits smoothly in LocalStorage / DB
    function handleImageUpload(event) {
      const file = event.target.files[0];
      if (!file) return;

      const reader = new FileReader();
      reader.onload = function(e) {
        const img = new Image();
        img.onload = function() {
          const canvas = document.createElement('canvas');
          const MAX_WIDTH = 600;
          const scale = Math.min(1, MAX_WIDTH / img.width);
          canvas.width = img.width * scale;
          canvas.height = img.height * scale;
          const ctx = canvas.getContext('2d');
          ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
          uploadedBase64Image = canvas.toDataURL('image/jpeg', 0.72);

          document.getElementById('imagePreview').src = uploadedBase64Image;
          document.getElementById('imagePreviewContainer').classList.remove('hidden');
        };
        img.src = e.target.result;
      };
      reader.readAsDataURL(file);
    }

    function clearUploadedImage() {
      uploadedBase64Image = '';
      document.getElementById('formImageFile').value = '';
      document.getElementById('imagePreviewContainer').classList.add('hidden');
    }

    function closeHouseModal() {
      document.getElementById('houseModal').classList.add('hidden');
      document.getElementById('houseForm').reset();
      clearUploadedImage();
    }

    function saveHouse(e) {
      e.preventDefault();
      const tags = [];
      if (document.getElementById('tagAllergy').checked) tags.push('allergy');
      if (document.getElementById('tagScary').checked) tags.push('scary');
      if (document.getElementById('tagToddler').checked) tags.push('toddler');
      if (document.getElementById('tagPhoto').checked) tags.push('photo');

      const newHouse = {
        id: 'house-' + Date.now(),
        community: document.getElementById('formCommunity').value,
        title: document.getElementById('formTitle').value.trim(),
        lat: parseFloat(document.getElementById('formLat').value),
        lng: parseFloat(document.getElementById('formLng').value),
        icon: document.getElementById('formIcon').value,
        status: document.getElementById('formStatus').value,
        desc: document.getElementById('formDesc').value.trim(),
        tags,
        likes: 1,
        image: uploadedBase64Image || document.getElementById('formImageUrl').value.trim() || ''
      };

      houses.unshift(newHouse);
      closeHouseModal();
      renderAll();
      map.flyTo([newHouse.lat, newHouse.lng], 17);
    }

    // --- 6. NAVIGATION, LIKES & FILTERS ---
    function flyToArea(area) {
      map.flyTo(COORDS[area].center, COORDS[area].zoom, { duration: 1.2 });
      document.querySelectorAll('.area-tab').forEach(btn => {
        btn.className = 'area-tab px-3 py-1.5 rounded-lg text-xs font-semibold text-purple-200 hover:text-white transition';
      });
      const activeBtn = document.getElementById(`tab-${area}`);
      if (activeBtn) {
        activeBtn.className = 'area-tab px-3 py-1.5 rounded-lg text-xs font-semibold bg-orange-500 text-white shadow transition';
      }
    }

    function focusHouse(id) {
      const h = houses.find(x => x.id === id);
      if (!h) return;
      if (window.innerWidth < 640) toggleMobileDrawer();
      map.flyTo([h.lat, h.lng], 17, { duration: 1 });
    }

    function upvoteHouse(id) {
      const h = houses.find(x => x.id === id);
      if (h) {
        h.likes = (h.likes || 0) + 1;
        renderAll();
      }
    }

    function cycleCandyStatus(id) {
      const order = ['plenty', 'low', 'out'];
      const h = houses.find(x => x.id === id);
      if (h) {
        const nextIdx = (order.indexOf(h.status) + 1) % order.length;
        h.status = order[nextIdx];
        renderAll();
      }
    }

    function setFilter(filter) {
      currentFilter = filter;
      document.querySelectorAll('.filter-pill').forEach(el => {
        el.className = 'filter-pill px-2.5 py-1 rounded-lg bg-[#231836] text-purple-300 border border-transparent hover:border-purple-500/40 shrink-0';
      });
      document.getElementById(`filter-${filter}`).className = 'filter-pill px-2.5 py-1 rounded-lg bg-orange-500/20 text-orange-300 border border-orange-500/40 font-semibold shrink-0';
      renderAll();
    }

    function setMapLayer(type) {
      if (type === 'hybrid') {
        map.removeLayer(googleStreets);
        googleHybrid.addTo(map);
        document.getElementById('layer-hybrid').className = 'px-3 py-1.5 rounded-lg bg-orange-500 text-slate-950 font-bold text-left flex items-center gap-2';
        document.getElementById('layer-streets').className = 'px-3 py-1.5 rounded-lg text-purple-200 hover:bg-white/5 font-medium text-left flex items-center gap-2';
      } else {
        map.removeLayer(googleHybrid);
        googleStreets.addTo(map);
        document.getElementById('layer-streets').className = 'px-3 py-1.5 rounded-lg bg-orange-500 text-slate-950 font-bold text-left flex items-center gap-2';
        document.getElementById('layer-hybrid').className = 'px-3 py-1.5 rounded-lg text-purple-200 hover:bg-white/5 font-medium text-left flex items-center gap-2';
      }
    }

    function locateUser() {
      if (!navigator.geolocation) return alert('Geolocation is not supported by your browser');
      navigator.geolocation.getCurrentPosition(pos => {
        const { latitude, longitude } = pos.coords;
        L.circleMarker([latitude, longitude], {
          radius: 8,
          fillColor: '#38bdf8',
          color: '#fff',
          weight: 3,
          fillOpacity: 1
        }).addTo(map).bindPopup('<b>You are here!</b>').openPopup();
        map.flyTo([latitude, longitude], 16);
      }, () => {
        alert('Could not access your GPS location. Make sure location permissions are enabled!');
      });
    }

    function toggleMobileDrawer() {
      document.getElementById('sidebar').classList.toggle('-translate-x-full');
    }

    // --- 7. SHARE / IMPORT JSON ---
    function exportImportModal() {
      document.getElementById('jsonExportArea').value = JSON.stringify(houses);
      document.getElementById('shareModal').classList.remove('hidden');
    }

    function copyExportJson() {
      const area = document.getElementById('jsonExportArea');
      area.select();
      document.execCommand('copy');
      alert('Copied! You can paste this in the Mudon / DAMAC Hills WhatsApp group.');
    }

    function importJsonData() {
      try {
        const imported = JSON.parse(document.getElementById('jsonExportArea').value);
        if (Array.isArray(imported)) {
          houses = imported;
          renderAll();
          document.getElementById('shareModal').classList.add('hidden');
        }
      } catch (e) {
        alert('Invalid JSON format!');
      }
    }

    // Initial boot
    renderAll();
  </script>
</body>
</html>
