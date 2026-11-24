# Mariela Rivero Montiel — Currículum Interactivo

Página web personal con asistente de IA integrado (Google Gemini). Un único archivo `index.html` sin dependencias de build.

## Estructura del proyecto

```
mariela-cv/
├── index.html          ← toda la web (HTML + CSS + JS)
└── videos/             ← coloca aquí tus vídeos
    ├── pitch.mp4
    ├── proyecto.mp4
    └── habilidades.mp4
```

## Añadir tus vídeos

Coloca los tres archivos MP4 en la carpeta `videos/` con exactamente esos nombres (minúsculas). Si aún no los tienes, la web muestra el reproductor vacío sin errores.

## Desplegar en GitHub Pages

1. Crea un repositorio en GitHub (p.ej. `mariela-cv` o `tu-usuario.github.io`).
2. Sube todos los archivos:
   ```bash
   git init
   git add .
   git commit -m "🚀 Initial commit"
   git remote add origin https://github.com/TU_USUARIO/mariela-cv.git
   git push -u origin main
   ```
3. En GitHub → Settings → Pages → Source: **Deploy from branch** → `main` → `/ (root)`.
4. En unos minutos tu web estará en `https://TU_USUARIO.github.io/mariela-cv/`.

> **Nota sobre los vídeos:** GitHub Pages tiene un límite de 100 MB por archivo. Si tus vídeos son más grandes, súbelos a Google Drive o YouTube (privado/no listado) y reemplaza las etiquetas `<video>` por `<iframe>`.

## Usar el chat con Gemini

1. Obtén una API Key gratuita en [https://aistudio.google.com/apikey](https://aistudio.google.com/apikey).
2. En la web, despliega el panel **"Configurar API Key de Gemini"** e introduce tu clave.
3. La clave se guarda en el `localStorage` de tu navegador y **nunca** pasa por ningún servidor tuyo.

## Cambiar el modelo de IA

En `index.html`, busca la línea:
```js
const MODEL = 'gemini-2.5-flash';
```
Cámbiala por `'gemini-1.5-flash'` u otro modelo soportado.
