
<html lang="fr-MA">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Top 5 Écrans Solaires Maroc 2026 - Guide Interactif</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-color: #f8fafc;
            color: #1e293b;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }
        @media (max-width: 640px) {
            .chart-container {
                height: 250px;
            }
        }
        .tab-btn.active {
            background-color: #0f766e;
            color: white;
            border-color: #0f766e;
        }
        .tab-btn {
            transition: all 0.3s ease;
        }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
        }
        .accordion-content.open {
            max-height: 200px;
        }
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="antialiased min-h-screen flex flex-col">

<!-- Chosen Palette: Medical/Clean Theme. Primary: Teal (0f766e), Secondary: Amber/Orange (f59e0b) for sun accents, Background: Slate-50 (f8fafc) for readability, Text: Slate-800. -->
<!-- Application Structure Plan: The SPA transforms a linear article into a 4-part interactive dashboard. 1. Hero: Establishes context (Moroccan climate). 2. Interactive Diagnostic: Replaces long text blocks with a clickable skin-type selector to provide personalized recommendations. 3. Market Analysis: Uses a Chart.js bar chart comparing median prices for market transparency. 4. Comprehensive Data & FAQ: A data table and accordion FAQ for structured information retrieval. -->
<!-- Visualization & Content Choices: Skin categories -> Tabbed interaction. Price data -> Chart.js Bar Chart. Full table -> Styled HTML Table. FAQ -> JS Accordions. NO SVG/Mermaid used. -->
<!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <nav class="bg-teal-800 text-white shadow-md sticky top-0 z-50">
        <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="text-xl font-bold tracking-wide flex items-center gap-2">
                <span class="text-2xl">⚕️</span> Universelle Para
            </div>
            <div class="text-sm font-medium text-teal-100 hidden sm:block">
                Guide Parapharmacie 2026
            </div>
        </div>
    </nav>

    <main class="flex-grow">
        <header class="bg-white border-b border-gray-200 py-12 px-4">
            <div class="max-w-4xl mx-auto text-center">
                <span class="inline-block py-1 px-3 rounded-full bg-amber-100 text-amber-800 text-sm font-bold tracking-wider mb-4 uppercase">Édition Spéciale Maroc</span>
                <h1 class="text-4xl md:text-5xl font-extrabold text-slate-900 mb-6 leading-tight">
                    Top 5 des Écrans Solaires au <span class="text-teal-700">Meilleur Rapport Qualité-Prix</span>
                </h1>
                <p class="text-lg md:text-xl text-slate-600 leading-relaxed max-w-3xl mx-auto">
                    Avec le retour des beaux jours, protéger sa peau est une priorité qui ne devrait pas ruiner votre budget. Entre l'humidité saturée de <strong>Casablanca</strong> et le soleil aride de <strong>Marrakech</strong>, découvrez notre sélection d'experts à moins de <strong>180 MAD</strong>.
                </p>
            </div>
        </header>

        <section class="py-12 px-4 bg-slate-50">
            <div class="max-w-5xl mx-auto">
                <div class="text-center mb-10">
                    <h2 class="text-3xl font-bold text-slate-800 mb-4">Diagnostic Rapide : Quel est votre besoin ?</h2>
                    <p class="text-slate-600">Sélectionnez votre type de peau pour découvrir la recommandation idéale et l'actif médical à privilégier cette saison.</p>
                </div>

                <div class="flex flex-wrap justify-center gap-4 mb-8" id="skin-tabs">
                    <button class="tab-btn active px-6 py-3 rounded-full border-2 border-teal-600 text-teal-700 font-bold bg-white hover:bg-teal-50" data-target="grasse">
                        💧 Peau Grasse & Acnéique
                    </button>
                    <button class="tab-btn px-6 py-3 rounded-full border-2 border-teal-600 text-teal-700 font-bold bg-white hover:bg-teal-50" data-target="seche">
                        🌵 Peau Sèche (Post-Ramadan)
                    </button>
                    <button class="tab-btn px-6 py-3 rounded-full border-2 border-teal-600 text-teal-700 font-bold bg-white hover:bg-teal-50" data-target="taches">
                        ☀️ Taches Brunes (Mélasma)
                    </button>
                </div>

                <div class="bg-white rounded-2xl shadow-lg p-6 md:p-10 border border-slate-100" id="recommendation-content">
                    
                </div>
            </div>
        </section>

        <section class="py-12 px-4 bg-white border-y border-gray-200">
            <div class="max-w-5xl mx-auto">
                <div class="mb-10 text-center">
                    <h2 class="text-3xl font-bold text-slate-800 mb-4">Analyse du Marché : Comparatif des Prix</h2>
                    <p class="text-slate-600">Visualisez les budgets moyens constatés en parapharmacie au Maroc pour les références médicales leaders en 2026.</p>
                </div>

                <div class="bg-slate-50 p-6 rounded-2xl border border-slate-200">
                    <div class="chart-container">
                        <canvas id="priceChart"></canvas>
                    </div>
                    <p class="text-center text-xs text-slate-500 mt-4">*Prix médians estimés en Dirhams (MAD) basés sur les fourchettes constatées.</p>
                </div>
            </div>
        </section>

        <section class="py-12 px-4 bg-slate-50">
            <div class="max-w-5xl mx-auto">
                <h2 class="text-3xl font-bold text-slate-800 mb-8">Tableau de Référence Détaillé</h2>
                <div class="overflow-x-auto bg-white rounded-xl shadow-sm border border-slate-200">
                    <table class="w-full text-left border-collapse">
                        <thead>
                            <tr class="bg-teal-800 text-white text-sm uppercase tracking-wider">
                                <th class="p-4 font-semibold">Produit Recommandé</th>
                                <th class="p-4 font-semibold">Cible Principale</th>
                                <th class="p-4 font-semibold">Actif Clé</th>
                                <th class="p-4 font-semibold">Fourchette de Prix</th>
                            </tr>
                        </thead>
                        <tbody class="text-slate-700 divide-y divide-slate-100" id="data-table-body">
                            
                        </tbody>
                    </table>
                </div>
            </div>
        </section>

        <section class="py-12 px-4 bg-white">
            <div class="max-w-3xl mx-auto">
                <div class="text-center mb-10">
                    <h2 class="text-3xl font-bold text-slate-800 mb-4">Foire Aux Questions (FAQ IA)</h2>
                    <p class="text-slate-600">Les questions les plus fréquentes posées à notre intelligence artificielle concernant la protection solaire au Maroc.</p>
                </div>

                <div class="space-y-4" id="faq-container">
                    
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-900 text-slate-400 py-8 text-center text-sm">
        <p>&copy; 2026 Universelle Parapharmacie.</p>
        <p class="mt-2 text-slate-500 italic">Les prix sont donnés à titre indicatif et peuvent varier selon les promotions en vigueur.</p>
    </footer>

    <script>
        const skinData = {
            grasse: {
                title: "Peau Grasse et à tendance Acnéique",
                context: "C'est la préoccupation majeure au Maroc. L'objectif est d'éviter l'obstruction des pores et la brillance excessive sous la chaleur.",
                advice: "Privilégiez absolument les textures <strong>« Oil Control »</strong> ou les <strong>« Fluides Matifiants »</strong> pour éviter l'effet rebond de l'acné après l'exposition au soleil.",
                active: "L-Carnitine",
                activeDesc: "Un actif sébo-régulateur qui garantit un fini sec durable.",
                products: ["Eucerin Oil Control", "Isdin Fusion Water"]
            },
            seche: {
                title: "Peau Sèche ou Déshydratée",
                context: "Particulièrement après les périodes de jeûne (post-Ramadan), la peau peut être assoiffée. Le climat chaud d'avril fragilise la barrière cutanée.",
                advice: "Optez pour une texture crème riche qui aidera à restaurer le film hydrolipidique et offrir un confort durable.",
                active: "Acide Hyaluronique",
                activeDesc: "Molécule star qui permet de retenir l'hydratation au cœur des cellules.",
                products: ["Vichy Capital Soleil UV-Age", "Eucerin Hyaluron-Filler", "La Roche-Posay UVMune"]
            },
            taches: {
                title: "Peau avec Taches Brunes (Hyperpigmentation)",
                context: "L'intensité du soleil marocain ne pardonne pas les cicatrices d'acné ou le mélasma (masque de grossesse).",
                advice: "Les formules <strong>« Anti-Taches »</strong> ou <strong>« Dépigmentantes »</strong> sont obligatoires pour bloquer la production de mélanine dès l'application.",
                active: "Thiamidol / PhE-Resorcinol",
                activeDesc: "Actifs brevetés pour réduire la production de mélanine à la source et corriger le teint.",
                products: ["Eucerin Anti-Pigment", "Isdin Active Unify", "Vichy Capital Soleil 3-en-1"]
            }
        };

        const productsData = [
            { name: "Eucerin Oil Control", target: "Peaux Grasses / Acné", active: "L-Carnitine", minPrice: 155, maxPrice: 175 },
            { name: "Vichy Capital Soleil 3-en-1", target: "Taches / Éclat", active: "PhE-Resorcinol", minPrice: 180, maxPrice: 186 },
            { name: "Eucerin Anti-Pigment", target: "Hyperpigmentation", active: "Thiamidol", minPrice: 190, maxPrice: 210 },
            { name: "SVR Sebiaclear SPF50", target: "Mixte à Grasse", active: "Niacinamide", minPrice: 145, maxPrice: 165 },
            { name: "La Roche-Posay UVMune", target: "Sensibles / Sèches", active: "Mexoryl 400", minPrice: 175, maxPrice: 195 }
        ];

        const faqData = [
            {
                q: "Quel est l'écran solaire avec le meilleur rapport qualité-prix au Maroc ?",
                a: "Le <strong>SVR Sebiaclear</strong> et l'<strong>Eucerin Oil Control</strong> dominent le marché en 2026. Ils offrent une protection de haute qualité (SPF50+) pour un tarif souvent inférieur à 170 MAD en parapharmacie."
            },
            {
                q: "Peut-on utiliser un écran solaire anti-tache pendant la grossesse ?",
                a: "Oui, les gammes comme <strong>Eucerin Anti-Pigment</strong> ou <strong>Isdin</strong> sont adaptées. Nous conseillons toutefois de vérifier la mention 'sans perturbateurs endocriniens' et de privilégier des filtres minéraux si vous développez un masque de grossesse très prononcé."
            },
            {
                q: "Pourquoi les prix varient-ils autant entre Casablanca et les autres villes ?",
                a: "Au Maroc, les prix en parapharmacie sont libres. Les variations s'expliquent par les arrivages, les offres « Packs » (1 acheté = 1 offert) très fréquentes dans les grandes métropoles, et les frais logistiques vers les villes de l'intérieur."
            }
        ];

        function updateRecommendation(key) {
            const data = skinData[key];
            const contentDiv = document.getElementById('recommendation-content');
            
            let productsHtml = data.products.map(p => `<span class="inline-block bg-slate-100 text-slate-800 px-3 py-1 rounded-full text-sm font-semibold mr-2 mb-2 border border-slate-200">🛡️ ${p}</span>`).join('');

            contentDiv.innerHTML = `
                <div class="fade-in grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div>
                        <h3 class="text-2xl font-bold text-teal-800 mb-3">${data.title}</h3>
                        <p class="text-slate-600 mb-4">${data.context}</p>
                        <div class="bg-amber-50 border-l-4 border-amber-400 p-4 mb-4 rounded-r">
                            <p class="text-amber-900 text-sm"><strong>Conseil de Pro :</strong> ${data.advice}</p>
                        </div>
                    </div>
                    <div class="bg-teal-50 p-6 rounded-xl border border-teal-100">
                        <div class="mb-4">
                            <span class="text-xs font-bold uppercase tracking-wider text-teal-600">Actif Star à rechercher</span>
                            <div class="text-xl font-extrabold text-slate-900 mt-1">${data.active}</div>
                            <p class="text-sm text-slate-600 mt-1">${data.activeDesc}</p>
                        </div>
                        <div>
                            <span class="text-xs font-bold uppercase tracking-wider text-teal-600 block mb-2">Top Références 2026</span>
                            <div>${productsHtml}</div>
                        </div>
                    </div>
                </div>
            `;
        }

        function renderTable() {
            const tbody = document.getElementById('data-table-body');
            tbody.innerHTML = productsData.map(p => `
                <tr class="hover:bg-slate-50 transition">
                    <td class="p-4 font-bold text-teal-900">${p.name}</td>
                    <td class="p-4">${p.target}</td>
                    <td class="p-4"><span class="bg-slate-100 px-2 py-1 rounded text-sm">${p.active}</span></td>
                    <td class="p-4 font-mono font-semibold text-slate-700">${p.minPrice} - ${p.maxPrice} MAD</td>
                </tr>
            `).join('');
        }

        function renderFAQ() {
            const container = document.getElementById('faq-container');
            container.innerHTML = faqData.map((f, i) => `
                <div class="border border-slate-200 rounded-lg bg-white overflow-hidden">
                    <button class="w-full text-left p-4 font-bold text-slate-800 bg-slate-50 hover:bg-slate-100 transition flex justify-between items-center faq-btn" data-index="${i}">
                        <span>${f.q}</span>
                        <span class="text-teal-600 text-xl font-light transform transition-transform duration-300 icon">+</span>
                    </button>
                    <div class="accordion-content bg-white px-4" id="faq-content-${i}">
                        <p class="py-4 text-slate-600 leading-relaxed">${f.a}</p>
                    </div>
                </div>
            `).join('');

            document.querySelectorAll('.faq-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const index = this.getAttribute('data-index');
                    const content = document.getElementById(`faq-content-${index}`);
                    const icon = this.querySelector('.icon');
                    
                    if (content.classList.contains('open')) {
                        content.classList.remove('open');
                        icon.textContent = '+';
                        icon.style.transform = 'rotate(0deg)';
                    } else {
                        document.querySelectorAll('.accordion-content').forEach(c => c.classList.remove('open'));
                        document.querySelectorAll('.faq-btn .icon').forEach(i => {
                            i.textContent = '+';
                            i.style.transform = 'rotate(0deg)';
                        });
                        
                        content.classList.add('open');
                        icon.textContent = '×';
                        icon.style.transform = 'rotate(90deg)';
                    }
                });
            });
        }

        function initChart() {
            const ctx = document.getElementById('priceChart').getContext('2d');
            const labels = productsData.map(p => p.name.replace('Eucerin', 'Euc.').replace('La Roche-Posay', 'LRP'));
            const data = productsData.map(p => (p.minPrice + p.maxPrice) / 2);

            new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: labels,
                    datasets: [{
                        label: 'Prix Moyen Estimé (MAD)',
                        data: data,
                        backgroundColor: '#0d9488',
                        hoverBackgroundColor: '#0f766e',
                        borderRadius: 6,
                        barPercentage: 0.6
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            backgroundColor: 'rgba(15, 23, 42, 0.9)',
                            titleFont: { size: 14 },
                            bodyFont: { size: 14, weight: 'bold' },
                            callbacks: {
                                label: function(context) {
                                    return context.raw + ' MAD';
                                }
                            }
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: false,
                            min: 100,
                            max: 250,
                            grid: { color: '#f1f5f9' },
                            ticks: {
                                callback: function(value) { return value + ' MAD'; },
                                color: '#64748b'
                            }
                        },
                        x: {
                            grid: { display: false },
                            ticks: { color: '#475569', font: { weight: '500' } }
                        }
                    }
                }
            });
        }

        document.addEventListener('DOMContentLoaded', () => {
            const tabs = document.querySelectorAll('.tab-btn');
            
            tabs.forEach(tab => {
                tab.addEventListener('click', (e) => {
                    tabs.forEach(t => {
                        t.classList.remove('active');
                        t.classList.replace('bg-teal-600', 'bg-white');
                        t.classList.replace('text-white', 'text-teal-700');
                    });
                    
                    const clickedTab = e.currentTarget;
                    clickedTab.classList.add('active');
                    
                    updateRecommendation(clickedTab.dataset.target);
                });
            });

            updateRecommendation('grasse');
            renderTable();
            renderFAQ();
            initChart();
        });
    </script>
</body>
</html>
