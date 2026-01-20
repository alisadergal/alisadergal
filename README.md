<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Siemens Interview Prep - Alisa's Guide</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --siemens-teal: #009999;
            --siemens-dark: #00202e;
            --siemens-light: #e8f5f5;
            --github-dark: #0d1117;
            --github-border: #30363d;
            --github-text: #c9d1d9;
            --github-text-secondary: #8b949e;
            --github-green: #238636;
            --github-blue: #1f6feb;
            --github-purple: #8957e5;
            --github-orange: #d29922;
            --github-red: #da3633;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: var(--github-dark);
            color: var(--github-text);
            line-height: 1.6;
            padding: 0;
            margin: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, var(--siemens-dark) 0%, #004d66 100%);
            border: 1px solid var(--github-border);
            border-radius: 12px;
            padding: 40px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, rgba(0, 153, 153, 0.2) 0%, transparent 70%);
            pointer-events: none;
        }

        .header h1 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 10px;
            color: white;
            position: relative;
            z-index: 1;
        }

        .header .subtitle {
            font-size: 1.2rem;
            color: var(--siemens-light);
            margin-bottom: 20px;
            position: relative;
            z-index: 1;
        }

        .badges {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
            font-family: 'JetBrains Mono', monospace;
        }

        .badge-date {
            background: var(--github-green);
            color: white;
        }

        .badge-location {
            background: var(--github-blue);
            color: white;
        }

        .badge-role {
            background: var(--github-purple);
            color: white;
        }

        .badge-company {
            background: var(--siemens-teal);
            color: white;
        }

        /* Stats Bar */
        .stats-bar {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .stat-card {
            background: #161b22;
            border: 1px solid var(--github-border);
            border-radius: 8px;
            padding: 20px;
            text-align: center;
        }

        .stat-card .number {
            font-size: 2rem;
            font-weight: 800;
            color: var(--siemens-teal);
            margin-bottom: 5px;
        }

        .stat-card .label {
            font-size: 0.9rem;
            color: var(--github-text-secondary);
        }

        /* Section */
        .section {
            background: #161b22;
            border: 1px solid var(--github-border);
            border-radius: 8px;
            padding: 30px;
            margin-bottom: 20px;
        }

        .section h2 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: white;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section h3 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-top: 30px;
            margin-bottom: 15px;
            color: var(--siemens-teal);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .section h4 {
            font-size: 1.1rem;
            font-weight: 600;
            margin-top: 20px;
            margin-bottom: 10px;
            color: var(--github-blue);
        }

        .icon {
            font-size: 1.5rem;
        }

        /* Lists */
        ul, ol {
            margin-left: 20px;
            margin-bottom: 15px;
        }

        li {
            margin-bottom: 8px;
            color: var(--github-text);
        }

        /* Highlight boxes */
        .highlight-box {
            background: rgba(31, 111, 235, 0.1);
            border-left: 4px solid var(--github-blue);
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .success-box {
            background: rgba(35, 134, 54, 0.1);
            border-left: 4px solid var(--github-green);
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .warning-box {
            background: rgba(210, 153, 34, 0.1);
            border-left: 4px solid var(--github-orange);
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .tip-box {
            background: rgba(137, 87, 229, 0.1);
            border-left: 4px solid var(--github-purple);
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .box-title {
            font-weight: 700;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* Code blocks */
        code {
            background: #0d1117;
            padding: 3px 8px;
            border-radius: 4px;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.9em;
            color: var(--siemens-teal);
        }

        .quote {
            border-left: 4px solid var(--github-border);
            padding-left: 20px;
            margin: 20px 0;
            font-style: italic;
            color: var(--github-text-secondary);
        }

        /* Collapsible sections */
        details {
            background: #0d1117;
            border: 1px solid var(--github-border);
            border-radius: 6px;
            padding: 15px;
            margin: 15px 0;
        }

        summary {
            font-weight: 600;
            cursor: pointer;
            user-select: none;
            display: flex;
            align-items: center;
            gap: 10px;
            color: var(--siemens-teal);
        }

        summary:hover {
            color: white;
        }

        details[open] summary {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid var(--github-border);
        }

        /* Project cards */
        .project-card {
            background: #0d1117;
            border: 1px solid var(--github-border);
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 15px;
            transition: border-color 0.2s;
        }

        .project-card:hover {
            border-color: var(--siemens-teal);
        }

        .project-title {
            font-weight: 700;
            font-size: 1.1rem;
            color: white;
            margin-bottom: 10px;
        }

        .project-meta {
            display: flex;
            gap: 10px;
            margin-bottom: 10px;
            flex-wrap: wrap;
        }

        .tag {
            background: rgba(0, 153, 153, 0.2);
            color: var(--siemens-teal);
            padding: 4px 10px;
            border-radius: 12px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        /* Table */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid var(--github-border);
        }

        th {
            background: #0d1117;
            font-weight: 700;
            color: var(--siemens-teal);
        }

        /* Question list */
        .question {
            background: #0d1117;
            border: 1px solid var(--github-border);
            border-radius: 6px;
            padding: 15px 20px;
            margin-bottom: 15px;
        }

        .question-title {
            font-weight: 700;
            color: var(--github-blue);
            margin-bottom: 8px;
        }

        .question-why {
            color: var(--github-text-secondary);
            font-size: 0.9rem;
            font-style: italic;
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid var(--github-border);
            color: var(--github-text-secondary);
            font-size: 0.9rem;
        }

        .footer strong {
            color: var(--siemens-teal);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }

            .container {
                padding: 20px 15px;
            }

            .stats-bar {
                grid-template-columns: 1fr;
            }
        }

        /* Print styles */
        @media print {
            body {
                background: white;
                color: black;
            }

            .section, .header {
                border: 1px solid #ddd;
                page-break-inside: avoid;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>🎯 Siemens Interview Preparation Guide</h1>
            <div class="subtitle">Business IT Industrial Placement • Manchester, UK</div>
            <div class="badges">
                <span class="badge badge-date">📅 January 21, 2026</span>
                <span class="badge badge-location">📍 Manchester</span>
                <span class="badge badge-role">💼 Business IT Placement</span>
                <span class="badge badge-company">⚡ Siemens AG</span>
            </div>
        </div>

        <!-- Stats Bar -->
        <div class="stats-bar">
            <div class="stat-card">
                <div class="number">€75.9B</div>
                <div class="label">FY2024 Revenue</div>
            </div>
            <div class="stat-card">
                <div class="number">312K+</div>
                <div class="label">Global Employees</div>
            </div>
            <div class="stat-card">
                <div class="number">£560M</div>
                <div class="label">HS2 UK Contract</div>
            </div>
            <div class="stat-card">
                <div class="number">2026</div>
                <div class="label">Chippenham Facility Opens</div>
            </div>
        </div>

        <!-- Company Overview -->
        <div class="section">
            <h2>🏢 About Siemens</h2>
            
            <div class="success-box">
                <div class="box-title">🎯 Company Mission</div>
                <strong>"Creating technology to transform the everyday, for everyone"</strong> by combining the real and digital worlds.
            </div>

            <h3>🔑 Four Core Focus Areas</h3>
            <div class="project-card">
                <div class="project-title">Industry</div>
                <div class="project-meta">
                    <span class="tag">Manufacturing</span>
                    <span class="tag">Automation</span>
                    <span class="tag">Industrial AI</span>
                </div>
                <p>Digital manufacturing, industrial automation, and AI-driven optimization</p>
            </div>

            <div class="project-card">
                <div class="project-title">Infrastructure</div>
                <div class="project-meta">
                    <span class="tag">Buildings</span>
                    <span class="tag">Energy Grids</span>
                    <span class="tag">Smart Cities</span>
                </div>
                <p>Smart building management, energy systems, and digital infrastructure</p>
            </div>

            <div class="project-card">
                <div class="project-title">Mobility</div>
                <div class="project-meta">
                    <span class="tag">Rail</span>
                    <span class="tag">Transportation</span>
                    <span class="tag">Signalling</span>
                </div>
                <p>Rail systems, signalling technology, and sustainable transportation</p>
            </div>

            <div class="project-card">
                <div class="project-title">Healthcare</div>
                <div class="project-meta">
                    <span class="tag">Medical Tech</span>
                    <span class="tag">Diagnostics</span>
                    <span class="tag">Siemens Healthineers</span>
                </div>
                <p>Medical technology and healthcare innovation through Siemens Healthineers</p>
            </div>

            <h3>📊 Recent Financial Performance</h3>
            <ul>
                <li><strong>Revenue:</strong> €75.9 billion (FY2024)</li>
                <li><strong>Net Income:</strong> €9.0 billion</li>
                <li><strong>Global Workforce:</strong> ~312,000 employees</li>
                <li><strong>Strategy:</strong> Transforming into a "ONE Tech Company"</li>
            </ul>
        </div>

        <!-- Strategic Initiatives -->
        <div class="section">
            <h2>🚀 Major Strategic Initiatives</h2>

            <details open>
                <summary>⚡ Siemens Xcelerator Platform - THE BIG ONE!</summary>
                <div class="highlight-box">
                    <div class="box-title">💡 What is Xcelerator?</div>
                    <p>Siemens' <strong>open digital business platform</strong> designed to accelerate digital transformation for companies of all sizes.</p>
                </div>

                <h4>Three Core Components:</h4>
                <ol>
                    <li><strong>Curated Portfolio:</strong> IoT-enabled hardware, software, and digital services from Siemens and certified third parties</li>
                    <li><strong>Partner Ecosystem:</strong> Collaborations with NVIDIA, AWS, Microsoft, Accenture</li>
                    <li><strong>Marketplace:</strong> Platform for customers, partners, and developers to interact and transact</li>
                </ol>

                <div class="tip-box">
                    <div class="box-title">🎯 Why Mention This</div>
                    This is Siemens' flagship platform for making digital transformation "easier, faster, and at scale." Showing you understand Xcelerator demonstrates deep company research.
                </div>
            </details>

            <details>
                <summary>🤖 Industrial AI Leadership</summary>
                
                <div class="quote">
                    <strong>CEO Roland Busch:</strong> "Industrial AI is a game-changer that will create significant positive impact in the real world across all industries."
                </div>

                <h4>Key AI Initiatives:</h4>
                <ul>
                    <li><strong>Vasi Philomin</strong> (former AWS VP of Generative AI) appointed as EVP of Data and AI - just hired!</li>
                    <li>Developing their <strong>first industrial foundation model</strong> for engineering optimization</li>
                    <li><strong>Bionic Agent:</strong> Gen AI solution for automated data extraction and process optimization</li>
                    <li><strong>Data Access Initiative:</strong> Creating a centralized data marketplace connecting Siemens' digital landscape</li>
                    <li><strong>Teamcenter Copilot:</strong> Natural language queries for PLM data</li>
                </ul>

                <div class="success-box">
                    <div class="box-title">✅ Bionic Agent Success Story</div>
                    <p>Deployed at Siemens Smart Infrastructure (SI Buildings UK) - achieved streamlined customer request management through automated entity extraction, PO validation, and real-time data checking. Transformed weeks of work into minutes!</p>
                </div>
            </details>

            <details>
                <summary>👥 Digital Twin Technology</summary>
                
                <h4>Key Partnerships & Technology:</h4>
                <ul>
                    <li><strong>NVIDIA Omniverse collaboration</strong> for industrial metaverse applications</li>
                    <li><strong>Teamcenter Digital Reality Viewer:</strong> Physically based visualization for product lifecycle management</li>
                    <li><strong>Energy System Twins:</strong> For decarbonization planning and optimization</li>
                    <li>Creating "digital threads" connecting design → manufacturing → operations</li>
                </ul>

                <div class="highlight-box">
                    <div class="box-title">🔗 Digital Threads Concept</div>
                    <p>Moving from managing <code>Bills of Materials</code> to orchestrating <code>Bills of Information</code> - dynamic, role-based information delivery across the product lifecycle.</p>
                </div>
            </details>

            <details>
                <summary>🤝 Major Strategic Partnerships (2025)</summary>
                
                <div class="project-card">
                    <div class="project-title">Accenture Siemens Business Group</div>
                    <div class="project-meta">
                        <span class="tag">7,000 professionals</span>
                        <span class="tag">Global</span>
                        <span class="tag">2025</span>
                    </div>
                    <p>Dedicated business practice combining Siemens' automation, AI, and software with Accenture's data and AI capabilities to help clients reinvent engineering and manufacturing.</p>
                </div>

                <div class="project-card">
                    <div class="project-title">JetZero Aviation Partnership</div>
                    <div class="project-meta">
                        <span class="tag">Sustainable Aviation</span>
                        <span class="tag">Digital Twin</span>
                        <span class="tag">CES 2025</span>
                    </div>
                    <p>Revolutionary blended wing aircraft design aiming for 50% fuel efficiency improvement and zero carbon emissions by 2035. Building "Factory of the Future" using Xcelerator platform.</p>
                </div>

                <div class="project-card">
                    <div class="project-title">AWS Strategic Collaboration</div>
                    <div class="project-meta">
                        <span class="tag">Smart Infrastructure</span>
                        <span class="tag">AI</span>
                        <span class="tag">Cloud</span>
                    </div>
                    <p>Implementing Building X platform with AWS cloud services and AI (Amazon Nova, Amazon Bedrock) for smart, sustainable infrastructure.</p>
                </div>
            </details>
        </div>

        <!-- UK Projects -->
        <div class="section">
            <h2>🇬🇧 UK-Specific Projects & Investments</h2>

            <div class="warning-box">
                <div class="box-title">💰 Total UK Investment</div>
                <strong>£340 million+</strong> invested in UK operations in recent years, including major infrastructure projects.
            </div>

            <h3>🚄 Major Infrastructure Projects</h3>

            <div class="project-card">
                <div class="project-title">HS2 Railway Contract - £560 Million</div>
                <div class="project-meta">
                    <span class="tag">Starting 2025</span>
                    <span class="tag">Rail Infrastructure</span>
                    <span class="tag">Digital Signalling</span>
                </div>
                <p><strong>What:</strong> Four major contracts for Britain's second high-speed railway (225km London to West Midlands)</p>
                <p><strong>Innovation:</strong> First time implementing <strong>Automatic Train Operations (ATO) over ETCS Level 2</strong> on a high-speed network</p>
                <p><strong>Impact:</strong> Semi-automated train operations improving capacity, punctuality, and energy efficiency</p>
                <p><strong>Scope:</strong> Digital signalling system, Engineering Management System, telecommunications, and long-term maintenance</p>
            </div>

            <div class="project-card">
                <div class="project-title">Chippenham Rail Technology Facility - £100 Million</div>
                <div class="project-meta">
                    <span class="tag">Opening 2026</span>
                    <span class="tag">800 employees</span>
                    <span class="tag">Breaking ground 2025</span>
                </div>
                <p><strong>What:</strong> State-of-the-art facility for rail signalling and control systems</p>
                <p><strong>Location:</strong> Chippenham, Wiltshire</p>
                <p><strong>Purpose:</strong> Development and production for domestic and international markets</p>
                <p><strong>Timeline:</strong> Construction started in 2025, operational in 2026</p>
            </div>

            <div class="project-card">
                <div class="project-title">Airbus Decarbonization Partnership</div>
                <div class="project-meta">
                    <span class="tag">3 UK sites</span>
                    <span class="tag">Sustainability</span>
                    <span class="tag">2025-2030</span>
                </div>
                <p><strong>Goal:</strong> 80kt CO₂e reduction annually by 2030</p>
                <p><strong>Technology:</strong> Energy System Twins, heat pumps, smart metering, renewable energy integration</p>
                <p><strong>Partner:</strong> Supported by Capgemini for digitalization expertise</p>
            </div>

            <div class="project-card">
                <div class="project-title">Manchester Digital Experience Centre</div>
                <div class="project-meta">
                    <span class="tag">Manchester</span>
                    <span class="tag">Demo Centre</span>
                    <span class="tag">Active</span>
                </div>
                <p><strong>Purpose:</strong> Fully operational showcase of transformative digital technologies</p>
                <p><strong>Focus:</strong> Productivity enhancement, flexible manufacturing, performance optimization</p>
                <p><strong>For:</strong> Industrial users to see digital enterprise solutions in action</p>
            </div>

            <div class="project-card">
                <div class="project-title">Kings Heath Multi-Functional Centre - £6 Million</div>
                <div class="project-meta">
                    <span class="tag">Northampton</span>
                    <span class="tag">30 jobs created</span>
                    <span class="tag">Opened 2024</span>
                </div>
                <p><strong>Purpose:</strong> Train modifications and upgrades for UK passenger fleet</p>
                <p><strong>First Project:</strong> East Midland Railway Class 360 refurbishment</p>
                <p><strong>Mobile Capability:</strong> Technicians deployed nationwide for modification work</p>
            </div>

            <h3>🌱 Sustainability Achievements</h3>
            <div class="success-box">
                <div class="box-title">✅ Siemens Mobility UK&I - 36% Emissions Cut in 2024</div>
                <ul>
                    <li>Over <strong>2,100 tonnes of CO₂e</strong> saved (Scope 1 & 2)</li>
                    <li><strong>1,000 kW</strong> solar panel capacity installed (powers ~307 homes)</li>
                    <li><strong>84%</strong> of diesel replaced with HVO (hydrotreated vegetable oil)</li>
                    <li><strong>50%</strong> emissions reduction at Welwyn North depot</li>
                    <li>Target: <strong>Net zero operations by 2030</strong></li>
                </ul>
            </div>
        </div>

        <!-- Digital Intelligence -->
        <div class="section">
            <h2>🧠 Digital Intelligence Focus Areas</h2>
            
            <div class="tip-box">
                <div class="box-title">🎯 Perfect for Your Head of Digital Intelligence Interviewer!</div>
                Digital Intelligence at Siemens encompasses data architecture, AI implementation, process automation, and digital twin technology.
            </div>

            <h3>1️⃣ Data Architecture & Governance</h3>
            <ul>
                <li><strong>Data Access Initiative:</strong> Centralized data marketplace empowering teams from shop floor to senior management</li>
                <li><strong>Data & AI Cloud:</strong> Powering strategic AI use cases across the company</li>
                <li><strong>Digital Threads:</strong> Connecting design, production, quality, and support in real-time</li>
                <li><strong>Data Ownership:</strong> Clearly defined ownership for high-quality, trusted data</li>
            </ul>

            <h3>2️⃣ AI/ML Implementation at Scale</h3>
            <div class="quote">
                <strong>Bob Jones (CRO):</strong> "It's not just about adopting AI—it's about being the fastest to adopt it."
            </div>
            <ul>
                <li><strong>GenAI Copilots:</strong> Natural language queries (Teamcenter Copilot, AI Chat)</li>
                <li><strong>Predictive Analytics:</strong> RapidMiner for quality issue detection</li>
                <li><strong>Automated Decision-Making:</strong> AI agents reducing manual effort</li>
                <li><strong>Industrial Foundation Models:</strong> Optimizing engineering and automation</li>
            </ul>

            <h3>3️⃣ Process Automation</h3>
            <ul>
                <li><strong>Bionic Agent:</strong> Cloud-based Gen AI for data analysis and productivity</li>
                <li><strong>Breaking Down Silos:</strong> Connecting disparate systems and data sources</li>
                <li><strong>IT/OT Integration:</strong> Merging Information Technology and Operational Technology</li>
                <li><strong>Low-code Tools:</strong> Mendix embedded across Teamcenter and Opcenter</li>
            </ul>

            <h3>4️⃣ Digital Twin Technology</h3>
            <ul>
                <li><strong>Comprehensive Digital Replicas:</strong> From design through production to operation</li>
                <li><strong>Real-time Monitoring:</strong> Live data synchronization with physical assets</li>
                <li><strong>Predictive Maintenance:</strong> AI-powered failure prediction</li>
                <li><strong>Simulation & Optimization:</strong> Testing scenarios before implementation</li>
            </ul>
        </div>

        <!-- Your Value Proposition -->
        <div class="section">
            <h2>💎 Your Unique Value Proposition</h2>

            <div class="success-box">
                <div class="box-title">🎯 Connect Your Experience to Siemens' Needs</div>
                Every point below should reference specific Siemens initiatives to show alignment.
            </div>

            <h3>1. Real-time Dashboard Experience (Q-Solutions)</h3>
            <div class="highlight-box">
                <strong>Your Achievement:</strong> Built operational dashboards that reduced reporting time by 40%<br><br>
                <strong>Siemens Connection:</strong> "At Q-Solutions, I developed real-time dashboards that transformed how the business made data-driven decisions. I see Siemens doing something similar but at industrial scale with your Data Access initiative—creating that single source of truth that empowers everyone from the shop floor to senior management."
            </div>

            <h3>2. Cross-functional Team Leadership (Lloyds, NHS)</h3>
            <div class="highlight-box">
                <strong>Your Achievement:</strong> Led teams across different business functions and stakeholder groups<br><br>
                <strong>Siemens Connection:</strong> "Leading cross-functional teams at Lloyds taught me how to bridge technical and business stakeholders—something I see as critical in Siemens' approach to Digital Intelligence, especially with initiatives like Bionic Agent that require collaboration between IT, business units, and end users."
            </div>

            <h3>3. Full-Stack Development (TrouDigital)</h3>
            <div class="highlight-box">
                <strong>Your Achievement:</strong> Building a B2B digital signage platform with content creation capabilities<br><br>
                <strong>Siemens Connection:</strong> "At TrouDigital, I'm building a B2B white-label platform with multiple access tiers and Canva-quality tools. This experience with user engagement and making complex technology accessible aligns perfectly with the User Engagement team's mission of driving IT adoption across the organization."
            </div>

            <h3>4. Hackathon Innovation & AI/ML</h3>
            <div class="highlight-box">
                <strong>Your Achievements:</strong>
                <ul>
                    <li><strong>Gesture:</strong> BSL translation system (1st place AccelerateMe)</li>
                    <li><strong>REST Quest:</strong> Emotion-aware travel assistant (3rd place Booking.com)</li>
                    <li>Multiple hackathon wins demonstrating rapid prototyping</li>
                </ul>
                <strong>Siemens Connection:</strong> "My work on emotion-aware AI systems and gesture recognition shows I understand how to apply AI to solve real-world problems—exactly what Siemens is doing with Industrial AI. The ability to rapidly prototype and iterate, which I've honed through hackathons, aligns with the speed-to-market approach you're taking with Xcelerator."
            </div>

            <h3>5. Academic Excellence & Research</h3>
            <div class="highlight-box">
                <strong>Your Achievement:</strong> First-class honors in IT Management for Business, extensive data analytics coursework<br><br>
                <strong>Siemens Connection:</strong> "My IT Management for Business degree gives me that crucial blend of technical skills and business acumen. Working on projects like Ford Motor Company business analysis and Istanbul Airbnb profitability modeling taught me to translate complex data into actionable business insights—exactly what Digital Intelligence does at scale."
            </div>
        </div>

        <!-- Role Expectations -->
        <div class="section">
            <h2>📋 Role-Specific Expectations</h2>

            <h3>🎯 Business IT Placement - What You'll Do</h3>
            <div class="project-card">
                <div class="project-title">50/50 Split Role</div>
                <div class="project-meta">
                    <span class="tag">IT Account Management</span>
                    <span class="tag">User Engagement</span>
                </div>
                <ul>
                    <li><strong>Encourage IT Service Utilization:</strong> Drive adoption of existing and planned IT services</li>
                    <li><strong>Requirements Gathering:</strong> Support IT Account/Demand Managers in collecting and analyzing customer requirements</li>
                    <li><strong>Translate to IT Demand:</strong> Convert business needs into technical requirements</li>
                    <li><strong>Strategic Project Coordination:</strong> Assist in delivery of strategic IT projects</li>
                    <li><strong>Innovation Deployment:</strong> Deploy innovative technology from global IT value centers into UK businesses</li>
                    <li><strong>ERP & Authorization:</strong> Work with ERP systems and authorization management tools</li>
                </ul>
            </div>

            <h3>✅ Key Skills They Value</h3>
            <table>
                <thead>
                    <tr>
                        <th>Skill</th>
                        <th>Why It Matters</th>
                        <th>You Have It? ✓</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>Logical Thinking</strong></td>
                        <td>Problem-solving in complex IT environments</td>
                        <td style="color: var(--github-green); font-weight: bold;">✅ Yes - Data analytics & coding projects</td>
                    </tr>
                    <tr>
                        <td><strong>Creative Problem-Solving</strong></td>
                        <td>Finding innovative solutions to business challenges</td>
                        <td style="color: var(--github-green); font-weight: bold;">✅ Yes - Hackathon wins & project work</td>
                    </tr>
                    <tr>
                        <td><strong>Self-Learning & Research</strong></td>
                        <td>Staying current with technology trends</td>
                        <td style="color: var(--github-green); font-weight: bold;">✅ Yes - Continuous tech exploration</td>
                    </tr>
                    <tr>
                        <td><strong>Passion for Digitalization</strong></td>
                        <td>Driving digital transformation initiatives</td>
                        <td style="color: var(--github-green); font-weight: bold;">✅ Yes - All your projects!</td>
                    </tr>
                    <tr>
                        <td><strong>Communication & Stakeholder Management</strong></td>
                        <td>Working with diverse teams and business units</td>
                        <td style="color: var(--github-green); font-weight: bold;">✅ Yes - Cross-functional leadership</td>
                    </tr>
                </tbody>
            </table>

            <h3>🎓 Intern Development Programme</h3>
            <ul>
                <li><strong>Individual Training Plan:</strong> Customized to your role and development needs</li>
                <li><strong>Soft Skills:</strong> Communication, teamwork, commercial awareness</li>
                <li><strong>Technical Skills:</strong> Digitalization, innovation, IT service delivery</li>
                <li><strong>Salary:</strong> £21,225 per annum (12-month placement)</li>
                <li><strong>Work Style:</strong> Flexible - office, hybrid, or remote options</li>
                <li><strong>Pathway:</strong> Strong potential for graduate role offers post-placement</li>
            </ul>
        </div>

        <!-- Questions to Ask -->
        <div class="section">
            <h2>❓ Excellent Questions to Ask</h2>

            <h3>🧠 For the Head of Digital Intelligence</h3>

            <div class="question">
                <div class="question-title">Question 1: Data Governance & Autonomy</div>
                <p>"I've read about Siemens' Data Access initiative and how it's creating a centralized data marketplace. How does the Digital Intelligence function balance the need for centralized data governance with the autonomy that individual business units need?"</p>
                <div class="question-why">✅ Shows deep research • Demonstrates understanding of organizational complexity</div>
            </div>

            <div class="question">
                <div class="question-title">Question 2: AI Strategy Evolution</div>
                <p>"Given Vasi Philomin's recent appointment as EVP of Data and AI, how is the Digital Intelligence team evolving its strategy to embed industrial AI across Siemens Xcelerator products?"</p>
                <div class="question-why">✅ Very current, shows you follow leadership changes • Positions you as interested in AI/ML strategy</div>
            </div>

            <div class="question">
                <div class="question-title">Question 3: Scaling GenAI</div>
                <p>"I noticed Siemens is implementing Bionic Agent for process automation. What's been the biggest challenge in scaling Gen AI solutions across different Siemens divisions, and how does Digital Intelligence help overcome those challenges?"</p>
                <div class="question-why">✅ Specific to a real initiative • Shows understanding of scaling challenges</div>
            </div>

            <div class="question">
                <div class="question-title">Question 4: Manchester Innovation Hub</div>
                <p>"With the Manchester Digital Experience Centre showcasing digital transformation technologies, how does Digital Intelligence work with business units to translate these innovations into practical implementations for UK customers?"</p>
                <div class="question-why">✅ Shows local awareness • Demonstrates interest in theory-to-practice</div>
            </div>

            <h3>💼 For the Other Interviewer</h3>

            <div class="question">
                <div class="question-title">Question 5: HS2 Project Opportunities</div>
                <p>"I saw that Siemens is investing £560 million in HS2's digital signalling systems. For someone in a Business IT role, what opportunities might there be to support major infrastructure projects like this?"</p>
                <div class="question-why">✅ Shows awareness of major UK projects • Demonstrates ambition</div>
            </div>

            <div class="question">
                <div class="question-title">Question 6: User Adoption Challenges</div>
                <p>"The placement description mentions working with the User Engagement team. What are the biggest challenges you face in driving IT adoption across such a technologically diverse organization?"</p>
                <div class="question-why">✅ Practical question about the role • Shows understanding of change management</div>
            </div>

            <div class="question">
                <div class="question-title">Question 7: Development Opportunities</div>
                <p>"How does the Intern Development Programme support placement students in developing both technical and soft skills? Are there opportunities to work on cross-divisional projects?"</p>
                <div class="question-why">✅ Shows long-term thinking • Demonstrates interest in breadth of experience</div>
            </div>

            <div class="question">
                <div class="question-title">Question 8: Digital Transformation Culture</div>
                <p>"I read about Siemens' 36% emissions reduction in 2024 through digitalization initiatives. How does the Business IT team contribute to Siemens' sustainability goals?"</p>
                <div class="question-why">✅ Connects IT to business impact • Shows awareness of corporate priorities</div>
            </div>
        </div>

        <!-- Impressive Talking Points -->
        <div class="section">
            <h2>🔥 Impressive Talking Points to Weave In</h2>

            <div class="tip-box">
                <div class="box-title">💡 Pro Tip</div>
                Don't just list these—weave them naturally into conversation when relevant. They show you've done serious research!
            </div>

            <h3>Recent Technology Partnerships</h3>
            <ul>
                <li>"I'm excited about Siemens' partnership with NVIDIA on the Teamcenter Digital Reality Viewer. In my projects, I've seen how real-time collaboration tools transform development cycles."</li>
                <li>"The JetZero partnership announced at CES 2025 is fascinating—using Xcelerator to build a fully digital aircraft with 50% better fuel efficiency shows the real-world impact of digital twins."</li>
            </ul>

            <h3>Digital Transformation Concepts</h3>
            <ul>
                <li>"The concept of 'digital threads' connecting engineering, manufacturing, and operations really resonates with my experience building end-to-end systems at TrouDigital."</li>
                <li>"I noticed Siemens is moving from managing 'Bills of Materials' to orchestrating 'Bills of Information.' This shift toward dynamic, role-based information delivery is fascinating and shows how data architecture is evolving."</li>
            </ul>

            <h3>UK-Specific Initiatives</h3>
            <ul>
                <li>"Your commitment to net zero by 2030 is impressive—the 36% emissions reduction in one year shows real action, not just targets."</li>
                <li>"Reading about the £100 million Chippenham facility opening in 2026 really demonstrates Siemens' long-term commitment to the UK market and rail technology innovation."</li>
                <li>"The HS2 contract for implementing ATO over ETCS is groundbreaking—it's the first time this has been done on a high-speed network in the UK."</li>
            </ul>

            <h3>AI & Innovation</h3>
            <ul>
                <li>"Hiring Vasi Philomin from AWS shows Siemens is serious about leading in industrial AI. His experience launching Amazon Bedrock will be transformative."</li>
                <li>"The Bionic Agent case study at SI Buildings UK is a perfect example of how GenAI can deliver immediate ROI—turning weeks of work into minutes."</li>
                <li>"Your approach to industrial AI feels different from consumer AI—it's grounded in domain expertise and real-world data, which makes it much more practical."</li>
            </ul>
        </div>

        <!-- Behavioral Questions -->
        <div class="section">
            <h2>🎭 Potential Behavioral Questions & Your Answers</h2>

            <details>
                <summary>📚 "Tell me about a time you had to learn a new technology quickly"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <p><strong>Situation:</strong> Economics coursework requiring professional R visualizations and statistical analysis</p>
                    <p><strong>Task:</strong> Needed to learn R programming and advanced visualization techniques in short timeframe</p>
                    <p><strong>Action:</strong> Systematically worked through documentation, online resources, and practice datasets</p>
                    <p><strong>Result:</strong> Delivered high-quality analysis with Harvard-style academic standards, maintained first-class performance</p>
                    <p><strong>Learning:</strong> Developed self-directed learning approach that I now use for all new technologies</p>
                </div>
                <p><strong>Alternative Example:</strong> Learning new frameworks for hackathons (e.g., BSL translation system "Gesture" - 1st place win)</p>
            </details>

            <details>
                <summary>🤝 "Describe a situation where you had to work with difficult stakeholders"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <p><strong>Situation:</strong> P&G Native brand digital transformation project analyzing 6,000+ customer cases</p>
                    <p><strong>Task:</strong> Needed buy-in from multiple departments with different priorities and technical understanding</p>
                    <p><strong>Action:</strong> Tailored communication to each stakeholder group, translated technical solutions into business value</p>
                    <p><strong>Result:</strong> Successfully developed SkinMatch AI and Internal Intelligence Hub with full stakeholder support</p>
                    <p><strong>Learning:</strong> Importance of speaking the stakeholder's language and focusing on outcomes they care about</p>
                </div>
            </details>

            <details>
                <summary>⚡ "Give an example of when you drove digital transformation"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <p><strong>Situation:</strong> Q-Solutions needed real-time operational visibility but relied on manual reporting</p>
                    <p><strong>Task:</strong> Build dashboard system to eliminate manual processes and enable data-driven decisions</p>
                    <p><strong>Action:</strong> Designed and implemented real-time operational dashboards with key metrics and KPIs</p>
                    <p><strong>Result:</strong> <strong>40% reduction in reporting time</strong>, transformed decision-making culture</p>
                    <p><strong>Siemens Connection:</strong> Similar to how Bionic Agent transforms manual processes at scale</p>
                </div>
                <p><strong>Alternative Example:</strong> TrouDigital B2B platform development - building white-label solution with enterprise features</p>
            </details>

            <details>
                <summary>🔄 "How do you stay current with technology trends?"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <ul>
                        <li><strong>Hands-on Learning:</strong> Regular hackathon participation keeps me working with cutting-edge tech</li>
                        <li><strong>Industry Research:</strong> Following company announcements (like Siemens at CES 2025, Hannover Messe)</li>
                        <li><strong>Deep Dives:</strong> Cryptocurrency research showing interest in emerging technologies and blockchain</li>
                        <li><strong>Academic Study:</strong> IT Management for Business degree keeps me grounded in both tech and business trends</li>
                        <li><strong>Real Projects:</strong> TrouDigital work exposes me to modern full-stack development practices</li>
                    </ul>
                </div>
            </details>

            <details>
                <summary>🏆 "Tell me about your biggest professional achievement"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <p><strong>Choose Based on Interviewer:</strong></p>
                    <ul>
                        <li><strong>Technical Achievement:</strong> Q-Solutions dashboard (40% time reduction) - quantifiable business impact</li>
                        <li><strong>Innovation Achievement:</strong> "Gesture" BSL translation system (1st place AccelerateMe) - solving accessibility challenges with AI</li>
                        <li><strong>Team Achievement:</strong> Leading cross-functional teams at Lloyds on accessible banking applications</li>
                    </ul>
                    <p><strong>Always Connect to Siemens:</strong> "This experience taught me [skill] which I see as directly applicable to [specific Siemens initiative]"</p>
                </div>
            </details>

            <details>
                <summary>❌ "Tell me about a time you failed"</summary>
                <div class="success-box">
                    <div class="box-title">Your Answer Framework:</div>
                    <p><strong>Rule:</strong> Choose a real failure with a strong learning outcome</p>
                    <p><strong>Structure:</strong></p>
                    <ul>
                        <li>What went wrong (be honest but professional)</li>
                        <li>Why it went wrong (take ownership)</li>
                        <li>What you learned (specific and actionable)</li>
                        <li>How you've applied that learning since (concrete example)</li>
                    </ul>
                    <p><strong>Example Topic:</strong> Early project where scope creep affected delivery, taught you about requirements management and stakeholder communication</p>
                </div>
            </details>
        </div>

        <!-- Final Tips -->
        <div class="section">
            <h2>⚡ Final Tips for Success</h2>

            <div class="success-box">
                <div class="box-title">✅ DO These Things</div>
                <ol>
                    <li><strong>Be Enthusiastic About Their Strategy:</strong> They're betting big on AI and digital transformation—show genuine excitement</li>
                    <li><strong>Connect to Business Value:</strong> Don't just talk tech; talk about impact (like your 40% time reduction)</li>
                    <li><strong>Ask About Manchester Specifically:</strong> You're studying there and the role is there—show local connection</li>
                    <li><strong>Mention Recent Events:</strong> Transform 2024, CES 2025, Hannover Messe 2025 show you follow their thought leadership</li>
                    <li><strong>Prepare 2-3 Specific Examples:</strong> From your experience that map to their challenges</li>
                    <li><strong>Show Cultural Fit:</strong> Siemens values innovation, diversity, collaboration—weave these in</li>
                    <li><strong>Be Yourself:</strong> Your experience is genuinely impressive—authentic confidence is key</li>
                </ol>
            </div>

            <div class="warning-box">
                <div class="box-title">⚠️ AVOID These Things</div>
                <ol>
                    <li><strong>Don't Memorize Scripts:</strong> Use these as talking points, not verbatim answers</li>
                    <li><strong>Don't Oversell:</strong> Be honest about what you know and what you want to learn</li>
                    <li><strong>Don't Ignore the Question:</strong> If you don't understand, ask for clarification</li>
                    <li><strong>Don't Bad-Mouth Previous Employers:</strong> Stay positive about all experiences</li>
                    <li><strong>Don't Forget to Listen:</strong> This is a conversation, not a monologue</li>
                </ol>
            </div>

            <div class="tip-box">
                <div class="box-title">🎯 The Secret Weapon</div>
                <p><strong>Remember:</strong> You're not just looking for any placement—you want THIS placement at Siemens. Show them you understand their vision, their challenges, and how you can contribute. Your research (this guide!) puts you ahead of 90% of candidates.</p>
            </div>

            <h3>📝 Pre-Interview Checklist</h3>
            <table>
                <thead>
                    <tr>
                        <th>Item</th>
                        <th>Done ✓</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Read through this entire guide</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Prepare 3-4 specific examples from your experience</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Choose which questions to ask (3-4 total)</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Review interviewers' LinkedIn profiles</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Test your tech setup (camera, mic, internet)</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Prepare a clean, professional background</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Have a notepad ready for notes</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                    <tr>
                        <td>Get good sleep the night before</td>
                        <td style="text-align: center;">☐</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p><strong>Good luck, Alisa! 🚀</strong></p>
            <p>You have incredible experience that aligns perfectly with what Siemens is doing.</p>
            <p>Just be confident, authentic, and show how your background positions you to contribute to their digital transformation journey.</p>
            <p style="margin-top: 20px; color: var(--siemens-teal); font-weight: 700;">Interview Date: January 21, 2026 • Manchester, UK</p>
        </div>
    </div>
</body>
</html>
