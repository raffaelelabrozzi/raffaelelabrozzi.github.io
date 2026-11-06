<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raffaele Labrozzi | Portfolio & Personal Site</title>
    <meta name="description" content="Sito personale di Raffaele Labrozzi - Senior Operations Manager, Program Lead & Process Re-engineering Professional.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-color: #f8fafc;
            --text-muted: #94a3b8;
            --accent-color: #38bdf8;
            --accent-hover: #0284c7;
            --border-color: #334155;
            --max-width: 1100px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 0 20px;
        }

        header {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 40px 0 20px 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--border-color);
        }

        .logo {
            font-size: 1.25rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            color: var(--text-color);
            text-decoration: none;
        }

        nav a {
            color: var(--text-muted);
            text-decoration: none;
            margin-left: 20px;
            font-size: 0.95rem;
            transition: color 0.2s;
        }

        nav a:hover {
            color: var(--accent-color);
        }

        .container {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 60px 0;
        }

        /* Hero Section */
        .hero {
            padding: 40px 0 80px 0;
        }

        .hero h1 {
            font-size: 3rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: var(--accent-color);
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 750px;
            margin-bottom: 30px;
        }

        .cta-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.2s;
            font-size: 0.95rem;
        }

        .btn-primary {
            background-color: var(--accent-color);
            color: #0f172a;
        }

        .btn-primary:hover {
            background-color: var(--accent-hover);
            color: #fff;
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--text-color);
            border: 1px solid var(--border-color);
        }

        .btn-secondary:hover {
            border-color: var(--accent-color);
            color: var(--accent-color);
        }

        /* Section Titles */
        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 40px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 40px;
            height: 3px;
            background-color: var(--accent-color);
            border-radius: 2px;
        }

        /* Experience / About */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 80px;
        }

        .about-card {
            background-color: var(--card-bg);
            padding: 25px;
            border-radius: 12px;
            border: 1px solid var(--border-color);
        }

        .about-card h3 {
            font-size: 1.1rem;
            color: var(--accent-color);
            margin-bottom: 10px;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 25px;
            margin-bottom: 80px;
        }

        .project-card {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 30px;
            border: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .project-card h3 {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }

        .project-meta {
            margin-bottom: 15px;
        }

        .project-meta p {
            font-size: 0.95rem;
            color: var(--text-muted);
            margin-bottom: 10px;
        }

        .project-meta strong {
            color: var(--text-color);
        }

        .tags {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-top: 15px;
        }

        .tag {
            background-color: rgba(56, 189, 248, 0.1);
            color: var(--accent-color);
            padding: 4px 10px;
            border-radius: 6px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        /* Skills Table */
        .skills-container {
            margin-bottom: 80px;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background-color: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--border-color);
        }

        th, td {
            padding: 18px 24px;
            text-align: left;
        }

        th {
            background-color: rgba(255, 255, 255, 0.03);
            color: var(--accent-color);
            font-weight: 600;
            border-bottom: 1px solid var(--border-color);
        }

        td {
            border-bottom: 1px solid var(--border-color);
            color: var(--text-muted);
        }

        tr:last-child td {
            border-bottom: none;
        }

        td strong {
            color: var(--text-color);
        }

        /* Footer */
        footer {
            max-width: var(--max-width);
            margin: 0 auto;
            padding: 40px 0;
            border-top: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        footer a {
            color: var(--accent-color);
            text-decoration: none;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            header {
                flex-direction: column;
                gap: 15px;
                align-items: flex-start;
            }
            nav a {
                margin-left: 0;
                margin-right: 15px;
            }
        }
    </style>
</head>
<body>

    <header>
        <a href="#" class="logo">Raffaele Labrozzi</a>
        <nav>
            <a href="#about">Chi Sono</a>
            <a href="#projects">Progetti</a>
            <a href="#skills">Competenze</a>
            <a href="#contact">Contatti</a>
        </nav>
    </header>

    <main class="container">
        
        <!-- HERO SECTION -->
        <section class="hero">
            <h1>Senior Operations Manager & <span>Program Lead</span></h1>
            <p>Oltre 16 anni di esperienza alla guida dell'ottimizzazione dei processi aziendali (BPR), della sicurezza informatica, della governance dei dati e dell'integrazione di soluzioni di AI generativa in contesti multinazionali.</p>
            <div class="cta-buttons">
                <a href="https://linkedin.com/in/raffaele-labrozzi-6473b715" target="_blank" class="btn btn-primary">Profilo LinkedIn</a>
                <a href="mailto:raffaelelabrozzi@gmail.com" class="btn btn-secondary">Invia un'Email</a>
            </div>
        </section>

        <!-- ABOUT SECTION -->
        <section id="about">
            <h2 class="section-title">Aree di Eccellenza</h2>
            <div class="about-grid">
                <div class="about-card">
                    <h3>Business Process Re-engineering</h3>
                    <p>Identificazione e risoluzione delle inefficienze operative attraverso la riprogettazione di flussi complessi da processi manuali ad automazioni batch scalabili.</p>
                </div>
                <div class="about-card">
                    <h3>Program & Project Management</h3>
                    <p>Gestione di iniziative cross-funzionali complesse in ambito Agile e Waterfall a livello globale (EMEA, APAC, Americas), garantendo tempi, budget e continuità.</p>
                </div>
                <div class="about-card">
                    <h3>Applied AI & Automation</h3>
                    <p>Progettazione di agenti virtuali e workflow con Large Language Models per la reportistica e l'analisi operativa. Promotore di forum manageriali sulla formazione AI.</p>
                </div>
                <div class="about-card">
                    <h3>Stakeholder Engagement</h3>
                    <p>Forte attitudine alla mediazione e al coordinamento tra architetture tecnologiche IT/Engineering e i requisiti pratici dei partner di business operativi.</p>
                </div>
            </div>
        </section>

        <!-- PROJECTS SECTION -->
        <section id="projects">
            <h2 class="section-title">Progetti & Case Studies</h2>
            <div class="projects-grid">
                
                <div class="project-card">
                    <div>
                        <h3>Re-Engineering & Automazione B2B</h3>
                        <div class="project-meta">
                            <p><strong>Sfida:</strong> Riconciliazione crediti ad alto volume gestita manualmente (circa 3.000 transazioni al mese).</p>
                            <p><strong>Soluzione:</strong> Ridisegno completo del processo verso un ciclo mensile automatizzato in batch con audit integrato.</p>
                            <p><strong>Risultato:</strong> Azzeramento del lavoro manuale ripetitivo, preservando la totale conformità finanziaria.</p>
                        </div>
                    </div>
                    <div class="tags">
                        <span class="tag">Process Automation</span>
                        <span class="tag">BPR</span>
                        <span class="tag">Finance Operations</span>
                    </div>
                </div>

                <div class="project-card">
                    <div>
                        <h3>Security & Application Migration</h3>
                        <div class="project-meta">
                            <p><strong>Sfida:</strong> Migrazione di 50+ applicazioni aziendali verso una nuova architettura di sicurezza Zero Trust senza downtime.</p>
                            <p><strong>Soluzione:</strong> Definizione di 3 track tecnici e 5 fasi operative con gate di verifica prima del rilascio.</p>
                            <p><strong>Risultato:</strong> 100% dei rilasci nei tempi e nel budget, con zero interruzioni sull'operatività live.</p>
                        </div>
                    </div>
                    <div class="tags">
                        <span class="tag">Zero Trust</span>
                        <span class="tag">Security Migration</span>
                        <span class="tag">Risk Management</span>
                    </div>
                </div>

                <div class="project-card">
                    <div>
                        <h3>Global Quality Data Governance</h3>
                        <p class="project-meta">
                            <strong style="display:block; margin-top:5px;">Sfida:</strong> 8+ processi di feedback qualitativo frammentati tra EMEA, APAC e Americas.<br>
                            <strong style="display:block; margin-top:5px;">Soluzione:</strong> Standardizzazione dei dati e implementazione di dashboard BI unificate.<br>
                            <strong style="display:block; margin-top:5px;">Risultato:</strong> Prima visibilità globale centralizzata per l'executive leadership.
                        </p>
                    </div>
                    <div class="tags">
                        <span class="tag">Tableau</span>
                        <span class="tag">Data Governance</span>
                        <span class="tag">Global Strategy</span>
                    </div>
                </div>

            </div>
        </section>

        <!-- SKILLS MATRIX -->
        <section id="skills">
            <h2 class="section-title">Competenze & Certificazioni</h2>
            <div class="skills-container">
                <table>
                    <thead>
                        <tr>
                            <th>Categoria</th>
                            <th>Competenze & Strumenti</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Project & Change Management</strong></td>
                            <td>SDLC, Agile / Waterfall, BPMN Process Mapping, Scope & Risk Management, UAT / QA Coordination</td>
                        </tr>
                        <tr>
                            <td><strong>Enterprise Systems & Analytics</strong></td>
                            <td>SAP (Solution Design - Logistics & Order Fulfilment), Tableau, Advanced Excel, Executive KPI Dashboards</td>
                        </tr>
                        <tr>
                            <td><strong>Applied AI & Automation</strong></td>
                            <td>Generative AI, Agentic Workflows, Automated Reporting, LLM Prompt Engineering, Process Automation</td>
                        </tr>
                        <tr>
                            <td><strong>Certificazioni</strong></td>
                            <td>Lean Six Sigma Yellow Belt, Professional Project Management, COPC Implementation Leader, IBM Generative AI, Machine Learning (Univ. of London)</td>
                        </tr>
                        <tr>
                            <td><strong>Lingue & Profilo</strong></td>
                            <td>Italiano (Madrelingua), Inglese (Fluente), Spagnolo (Base) | Giornalista Pubblicista iscritto all'Ordine</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

    </main>

    <footer id="contact">
        <p>&copy; 2026 Raffaele Labrozzi — Cork, Ireland</p>
        <p>Email: <a href="mailto:raffaelelabrozzi@gmail.com">raffaelelabrozzi@gmail.com</a> | <a href="https://linkedin.com/in/raffaele-labrozzi-6473b715" target="_blank">LinkedIn</a></p>
    </footer>

</body>
</html>
