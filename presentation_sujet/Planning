<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Planning TMDC - 14 Semaines</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
      min-height: 100vh;
      padding: 30px 20px;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
    }

    .header {
      text-align: center;
      margin-bottom: 40px;
      color: white;
    }

    .header h1 {
      font-size: 36px;
      margin-bottom: 10px;
      background: linear-gradient(135deg, #ff6b6b 0%, #feca57 50%, #48dbfb 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .header p {
      font-size: 16px;
      color: #bbb;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
      margin-bottom: 30px;
    }

    .stat-card {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      color: white;
    }

    .stat-value {
      font-size: 32px;
      font-weight: bold;
      background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .stat-label {
      font-size: 12px;
      color: #aaa;
      text-transform: uppercase;
      margin-top: 8px;
      letter-spacing: 1px;
    }

    .progress-bar {
      height: 6px;
      background: rgba(255, 255, 255, 0.1);
      margin-bottom: 30px;
      border-radius: 3px;
      overflow: hidden;
    }

    .progress-fill {
      height: 100%;
      background: linear-gradient(90deg, #ff6b6b 0%, #feca57 50%, #48dbfb 100%);
      width: 0%;
      transition: width 0.4s ease;
    }

    .filters {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 30px;
    }

    .filter-btn {
      padding: 10px 20px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      background: transparent;
      color: #bbb;
      border-radius: 25px;
      cursor: pointer;
      font-size: 13px;
      transition: all 0.3s;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      font-weight: 500;
    }

    .filter-btn:hover {
      background: rgba(255, 255, 255, 0.1);
      border-color: #48dbfb;
      color: #48dbfb;
    }

    .filter-btn.active {
      background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%);
      color: #1a1a2e;
      border-color: transparent;
    }

    .timeline {
      position: relative;
    }

    .semaine-block {
      margin-bottom: 30px;
      position: relative;
    }

    .semaine-header {
      display: flex;
      align-items: center;
      margin-bottom: 15px;
      gap: 15px;
    }

    .semaine-number {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      color: white;
      font-size: 18px;
      flex-shrink: 0;
    }

    .semaine-1 .semaine-number { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); }
    .semaine-2 .semaine-number { background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); }
    .semaine-3 .semaine-number { background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); }
    .semaine-4 .semaine-number { background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%); }
    .semaine-5 .semaine-number { background: linear-gradient(135deg, #fa709a 0%, #fee140 100%); }
    .semaine-6 .semaine-number { background: linear-gradient(135deg, #30cfd0 0%, #330867 100%); }
    .semaine-7 .semaine-number { background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%); }
    .semaine-8 .semaine-number { background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); }
    .semaine-9 .semaine-number { background: linear-gradient(135deg, #ff9a56 0%, #ff6a88 100%); }
    .semaine-10 .semaine-number { background: linear-gradient(135deg, #2af598 0%, #009efd 100%); }
    .semaine-11 .semaine-number { background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%); }
    .semaine-12 .semaine-number { background: linear-gradient(135deg, #ff9a56 0%, #ffb88c 100%); }
    .semaine-13 .semaine-number { background: linear-gradient(135deg, #a1c4fd 0%, #c2e9fb 100%); }
    .semaine-14 .semaine-number { background: linear-gradient(135deg, #fad0c4 0%, #ffecd2 100%); }

    .semaine-title {
      color: white;
    }

    .semaine-title h3 {
      font-size: 18px;
      margin-bottom: 5px;
    }

    .semaine-subtitle {
      font-size: 13px;
      color: #aaa;
    }

    .taches-container {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 10px;
      padding: 20px;
      margin-left: 65px;
      backdrop-filter: blur(5px);
    }

    .tache-item {
      display: flex;
      gap: 12px;
      margin-bottom: 12px;
      padding: 10px;
      border-radius: 6px;
      align-items: flex-start;
      cursor: pointer;
      transition: all 0.2s;
    }

    .tache-item:hover {
      background: rgba(255, 255, 255, 0.05);
    }

    .tache-item.completed {
      opacity: 0.6;
    }

    .tache-item.completed .tache-text {
      text-decoration: line-through;
      color: #888;
    }

    .checkbox-wrapper {
      margin-top: 3px;
    }

    .custom-checkbox {
      width: 20px;
      height: 20px;
      cursor: pointer;
      accent-color: #48dbfb;
    }

    .tache-text {
      color: #ddd;
      font-size: 13px;
      line-height: 1.5;
      flex: 1;
    }

    .tache-tag {
      display: inline-block;
      background: rgba(72, 219, 251, 0.2);
      color: #48dbfb;
      padding: 3px 8px;
      border-radius: 4px;
      font-size: 11px;
      margin-right: 6px;
      margin-top: 5px;
    }

    .semaine-block.hidden {
      display: none;
    }

    .export-btn {
      position: fixed;
      bottom: 30px;
      right: 30px;
      padding: 15px 25px;
      background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%);
      color: #1a1a2e;
      border: none;
      border-radius: 50px;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      box-shadow: 0 8px 30px rgba(255, 107, 107, 0.3);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .export-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 40px rgba(255, 107, 107, 0.5);
    }

    @media (max-width: 768px) {
      .header h1 {
        font-size: 24px;
      }

      .taches-container {
        margin-left: 0;
        margin-top: 15px;
      }

      .semaine-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .tache-text {
        font-size: 12px;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="header">
      <h1>🧬 TMDC as Photosensitizers</h1>
      <p>14-week Theoretical Calculation & Research Journey</p>
    </div>

    <div class="stats">
      <div class="stat-card">
        <div class="stat-value" id="total-tasks">0</div>
        <div class="stat-label">Tâches totales</div>
      </div>
      <div class="stat-card">
        <div class="stat-value" id="completed-tasks">0</div>
        <div class="stat-label">Complétées</div>
      </div>
      <div class="stat-card">
        <div class="stat-value" id="progress-percent">0%</div>
        <div class="stat-label">Progression</div>
      </div>
    </div>

    <div class="progress-bar">
      <div class="progress-fill" id="progress-fill"></div>
    </div>

    <div class="filters">
      <button class="filter-btn active" onclick="filterSemaines('all')">Toutes les semaines</button>
      <button class="filter-btn" onclick="filterSemaines('apprentissage')">Apprentissage</button>
      <button class="filter-btn" onclick="filterSemaines('simulations')">Simulations</button>
      <button class="filter-btn" onclick="filterSemaines('analyse')">Analyse</button>
      <button class="filter-btn" onclick="filterSemaines('redaction')">Rédaction</button>
    </div>

    <div class="timeline" id="timeline">
      <!-- Les semaines seront générées par JavaScript -->
    </div>
  </div>

  <button class="export-btn" onclick="exportToCSV()">📥 Exporter</button>

  <script>
    const planningData = [
      // SEMAINES 1-3: APPRENTISSAGE FONDAMENTAL
      {
        semaine: 1,
        titre: "Fondations cristallographiques",
        categorie: "apprentissage",
        soustitre: "Structures & Principes DFT",
        taches: [
          { texte: "Maîtriser les réseaux de Bravais, zones de Brillouin, réseaux réciproques", tag: "Théorie" },
          { texte: "Premiers calculs DFT: optimisation géométrique MoSe₂ avec Quantum ESPRESSO", tag: "Pratique" },
          { texte: "Étudier la structure cristalline des TMDC (groupe d'espace P63/mmc)", tag: "Théorie" },
          { texte: "Extraire et interpréter les paramètres de maille calculés", tag: "Analyse" }
        ]
      },
      {
        semaine: 2,
        titre: "Structure électronique & bandes",
        categorie: "apprentissage",
        soustitre: "Diagrammes de bandes énergétiques",
        taches: [
          { texte: "Cours approfondi sur DFT, approximation GGA, limite de Kohn-Sham", tag: "Théorie" },
          { texte: "Calculs de structure de bandes (chemin Γ-M-K-Γ) pour MoSe₂ et WSe₂", tag: "Pratique" },
          { texte: "Analyse du caractère orbital (d vs p) aux points critiques", tag: "Analyse" },
          { texte: "Interprétation de la limite directe/indirecte du gap", tag: "Analyse" }
        ]
      },
      {
        semaine: 3,
        titre: "Couplage spin-orbite & excitons",
        categorie: "apprentissage",
        soustitre: "Au-delà de la DFT classique",
        taches: [
          { texte: "Comprendre le couplage spin-orbite (SOC) et son rôle dans les TMDC", tag: "Théorie" },
          { texte: "Relancer calculs avec SOC activé - Observer le dédoublement de bandes", tag: "Pratique" },
          { texte: "Introduction à TD-DFT pour excitons et transitions optiques", tag: "Théorie" },
          { texte: "Premiers calculs d'états excités (énergies, forces d'oscillateur)", tag: "Pratique" }
        ]
      },

      // SEMAINES 4-6: DYNAMIQUE & STABILITÉ
      {
        semaine: 4,
        titre: "Dynamique moléculaire",
        categorie: "simulations",
        soustitre: "Stabilité thermique & trajectoires",
        taches: [
          { texte: "Cours complet sur MD: ensembles NVT, NPT, thermostat Nosé-Hoover", tag: "Théorie" },
          { texte: "Installation LAMMPS et création de premiers scripts de simulation", tag: "Pratique" },
          { texte: "Lancer MD NVT à 300K (10 ps) sur supercellule MoSe₂", tag: "Pratique" },
          { texte: "Analyser RMSD, RMSF, stabilité énergétique avec trajectoire", tag: "Analyse" }
        ]
      },
      
      
      
      
      {
        semaine: 5,
        titre: "Propriétés dynamiques",
        categorie: "simulations",
        soustitre: "Corrélations & ab initio MD",
        taches: [
          { texte: "Extraire propriétés: diffusion atomique, fonctions de corrélation radiale", tag: "Analyse" },
          { texte: "Comparaison potentiels empiriques vs DFT pour transférabilité", tag: "Théorie" },
          { texte: "Premier test de Car-Parrinello MD avec CP2K (1 ps court)", tag: "Pratique" },
          { texte: "Benchmark DM classique vs ab initio - Analyser les écarts", tag: "Analyse" }
        ]
      },
      {
        semaine: 6,
        titre: "Phonons & thermique",
        categorie: "simulations",
        soustitre: "Propriétés vibrationnelles",
        taches: [
          { texte: "Calculs des modes de phonons avec Quantum ESPRESSO", tag: "Pratique" },
          { texte: "Extraction densité d'états vibrationnels (PDOS) et analyse stabilité", tag: "Analyse" },
          { texte: "Comparaison MoSe₂ vs WSe₂: fréquences, stabilité dynamique", tag: "Analyse" },
          { texte: "Évaluation influence défauts structuraux sur phonons", tag: "Analyse" }
        ]
      },

      // SEMAINES 7-9: ANALYSE PHOTOPHYSIQUE & BENCHMARK
      {
        semaine: 7,
        titre: "Spectroscopie calculée",
        categorie: "analyse",
        soustitre: "Longueurs d'onde & comparaison expérience",
        taches: [
          { texte: "Calculs TD-DFT complets pour MoSe₂ et WSe₂ (énergies, oscillateurs)", tag: "Pratique" },
          { texte: "Extraction λ_max théoriques et comparaison avec littérature expérimentale", tag: "Analyse" },
          { texte: "Étude effet nombre de couches (mono- vs bi-couche) et confinement", tag: "Analyse" },
          { texte: "Analyse du caractère des transitions: local vs charge-transfer", tag: "Analyse" }
        ]
      },
      {
        semaine: 8,
        titre: "Ciblage mitochondrial",
        categorie: "analyse",
        soustitre: "Modélisation TMDC + TPP+",
        taches: [
          { texte: "Cours sur ciblage subcellulaire et triphenylphosphonium (TPP+)", tag: "Théorie" },
          { texte: "Construction et optimisation géométrie TMDC-TPP+ dans Gaussian 09", tag: "Pratique" },
          { texte: "Calculs TD-DFT du conjugué et analyse charge-transfer (CT)", tag: "Pratique" },
          { texte: "Cartographie MEP (potentiel électrostatique) avec Multiwfn", tag: "Analyse" }
        ]
      },
      {
        semaine: 9,
        titre: "Benchmarking complet",
        categorie: "analyse",
        soustitre: "ROS, photostabilité & sélection candidat",
        taches: [
          { texte: "Analyse facteurs production ROS (Type I vs Type II photosensitization)", tag: "Théorie" },
          { texte: "Calcul constantes décroissance non-radiative et durée de vie singulet", tag: "Pratique" },
          { texte: "Graphique radar multi-critères: λ_max, SOC, CT, photostabilité, k_nr", tag: "Analyse" },
          { texte: "Sélection meilleur candidat avec justification quantitative", tag: "Analyse" }
        ]
      },

      // SEMAINES 10-14: RÉDACTION & PRÉSENTATION
      {
        semaine: 10,
        titre: "Rédaction Partie 1",
        categorie: "redaction",
        soustitre: "Intro + Méthodes + Résultats élec.",
        taches: [
          { texte: "Plan détaillé du rapport et rédaction Introduction (objectifs, TNBC, PDT)", tag: "Écriture" },
          { texte: "Section Méthodes complète: DFT, TD-DFT, SOC, MD + workflow schémas", tag: "Écriture" },
          { texte: "Résultats partie 1: structures, bandes, spectres + figures haute résolution", tag: "Écriture" },
          { texte: "Relecture cohérence et logique narrative", tag: "Révision" }
        ]
      },
      {
        semaine: 11,
        titre: "Rédaction Partie 2",
        categorie: "redaction",
        soustitre: "Discussion & perspectives",
        taches: [
          { texte: "Résultats partie 2: MD, phonons, propriétés dynamiques + tableaux", tag: "Écriture" },
          { texte: "Discussion complète: validation méthode, comparaison prototypes, ciblage", tag: "Écriture" },
          { texte: "Lien avec défis cliniques: hypoxie, sélectivité microenvironnement tumoral", tag: "Écriture" },
          { texte: "Conclusion et perspectives recherche future", tag: "Écriture" }
        ]
      },
      {
        semaine: 12,
        titre: "Présentation Slide 1",
        categorie: "redaction",
        soustitre: "Création support visuel",
        taches: [
          { texte: "Intégration retours encadrant - corrections majeures et figures finales", tag: "Révision" },
          { texte: "Structure présentation (20-25 diapos) et préparation des diapos visuelles", tag: "Design" },
          { texte: "Slides 1-8: Contexte, motivation, TMDC, PDT, approche théorique", tag: "Design" },
          { texte: "Slides 9-14: Résultats structures, bandes, spectres avec schémas simplifiés", tag: "Design" }
        ]
      },
      {
        semaine: 13,
        titre: "Présentation Slide 2",
        categorie: "redaction",
        soustitre: "Finition & répétition",
        taches: [
          { texte: "Slides 15-20: MD, benchmark, ciblage, discussion et conclusions", tag: "Design" },
          { texte: "Préparation fiche réponses questions techniques + timing (15 min)", tag: "Préparation" },
          { texte: "Vérification technique vidéoprojecteur, animations, PDF export", tag: "Technique" },
          { texte: "Répétition finale complète avec feedback encadrant", tag: "Répétition" }
        ]
      },
      {
        semaine: 14,
        titre: "Soutenance & clôture",
        categorie: "redaction",
        soustitre: "Le grand jour!",
        taches: [
          { texte: "Soumission rapport final version complète & archivage fichiers calcul", tag: "Admin" },
          { texte: " SOUTENANCE ORALE (15 min présentation + 10 min questions)", tag: "Événement" },
          { texte: "Bilan personnel: compétences acquises, défis surmontés, leçons", tag: "Réflexion" },
          { texte: "Préparation suite: thèse, publications, poster conférence", tag: "Perspective" }
        ]
      }
    ];

    function renderTimeline() {
      const timeline = document.getElementById('timeline');
      timeline.innerHTML = '';

      planningData.forEach((sem) => {
        const block = document.createElement('div');
        block.className = `semaine-block semaine-${sem.semaine}`;
        block.setAttribute('data-categorie', sem.categorie);

        block.innerHTML = `
          <div class="semaine-header">
            <div class="semaine-number">${sem.semaine}</div>
            <div class="semaine-title">
              <h3>${sem.titre}</h3>
              <div class="semaine-subtitle">${sem.soustitre}</div>
            </div>
          </div>
          <div class="taches-container">
            ${sem.taches.map((tache, idx) => `
              <div class="tache-item" onclick="toggleCheckbox(event)">
                <div class="checkbox-wrapper">
                  <input type="checkbox" class="custom-checkbox" data-semaine="${sem.semaine}" data-index="${idx}" onchange="updateProgress()">
                </div>
                <div class="tache-text">
                  ${tache.texte}
                  <div class="tache-tag">${tache.tag}</div>
                </div>
              </div>
            `).join('')}
          </div>
        `;

        timeline.appendChild(block);
      });

      updateProgress();
    }

    function toggleCheckbox(e) {
      if (e.target.tagName !== 'INPUT') {
        const checkbox = e.currentTarget.querySelector('.custom-checkbox');
        checkbox.checked = !checkbox.checked;
        updateProgress();
      }
    }

    function updateProgress() {
      const checkboxes = document.querySelectorAll('.custom-checkbox');
      const total = checkboxes.length;
      const completed = Array.from(checkboxes).filter(cb => cb.checked).length;
      const percentage = total > 0 ? Math.round((completed / total) * 100) : 0;

      document.getElementById('total-tasks').textContent = total;
      document.getElementById('completed-tasks').textContent = completed;
      document.getElementById('progress-percent').textContent = percentage + '%';
      document.getElementById('progress-fill').style.width = percentage + '%';

      checkboxes.forEach(cb => {
        const item = cb.closest('.tache-item');
        if (cb.checked) {
          item.classList.add('completed');
        } else {
          item.classList.remove('completed');
        }
      });

      saveProgress();
    }

    function filterSemaines(categorie) {
      const buttons = document.querySelectorAll('.filter-btn');
      buttons.forEach(btn => btn.classList.remove('active'));
      event.target.classList.add('active');

      const blocks = document.querySelectorAll('.semaine-block');
      blocks.forEach(block => {
        if (categorie === 'all') {
          block.classList.remove('hidden');
        } else {
          block.classList.toggle('hidden', block.getAttribute('data-categorie') !== categorie);
        }
      });
    }

    function saveProgress() {
      const checkboxes = document.querySelectorAll('.custom-checkbox');
      const progress = {};
      checkboxes.forEach(cb => {
        const key = `${cb.dataset.semaine}-${cb.dataset.index}`;
        progress[key] = cb.checked;
      });
      localStorage.setItem('tmdcProgress', JSON.stringify(progress));
    }

    function loadProgress() {
      const saved = localStorage.getItem('tmdcProgress');
      if (saved) {
        const progress = JSON.parse(saved);
        Object.keys(progress).forEach(key => {
          const checkbox = document.querySelector(`[data-semaine="${key.split('-')[0]}"][data-index="${key.split('-')[1]}"]`);
          if (checkbox) {
            checkbox.checked = progress[key];
          }
        });
        updateProgress();
      }
    }

    function exportToCSV() {
      let csv = 'Semaine,Titre,Catégorie,Tâche,Statut\n';

      const blocks = document.querySelectorAll('.semaine-block');
      blocks.forEach(block => {
        const semaine = block.getAttribute('class').match(/semaine-(\d+)/)[1];
        const titre = block.querySelector('h3').textContent;
        const categorie = block.getAttribute('data-categorie');
        
        block.querySelectorAll('.custom-checkbox').forEach(cb => {
          const tache = cb.closest('.tache-item').querySelector('.tache-text').textContent.trim().split('\n')[0];
          const status = cb.checked ? 'Complété' : 'À faire';
          const escaped = tache.replace(/"/g, '""');
          csv += `"${semaine}","${titre}","${categorie}","${escaped}","${status}"\n`;
        });
      });

      const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });
      const link = document.createElement('a');
      const url = URL.createObjectURL(blob);
      link.setAttribute('href', url);
      link.setAttribute('download', 'planning_tmdc_14semaines.csv');
      link.style.visibility = 'hidden';
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }

    // Initialisation
    renderTimeline();
    loadProgress();
  </script>
</body>
</html>
