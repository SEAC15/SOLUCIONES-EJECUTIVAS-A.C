<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículum Vitae - Adrián Carbajal</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Montserrat para un estilo corporativo y elegante -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    <!-- Font Awesome para iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #f8f8f8; /* Light gray background */
            color: #333; /* Dark gray text */
            line-height: 1.5; /* Slightly tighter line height for compactness */
            padding: 1.5rem 1rem; /* Reduced padding for more space */
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
        }
        .resume-container {
            max-width: 850px; /* Slightly narrower to encourage single page */
            width: 100%;
            background-color: #ffffff; /* White content background */
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.07); /* Softer shadow */
            border-radius: 1.25rem; /* Slightly less rounded for compactness */
            overflow: hidden;
        }

        /* Header Section */
        .header-section {
            background-color: #0c1a2d; /* Dark navy blue from logo */
            color: #fff;
            padding: 2rem 1.5rem; /* Reduced padding */
            text-align: center;
            border-bottom-left-radius: 1.25rem;
            border-bottom-right-radius: 1.25rem;
        }
        .header-section h1 {
            font-size: 2.5rem; /* Slightly smaller font */
            font-weight: 800;
            margin-bottom: 0.4rem; /* Reduced margin */
            color: #E2B870; /* Gold accent from logo */
            letter-spacing: -0.04em; /* Tighter letter spacing */
        }
        .header-section h2 {
            font-size: 1.3rem; /* Slightly smaller */
            font-weight: 600;
            opacity: 0.9;
            margin-bottom: 1.2rem; /* Reduced margin */
        }
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.2rem; /* Reduced gap */
            font-size: 0.95rem; /* Slightly smaller font */
            margin-top: 1.2rem;
            border-top: 1px solid rgba(255,255,255,0.15); /* Thinner, lighter border */
            padding-top: 1.2rem;
        }
        .contact-info div {
            display: flex;
            align-items: center;
            gap: 0.4rem; /* Reduced gap */
        }
        .contact-info i {
            color: #E2B870; /* Gold accent for icons */
            font-size: 1rem; /* Slightly smaller */
        }
        .contact-info a {
            color: #fff;
            text-decoration: none;
            transition: color 0.2s ease;
        }
        .contact-info a:hover {
            color: #d4d4d4;
        }

        /* Main Content Sections */
        .content-section {
            padding: 2rem 1.5rem; /* Reduced padding */
            border-bottom: 1px solid #eee;
        }
        .content-section:last-of-type {
            border-bottom: none;
        }
        .content-section h3 {
            font-size: 1.7rem; /* Smaller section titles */
            font-weight: 700;
            color: #0c1a2d; /* Dark navy blue */
            margin-bottom: 1rem; /* Reduced margin */
            text-align: center;
            border-bottom: 2px solid #e2b870; /* Gold accent */
            padding-bottom: 0.4rem; /* Reduced padding */
        }
        .content-section p {
            font-size: 1rem; /* Slightly smaller paragraph text */
            color: #555;
            margin-bottom: 0.8rem; /* Reduced margin */
            text-align: justify;
        }
        
        /* Skills/Experience List */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); /* Adjusted minmax for more compactness */
            gap: 1.2rem; /* Reduced gap */
            margin-top: 1.2rem;
        }
        .skill-category {
            background-color: #fcfcfc; /* Lighter background for skill category */
            border-left: 3px solid #2C847A; /* Thinner teal line accent */
            border-radius: 0.5rem;
            padding: 0.8rem 1rem; /* Reduced padding */
            box-shadow: 0 1px 5px rgba(0,0,0,0.03); /* Lighter shadow */
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .skill-category h4 {
            font-size: 1.1rem; /* Slightly smaller category titles */
            font-weight: 700;
            color: #2C847A;
            margin-bottom: 0.6rem; /* Reduced margin */
        }
        .skill-category ul {
            list-style: none;
            padding: 0;
            flex-grow: 1;
            margin-bottom: 0;
        }
        .skill-category ul li {
            font-size: 0.85rem; /* Smaller list items */
            color: #444;
            margin-bottom: 0.3rem; /* Reduced margin */
            display: flex;
            align-items: flex-start;
            gap: 0.4rem; /* Reduced gap */
        }
        .skill-category ul li i {
            color: #E2B870;
            font-size: 0.8rem; /* Smaller icon */
            margin-top: 0.15rem;
            flex-shrink: 0;
        }
       
        /* Professional Experience */
        .experience-item {
            margin-bottom: 1.5rem; /* Reduced margin */
            padding-bottom: 1rem; /* Reduced padding */
            border-bottom: 1px dashed #e9e9e9; /* Lighter dashed border */
        }
        .experience-item:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        .experience-item h4 {
            font-size: 1.25rem; /* Smaller role title */
            font-weight: 700;
            color: #0c1a2d;
            margin-bottom: 0.15rem;
        }
        .experience-item p.role {
            font-size: 1rem; /* Smaller role text */
            font-weight: 600;
            color: #2C847A;
            margin-bottom: 0.4rem; /* Reduced margin */
        }
        .experience-item p.duration-location {
            font-size: 0.85rem; /* Smaller duration/location */
            color: #777;
            font-style: italic;
            margin-bottom: 0.8rem; /* Reduced margin */
        }
        .experience-item ul {
            list-style: disc;
            padding-left: 1.2rem; /* Reduced padding */
            color: #444;
        }
        .experience-item ul li {
            margin-bottom: 0.3rem; /* Reduced margin */
            font-size: 0.9rem; /* Smaller list items */
        }

        /* Call to Action Section */
        .call-to-action-section {
            background-color: #0c1a2d;
            color: #fff;
            padding: 2rem 1.5rem; /* Reduced padding */
            text-align: center;
            border-top-left-radius: 1.25rem;
            border-top-right-radius: 1.25rem;
            margin-top: 1.5rem; /* Reduced margin */
        }
        .call-to-action-section h4 {
            font-size: 1.8rem; /* Smaller title */
            font-weight: 700;
            color: #E2B870;
            margin-bottom: 0.8rem; /* Reduced margin */
            line-height: 1.2;
        }
        .call-to-action-section p {
            font-size: 1.05rem; /* Slightly smaller text */
            font-weight: 500;
            margin-bottom: 1.2rem; /* Reduced margin */
            opacity: 0.9;
        }
        .call-to-action-section .contact-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.2rem; /* Reduced gap */
            font-size: 1rem; /* Slightly smaller font */
        }
        .call-to-action-section .contact-links div {
            display: flex;
            align-items: center;
            gap: 0.6rem; /* Reduced gap */
        }
        .call-to-action-section .contact-links i {
            font-size: 1.3rem; /* Slightly smaller icon */
            color: #51B0A6;
        }
        .call-to-action-section .contact-links a {
            color: #fff;
            text-decoration: none;
            transition: color 0.2s ease;
            font-weight: 600;
        }
        .call-to-action-section .contact-links a:hover {
            color: #E2B870;
            text-decoration: underline;
        }

        /* Footer */
        .footer {
            background-color: #1a1a1a;
            color: #9ca3af;
            text-align: center;
            font-size: 0.75em; /* Smaller font */
            padding: 0.8rem; /* Reduced padding */
            border-bottom-left-radius: 1.25rem;
            border-bottom-right-radius: 1.25rem;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            body {
                padding: 1rem;
            }
            .resume-container {
                border-radius: 1rem;
            }
            .header-section {
                padding: 1.2rem;
                border-bottom-left-radius: 1rem;
                border-bottom-right-radius: 1rem;
            }
            .header-section h1 {
                font-size: 2rem;
            }
            .header-section h2 {
                font-size: 1rem;
            }
            .contact-info {
                flex-direction: column;
                gap: 0.6rem;
                font-size: 0.85rem;
                padding-top: 0.8rem;
                margin-top: 0.8rem;
            }
            .content-section {
                padding: 1.2rem;
            }
            .content-section h3 {
                font-size: 1.4rem;
                margin-bottom: 0.8rem;
            }
            .content-section p {
                font-size: 0.9rem;
            }
            .skills-grid {
                grid-template-columns: 1fr; /* Stack on small screens */
                gap: 0.8rem;
            }
            .skill-category {
                padding: 0.6rem 0.8rem;
            }
            .skill-category h4 {
                font-size: 1rem;
            }
            .skill-category ul li {
                font-size: 0.75rem;
            }
            .experience-item {
                margin-bottom: 1rem;
                padding-bottom: 0.8rem;
            }
            .experience-item h4 {
                font-size: 1.1rem;
            }
            .experience-item p.role {
                font-size: 0.9rem;
            }
            .experience-item p.duration-location {
                font-size: 0.75rem;
            }
            .experience-item ul {
                padding-left: 1rem;
            }
            .experience-item ul li {
                font-size: 0.8rem;
            }
            .call-to-action-section {
                padding: 1.2rem;
                border-top-left-radius: 1rem;
                border-top-right-radius: 1rem;
            }
            .call-to-action-section h4 {
                font-size: 1.4rem;
                margin-bottom: 0.6rem;
            }
            .call-to-action-section p {
                font-size: 0.95rem;
                margin-bottom: 1rem;
            }
            .call-to-action-section .contact-links {
                flex-direction: column;
                gap: 0.6rem;
                font-size: 0.9rem;
            }
            .call-to-action-section .contact-links i {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>

    <div class="resume-container">
        <!-- Header: Name, Title, Contact Info -->
        <header class="header-section">
            <h1>ADRIÁN CARBAJAL</h1>
            <h2>Especialista en Soluciones Ejecutivas y Consultoría</h2>
            <div class="contact-info">
                <div><i class="fas fa-envelope"></i> <a href="mailto:solucionesejecutivasac@gmail.com">solucionesejecutivasac@gmail.com</a></div>
                <div><i class="fab fa-whatsapp"></i> <a href="https://wa.me/526341085667">+52 6341085667</a></div>
                <div><i class="fas fa-map-marker-alt"></i> Remoto desde México</div>
            </div>
        </header>

        <!-- Professional Profile -->
        <section class="content-section">
            <h3>Perfil Profesional</h3>
            <p>
                Profesional proactivo y altamente organizado con una trayectoria en la provisión de soluciones ejecutivas y estratégicas. Mi experiencia abarca la optimización de productividad, gestión eficiente de proyectos y eventos, control financiero, desarrollo de menús personalizados y capacitación en ventas. Compromiso con la excelencia, discreción y entrega de resultados tangibles.
            </p>
        </section>

        <!-- Areas of Expertise / Key Skills -->
        <section class="content-section">
            <h3>Áreas de Especialización</h3>
            <div class="skills-grid">
                <!-- Asistente Virtual Personal o Ejecutivo -->
                <div class="skill-category">
                    <div>
                        <h4>Asistencia Ejecutiva Virtual</h4>
                        <ul>
                            <li><i class="fas fa-dot-circle"></i> Gestión administrativa y operativa</li>
                            <li><i class="fas fa-dot-circle"></i> Optimización de flujos de trabajo</li>
                            <li><i class="fas fa-dot-circle"></i> Gestión de comunicaciones</li>
                        </ul>
                    </div>
                </div>

                <!-- Organización de Eventos / Proyectos -->
                <div class="skill-category">
                    <div>
                        <h4>Organización y Gestión de Proyectos</h4>
                        <ul>
                            <li><i class="fas fa-dot-circle"></i> Planificación y conceptualización</li>
                            <li><i class="fas fa-dot-circle"></i> Gestión de logística y recursos</li>
                            <li><i class="fas fa-dot-circle"></i> Control presupuestario</li>
                        </ul>
                    </div>
                </div>

                <!-- Control Financiero Personal o de Negocios -->
                <div class="skill-category">
                    <div>
                        <h4>Optimización Financiera</h4>
                        <ul>
                            <li><i class="fas fa-dot-circle"></i> Diseño de plantillas de control</li>
                            <li><i class="fas fa-dot-circle"></i> Monitoreo y reportes financieros</li>
                            <li><i class="fas fa-dot-circle"></i> Asesoría en optimización de recursos</li>
                        </ul>
                    </div>
                </div>

                <!-- Menús Personalizados -->
                <div class="skill-category">
                    <div>
                        <h4>Diseño de Menús Estratégicos</h4>
                        <ul>
                            <li><i class="fas fa-dot-circle"></i> Creación de menús equilibrados</li>
                            <li><i class="fas fa-dot-circle"></i> Adaptación a requerimientos dietéticos</li>
                            <li><i class="fas fa-dot-circle"></i> Optimización de costos</li>
                        </ul>
                    </div>
                </div>

                <!-- Entrenamiento en Ventas 1 a 1 -->
                <div class="skill-category">
                    <div>
                        <h4>Coaching Estratégico en Ventas</h4>
                        <ul>
                            <li><i class="fas fa-dot-circle"></i> Capacitación individualizada</li>
                            <li><i class="fas fa-dot-circle"></i> Técnicas de prospección y cierre</li>
                            <li><i class="fas fa-dot-circle"></i> Optimización de mensajes comerciales</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <!-- Professional Experience -->
        <section class="content-section">
            <h3>Experiencia Profesional</h3>
            <div class="experience-item">
                <h4>Soluciones Ejecutivas A.C.</h4>
                <p class="role">Especialista en Soluciones Ejecutivas y Consultoría</p>
                <p class="duration-location">Remoto desde México</p>
                <ul>
                    <li>Provisión de soporte administrativo y operativo a ejecutivos y empresas, mejorando productividad y eficiencia.</li>
                    <li>Implementación de estrategias integrales para organización y gestión de proyectos/eventos exitosos.</li>
                    <li>Desarrollo de metodologías de control financiero y reportes para toma de decisiones.</li>
                    <li>Creación de menús personalizados, optimizando recursos y costos.</li>
                </ul>
            </div>
        </section>

        <!-- Call to Action Section -->
        <section class="call-to-action-section">
            <h4>¿Listo para Optimizar su Potencial?</h4>
            <p>Contácteme hoy mismo para una consulta estratégica y descubra cómo mis soluciones pueden impulsar su éxito.</p>
            <div class="contact-links">
                <div>
                    <i class="fas fa-envelope"></i>
                    <a href="mailto:solucionesejecutivasac@gmail.com" target="_blank">solucionesejecutivasac@gmail.com</a>
                </div>
                <div>
                    <i class="fab fa-whatsapp"></i>
                    <a href="https://wa.me/526341085667" target="_blank">+52 6341085667</a>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="footer">
            <p>&copy; 2025 Adrián Carbajal. Todos los derechos reservados.</p>
        </footer>
    </div>

</body>
</html>
