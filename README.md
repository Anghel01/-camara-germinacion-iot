# 🌱 Cámara de Germinación Inteligente para Semilleros (Grupo 1)
**Proyecto de Ingeniería IoT — Escuela Politécnica Nacional (EPN), FIEE**  
**Período:** 2026-B | **Docente:** PhD. Soraya Sinche  
**Integrantes:** Xavier Anatoa, Angelo Conterón, Fernando Guarderas  

---

## 📌 Descripción
Aplicación web *mobile-first*, reactiva y autónoma (PWA sin dependencias de servidor) diseñada para gestionar de punta a punta el desarrollo del proyecto de ingeniería IoT:
- **33 tareas técnicas** (`T1.01` a `T1.16` en Parte 1 y `T2.01` a `T2.17` en Parte 2) con pasos en checklist, dependencias, revisiones cruzadas y criterios de aceptación.
- **19 decisiones de diseño** (`D01` a `D19`), **16 riesgos técnicos** (`R01` a `R16`), **14 pruebas de validación** (`P1` a `P14`) y **6 preguntas docentes** (`Q1` a `Q6`).
- **Bitácora de laboratorio** con calculadoras en tiempo real:
  - Fórmula `map(adc, ADC_aire, ADC_agua, 0, 100)` para los sensores capacitivos.
  - Curva gráfica SVG de `% de germinación vs tiempo` para el lote piloto.
  - Checklist para la sesión semanal con la Raspberry Pi 4.
- **Lista de compras y verificación en tienda** (Secciones 6 y 18).
- **Cálculo automático de Ruta Crítica (CPM)** sobre el grafo del proyecto.

---

## 🚀 Inicio Rápido (En tu computadora)
Simplemente haz doble clic sobre el archivo [`index.html`](./index.html) para abrirlo en cualquier navegador web moderno (Edge, Chrome, Firefox). No requiere Node.js, Python ni instalación de paquetes.

---

## 📱 Publicación Gratuita en GitHub Pages (Para usar en el celular)
Para que tú (**Angelo Conterón**, `@Anghel01`) y tus compañeros de equipo (**Xavier Anatoa** y **Fernando Guarderas**) puedan acceder en tiempo real desde sus teléfonos en el laboratorio o en la tienda de componentes:

1. Abre PowerShell o tu terminal favorita dentro de esta carpeta (`camara-germinacion`) y sube el repositorio a tu cuenta de GitHub (`Anghel01`):
   ```powershell
   git init
   git add .
   git commit -m "feat: Aplicacion Plan Maestro v2.0 Camara Germinacion Grupo 1 - Angelo Conteron @Anghel01"
   git branch -M main
   git remote add origin https://github.com/Anghel01/-camara-germinacion-iot.git
   git push -u origin main
   ```

2. En tu repositorio de GitHub, ve a **Settings** ➔ **Pages**.
3. En **Source**, selecciona `Deploy from a branch`, en Branch elige `main` y directorio `/(root)`. Haz clic en **Save**.
4. En unos 60 segundos tu aplicación estará activa y disponible en:  
   👉 **`https://anghel01.github.io/-camara-germinacion-iot/`**
5. Abre esa URL en el navegador de tu celular (Chrome o Safari) y toca en **"Agregar a pantalla de inicio"** o **"Instalar aplicación"**. Se instalará como una App nativa con icono de germinación gracias a su Service Worker (`sw.js`) y `manifest.json`, permitiendo uso 100% offline.

---

## ☁️ Sincronización en Tiempo Real con Firebase (Opcional)
Si desean compartir cambios instantáneos entre los 3 dispositivos:
1. Crea una base de datos en [Firebase Console](https://console.firebase.google.com/) (*Realtime Database*).
2. Configura las reglas de seguridad:
   ```json
   {
     "rules": {
       "epn_iot_grupo1_camara": {
         ".read": "auth != null || request.auth != null",
         ".write": "auth != null || request.auth != null"
       }
     }
   }
   ```
3. En la pestaña **11. Configuración** de la aplicación, activa la casilla de Firebase, pega tu URL y presiona **Subir a Firebase**.

---

## 📦 Estructura de Archivos
```
camara-germinacion/
├── index.html       # Aplicación web completa y autocontenida (HTML + CSS + JS)
├── manifest.json    # Configuración de Progressive Web App (PWA)
├── sw.js            # Service Worker para funcionamiento 100% offline
└── README.md        # Documentación y guía de despliegue
```
