# ShadowAuth (AdGuardian Extension)

**ShadowAuth** es un proyecto académico y de demostración que explora cómo una extensión aparentemente legítima puede ser utilizada para capturar cookies de sesión en navegadores web modernos, evidenciando riesgos reales de seguridad para usuarios finales.

> ⚠️ **Aviso ético**: Este proyecto es un Proof of Concept (PoC). No envía datos reales a servidores externos ni ejecuta ataques efectivos. Está desarrollado únicamente con fines educativos y de concienciación en ciberseguridad.

---

## 🚀 Objetivos del proyecto

- **Desarrollar** una extensión realista que funcione como un adblocker efectivo ("AdGuardian").
- **Demostrar** técnicas de captura de cookies de sesión accesibles vía API del navegador.
- **Concienciar** sobre los riesgos de permisos excesivos en extensiones de navegador.
- **Aplicar** buenas prácticas de desarrollo y documentación profesional de proyectos.

---

## 🛠️ Tecnologías utilizadas

- **Manifest V3** (Extensiones Chrome modernas)
- **JavaScript ES6+**
- **APIs de Chrome** (`cookies`, `tabs`, `webRequest`, `storage`)
- **HTML5 / CSS3** para la interfaz de usuario
- **Diagramas y documentación** (`.md`, `.png`)

---

## 🧱 Estructura del repositorio

ShadowAuth/
├── README.md               # Documentación principal del proyecto
├── LICENSE                 # Licencia del proyecto (por ejemplo, MIT)
├── manifest.json           # Configuración de la extensión
├── src/                    
│   ├── background.js       # Lógica de la captura de cookies
│   ├── content.js          # Lógica de inyección (opcional)
│   ├── popup/              
│   │   ├── popup.html      # Interfaz de usuario del popup
│   │   ├── popup.css       # Estilos para el popup
│   │   └── popup.js        # Lógica del popup
│   ├── assets/             
│   │   ├── icon128.png     # Ícono de alta resolución
│   │   └── icon48.png      # Ícono de baja resolución
│   └── util/               
│       └── cookieManager.js # Utilidades para gestionar cookies
├── docs/                   
│   ├── defense_agaisnt.md  # Documento de defensa contra ataques
│   ├── attack_flowchart.md # Diagrama del flujo de ataque
│   ├── installation.md     # Manual de instalación para poder auditar o probar la extensión 
│   └── explanation.md      # Explicación detallada del proyecto



---

## 📐 Arquitectura general

- **`background.js`**: Servicio principal que intercepta y gestiona cookies de sesión.
- **`cookieManager.js`**: Librería modular que facilita la captura y gestión de cookies.
- **`popup/`**: Interfaz gráfica accesible para el usuario final, mostrando actividad y control básico.
- **`assets/`**: Iconografía y recursos gráficos.
- **`docs/`**: Documentación técnica y diagramas explicativos.

---

## 🎯 Principales funcionalidades

### Funciones legítimas
- Bloqueo básico de anuncios mediante filtrado de peticiones HTTP.
- Interfaz de usuario amigable con estadísticas de bloqueo.

### Funciones de demostración (PoC de ciberseguridad)
- Captura de cookies no marcadas como `HttpOnly`.
- Almacenamiento seguro y local de cookies capturadas.
- Simulación de posibles flujos de exfiltración (documentados, no ejecutados).

---

## 🔥 Riesgos de seguridad demostrados

- **Permisos de alto riesgo** (`cookies`, `webRequest`, `tabs`).
- **Acceso a información sensible** en segundo plano.
- **Falsa sensación de confianza** por parte del usuario final.

---

## 🔒 Consideraciones éticas

Este proyecto sigue un enfoque **ético y responsable**:

- No envía información a servidores externos.
- No vulnera plataformas reales.
- Se recomienda su uso únicamente en entornos controlados o de laboratorio.

---

## 📚 Recursos adicionales

- Diagrama de arquitectura interna (`docs/architecture_diagram.png`)
- Flujo detallado de ataque simulado (`docs/attack_flowchart.png`)
- Explicación técnica completa (`docs/explanation.md`)

---

## ✍️ Autor

**Nombre:** lomina.  
**Proyecto para:** Formación avanzada en Ciberseguridad / Desarrollo de extensiones  
**Licencia:** MIT License

---

> Para más información técnica detallada, consulta el documento [`explanation.md`](docs/explanation.md).

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.