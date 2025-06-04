# Proyecto: Minimapa Estilo GTA con Cámara y Geolocalización

Este proyecto web permite mostrar una cámara en vivo con un minimapa circular superpuesto al estilo GTA: San Andreas, utilizando la API de geolocalización del navegador y Google Maps Static API.

---

## 🚀 Características

- Captura en vivo desde cualquier cámara disponible (puedes seleccionar entre varias).
- Minimapa circular con diseño estilo GTA.
- Ubicación en tiempo real usando `navigator.geolocation`.
- Mapa personalizado generado dinámicamente con Google Maps Static API.
- API Key segura: se solicita manualmente en un popup, no queda expuesta en el código.

---

## 🧾 Requisitos

- Navegador moderno con soporte para:
  - WebRTC (`getUserMedia`)
  - Geolocalización
- Conexión HTTPS (obligatoria para acceder a la cámara y ubicación)
- Una API Key de Google Maps habilitada y restringida

---

## 🔑 Cómo obtener una API Key de Google Maps

1. Ve a: https://console.cloud.google.com/
2. Crea un nuevo proyecto (o selecciona uno existente).
3. Habilita la API "Maps Static API":
   - Menú → APIs y servicios → Biblioteca → Buscar "Maps Static API" → Habilitar
4. Crea una clave:
   - Menú → APIs y servicios → Credenciales → Crear credencial → Clave de API
5. (Opcional y recomendado) Restringe la clave:
   - Tipo de restricción: **HTTP referrers**
   - Agrega tu dominio: `https://tusitio.netlify.app/*`
   - Restringe el uso solo a "Maps Static API"
6. Guarda la clave, se verá algo así: AIzaSyA***************-AbCdEfGh


---

## 🔧 Uso del proyecto

1. Clona este repositorio o descarga los archivos `index.html`, `style.css` y el marco `minimap-frame.png`.
2. Abre el archivo `index.html` en un navegador (preferiblemente desde un servidor HTTPS o localhost).
3. El sistema te pedirá que ingreses tu API Key de Google Maps.
4. Selecciona tu cámara en el desplegable.
5. Disfruta del radar al estilo GTA con ubicación real.

---

## 📁 Estructura de archivos

´´´
/index.html → Página principal
/style.css → Estilos (radar, posición, cámaras, info)
/minimap-frame.png → Imagen PNG circular con marco estilo GTA
´´´


---

## 🛡️ Seguridad de la API Key

- La clave se solicita al usuario y se guarda solo en **memoria temporal** (no queda en el código, localStorage ni cookies).
- Recomendado: usar **restricciones de dominio y de API** en la consola de Google Cloud.

---

## 🧠 Créditos e inspiración

- Diseño basado en el radar de **GTA: San Andreas**
- Imagen de referencia: cortesía de [MixMods.com.br]
- Proyecto web educativo y demostrativo, sin fines comerciales.

---

## 📜 Licencia

MIT License. Puedes modificar y usar este proyecto para fines educativos o personales.
