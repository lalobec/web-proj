# Portfolio Web - Proyectos en Desarrollo

Este repositorio contiene múltiples sitios web en desarrollo, accesibles a través de una página portfolio minimalista.

## 🌐 URL en Vivo

**GitHub Pages:** `https://YOUR_USERNAME.github.io/disenoria/`

## 📁 Estructura del Repositorio

```
disenoria/
├── index.html              # Portfolio home (página principal)
├── style.css               # Estilos del portfolio
│
└── sites/                  # Todos los sitios web
    └── disenoria/          # Sitio web de muebles a medida
        ├── index.html
        ├── styles.css
        ├── script.js
        ├── LOGO25.png
        ├── images/
        ├── proyectos/
        ├── README.md       # Documentación del sitio
        ├── CLAUDE.md
        └── CUSTOMIZATION_CHECKLIST.md
```

## 🚀 Ver Localmente

```bash
# Desde la raíz del repositorio
python3 -m http.server 8000

# Visita:
# http://localhost:8000                    → Portfolio home
# http://localhost:8000/sites/disenoria/   → Sitio Diseñoría
```

## ➕ Agregar Nuevo Sitio Web

1. **Crear carpeta para el nuevo sitio:**
   ```bash
   mkdir -p sites/nombre-del-sitio
   ```

2. **Agregar archivos del sitio** en la nueva carpeta

3. **Actualizar `index.html`** en la raíz:
   ```html
   <a href="sites/nombre-del-sitio/" class="project-card">
       <div class="project-number">02</div>
       <div class="project-info">
           <h2 class="project-title">Nombre del Proyecto</h2>
           <p class="project-description">Descripción breve del sitio</p>
           <div class="project-meta">
               <span class="tag">HTML/CSS/JS</span>
               <span class="status status-active">En desarrollo</span>
           </div>
       </div>
       <svg class="arrow" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
           <path d="M5 12h14M12 5l7 7-7 7"/>
       </svg>
   </a>
   ```

4. **Commit y push:**
   ```bash
   git add .
   git commit -m "Agregar nuevo sitio: nombre-del-sitio"
   git push
   ```

## 📦 Sitios Incluidos

### 1. Diseñoría
- **Ruta:** `/sites/disenoria/`
- **Descripción:** Sitio web para negocio de muebles a medida y carpintería de cocina
- **Tecnologías:** HTML, CSS, JavaScript vanilla
- **Estado:** En desarrollo
- **Documentación:** Ver `sites/disenoria/README.md`

## 🎨 Personalizar Portfolio Home

### Cambiar Colores
Edita `style.css` líneas 10-14:
```css
body {
    background: #0a0a0a;  /* Fondo oscuro */
    color: #e0e0e0;       /* Texto claro */
}
```

### Cambiar Título
Edita `index.html` línea ~13:
```html
<h1 class="title">Tu Nombre</h1>
<p class="subtitle">Portfolio</p>
```

## 📤 Publicar en GitHub Pages

1. **Push a GitHub:**
   ```bash
   git add .
   git commit -m "Add portfolio home page"
   git push origin main
   ```

2. **Activar GitHub Pages:**
   - Ve a Settings → Pages
   - Source: **main** branch
   - Click **Save**

3. **Acceder:**
   - Espera 1-2 minutos
   - Visita: `https://YOUR_USERNAME.github.io/disenoria/`

## 🔗 URLs de Acceso

Cuando esté publicado en GitHub Pages:

- **Portfolio home:** `https://YOUR_USERNAME.github.io/disenoria/`
- **Diseñoría:** `https://YOUR_USERNAME.github.io/disenoria/sites/disenoria/`
- **Futuro sitio 2:** `https://YOUR_USERNAME.github.io/disenoria/sites/sitio-2/`

## 💡 Notas

- Todos los sitios están en la carpeta `sites/`
- El portfolio home (`index.html`) es minimalista y fácil de modificar
- Cada sitio tiene su propia documentación en su carpeta
- GitHub Pages actualiza automáticamente al hacer push

## 📝 To-Do

- [ ] Configurar GitHub Pages
- [ ] Compartir URL con cliente
- [ ] Agregar más proyectos según sea necesario
- [ ] Considerar dominio personalizado (opcional)

---

**Desarrollado con ❤️**
