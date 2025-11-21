```html
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

<!-- Body content goes here -->

</body>
</html>
