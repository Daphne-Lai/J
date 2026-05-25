<!DOCTYPE html>
<html lang="zh-TW" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>駿笙棚架舞台 | 大型活動硬體工程首選</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@300;400;500;700;900&family=Oswald:wght@400;600;700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        grayBase: '#0d0f12',
                        graySec: '#14181f',
                        grayCard: '#1c222b',
                        brandOrange: '#ff5500',
                        brandHover: '#e04b00',
                        textMuted: '#64748b'
                    },
                    fontFamily: {
                        sans: ['Noto Sans TC', 'sans-serif'],
                        oswald: ['Oswald', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        /* 建設風格藍圖網格背景 */
        .blueprint-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background-image: 
                linear-gradient(to right, rgba(255, 85, 0, 0.05) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(255, 85, 0, 0.05) 1px, transparent 1px);
            background-size: 40px 40px;
            pointer-events: none;
            z-index: 0;
        }

        .section-title {
            position: relative;
            padding-left: 1rem;
            border-left: 4px solid #ff5500;
        }

        .glass-nav {
            background-color: rgba(13, 15, 18, 0.9);
            backdrop-filter: blur(12px);
        }

        .img-hover-zoom {
            overflow: hidden;
            background-color: #1c222b; /* 圖片載入前的底色 */
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .img-hover-zoom img {
            transition: transform 0.6s ease;
        }
        .group:hover .img-hover-zoom img {
            transform: scale(1.08);
        }

        .btn-outline-custom {
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        .btn-outline-custom::before {
            content: '';
            position: absolute;
            top: 0; left: -100%; width: 100%; height: 100%;
            background-color: #ff5500;
            transition: all 0.4s ease;
            z-index: -1;
        }
        .btn-outline-custom:hover::before {
            left: 0;
        }
        .btn-outline-custom:hover {
            color: #fff;
            border-color: #ff5500;
        }
    </style>
</head>
<body class="bg-grayBase text-gray-100 font-sans antialiased relative">

    <div class="blueprint-bg"></div>

    <!-- 導覽列 -->
    <header class="fixed w-full top-0 z-50 glass-nav border-b border-gray-800 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <a href="#" class="font-oswald text-2xl font-black tracking-wider flex items-center gap-2 relative z-10">
                駿笙<span class="text-brandOrange">棚架舞台</span>
            </a>
            
            <nav class="hidden md:flex gap-8 items-center font-medium text-sm relative z-10">
                <a href="#about" class="hover:text-brandOrange transition-colors py-2">關於駿笙</a>
                <a href="#equipment" class="hover:text-brandOrange transition-colors py-2">高規設備</a>
                <a href="#solutions" class="hover:text-brandOrange transition-colors py-2">舞台方案</a>
                <a href="#portfolio" class="hover:text-brandOrange transition-colors py-2">經典實績</a>
                <a href="#contact" class="border border-white px-5 py-2 hover:bg-white hover:text-grayBase transition-colors duration-300">快速詢價</a>
            </nav>

            <button class="md:hidden text-2xl text-white p-2">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- 首頁 Hero Section -->
    <section class="relative h-screen flex items-center pt-20 overflow-hidden z-10">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-r from-grayBase via-grayBase/85 to-transparent z-10"></div>
            <!-- 主視覺：替換為中正紀念堂空拍圖 -->
            <img src="images/01-中正紀念堂.jpg" alt="中正紀念堂大型圓形棚架空拍" class="w-full h-full object-cover opacity-70">
        </div>

        <div class="max-w-7xl mx-auto px-6 relative z-20 w-full">
            <div class="max-w-2xl">
                <div class="flex items-center gap-4 mb-4">
                    <span class="w-10 h-[2px] bg-brandOrange"></span>
                    <span class="font-oswald text-brandOrange tracking-[0.3em] font-bold text-sm uppercase">Heavy Duty Engineering</span>
                </div>
                <h1 class="text-5xl md:text-7xl font-black leading-tight mb-6 tracking-wide drop-shadow-lg">
                    構築巔峰時刻的<br>穩固基石
                </h1>
                <p class="text-lg text-gray-300 mb-10 leading-relaxed max-w-xl drop-shadow-md">
                    專注戶外萬人演唱會、大型造勢晚會與高規格校慶活動。<br>以建設公司的嚴苛安全標準，打造頂級震撼的舞台視覺空間。
                </p>
                <div class="flex flex-col sm:flex-row gap-4">
                    <a href="#portfolio" class="bg-brandOrange hover:bg-brandHover text-white px-8 py-4 text-center font-bold tracking-widest transition-colors">
                        瀏覽大型實績
                    </a>
                    <a href="#contact" class="border-2 border-white bg-black/30 backdrop-blur-sm px-8 py-4 text-center font-bold tracking-widest btn-outline-custom relative z-10">
                        啟動專案評估
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 數據實績 Stats -->
    <section class="bg-graySec border-y border-gray-800 relative z-10 py-12">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8 divide-x-0 md:divide-x divide-gray-800 text-center">
                <div class="p-4">
                    <div class="font-oswald text-4xl md:text-5xl font-bold text-brandOrange mb-2">500+</div>
                    <div class="text-gray-400 text-sm tracking-wider">大型活動搭建經驗</div>
                </div>
                <div class="p-4">
                    <div class="font-oswald text-4xl md:text-5xl font-bold text-brandOrange mb-2">100%</div>
                    <div class="text-gray-400 text-sm tracking-wider">結構技師安全認證</div>
                </div>
                <div class="p-4">
                    <div class="font-oswald text-4xl md:text-5xl font-bold text-brandOrange mb-2">15+</div>
                    <div class="text-gray-400 text-sm tracking-wider">專業工程團隊資歷</div>
                </div>
                <div class="p-4">
                    <div class="font-oswald text-4xl md:text-5xl font-bold text-brandOrange mb-2">0</div>
                    <div class="text-gray-400 text-sm tracking-wider">歷史工安事故紀錄</div>
                </div>
            </div>
        </div>
    </section>

    <!-- 關於我們 About -->
    <section id="about" class="py-24 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div>
                    <h2 class="section-title text-3xl md:text-4xl font-black mb-8">
                        <span class="block font-oswald text-brandOrange text-sm tracking-[0.2em] mb-2 font-semibold">ABOUT US</span>
                        建築結構級的活動防線
                    </h2>
                    <p class="text-gray-400 mb-6 leading-relaxed">
                        駿笙棚架舞台工程創立以來，始終堅持將「建築結構級的安全」注入每一次的活動搭建中。我們深刻了解，一場萬人演唱會或關鍵的造勢晚會，硬體結構不僅是視覺的焦點，更是所有演職人員與現場觀眾的生命安全防線。
                    </p>
                    <p class="text-gray-400 mb-10 leading-relaxed">
                        有別於傳統搭棚業的流水帳作業，我們導入現代化工程管理制度、高規格抗風結構計算。從前期動線規劃、結構受重評估到現場施工，皆由經驗豐富的專業團隊一條龍統包。
                    </p>
                    
                    <div class="grid sm:grid-cols-2 gap-6">
                        <div class="bg-graySec p-5 border border-gray-800 flex gap-4">
                            <i class="fa-solid fa-shield-halved text-2xl text-brandOrange mt-1"></i>
                            <div>
                                <h4 class="font-bold mb-1">結構技師簽證</h4>
                                <p class="text-xs text-textMuted">嚴格執行配重與抗風計算，提供合法安全簽證。</p>
                            </div>
                        </div>
                        <div class="bg-graySec p-5 border border-gray-800 flex gap-4">
                            <i class="fa-solid fa-helmet-safety text-2xl text-brandOrange mt-1"></i>
                            <div>
                                <h4 class="font-bold mb-1">高額公共意外險</h4>
                                <p class="text-xs text-textMuted">工程全面投保，合法合規，主辦方免除後顧之憂。</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="relative">
                    <div class="absolute -top-4 -left-4 w-24 h-24 border-t-4 border-l-4 border-brandOrange z-0"></div>
                    <div class="absolute -bottom-4 -right-4 w-24 h-24 border-b-4 border-r-4 border-brandOrange z-0"></div>
                    <!-- 關於我們：替換為體育館紅毯大舞台正面 -->
                    <img src="images/02-體育館正面.jpg" alt="體育館大型舞台施工現場" class="relative z-10 w-full h-[500px] object-cover border border-gray-800">
                </div>
            </div>
        </div>
    </section>

    <!-- 硬體設備 Equipment -->
    <section id="equipment" class="py-24 bg-graySec relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-oswald text-brandOrange text-sm tracking-[0.2em] mb-2 font-semibold uppercase">Hardware Systems</h2>
                <h3 class="text-3xl md:text-4xl font-black">高規格硬體結構設備</h3>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8">
                <!-- 設備卡片 1 -->
                <div class="group bg-grayCard border border-gray-800 hover:border-brandOrange transition-all duration-300">
                    <div class="h-60 img-hover-zoom">
                        <!-- 硬體設備1：替換為台灣祭帳篷與拱門 -->
                        <img src="images/03-台灣祭帳篷.jpg" alt="重型 TRUSS 與帳篷" class="w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-bold mb-3">重型 TRUSS 鋼骨結構</h3>
                        <p class="text-gray-400 text-sm mb-6 h-20">具備極高的垂直耐重與抗風能力，完美吊掛大型 LED 牆、頂級燈光陣列，亦可搭建巨型活動帳篷與拱門。</p>
                        <ul class="text-sm space-y-3 border-t border-gray-800 pt-5">
                            <li class="flex justify-between"><span class="text-textMuted">材質</span> <span>航空級高張力鋁合金</span></li>
                            <li class="flex justify-between"><span class="text-textMuted">應用</span> <span>大型主舞台、迎賓拱門</span></li>
                        </ul>
                    </div>
                </div>

                <!-- 設備卡片 2 -->
                <div class="group bg-grayCard border border-gray-800 hover:border-brandOrange transition-all duration-300">
                    <div class="h-60 img-hover-zoom">
                        <!-- 硬體設備2：替換為新屋米寶路跑拱門 -->
                        <img src="images/04-新屋路跑.jpg" alt="大型客製化結構" class="w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-bold mb-3">大型客製大圖結構棚</h3>
                        <p class="text-gray-400 text-sm mb-6 h-20">結合 TRUSS 結構與高解析大圖輸出，打造專屬賽事、慶典的高端視覺門面，具備優異抗風係數。</p>
                        <ul class="text-sm space-y-3 border-t border-gray-800 pt-5">
                            <li class="flex justify-between"><span class="text-textMuted">特色</span> <span>高辨識度、穩固防風</span></li>
                            <li class="flex justify-between"><span class="text-textMuted">適用</span> <span>路跑賽事、造勢晚會主視覺</span></li>
                        </ul>
                    </div>
                </div>

                <!-- 設備卡片 3 -->
                <div class="group bg-grayCard border border-gray-800 hover:border-brandOrange transition-all duration-300">
                    <div class="h-60 img-hover-zoom">
                        <!-- 硬體設備3：替換為體育館斜坡道 -->
                        <img src="images/05-體育館斜坡.jpg" alt="安全無障礙設施" class="w-full h-full object-cover">
                    </div>
                    <div class="p-8">
                        <h3 class="text-xl font-bold mb-3">附屬安全無障礙設備</h3>
                        <p class="text-gray-400 text-sm mb-6 h-20">提供大型活動不可或缺的周邊配套，包含舞台專用高低階梯、無障礙斜坡道及防暴阻隔護欄。</p>
                        <ul class="text-sm space-y-3 border-t border-gray-800 pt-5">
                            <li class="flex justify-between"><span class="text-textMuted">品項</span> <span>無障礙坡道 / 階梯系統</span></li>
                            <li class="flex justify-between"><span class="text-textMuted">規範</span> <span>符合大型集會安全標準</span></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 舞台方案 Solutions -->
    <section id="solutions" class="py-24 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="mb-20">
                <h2 class="section-title text-3xl md:text-4xl font-black">
                    <span class="block font-oswald text-brandOrange text-sm tracking-[0.2em] mb-2 font-semibold">STAGE SOLUTIONS</span>
                    情境式舞台工程推薦
                </h2>
            </div>

            <!-- 方案 1 -->
            <div class="grid md:grid-cols-2 gap-12 items-center mb-24">
                <div class="order-2 md:order-1 relative img-hover-zoom border border-gray-800 group">
                    <!-- 舞台方案1：替換為火舞表演 -->
                    <img src="images/06-火舞表演.jpg" alt="火舞特效演出舞台" class="w-full h-[400px] object-cover">
                    <div class="absolute inset-0 border-2 border-transparent group-hover:border-brandOrange transition-colors duration-300 z-10 pointer-events-none"></div>
                </div>
                <div class="order-1 md:order-2 md:pl-10">
                    <h3 class="text-2xl font-bold mb-4 flex items-center gap-3">
                        <i class="fa-solid fa-guitar text-brandOrange"></i> 大型演唱會 / 特效舞台
                    </h3>
                    <p class="text-gray-400 mb-8 leading-relaxed">
                        針對音樂祭、火舞等特效演出，我們提供具備「高載重、大跨距、高特效擴充性」的旗艦級主舞台。完美支援數十噸重音響懸吊與特殊火焰機關，並規劃安全流暢的後台藝人動線。
                    </p>
                    <ul class="grid grid-cols-1 sm:grid-cols-2 gap-4 text-sm text-gray-300">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 特效機關安全懸掛結構</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 搖滾區安全動線規劃</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 藝人專屬獨立後台棚</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 結構技師動態簽證</li>
                    </ul>
                </div>
            </div>

            <!-- 方案 2 -->
            <div class="grid md:grid-cols-2 gap-12 items-center mb-24">
                <div class="md:pr-10">
                    <h3 class="text-2xl font-bold mb-4 flex items-center gap-3">
                        <i class="fa-solid fa-users-viewfinder text-brandOrange"></i> 跨年晚會 / 選舉造勢
                    </h3>
                    <p class="text-gray-400 mb-8 leading-relaxed">
                        大型節慶與造勢晚會講求「視野開闊度」與「超高承重能力」。我們的舞台能同時承載破百位貴賓站台，完美結合巨型藝人卡司主視覺背板，同步配置多機位攝影高台。
                    </p>
                    <ul class="grid grid-cols-1 sm:grid-cols-2 gap-4 text-sm text-gray-300">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 巨型主視覺防風背板</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 百人站台高承重基礎</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 階梯式攝影媒體高台</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 全區大範圍防雨棚架</li>
                    </ul>
                </div>
                <div class="relative img-hover-zoom border border-gray-800 group">
                    <!-- 舞台方案2：替換為羅東跨年背板 -->
                    <img src="images/07-羅東跨年.jpg" alt="羅東跨年晚會" class="w-full h-[400px] object-cover">
                    <div class="absolute inset-0 border-2 border-transparent group-hover:border-brandOrange transition-colors duration-300 z-10 pointer-events-none"></div>
                </div>
            </div>

            <!-- 方案 3 -->
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="order-2 md:order-1 relative img-hover-zoom border border-gray-800 group">
                    <!-- 舞台方案3：替換為花蓮龍舟節 -->
                    <img src="images/08-花蓮龍舟.jpg" alt="國際龍舟節舞台" class="w-full h-[400px] object-cover">
                    <div class="absolute inset-0 border-2 border-transparent group-hover:border-brandOrange transition-colors duration-300 z-10 pointer-events-none"></div>
                </div>
                <div class="order-1 md:order-2 md:pl-10">
                    <h3 class="text-2xl font-bold mb-4 flex items-center gap-3">
                        <i class="fa-solid fa-graduation-cap text-brandOrange"></i> 國際賽事 / 大型慶典
                    </h3>
                    <p class="text-gray-400 mb-8 leading-relaxed">
                        因應戶外特殊地形（如：港口、河岸、學校操場）的嚴格要求，我們採用不傷地面的特殊配重與水平基座，配合高規格迎賓門面與選手/貴賓休息區一體化帳篷規劃。
                    </p>
                    <ul class="grid grid-cols-1 sm:grid-cols-2 gap-4 text-sm text-gray-300">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 崎嶇地形精準水平調整</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 戶外場地無痕防護施工</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 選手帳篷區一條龍統包</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brandOrange"></i> 具備抗海風/強陣風結構</li>
                    </ul>
                </div>
            </div>

        </div>
    </section>

    <!-- 實績 Portfolio -->
    <section id="portfolio" class="py-24 bg-graySec relative z-10 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-end mb-12 gap-6">
                <div>
                    <h2 class="font-oswald text-brandOrange text-sm tracking-[0.2em] mb-2 font-semibold uppercase">Portfolio</h2>
                    <h3 class="text-3xl md:text-4xl font-black">經典巨型實績展示</h3>
                </div>
                <div class="flex flex-wrap gap-3">
                    <button class="bg-brandOrange text-white px-5 py-2 text-sm font-medium">全部實績</button>
                    <button class="border border-gray-600 text-gray-400 hover:border-brandOrange hover:text-white px-5 py-2 text-sm font-medium transition-colors">音樂祭/演唱會</button>
                    <button class="border border-gray-600 text-gray-400 hover:border-brandOrange hover:text-white px-5 py-2 text-sm font-medium transition-colors">客製化節慶</button>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-6">
                <!-- 專案 1 -->
                <div class="group relative h-80 overflow-hidden border border-gray-800 cursor-pointer bg-grayBase">
                    <!-- 實績1：替換為台灣祭導覽背板 -->
                    <img src="images/09-台灣祭背板.jpg" alt="台灣祭音樂祭導覽牆" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-grayBase via-grayBase/60 to-transparent opacity-80 group-hover:opacity-95 transition-opacity duration-300"></div>
                    <div class="absolute inset-0 p-6 flex flex-col justify-end translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                        <span class="text-brandOrange text-xs font-bold tracking-wider mb-2">指標音樂祭</span>
                        <h4 class="text-xl font-bold mb-3">台灣祭音樂祭 - 大型 TRUSS 導覽主牆</h4>
                        <div class="flex justify-between text-xs text-gray-400 border-t border-gray-700 pt-3 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100">
                            <span><i class="fa-solid fa-tree mr-1"></i> 草地無痕配重</span>
                            <span><i class="fa-solid fa-wind mr-1"></i> 高抗風係數</span>
                        </div>
                    </div>
                </div>

                <!-- 專案 2 -->
                <div class="group relative h-80 overflow-hidden border border-gray-800 cursor-pointer bg-grayBase">
                    <!-- 實績2：替換為南方澳鯖魚節 -->
                    <img src="images/10-南方澳鯖魚.jpg" alt="南方澳鯖魚節菱形結構" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-grayBase via-grayBase/60 to-transparent opacity-80 group-hover:opacity-95 transition-opacity duration-300"></div>
                    <div class="absolute inset-0 p-6 flex flex-col justify-end translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                        <span class="text-brandOrange text-xs font-bold tracking-wider mb-2">客製化節慶</span>
                        <h4 class="text-xl font-bold mb-3">南方澳鯖魚節 - 創意菱形地標結構</h4>
                        <div class="flex justify-between text-xs text-gray-400 border-t border-gray-700 pt-3 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100">
                            <span><i class="fa-solid fa-shapes mr-1"></i> 特殊幾何結構</span>
                            <span><i class="fa-solid fa-anchor mr-1"></i> 港區高抗風設計</span>
                        </div>
                    </div>
                </div>

                <!-- 專案 3 -->
                <div class="group relative h-80 overflow-hidden border border-gray-800 cursor-pointer bg-grayBase">
                    <!-- 實績3：再次使用體育館正面以展示室內大型統包能力 -->
                    <img src="images/02-體育館正面.jpg" alt="室內大型展演" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-grayBase via-grayBase/60 to-transparent opacity-80 group-hover:opacity-95 transition-opacity duration-300"></div>
                    <div class="absolute inset-0 p-6 flex flex-col justify-end translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                        <span class="text-brandOrange text-xs font-bold tracking-wider mb-2">大型室內場館</span>
                        <h4 class="text-xl font-bold mb-3">萬人體育館 - 典禮大舞台與坡道建置</h4>
                        <div class="flex justify-between text-xs text-gray-400 border-t border-gray-700 pt-3 opacity-0 group-hover:opacity-100 transition-opacity duration-500 delay-100">
                            <span><i class="fa-solid fa-wheelchair mr-1"></i> 無障礙動線</span>
                            <span><i class="fa-solid fa-shield-halved mr-1"></i> 防刮地坪保護</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 聯絡與詢價 Contact -->
    <section id="contact" class="py-24 relative z-10">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid lg:grid-cols-5 gap-16">
                <div class="lg:col-span-2">
                    <h2 class="section-title text-3xl md:text-4xl font-black mb-6">
                        <span class="block font-oswald text-brandOrange text-sm tracking-[0.2em] mb-2 font-semibold">CONTACT US</span>
                        與硬體專家<br>啟動您的頂級盛宴
                    </h2>
                    <p class="text-gray-400 mb-10 leading-relaxed">
                        不論您的活動處於前期籌備，或已有明確的硬體工程需求，駿笙的專業團隊都能提供最精準的結構建議與安全搭建方案。請填寫表單，我們將於 24 小時內專人聯繫。
                    </p>
                    
                    <ul class="space-y-8">
                        <li class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-graySec border border-gray-800 flex items-center justify-center text-brandOrange shrink-0">
                                <i class="fa-solid fa-phone"></i>
                            </div>
                            <div>
                                <h5 class="text-xs text-textMuted tracking-wider mb-1 uppercase">服務專線</h5>
                                <p class="font-medium text-lg font-oswald tracking-wide">02-2345-6789</p>
                            </div>
                        </li>
                        <li class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-graySec border border-gray-800 flex items-center justify-center text-brandOrange shrink-0">
                                <i class="fa-solid fa-envelope"></i>
                            </div>
                            <div>
                                <h5 class="text-xs text-textMuted tracking-wider mb-1 uppercase">電子郵件</h5>
                                <p class="font-medium">service@junshengstage.com</p>
                            </div>
                        </li>
                        <li class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-graySec border border-gray-800 flex items-center justify-center text-brandOrange shrink-0">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <h5 class="text-xs text-textMuted tracking-wider mb-1 uppercase">工程總部</h5>
                                <p class="font-medium">台北市大安區工程路 88 號 1 樓</p>
                            </div>
                        </li>
                    </ul>
                </div>

                <!-- B2B 詢價表單 -->
                <div class="lg:col-span-3 bg-graySec border border-gray-800 p-8 md:p-12 relative">
                    <div class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-brandOrange"></div>
                    
                    <form action="#" method="POST" class="space-y-6 relative z-10">
                        <div class="grid md:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">公司/機關全銜 *</label>
                                <input type="text" class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors" placeholder="例如：駿笙公關股份有限公司" required>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">聯絡人姓名 *</label>
                                <input type="text" class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors" placeholder="陳先生 / 林小姐" required>
                            </div>
                        </div>

                        <div class="grid md:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">聯絡電話 / 手機 *</label>
                                <input type="tel" class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors" placeholder="0912-345-678" required>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">活動類型 *</label>
                                <select class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors appearance-none" required>
                                    <option value="" disabled selected>請選擇活動類型</option>
                                    <option>戶外萬人演唱會 / 音樂祭</option>
                                    <option>選舉造勢晚會 / 全民集會</option>
                                    <option>校慶活動 / 校園展演</option>
                                    <option>企業大型年會 / 尾牙</option>
                                    <option>其他大型硬體統包需求</option>
                                </select>
                            </div>
                        </div>

                        <div class="grid md:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">預估活動規模 (人數)</label>
                                <select class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors appearance-none">
                                    <option>1,000 人以下</option>
                                    <option>1,000 - 5,000 人</option>
                                    <option>5,000 - 10,000 人</option>
                                    <option>10,000 人以上萬人級活動</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-400 mb-2">預計活動日期</label>
                                <input type="date" class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors [color-scheme:dark]">
                            </div>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-400 mb-2">硬體需求描述 / 特殊地形備註</label>
                            <textarea rows="4" class="w-full bg-grayBase border border-gray-700 focus:border-brandOrange focus:ring-1 focus:ring-brandOrange text-white px-4 py-3 outline-none transition-colors" placeholder="請簡述您的舞台尺寸需求，或是否有 PU 跑道保護、草地配重等特殊施作環境要求..."></textarea>
                        </div>

                        <button type="button" class="w-full bg-brandOrange hover:bg-brandHover text-white font-bold tracking-widest py-4 transition-colors">
                            送出精準詢價單
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- 頁尾 Footer -->
    <footer class="bg-[#080a0c] border-t border-gray-800 py-12 relative z-10">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
            <a href="#" class="font-oswald text-2xl font-black tracking-wider text-white">
                駿笙<span class="text-brandOrange">棚架舞台</span>
            </a>
            
            <div class="text-gray-500 text-sm text-center md:text-left">
                &copy; 2026 駿笙棚架舞台工程有限公司. 築夢踏實，為您的巔峰時刻搭建穩固基石.
            </div>

            <div class="flex gap-4">
                <a href="#" class="w-10 h-10 bg-graySec border border-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-brandOrange hover:border-brandOrange transition-all rounded-full"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#" class="w-10 h-10 bg-graySec border border-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-brandOrange hover:border-brandOrange transition-all rounded-full"><i class="fa-brands fa-line"></i></a>
                <a href="#" class="w-10 h-10 bg-graySec border border-gray-800 flex items-center justify-center text-gray-400 hover:text-white hover:bg-brandOrange hover:border-brandOrange transition-all rounded-full"><i class="fa-brands fa-youtube"></i></a>
            </div>
        </div>
    </footer>

    <!-- 簡易互動腳本 -->
    <script>
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 50) {
                nav.classList.add('py-0');
                nav.classList.remove('py-2');
            } else {
                nav.classList.add('py-2');
                nav.classList.remove('py-0');
            }
        });
    </script>
</body>
</html>
