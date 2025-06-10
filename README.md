<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>제로 웨이스트 레시피: 새로운 발견</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Do+Hyeon&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        /* 커스텀 폰트 적용 */
        body {
            font-family: 'Noto Sans KR', sans-serif;
            background-color: #1a1a1a;
            color: #f0f0f0;
        }
        h1, h2, h3, h4, h5, h6 {
            font-family: 'Do Hyeon', sans-serif;
        }
        /* 스크롤 애니메이션을 위한 클래스 */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 1s ease-out, transform 1s ease-out;
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
        /* 페이지 전환 애니메이션 */
        .page {
            transition: opacity 0.5s ease-in-out;
        }
        /* 커스텀 스크롤바 (선택 사항) */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #2c2c2c;
        }
        ::-webkit-scrollbar-thumb {
            background: #F59E0B; /* Amber-500 */
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D97706; /* Amber-600 */
        }
    </style>
</head>
<body class="bg-gray-900 text-white">

    <!-- 메인 페이지 -->
    <div id="home" class="page">
        <!-- 섹션 1: 음식물 쓰레기 심각성 재고 -->
        <section class="h-screen flex flex-col items-center justify-center text-center p-4 bg-black">
            <h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-4 leading-tight">
                우리가 버리는 음식들,<br>다시 태어날 수 있다면?
            </h1>
            <p class="text-lg md:text-xl max-w-2xl text-gray-300">
                매년 전 세계 식량의 3분의 1이 버려지고 있습니다.<br class="hidden md:block">
                버려지는 껍질 속에 숨겨진 놀라운 변신을 만나보세요.
            </p>
            <div class="absolute bottom-10 animate-bounce">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                </svg>
            </div>
        </section>

        <!-- 섹션 2: 3가지 음식 소개 -->
        <section id="recipes" class="min-h-screen container mx-auto px-6 py-20">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold reveal">새로운 발견, 제로 웨이스트 레시피</h2>
                <p class="text-xl text-gray-400 mt-4 reveal" style="transition-delay: 200ms;">음식의 모든 부분을 즐기는 창의적인 방법을 소개합니다.</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 바나나껍질 튀김 -->
                <div class="reveal" style="transition-delay: 400ms;">
                    <a href="#" onclick="showPage('banana-page'); return false;" class="group block rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <div class="relative">
                            <img src="https://placehold.co/600x400/854d0e/ffffff?text=바나나껍질+튀김" alt="바나나껍질 튀김 이미지" class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-300 flex items-center justify-center">
                                <h3 class="text-3xl font-bold text-white">바나나껍질 튀김</h3>
                            </div>
                        </div>
                    </a>
                </div>

                <!-- 오렌지껍질 정과 -->
                <div class="reveal" style="transition-delay: 600ms;">
                    <a href="#" onclick="showPage('orange-page'); return false;" class="group block rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <div class="relative">
                            <img src="https://placehold.co/600x400/d97706/ffffff?text=오렌지껍질+정과" alt="오렌지껍질 정과 이미지" class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-300 flex items-center justify-center">
                                <h3 class="text-3xl font-bold text-white">오렌지껍질 정과</h3>
                            </div>
                        </div>
                    </a>
                </div>

                <!-- 수박김치 -->
                <div class="reveal" style="transition-delay: 800ms;">
                    <a href="#" onclick="showPage('watermelon-page'); return false;" class="group block rounded-lg overflow-hidden shadow-lg transform hover:scale-105 transition-transform duration-300">
                        <div class="relative">
                            <img src="https://placehold.co/600x400/15803d/ffffff?text=수박김치" alt="수박김치 이미지" class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-black bg-opacity-40 group-hover:bg-opacity-20 transition-all duration-300 flex items-center justify-center">
                                <h3 class="text-3xl font-bold text-white">수박김치</h3>
                            </div>
                        </div>
                    </a>
                </div>
            </div>
        </section>
    </div>

    <!-- 레시피 상세 페이지 컨테이너 -->
    <div id="recipe-details-container" class="bg-gray-800">
        <!-- 바나나껍질 튀김 페이지 -->
        <div id="banana-page" class="page hidden min-h-screen">
            <!-- 상세 페이지 템플릿은 JS로 동적 생성 -->
        </div>

        <!-- 오렌지껍질 정과 페이지 -->
        <div id="orange-page" class="page hidden min-h-screen">
            <!-- 상세 페이지 템플릿은 JS로 동적 생성 -->
        </div>

        <!-- 수박김치 페이지 -->
        <div id="watermelon-page" class="page hidden min-h-screen">
            <!-- 상세 페이지 템플릿은 JS로 동적 생성 -->
        </div>
    </div>


    <script>
        // --- 스크롤 애니메이션 로직 ---
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                }
            });
        }, { threshold: 0.1 }); // 요소가 10% 보일 때 애니메이션 실행

        document.querySelectorAll('.reveal').forEach(el => {
            observer.observe(el);
        });

        // --- 페이지 네비게이션 로직 ---
        const pages = {
            'banana-page': {
                title: '바삭하고 달콤한, 바나나껍질 튀김',
                youtubeId: 'dQw4w9WgXcQ', // 예시 유튜브 ID
                description: '버려지던 바나나 껍질의 놀라운 변신! 풀드포크와 비슷한 식감과 달콤한 맛으로 아이들 간식으로도, 맥주 안주로도 손색이 없습니다.',
                ingredients: [
                    '유기농 바나나 껍질 2개',
                    '튀김가루 1컵',
                    '물 1컵',
                    '식용유',
                    '간장 1큰술',
                    '설탕 1큰술',
                    '원하는 시즈닝 (파프리카 가루, 칠리 등)'
                ],
                instructions: [
                    '바나나 껍질을 깨끗이 세척한 후, 숟가락으로 내부의 흰 부분을 가볍게 긁어냅니다.',
                    '껍질을 포크로 길게 찢어 결을 만듭니다.',
                    '간장과 설탕으로 밑간을 하고 10분간 재워둡니다.',
                    '튀김가루와 물을 섞어 튀김 반죽을 만듭니다.',
                    '밑간한 껍질에 튀김옷을 입혀 170도로 예열된 기름에 노릇하게 튀겨냅니다.',
                    '기름을 빼고 원하는 시즈닝을 뿌려 마무리합니다.'
                ]
            },
            'orange-page': {
                title: '향긋하고 쫀득한, 오렌지껍질 정과',
                youtubeId: 'dQw4w9WgXcQ', // 예시 유튜브 ID
                description: '상큼한 오렌지 향을 그대로 담은 고급 디저트. 쌉쌀한 맛은 줄이고 향긋함은 살려 차나 커피와 함께 즐기기 좋습니다.',
                ingredients: [
                    '무농약 오렌지 껍질 3개 분량',
                    '설탕 1.5컵',
                    '물 1컵',
                    '물엿 또는 올리고당 0.5컵'
                ],
                instructions: [
                    '오렌지 껍질을 깨끗이 씻어 흰 부분을 최대한 제거하고 얇게 채 썹니다.',
                    '끓는 물에 껍질을 넣고 2-3번 데쳐 쓴맛을 제거합니다.',
                    '냄비에 데친 껍질, 설탕, 물을 넣고 중불에서 졸이기 시작합니다.',
                    '수분이 거의 증발하면 약불로 줄이고 물엿을 넣어 윤기나게 졸여줍니다.',
                    '꾸덕해지면 유산지 위에 넓게 펼쳐 반나절 이상 건조시킵니다.',
                    '기호에 따라 설탕을 묻혀 마무리합니다.'
                ]
            },
            'watermelon-page': {
                title: '아삭함이 살아있는, 수박김치',
                youtubeId: 'dQw4w9WgXcQ', // 예시 유튜브 ID
                description: '수박의 흰 껍질 부분을 이용한 별미 김치. 무생채보다 시원하고 아삭한 식감이 입맛을 돋웁니다. 비빔밥이나 고기 요리에 곁들여보세요.',
                ingredients: [
                    '수박 흰 껍질 500g',
                    '고춧가루 3큰술',
                    '멸치액젓 2큰술',
                    '다진 마늘 1큰술',
                    '다진 생강 1작은술',
                    '매실청 1큰술',
                    '쪽파 약간, 통깨'
                ],
                instructions: [
                    '수박의 초록색 겉껍질을 필러로 벗겨내고, 흰 부분만 분리합니다.',
                    '흰 껍질을 얇게 나박썰기 한 후, 소금에 15분간 절여 물기를 꼭 짭니다.',
                    '볼에 절인 수박 껍질과 모든 양념 재료를 넣고 골고루 버무립니다.',
                    '마지막으로 쪽파와 통깨를 넣고 가볍게 섞어줍니다.',
                    '바로 먹어도 맛있고, 반나절 숙성 후 먹으면 더욱 깊은 맛을 느낄 수 있습니다.'
                ]
            }
        };

        function createRecipePageHTML(pageId) {
            const data = pages[pageId];
            if (!data) return '';

            return `
                <div class="container mx-auto px-6 py-12">
                    <button onclick="showPage('home')" class="mb-8 inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-amber-700 bg-amber-100 hover:bg-amber-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-amber-500">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-2" viewBox="0 0 20 20" fill="currentColor">
                          <path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" />
                        </svg>
                        모든 레시피 보기
                    </button>

                    <div class="text-center">
                        <h1 class="text-4xl md:text-5xl font-bold text-amber-400">${data.title}</h1>
                        <p class="mt-4 text-lg max-w-3xl mx-auto text-gray-300">${data.description}</p>
                    </div>

                    <!-- 유튜브 영상 -->
                    <div class="my-12 aspect-w-16 aspect-h-9 max-w-4xl mx-auto rounded-lg overflow-hidden shadow-2xl">
                         <iframe src="https://www.youtube.com/embed/${data.youtubeId}" 
                            frameborder="0" 
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                            allowfullscreen
                            class="w-full h-full">
                        </iframe>
                    </div>

                    <!-- 레시피 -->
                    <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
                        <div class="md:col-span-1">
                            <h2 class="text-3xl font-bold border-l-4 border-amber-500 pl-4 text-white">재료</h2>
                            <ul class="mt-4 list-disc list-inside text-gray-300 space-y-2">
                                ${data.ingredients.map(item => `<li>${item}</li>`).join('')}
                            </ul>
                        </div>
                        <div class="md:col-span-2">
                             <h2 class="text-3xl font-bold border-l-4 border-amber-500 pl-4 text-white">만드는 법</h2>
                            <ol class="mt-4 list-decimal list-inside text-gray-300 space-y-4">
                                ${data.instructions.map(item => `<li>${item}</li>`).join('')}
                            </ol>
                        </div>
                    </div>
                </div>
            `;
        }

        function showPage(pageId) {
            const homePage = document.getElementById('home');
            const recipeContainer = document.getElementById('recipe-details-container');
            
            // 모든 페이지 숨기기
            document.querySelectorAll('.page').forEach(p => p.classList.add('hidden'));

            if (pageId === 'home') {
                homePage.classList.remove('hidden');
                homePage.style.opacity = 1;
                recipeContainer.style.display = 'none';
            } else {
                const targetPage = document.getElementById(pageId);
                if (targetPage) {
                    // [수정된 부분]
                    // 상세 페이지 내용 동적 생성 (요소(element)가 없는 경우에만 생성)
                    if (targetPage.children.length === 0) {
                       targetPage.innerHTML = createRecipePageHTML(pageId);
                    }
                    
                    homePage.style.opacity = 0;
                    setTimeout(() => {
                        homePage.classList.add('hidden');
                        recipeContainer.style.display = 'block';
                        targetPage.classList.remove('hidden');
                        window.scrollTo(0, 0);
                    }, 500); // fade-out 시간과 맞춤
                }
            }
        }
        
        // 초기 로드 시 레시피 컨테이너 숨기기
        document.getElementById('recipe-details-container').style.display = 'none';
    </script>
</body>
</html>
