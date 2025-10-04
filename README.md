# PROYEC
MODIFICACION CALENDARIO
________________________________________
📄 Declaración Estratégica y Arquitectura Técnica (Versión Extendida): Portal Universitario Digital 3.0
Resumen Ejecutivo
El Portal Universitario Digital representa el pilar fundamental de la estrategia de Transformación Digital de la institución. Más allá de ser un sitio web, se establecerá como un Ecosistema Unificado de Servicios (EUS), diseñado para centralizar la gestión académica, administrativa y financiera. Su objetivo es migrar del modelo de operación tradicional a un entorno ágil, centrado en la experiencia del usuario (UX) y dirigido por la inteligencia de datos. Este documento detalla la visión estratégica, la arquitectura técnica recomendada y el plan de escalabilidad para asegurar su éxito a largo plazo.
________________________________________
HOJA 1: El Mandato Estratégico, la Visión del Ecosistema y Análisis Inicial
I. Declaración de Rol y Responsabilidad
OMAR CAMPOS  Jefe de Grupo de lideres me toco llevar la coordinación de gerencia,jefe de diseño sistemas y otros departamentos  en esta fase inicial de código abierto (Open Source), mi responsabilidad ha sido liderar la concepción del prototipo (V0.9 - Beta) y definir la Visión Estratégica del proyecto a gran escala. Esta visión abarca la integración de los servicios académicos, la arquitectura técnica necesaria para una escalabilidad infinita y la elaboración de la hoja de ruta para la implementación de la versión 3.0 (Producción).
II. Visión Estratégica: De Plataforma a Ecosistema de Valor
El Portal Digital 3.0 tiene un triple mandato estratégico que aborda los desafíos críticos de la educación superior moderna:
A. Democratización y Acceso 24/7
El portal debe ser la herramienta principal para eliminar las barreras geográficas y temporales, garantizando que la información y los servicios críticos estén disponibles las 24 horas del día, los 7 días de la semana. Esto soporta directamente las modalidades de estudio híbridas (Blended Learning) y a distancia.
B. Empoderamiento del Usuario y Eficiencia
Se busca dotar a cada actor (estudiante, docente, administrador) de herramientas de autogestión altamente intuitivas. Esto reduce la carga operativa del personal administrativo, liberándolos para enfocarse en tareas de mayor valor estratégico y mejorando la tasa de resolución de consultas.
C. Transparencia Operacional y Trazabilidad
Al centralizar todos los procesos (matrícula, calificaciones, asistencias, logs de actividad), el sistema garantizará una trazabilidad completa y un alto nivel de transparencia. Esto es vital para la rendición de cuentas institucional y para cumplir con los estándares regulatorios.
III. Módulos del Ecosistema Unificado de Servicios (EUS)
Módulo de Servicio	Usuarios Principales	Funcionalidades Clave
Portal Académico (LMS)	Estudiantes, Docentes	Distribución de Tareas/Materiales, e-Learning, Seguimiento de Asistencia, Historial de Notas y Avance Curricular.
Portal de Gestión	Docentes, Administradores	Gestión de Cargas Horarias, Aulas y Asignaciones. Cierre y Validación de Actas de Calificaciones, Solicitudes de Licencia.
Portal de Servicios al Alumno	Estudiantes, Administración	Matrícula y Reinscripción Online, Solicitud de Documentos (Constancias, Créditos), Estado de Cuenta y Pagos.
Portal de Inteligencia (BI)	Alta Dirección, Administración	Dashboards de Deserción (Analítica Predictiva), Indicadores de Rendimiento Docente y Eficiencia Administrativa.
Exportar a Hojas de cálculo
________________________________________
HOJA 2: Análisis FODA y Arquitectura Técnica Recomendada
IV. Análisis FODA (Fortalezas, Oportunidades, Debilidades y Amenazas)
Este análisis se centra en la transición del prototipo a la versión final del sistema productivo.
Fortalezas (Aspectos Internos Positivos)
Fortalezas	Descripción
Modelo Modular Basado en Roles	El diseño inicial ya separa claramente las vistas de Estudiante, Docente y Admin, lo que facilita la implementación de la Arquitectura de Microservicios sin colapsar la lógica.
Usabilidad y UX Moderna	El prototipo utiliza diseño Glassmorphism y es completamente responsive, asegurando una alta satisfacción del usuario (NPS) desde la fase Beta.
Tecnologías Universales	El Front-end está construido en HTML/CSS/JavaScript vanilla, lo que reduce la dependencia de frameworks pesados en la fase inicial y facilita la transición a React/Vue.js.
Código Abierto (Open Source)	Al ser un proyecto Open Source en su origen, se fomenta la colaboración interna entre los equipos de desarrollo y la transparencia del código.
Exportar a Hojas de cálculo
Debilidades (Aspectos Internos a Mejorar)
Debilidades	Descripción
Dependencia de Datos Simulados	El prototipo actual no tiene persistencia de datos (usa variables JS), lo que lo hace inútil en un entorno productivo hasta la conexión a una BBDD real.
Seguridad Inexistente	La autenticación es simulada (sin contraseña) y no hay mecanismos de cifrado ni JWT, representando el riesgo más alto en la fase de escalabilidad.
Monolito de Front-end	Todo el código (Estructura, Estilos, Lógica) reside en un único archivo (portal.html), dificultando la mantenibilidad y la escalabilidad de la base de código.
Carencia de Testing	Ausencia de pruebas unitarias o de integración, lo que aumenta el riesgo de bugs críticos al añadir nuevas funcionalidades.
Exportar a Hojas de cálculo
Oportunidades (Aspectos Externos Favorables)
•	Migración a la Nube: Aprovechar la infraestructura de nube (AWS/Azure) para implementar un modelo de pago por uso y garantizar la escalabilidad elástica en picos de matrícula.
•	Inteligencia Artificial (IA): Integrar chatbots basados en LLMs (Large Language Models) para soporte al alumno y análisis predictivo de la deserción.
•	Adopción Institucional: Alta demanda de la comunidad para digitalizar procesos (trámites, pagos), garantizando una alta tasa de adopción post-lanzamiento.
Amenazas (Riesgos Externos a Mitigar)
•	Ataques Cibernéticos: El riesgo de ataques de phishing o inyección SQL aumenta con la exposición pública del portal, lo que requiere invertir en Seguridad Perimetral (WAF).
•	Resistencia al Cambio: Posible resistencia de docentes o personal administrativo a adoptar las nuevas herramientas de gestión.
•	Regulación de Datos: Necesidad de cumplir con normativas de protección de datos (ej. GDPR o leyes locales) al manejar información personal sensible.
V. Arquitectura de Sistemas: Microservicios y API Gateway
Para garantizar la escalabilidad, la robustez y la independencia de las funcionalidades, el sistema se construirá bajo una Arquitectura de Microservicios desacoplada de la interfaz de usuario.
A. El Stack Tecnológico Recomendado
Capa	Herramienta Clave	Razón Estratégica
Front-end (Presentación)	React.js / Vue.js	Permite crear una Single Page Application (SPA) ágil y rápida, y facilita la modularización del desarrollo en componentes reutilizables.
Back-end (Lógica)	Node.js con Express.js (TypeScript)	Ofrece un entorno de alto rendimiento no bloqueante, ideal para manejar grandes volúmenes de solicitudes asíncronas de la comunidad.
Base de Datos (Transaccional)	PostgreSQL	Preferido para datos críticos y estructurados (Calificaciones, Matrícula) debido a su fuerte integridad de datos y robustez ACID.
Base de Datos (NoSQL/Flexible)	MongoDB	Utilizado para datos semi-estructurados (Avisos, Logs, Material Didáctico), brindando flexibilidad en el desarrollo rápido de nuevos módulos.
Exportar a Hojas de cálculo
________________________________________
HOJA 3: Seguridad, DRP y Plan de Implementación
VI. Seguridad, Respaldo y Continuidad Operacional (DRP)
La protección de datos sensibles es una prioridad. El sistema se diseñará bajo el marco de Seguridad por Diseño (Security by Design).
1.	Autenticación y Autorización: Implementación de Bcrypt para el hashing seguro de contraseñas. Uso estricto del Control de Acceso Basado en Roles (RBAC), donde el AuthService verifica los permisos mediante JWT antes de que el Back-end procese cualquier solicitud.
2.	Infraestructura en la Nube: Despliegue en proveedores de nube líderes (AWS, Azure o Google Cloud) utilizando contenedores (Docker y Kubernetes) para garantizar la escalabilidad horizontal (capacidad de auto-crear instancias en picos de demanda).
3.	Recuperación ante Desastres (DRP): Implementación de respaldos automatizados e incrementales diarios de la base de datos (PostgreSQL), replicación de datos a una zona geográfica distinta y un plan de Recuperación ante Desastres (DRP) con un Tiempo Objetivo de Recuperación (RTO) máximo de 4 horas.
VII. Hoja de Ruta del Proyecto (Roadmap)
El desarrollo se ejecutará con una metodología Ágil (Scrum), con sprints de 2-4 semanas, asegurando la entrega continua de valor.
Fase	Enfoque Principal	Hitos Clave	Duración (Estimada)
Fase 1: Infraestructura y Núcleo	Migración de Arquitectura. Desarrollo del AuthService y el Front-end principal.	V1.0 (MVP) Lanzamiento: Login seguro (JWT) y Perfil Básico (Estudiante/Docente/Admin). Repositorio listo para testing.	4 Meses
Fase 2: Motor Académico	Desarrollo del AcademicService y la integración de datos históricos (Matrícula y Notas).	Módulos de Horarios y Calificaciones en Producción. Sincronización de Datos del Sistema Heredado.	5 Meses
Fase 3: Expansión de Servicios	Implementación del LMS para tareas/materiales y el NotificationService.	Gestión de Tareas (Subida/Calificación). Sistema de Avisos Multi-Canal (Email/App).	4 Meses
Fase 4: Optimización y BI	Desarrollo de Dashboards de BI y Pruebas de Carga/Seguridad.	Dashboards de Analítica Predictiva (ej. Alerta de Deserción). Pruebas de Pentesting y Lanzamiento Oficial de V3.0.	3 Meses
Exportar a Hojas de cálculo
VIII. Criterios de Éxito e Indicadores de Rendimiento (KPIs)
El éxito del proyecto se medirá no solo por el lanzamiento técnico, sino por el impacto real en la comunidad universitaria.
A. KPIs de Rendimiento Técnico
•	Disponibilidad (Uptime): 99.95% (Menos de 4 horas de inactividad anual).
•	Latencia de API: Tiempo promedio de respuesta de las consultas críticas (ej. consulta de notas) debe ser inferior a 200 milisegundos.
•	Escalabilidad de Carga: El sistema debe soportar un pico de 10,000 usuarios concurrentes sin degradación del servicio.
B. KPIs de Impacto Estratégico
•	Tasa de Adopción (Estudiantes): 98% de la población activa usando el portal al menos una vez por semana.
•	Tasa de Digitalización de Trámites: Migración del 85% de los trámites administrativos clave a la plataforma digital.
•	Reducción de Costos Operativos: Disminución del 20% en los costos de papelería y gestión manual de trámites durante el primer año.
El Portal Universitario Digital 3.0 será la herramienta que posicione a la institución a la vanguardia educativa, garantizando una gestión moderna, eficiente y preparada para los retos de la próxima década


