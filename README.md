# Bingo-Go Landing Page

Landing page oficial para la extensión de Chrome **Bingo-Go**, creada por ByKaizenES para ser desplegada en GitHub Pages.

## 🌐 Estructura de la Página

1. **Hero** - Presentación del nombre y título de la extensión
2. **Descripción Extensa** - Explicación completa de qué hace Bingo-Go
3. **Descarga** - Enlace a Google Drive para descargar la extensión
4. **Redes Sociales** - Enlaces a las redes sociales del autor
5. **Donaciones** - Botón de PayPal para apoyar el proyecto
6. **Footer** - Información del autor (ByKaizenES)

## 📁 Archivos

```
landingpage/
├── index.html          # Página principal
├── styles.css          # Estilos CSS
├── script.js           # JavaScript para animaciones
└── README.md           # Esta documentación
```

## 🚀 Desplegar en GitHub Pages

1. Sube el repositorio a GitHub
2. Ve a **Settings > Pages**
3. En **Source**, selecciona la rama principal
4. En **Folder**, selecciona `/landingpage`
5. Guarda y tu sitio estará disponible en: `https://tuusuario.github.io/bingo/`

## ✏️ Personalización

### Actualizar enlace de Google Drive
En `index.html`, busca y reemplaza el `#` en el botón de descarga:
```html
<a href="TU_ENLACE_DE_GOOGLE_DRIVE_AQUI" class="btn btn-primary btn-large">
```

### Actualizar enlace de PayPal
En `index.html`, busca y actualiza el enlace de donación:
```html
<a href="https://www.paypal.com/donate/?hosted_button_id=TU_CODIGO_AQUI" ...>
```

### Actualizar redes sociales
Reemplaza los enlaces en las secciones de redes sociales con tus URLs reales:
- Twitter/X
- Instagram
- YouTube
- Facebook

## 🎨 Características

- Diseño limpio y profesional
- Responsive (móvil y escritorio)
- Animaciones suaves al scroll
- Tema oscuro consistente
- Botones de redes sociales con efectos hover

## 👤 Autor

**ByKaizenES**

---

Página creada para presentar la extensión Bingo-Go de forma simple y efectiva.


## 🚀 Desplegar en GitHub Pages

### Opción 1: Desde la raíz del repositorio

1. Ve a la configuración del repositorio en GitHub
2. Navega a **Settings > Pages**
3. En **Source**, selecciona la rama `main` (o `master`)
4. En **Folder**, selecciona `/landingpage`
5. Haz clic en **Save**
6. Tu sitio estará disponible en: `https://bykaizenes.github.io/bingo/`

### Opción 2: Usando GitHub Actions (recomendado)

1. Crea un archivo `.github/workflows/deploy.yml` en la raíz del repositorio:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./landingpage
```

2. Haz commit y push de los cambios
3. El sitio se desplegará automáticamente

### Opción 3: Rama gh-pages dedicada

1. Crea una nueva rama `gh-pages`:
```bash
git checkout --orphan gh-pages
```

2. Copia solo los archivos de landingpage:
```bash
git rm -rf .
cp -r landingpage/* .
rm -rf landingpage
```

3. Haz commit y push:
```bash
git add .
git commit -m "Deploy landing page"
git push origin gh-pages
```

4. Configura GitHub Pages para usar la rama `gh-pages`

## 🎨 Personalización

### Colores
Los colores están definidos como variables CSS en `styles.css`:
```css
:root {
    --primary-color: #3b82f6;
    --bg-dark: #0f172a;
    --text-primary: #f1f5f9;
    /* ... más variables */
}
```

### Enlaces
Actualiza los enlaces en `index.html` si tu repositorio tiene un nombre diferente:
- Reemplaza `https://github.com/ByKaizenES/bingo` con tu URL
- Actualiza los enlaces a Issues, documentación, etc.

### Contenido
Edita el contenido directamente en `index.html`:
- Características de la extensión
- Secciones de la landing page
- Información de contacto

## 📱 Secciones Incluidas

1. **Hero**: Presentación principal con CTA
2. **Características**: Grid de funcionalidades destacadas
3. **Cómo Funciona**: Proceso paso a paso
4. **Sistema de Premios**: Explicación del cálculo de premios
5. **Tecnologías**: Stack técnico utilizado
6. **Instalación**: Guía de instalación completa
7. **CTA Final**: Call to action con enlaces
8. **Footer**: Información adicional y enlaces

## 🛠️ Desarrollo Local

Para probar la landing page localmente:

```bash
# Usando Python
cd landingpage
python -m http.server 8000

# O usando Node.js con http-server
npx http-server landingpage -p 8000
```

Luego abre: `http://localhost:8000`

## ✨ Características Técnicas

- **CSS Variables**: Para fácil personalización de colores
- **Flexbox y Grid**: Layout moderno y responsive
- **Intersection Observer API**: Animaciones al hacer scroll
- **Smooth Scroll**: Navegación fluida entre secciones
- **CSS Animations**: Efectos visuales atractivos
- **Mobile First**: Diseño optimizado para móviles

## 📄 Licencia

Esta landing page es parte del proyecto Bingo-Go creado por ByKaizenES.

## 👤 Autor

**ByKaizenES**
- GitHub: [@ByKaizenES](https://github.com/ByKaizenES)

---

¿Preguntas o sugerencias? Abre un [issue](https://github.com/ByKaizenES/bingo/issues) en GitHub.
