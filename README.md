# ontologia-ciberseguridda
La presente ontología de ciberseguridad tiene como propósito estructurar y representar de manera formal los conceptos fundamentales relacionados con la gestión de riesgos en entornos digitales. Fue desarrollada utilizando el editor de ontologías Protégé bajo el estándar OWL (Web Ontology Language).
El objetivo principal es facilitar el análisis, comprensión e interoperabilidad del conocimiento en el dominio de la ciberseguridad, permitiendo modelar amenazas, vulnerabilidades, activos y mecanismos de protección de forma lógica y reutilizable.
Objetivo
Representar los conceptos clave de ciberseguridad para apoyar el análisis de riesgos, permitiendo identificar relaciones entre elementos críticos como amenazas, activos afectados y controles de mitigación.
Estructura de la Ontología
Clases Principales
La ontología se organiza en cinco clases fundamentales:
Amenaza: Eventos o acciones que pueden comprometer la seguridad.
Vulnerabilidad: Debilidades explotables en un sistema.
Activo: Recursos valiosos que requieren protección.
Control: Medidas de seguridad implementadas.
Política: Normativas o reglas que regulan la seguridad.
Cada clase contiene subclases que permiten una clasificación más específica. Por ejemplo, dentro de Amenaza se incluyen Phishing, Malware y Ataque_DDoS.
Propiedades de Objeto
Se definieron relaciones semánticas entre las clases:
afecta (Amenaza → Activo): Indica qué activo es impactado por una amenaza.
mitiga (Control → Amenaza): Representa qué controles reducen o eliminan amenazas.
requiere (Política → Control): Define los controles necesarios para cumplir una política.
Ejemplo:
Phishing afecta Cuenta_Correo
Autenticación_Doble_Factor mitiga Phishing
Propiedades de Datos
Se incluyeron atributos para describir características específicas:
nivelRiesgo (Amenaza): Valor numérico del riesgo.
criticidad (Activo): Nivel de importancia del activo.
fechaDetección (Vulnerabilidad): Momento en que se detectó.
Ejemplo:
Servidor_Web → criticidad = 5
Phishing → nivelRiesgo = 4
Individuos (Instancias)
Se definieron instancias concretas para representar casos reales:
Phishing_Corporativo (tipo Phishing)
Servidor_Web (tipo Activo)
FirewallCisco (tipo Control)
Estas instancias permiten ejemplificar el uso práctico de la ontología.
Restricciones y Axiomas
Se incorporaron reglas lógicas para garantizar coherencia:
Todo activo crítico debe estar protegido por al menos un control.
Formalmente:
Activo ⊑ ∃ protegidoPor.Control
Estas restricciones permiten al razonador inferir relaciones adicionales y validar la consistencia del modelo.
Razonamiento y Validación
Se utilizó un razonador (como HermiT o Pellet) para verificar la consistencia de la ontología. A través de este proceso, se pueden descubrir relaciones implícitas, como la asignación automática de controles a activos críticos o la identificación de dependencias no explícitas.
Importancia de la Ontología
La ontología permite:
Estandarizar el conocimiento en ciberseguridad.
Facilitar el análisis de riesgos.
Mejorar la comunicación entre sistemas y expertos.
Apoyar la toma de decisiones basada en relaciones lógicas.
Conclusión
El desarrollo de esta ontología demuestra cómo la representación formal del conocimiento puede mejorar la comprensión de escenarios complejos en ciberseguridad. Como mejora futura, se podrían integrar más clases, ampliar las reglas lógicas y conectar la ontología con datos reales para aplicaciones prácticas como sistemas de detección de amenazas o análisis automatizado de riesgos.
