<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fedora Linux - Documentación Completa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #073763;
            background: linear-gradient(135deg, #f5f9fc 0%, #e8f2f7 100%);
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(7, 55, 99, 0.1);
        }

        h2 {
            color: #073763;
            font-size: 2.2em;
            margin: 40px 0 20px;
            padding-bottom: 15px;
            border-bottom: 3px solid #0a5fa5;
            position: relative;
        }

        h2::before {
            content: '';
            position: absolute;
            bottom: -3px;
            left: 0;
            width: 80px;
            height: 3px;
            background: #51a6d8;
        }

        h3 {
            color: #0a5fa5;
            font-size: 1.6em;
            margin: 30px 0 15px;
            padding-left: 15px;
            border-left: 4px solid #51a6d8;
        }

        h4 {
            color: #073763;
            font-size: 1.3em;
            margin: 20px 0 10px;
            font-weight: 600;
        }

        p {
            margin: 15px 0;
            text-align: justify;
            font-size: 1.05em;
            line-height: 1.7;
        }

        ul {
            margin: 20px 0 20px 30px;
            list-style: none;
        }

        ul li {
            margin: 12px 0;
            padding-left: 25px;
            position: relative;
            line-height: 1.6;
        }

        ul li::before {
            content: '▸';
            color: #0a5fa5;
            font-weight: bold;
            position: absolute;
            left: 0;
            font-size: 1.2em;
        }

        table {
            width: 100%;
            margin: 30px 0;
            border-collapse: collapse;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(7, 55, 99, 0.1);
        }

        thead {
            background: linear-gradient(135deg, #073763 0%, #0a5fa5 100%);
            color: white;
        }

        th {
            padding: 15px 12px;
            text-align: left;
            font-weight: 600;
            font-size: 1em;
        }

        td {
            padding: 12px 12px;
            border-bottom: 1px solid #e8f2f7;
        }

        tbody tr {
            background: white;
            transition: all 0.3s ease;
        }

        tbody tr:hover {
            background: #f5f9fc;
        }

        tbody tr:nth-child(even) {
            background: #fafcfd;
        }

        tbody tr:nth-child(even):hover {
            background: #f0f7fb;
        }

        .image-container {
            text-align: center;
            margin: 40px 0;
            padding: 20px;
            background: #f5f9fc;
            border-radius: 15px;
        }

        .image-container img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 8px 25px rgba(7, 55, 99, 0.15);
            transition: transform 0.3s ease;
        }

        .image-container img:hover {
            transform: scale(1.02);
        }

        .image-caption {
            margin-top: 15px;
            font-weight: 600;
            color: #073763;
            font-size: 1.05em;
        }

        .image-source {
            margin-top: 8px;
            font-size: 0.9em;
            color: #0a5fa5;
            font-style: italic;
        }

        hr {
            border: none;
            height: 2px;
            background: linear-gradient(to right, transparent, #51a6d8, transparent);
            margin: 50px 0;
        }

        .video-container {
            text-align: center;
            margin: 40px 0;
            padding: 30px;
            background: #f5f9fc;
            border-radius: 15px;
        }

        iframe {
            border-radius: 10px;
            box-shadow: 0 8px 25px rgba(7, 55, 99, 0.15);
            max-width: 100%;
            height: auto;
        }

        .team-member {
            display: inline-block;
            margin: 20px 15px;
            text-align: center;
            padding: 20px;
            background: #f5f9fc;
            border-radius: 15px;
            transition: all 0.3s ease;
            vertical-align: top;
            width: 200px;
        }

        .team-member:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(7, 55, 99, 0.15);
        }

        .team-member img {
            border-radius: 50%;
            border: 4px solid #51a6d8;
            margin-bottom: 15px;
            transition: border-color 0.3s ease;
            width: 150px;
            height: 150px;
            object-fit: cover;
        }

        .team-member:hover img {
            border-color: #0a5fa5;
        }

        .team-member b {
            display: block;
            color: #073763;
            font-size: 1.2em;
            margin-top: 10px;
        }

        .info-box {
            background: linear-gradient(135deg, #e8f2f7 0%, #f5f9fc 100%);
            padding: 25px;
            border-radius: 12px;
            border-left: 5px solid #0a5fa5;
            margin: 25px 0;
            box-shadow: 0 4px 15px rgba(7, 55, 99, 0.08);
        }
        tr {
      color: #073763;
        }

        .info-box ul {
            margin: 10px 0 10px 20px;
        }

        .info-box ul li::before {
            content: '●';
            color: #0a5fa5;
        }

        a {
            color: #0a5fa5;
            text-decoration: none;
            transition: color 0.3s ease;
            border-bottom: 2px solid transparent;
        }

        a:hover {
            color: #073763;
            border-bottom: 2px solid #51a6d8;
        }

        strong, b {
            color: #073763;
            font-weight: 600;
        }

        .table-container {
            overflow-x: auto;
            margin: 30px 0;
            border-radius: 10px;
        }

        /* Media Queries para Responsividad */
        
        /* Pantallas grandes (computadoras) */
        @media (min-width: 1201px) {
            .container {
                max-width: 1200px;
                padding: 50px;
            }
            
            .team-member {
                width: 220px;
            }
        }
        
        /* Pantallas medianas (computadoras pequeñas, tablets grandes) */
        @media (min-width: 992px) and (max-width: 1200px) {
            .container {
                max-width: 960px;
                padding: 40px;
            }
            
            .team-member {
                width: 200px;
                margin: 15px 10px;
            }
            
            table {
                font-size: 0.95em;
            }
        }
        
        /* Tablets */
        @media (min-width: 768px) and (max-width: 991px) {
            .container {
                padding: 30px;
            }
            
            h2 {
                font-size: 1.9em;
            }
            
            h3 {
                font-size: 1.5em;
            }
            
            .team-member {
                width: 180px;
                margin: 15px 10px;
            }
            
            table {
                font-size: 0.9em;
            }
            
            th, td {
                padding: 10px 8px;
            }
        }
        
        /* Teléfonos grandes y tablets pequeñas */
        @media (min-width: 576px) and (max-width: 767px) {
            body {
                padding: 10px;
            }
            
            .container {
                padding: 25px 20px;
            }
            
            h2 {
                font-size: 1.7em;
            }
            
            h3 {
                font-size: 1.4em;
            }
            
            .team-member {
                display: block;
                width: 100%;
                max-width: 280px;
                margin: 15px auto;
            }
            
            iframe {
                height: 300px;
            }
            
            table {
                font-size: 0.85em;
            }
            
            th, td {
                padding: 8px 6px;
            }
        }
        
        /* Teléfonos pequeños */
        @media (max-width: 575px) {
            body {
                padding: 5px;
            }
            
            .container {
                padding: 20px 15px;
                border-radius: 15px;
            }
            
            h2 {
                font-size: 1.5em;
            }
            
            h3 {
                font-size: 1.3em;
            }
            
            h4 {
                font-size: 1.1em;
            }
            
            p {
                font-size: 1em;
                text-align: left;
            }
            
            .team-member {
                display: block;
                width: 100%;
                max-width: 260px;
                margin: 10px auto;
                padding: 15px;
            }
            
            .team-member img {
                width: 120px;
                height: 120px;
            }
            
            iframe {
                height: 250px;
            }
            
            .info-box {
                padding: 20px 15px;
            }
            
            ul {
                margin-left: 20px;
            }
            
            ul li {
                padding-left: 20px;
            }
            
            table {
                font-size: 0.8em;
            }
            
            th, td {
                padding: 6px 4px;
                white-space: nowrap;
            }
            
            .image-container, .video-container {
                padding: 15px;
                margin: 30px 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Introducción</h2>
        <p>Los sistemas operativos constituyen el componente fundamental que posibilita la interacción entre el hardware del computador y el usuario final. Fedora, como distribución líder de Linux, encarna los principios del software libre y código abierto, ofreciendo una plataforma robusta y confiable para desarrollo, investigación y uso cotidiano. Su naturaleza comunitaria, combinada con el respaldo corporativo de Red Hat, lo posiciona como una solución tecnológica tanto para entornos empresariales como personales.</p>

        <p>La evolución constante de Fedora refleja un compromiso inquebrantable con la innovación tecnológica, sirviendo como banco de pruebas para características avanzadas que posteriormente se incorporarán en Red Hat Enterprise Linux. Esta sinergia única entre comunidad y corporación garantiza un equilibrio perfecto entre estabilidad probada y vanguardia tecnológica.</p>

        <hr>

        <h2>Reseña histórica</h2>
        <p>Fedora emerge en el panorama del software libre en 2003 como el sucesor natural de Red Hat Linux, marcando el inicio de un proyecto comunitario con visión de futuro. Desde sus inicios como Fedora Core 1, esta distribución ha mantenido un ciclo de desarrollo constante, liberando nuevas versiones cada seis meses que incorporan las últimas innovaciones del ecosistema Linux.</p>

        <p>A lo largo de su evolución, Fedora ha sido pionera en la adopción de tecnologías fundamentales. En 2015 introdujo el gestor de paquetes DNF, modernizando significativamente la gestión de software. Para 2020, Fedora 33 estableció Btrfs como sistema de archivos predeterminado, mejorando la confiabilidad y eficiencia del almacenamiento. Estos hitos tecnológicos demuestran el compromiso de Fedora con el progreso continuo y la excelencia técnica.</p>

        <div class="image-container">
            <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi_jL2u85uOIO5YTq7xD1b-smaqo5fWSaG6znBcwTHQbdbMsvYBaGhxiFD4cpLB-Q0l1VThyTG7_ITTgE-wbEZ-FfiHnXg3CIRZzvNy1I8VBHPvatwsmN9pNwUpNRr3_gD6ZiOew1czo3nsL-SmTEwqbaVqeHmQAmHI7DqrVFhlVFGSHfFAsAOPNfwJ-lM/s1920/fedora-feat-5b9fe676c9e77c0050ce388c.jpg" alt="Fedora Linux">
            <div class="image-caption">Figura #1 - Fedora</div>
            <div class="image-source">Fuente: https://www.lifewire.com/thmb/ftZ1L1jJdEj3e2zzHObw3988buU=/1920x1080/filters:fill(auto,1)/fedora-feat-5b9fe676c9e77c0050ce388c.jpg</div>
        </div>

        <h2>Características</h2>
        <h3>Arquitectura técnica</h3>
        <p>Fedora se construye sobre una base técnica sólida que integra el kernel Linux más reciente con systemd como sistema de inicialización, proporcionando un entorno estable y eficiente. La inclusión de SELinux (Security-Enhanced Linux) habilitado por defecto establece un estándar de seguridad empresarial desde el primer momento. El entorno de escritorio GNOME Shell, combinado con el protocolo de display Wayland, ofrece una experiencia de usuario moderna y fluida.</p>

        <p>La gestión de paquetes mediante DNF representa uno de los pilares fundamentales del sistema, permitiendo instalación, actualización y mantenimiento eficiente del software. Esta herramienta, compatible con paquetes RPM, asegura dependencias resueltas automáticamente y transacciones atómicas que preservan la integridad del sistema incluso en caso de interrupciones.</p>

        <h3>Requerimientos del sistema</h3>
        
        <h4>Requerimientos mínimos</h4>
        <div class="info-box">
            <ul>
                <li><strong>Procesador:</strong> 1 GHz dual-core 64-bit</li>
                <li><strong>Memoria RAM:</strong> 2 GB</li>
                <li><strong>Almacenamiento:</strong> 15 GB espacio libre</li>
                <li><strong>Tarjeta gráfica:</strong> Resolución 1024x768</li>
                <li><strong>Medio de instalación:</strong> USB o DVD booteable</li>
            </ul>
        </div>

        <h4>Requerimientos recomendados</h4>
        <div class="info-box">
            <ul>
                <li><strong>Procesador:</strong> 2 GHz quad-core 64-bit</li>
                <li><strong>Memoria RAM:</strong> 8 GB o más</li>
                <li><strong>Almacenamiento:</strong> 40 GB SSD</li>
                <li><strong>Tarjeta gráfica:</strong> Aceleración 3D, 1920x1080</li>
                <li><strong>Conexión:</strong> Internet para actualizaciones</li>
            </ul>
        </div>

        <h4>Para desarrollo profesional</h4>
        <div class="info-box">
            <ul>
                <li><strong>Memoria RAM:</strong> 16 GB</li>
                <li><strong>Almacenamiento:</strong> 100 GB SSD</li>
                <li><strong>Conectividad:</strong> Internet de alta velocidad</li>
                <li><strong>Gráficos:</strong> Tarjeta dedicada para desarrollo gráfico</li>
            </ul>
        </div>

        <hr>

        <h2>Análisis comparativo</h2>
        <p>Esta comparación incluye diferentes categorías de sistemas operativos para proporcionar una perspectiva completa. Fedora y Ubuntu son distribuciones Linux, mientras que Windows y macOS representan sistemas operativos propietarios. Esta comparación multidimensional permite entender las ventajas y desventajas de cada enfoque en el ecosistema actual de computación.</p>

        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>Característica</th>
                        <th>Fedora</th>
                        <th>Ubuntu</th>
                        <th>Windows 11</th>
                        <th>macOS Sonoma</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>Tipo</strong></td>
                        <td>Distribución Linux</td>
                        <td>Distribución Linux</td>
                        <td>Sistema Operativo</td>
                        <td>Sistema Operativo</td>
                    </tr>
                    <tr>
                        <td><strong>Licencia</strong></td>
                        <td>Open Source</td>
                        <td>Open Source</td>
                        <td>Propietario</td>
                        <td>Propietario</td>
                    </tr>
                    <tr>
                        <td><strong>Costo</strong></td>
                        <td>Gratuito</td>
                        <td>Gratuito</td>
                        <td>Pago</td>
                        <td>Incluido con hardware</td>
                    </tr>
                    <tr>
                        <td><strong>Ciclo de lanzamiento</strong></td>
                        <td>6 meses</td>
                        <td>6 meses LTS/2 años</td>
                        <td>Variable</td>
                        <td>Anual</td>
                    </tr>
                    <tr>
                        <td><strong>Gestor de paquetes</strong></td>
                        <td>DNF/RPM</td>
                        <td>APT/DEB</td>
                        <td>MSI/Winget</td>
                        <td>Homebrew</td>
                    </tr>
                    <tr>
                        <td><strong>Entorno escritorio</strong></td>
                        <td>GNOME</td>
                        <td>GNOME</td>
                        <td>Explorer</td>
                        <td>Aqua</td>
                    </tr>
                    <tr>
                        <td><strong>Seguridad base</strong></td>
                        <td>SELinux</td>
                        <td>AppArmor</td>
                        <td>Windows Defender</td>
                        <td>SIP</td>
                    </tr>
                    <tr>
                        <td><strong>Curva de aprendizaje</strong></td>
                        <td>Media</td>
                        <td>Baja</td>
                        <td>Baja</td>
                        <td>Media</td>
                    </tr>
                    <tr>
                        <td><strong>Soporte hardware</strong></td>
                        <td>Amplio</td>
                        <td>Muy amplio</td>
                        <td>Universal</td>
                        <td>Exclusivo Apple</td>
                    </tr>
                    <tr>
                        <td><strong>Comunidad</strong></td>
                        <td>Técnica/Activa</td>
                        <td>Enorme</td>
                        <td>Corporativa</td>
                        <td>Limitada</td>
                    </tr>
                    <tr>
                        <td><strong>Innovación</strong></td>
                        <td>Alta</td>
                        <td>Media</td>
                        <td>Media</td>
                        <td>Alta</td>
                    </tr>
                    <tr>
                        <td><strong>Estabilidad</strong></td>
                        <td>Alta</td>
                        <td>Muy alta</td>
                        <td>Media</td>
                        <td>Muy alta</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <h3>Fortalezas y debilidades</h3>
        <p>Las principales fortalezas de Fedora radican en su acceso a tecnologías de vanguardia, seguridad empresarial integrada y comunidad técnica activa. Como plataforma de desarrollo, ofrece herramientas modernas como Podman para contenedores y Toolbox para entornos aislados. Su relación simbiótica con Red Hat Enterprise Linux asegura que las innovaciones probadas en Fedora eventualmente lleguen a entornos productivos empresariales.</p>

        <p>Entre las limitaciones se encuentra una curva de aprendizaje moderada para usuarios noveles en Linux, soporte de hardware menos extenso que Ubuntu en algunos casos específicos, y la necesidad de mantenimiento más frecuente debido al ciclo de actualizaciones acelerado. Estas características posicionan a Fedora como ideal para usuarios técnicos pero menos adecuado para usuarios casuales sin experiencia previa en Linux.</p>

        <div class="image-container">
            <img src="https://www.somoslibres.org/images/2024/07/12/fedora41linux.webp" alt="Fedora Tux">
            <div class="image-caption">Figura #2 - Tux</div>
            <div class="image-source">Fuente: https://www.somoslibres.org/images/2024/07/12/fedora41linux.webp</div>
        </div>

        <h2>Casos de uso y aplicaciones prácticas</h2>
        <h3>Escenarios de Implementación</h3>
        <p>Fedora demuestra versatilidad excepcional en múltiples dominios tecnológicos. En desarrollo de software, proporciona un stack tecnológico completo con soporte nativo para lenguajes modernos como Python, Go, Rust y Node.js, junto con herramientas de desarrollo enterprise-grade. La integración de Flatpak y Toolbox facilita el manejo de dependencias y entornos aislados, crucial para proyectos complejos.</p>

        <p>En el ámbito científico y académico, Fedora es la plataforma preferida para computación de alto rendimiento, análisis de datos e investigación. Instituciones como la NASA y el CERN emplean Fedora en simulaciones y análisis complejos, aprovechando su estabilidad, rendimiento y herramientas especializadas. La disponibilidad de paquetes científicos actualizados y soporte para hardware especializado lo hace ideal para estos entornos.</p>

        <p>Para infraestructura cloud y servidores, Fedora Server ofrece una base sólida con soporte integrado para Kubernetes, Podman y tecnologías containerizadas. Su naturaleza innovadora lo convierte en la plataforma perfecta para evaluar y desarrollar soluciones cloud-native antes de su implementación en entornos productivos empresariales.</p>

        <hr>

        <h2>Proceso de Instalación y Configuración</h2>
        
        <div class="image-container">
            <img src="https://blogger.googleusercontent.com/img/a/AVvXsEgK1zTuCC4yR9Y1pD1aWwLN_ndflYxRs4o43hhCvgLu04Bqt7-4ZfFHztbdn1Y0x2240vw38YrlqEiyg8LJR-lItF7-5hq6BwzH4UPxEPFIfV84rFUJc2GrZvJZUxiDxPuIUXo42a24X-rFKjtpvgFIQX6a8n7LUABNEn0YEohk7lkyoLGmKj_z2BUk86w" alt="Instalación de Fedora">
            <div class="image-caption">Figura #3 - Instalación de Fedora</div>
            <div class="image-source">Fuente: https://www.dedoimedo.com/computers/fedora-42-gnome.html</div>
        </div>

        <h3>Implementación del sistema</h3>
        <p>La instalación de Fedora se caracteriza por su equilibrio entre simplicidad y control granular. El proceso inicia con la descarga de la imagen ISO desde el sitio oficial, seguido por la verificación de integridad mediante checksums criptográficos. La creación de medio booteable conduce al asistente de instalación Anaconda, que guía al usuario through configuración de idioma, particionamiento de disco y selección de software.</p>

        <p>Post-instalación, Fedora requiere configuraciones adicionales para optimizar su funcionalidad. La habilitación de repositorios RPM Fusion expande significativamente el catálogo de software disponible, mientras que la instalación de codecs multimedia asegura compatibilidad con formatos de audio y video prevalentes. Para desarrolladores, la instalación de grupos de paquetes "Development Tools" y "Development Libraries" establece un entorno de programación completo listo para producción.</p>

        <hr>

        <h2>Video ilustrativo</h2>
        <div class="video-container">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/u3jBw9ZOyTI" frameborder="0" allowfullscreen></iframe>
            <p style="margin-top: 20px;"><strong>Video #1. Fedora Linux // Review y opinión</strong><br>
            Fuente: YouTube, Tutos PC (2021)<br>
            URL: https://www.youtube.com/watch?v=u3jBw9ZOyTI</p>
        </div>

        <h2>Recursos y referencias</h2>
        <h3>Documentación y comunidad</h3>
        <p>La documentación oficial de Fedora, disponible en múltiples idiomas, constituye el recurso principal para usuarios y administradores. Complementando la documentación formal, la Wiki comunitaria ofrece guías prácticas, soluciones a problemas comunes y mejores prácticas compiladas por usuarios experimentados. Los foros de soporte y listas de correo proporcionan asistencia en tiempo real para desafíos técnicos específicos.</p>

        <p>Para desarrolladores, el Fedora Developer Portal centraliza recursos técnicos, tutoriales y guías de empaquetamiento. La infraestructura de construcción Koji y el sistema de control de código fuente permiten a los contribuidores participar activamente en el desarrollo de la distribución, reforzando el modelo comunitario que sustenta el proyecto.</p>

        <hr>

        <h2>Conclusiones</h2>
        <p>Fedora se consolida como una distribución Linux de referencia que armoniza innovación disruptiva con estabilidad operacional. Su ciclo de desarrollo de seis meses garantiza acceso prioritario a las tecnologías más avanzadas, mientras que su relación simbiótica con Red Hat Enterprise Linux asegura calidad y confiabilidad empresarial. Esta dualidad única posiciona a Fedora como plataforma ideal para early adopters y entornos que requieren tecnologías cutting-edge.</p>

        <p>El enfoque en seguridad proactiva mediante SELinux, combinado con herramientas modernas de containerización como Podman, establece estándares industriales que otras distribuciones eventualmente adoptan. Para desarrolladores, Fedora ofrece un ecosistema completo con soporte nativo para lenguajes de programación contemporáneos, frameworks de desarrollo y plataformas de deployment, acelerando significativamente el ciclo de desarrollo de aplicaciones.</p>

        <p>La vitalidad de la comunidad Fedora, demostrada through contribuciones técnicas, mantenimiento de paquetes y soporte a usuarios, constituye el pilar fundamental del proyecto. Esta colaboración orgánica entre voluntarios globales y el soporte institucional de Red Hat crea un modelo sostenible que asegura la continuidad y relevancia futura de la distribución.</p>

        <hr>

        <h2>Integrantes del Grupo</h2>
        <div style="text-align: center;">
            <div class="team-member">
                <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgxKQRtu9NgqEbAuIGEHzoVICB_Q1N35RuDvgBp4eaZy7Sq9R-Edg-uy9i8sWGKQV4GFF2J38eG7cjcneoCh3BbukGOODp11tXw4_G66jQH8210JRo2lHDmLlqR3cO5wyUzvEyPC94yRDfaGWSvajbaERMbbaJJdt9UVExAUpDINn4clxFjq_9G821UORY/s320/Imagen%20de%20WhatsApp%202025-10-06%20a%20las%2021.59.13_092076fa.jpg" alt="Abdiel Abrego">
                <b>Abdiel Abrego</b>
            </div>
            <div class="team-member">
                <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgSVk2cEnpeVt48BG-EUIMHSq2ge0cfKTiYcGlguxISQJPdw4_xcxPGGFYP8-94zwhVK1wQ5e3nQkt_e6lTU3drb-AitgsjA2REj9E7qIf-jrNR2AydjyVfmKM_3jPUWFdW3uiddl_ELnFeTHsQkMaA36LSJIECnsngG6efwUsuJXXi3abQe_t2qB3_x1s/w226-h282/Screenshot_20250927_215011_BeReal.jpg" alt="Nathaly Bonilla">
                <b>Nathaly Bonilla</b>
            </div>
            <div class="team-member">
                <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjgHrmX3YpcjBMrcD-mXyR-AGc5GefTZaJgScD_Sc2G5lpbNK7zu8iYbJmPZRXd5Jo8lMjdwLha98us2YbveJZgdIOj_HTap1gecJLcgsrOhYNdhNkRVkz6TAe0CUkc1rIks0dbuqvbMotUEAVs1kmnBjlqinbbUTHRspzoFXYKu5ervqVNVUmGbhwngk0/s320/eimy.jpg" alt="Eimy Félix">
                <b>Eimy Félix</b>
            </div>
            <div class="team-member">
                <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhvpZV9byjhBMfPifqtg0J3VTZz3tXwZ6HXcIlTqFZVeZ7BfviSYwH4k7aJZ8cp8UV4lWnjRdrwgJN81JyuHvyi1sAu-TvhtOdaT3FPe5NkqcJwVTeWJBGxWfMgMHaE6OdbOqu66CjXp_olH0Pes2fRPR_Xmkx-xSQEfGgJePxojBJoSPFq08S6KvEUj_8/s320/amanda.jpg" alt="Amanda Green">
                <b>Amanda Green</b>
            </div>
        </div>

        <div class="info-box" style="margin-top: 40px;">
            <p><strong>Profesor:</strong> Isaac Esquivel<br>
            <strong>Institución:</strong> Universidad Tecnológica de Panamá<br>
            <strong>Facultad:</strong> Ingeniería de Sistemas Computacionales<br>
            <strong>Departamento:</strong> Arquitectura y Redes de Computadoras<br>
            <strong>Grupo:</strong> 1SF132 - 4</p>
        </div>

        <h2>Referencias Bibliográficas</h2>
        <ul>
            <li>Fedora Project. (2024). <em>Fedora Documentation</em>. Recuperado de <a href="https://docs.fedoraproject.org/">https://docs.fedoraproject.org</a></li>
            <li>Ubuntu Documentation Team. (2024). <em>Ubuntu 24.04 LTS Documentation</em>. Canonical Ltd.</li>
            <li>Microsoft Corporation. (2024). <em>Windows 11 Technical Specifications</em>. Recuperado de <a href="https://www.microsoft.com/windows/windows-11-specifications">https://www.microsoft.com/windows/windows-11-specifications</a></li>
            <li>Linux Foundation. (2025). <em>Linux Kernel Development Report</em>. Recuperado de <a href="https://www.linuxfoundation.org">https://www.linuxfoundation.org</a></li>
            <li>Timetoast. (n.d.). Línea de tiempo de Fedora. Recuperado de <a href="https://www.timetoast.com/timelines/linea-de-tiempo-de-fedora">https://www.timetoast.com/timelines/linea-de-tiempo-de-fedora</a></li>
            <li>Slant. (2025). Fedora vs macOS: Comparación detallada a partir de 2025. Recuperado de <a href="https://www.slant.co/versus/2688/11499/~fedora_vs_macos">https://www.slant.co/versus/2688/11499/~fedora_vs_macos</a></li>
            <li>WindowsForum. (2025). Por qué Fedora es el mejor reemplazo de Windows en 2025: 7 razones clave. Recuperado de <a href="https://windowsforum.com/threads/why-fedora-is-the-best-windows-replacement-in-2025-7-key-reasons.365573/">https://windowsforum.com/threads/why-fedora-is-the-best-windows-replacement-in-2025-7-key-reasons.365573/</a></li>
            <li>Dedoimedo. (2025). <em>Fedora Workstation 42 review – Strangely good and bad</em>. Recuperado de <a href="https://www.dedoimedo.com/computers/fedora-42-gnome.html">https://www.dedoimedo.com/computers/fedora-42-gnome.html</a></li>
        </ul>
    </div>
</body>
</html>
