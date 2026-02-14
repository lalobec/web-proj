# Carpeta de Proyectos (proyectos/)

Esta carpeta contiene las páginas de detalle individuales para proyectos del portafolio.

## 📋 Archivos Incluidos

### `template-proyecto.html`
**Plantilla base para crear nuevos proyectos**
- Copia este archivo para crear cada nuevo proyecto
- Reemplaza todos los marcadores `[TEXTO]` con tu contenido
- Usa como guía para mantener consistencia

### `cocina-moderna-minimalista.html`
**Ejemplo completo de una página de proyecto**
- Muestra cómo llenar la plantilla
- Usa como referencia para tus propios proyectos
- Puedes eliminar o modificar según necesites

## 🚀 Cómo Crear un Nuevo Proyecto

### Paso 1: Duplicar la Plantilla

```bash
# En la carpeta proyectos/
cp template-proyecto.html mi-nuevo-proyecto.html
```

**Convención de nombres:**
- Usa minúsculas
- Separa palabras con guiones
- Sé descriptivo
- Ejemplos: `cocina-rustica-moderna.html`, `closet-walk-in-familiar.html`

### Paso 2: Editar el Contenido

Abre el nuevo archivo y reemplaza estos elementos:

#### Meta Tags (líneas 5-7)
```html
<meta name="description" content="Tu descripción del proyecto">
<title>Nombre del Proyecto | Diseñoría</title>
```

#### Información del Proyecto (líneas ~77-97)
```html
<h1 class="project-title">Nombre del Proyecto</h1>

<!-- Meta información -->
<span class="project-meta-value">Nombre del Cliente</span>
<span class="project-meta-value">Cocina/Muebles/Closet</span>
<span class="project-meta-value">2024/2025/2026</span>
<span class="project-meta-value">X semanas</span>
```

#### Contenido del Proyecto
- **Resumen**: 2-3 párrafos sobre el proyecto
- **El Desafío**: Qué problema tenía el cliente
- **La Solución**: Cómo lo resolviste
- **Características**: Lista de 4-6 características destacadas
- **El Resultado**: Impacto final del proyecto
- **Testimonio**: (Opcional) Cita del cliente

#### Imágenes
Reemplaza las rutas de imágenes:
```html
<img src="../images/portfolio/tu-imagen.jpg" alt="Descripción">
```

### Paso 3: Enlazar desde el Portafolio Principal

Edita `index.html` en la sección de portafolio (líneas ~142-197):

```html
<div class="portfolio-item">
    <a href="proyectos/mi-nuevo-proyecto.html">
        <img src="images/portfolio/proyecto-1.jpg" alt="Descripción">
        <div class="portfolio-overlay">
            <h4>Nombre del Proyecto</h4>
            <p>Breve descripción</p>
        </div>
    </a>
</div>
```

**Importante:** Envuelve el contenido en un tag `<a>` para que sea clickeable.

## 📐 Estructura de una Página de Proyecto

```
┌─────────────────────────────────┐
│ Header (mismo que página main)  │
├─────────────────────────────────┤
│ Hero del Proyecto               │
│ - Título                        │
│ - Metadata (cliente, año, etc)  │
├─────────────────────────────────┤
│ Resumen del Proyecto            │
├─────────────────────────────────┤
│ Imagen Principal (grande)       │
├─────────────────────────────────┤
│ El Desafío                      │
│ La Solución                     │
├─────────────────────────────────┤
│ Características Destacadas      │
│ (caja con lista de checkmarks)  │
├─────────────────────────────────┤
│ Galería de Imágenes             │
│ (grid de 4+ imágenes)           │
├─────────────────────────────────┤
│ El Resultado                    │
│ + Testimonio (opcional)         │
├─────────────────────────────────┤
│ CTA (Llamado a la acción)       │
├─────────────────────────────────┤
│ Footer (mismo que página main)  │
└─────────────────────────────────┘
```

## 🎨 Consejos de Contenido

### Títulos de Proyecto
- ✅ Bueno: "Cocina Moderna Minimalista", "Sistema de Closet Walk-in"
- ❌ Malo: "Proyecto 1", "Cocina de Juan"

### Descripciones
- Usa 2-3 párrafos para el resumen
- Enfócate en el problema y la solución
- Menciona resultados específicos (ej: "40% más almacenamiento")

### Características
- 4-6 características clave
- Sé específico (no solo "Buena calidad", sino "Madera contrachapada de abedul premium")
- Menciona marcas/sistemas cuando sea relevante (ej: "Herrajes Blum")

### Testimonios
- Si tienes permiso del cliente, usa su nombre real
- Si no, usa solo el primer nombre o iniciales
- Mantén las citas auténticas y específicas

## 📸 Imágenes Recomendadas

Para cada proyecto incluye:
- **1 imagen hero** (grande, destacada): 1920x1080px
- **4-6 imágenes de galería**: 1200x900px cada una
- Muestra diferentes ángulos y detalles
- Incluye close-ups de características especiales

**Nombres de archivo sugeridos:**
```
images/portfolio/
├── cocina-moderna-hero.jpg
├── cocina-moderna-01.jpg
├── cocina-moderna-02.jpg
├── cocina-moderna-03.jpg
└── cocina-moderna-04.jpg
```

## 🔗 URLs de Ejemplo

Con esta estructura, tus proyectos tendrán URLs como:
- `www.disenoria.com/proyectos/cocina-moderna-minimalista.html`
- `www.disenoria.com/proyectos/closet-walk-in-familiar.html`
- `www.disenoria.com/proyectos/isla-de-cocina-industrial.html`

## ✅ Checklist para Nuevo Proyecto

Antes de publicar un nuevo proyecto, verifica:

- [ ] Copiaste `template-proyecto.html` con un nombre descriptivo
- [ ] Actualizaste el `<title>` y meta `description`
- [ ] Reemplazaste el nombre del proyecto
- [ ] Completaste toda la metadata (cliente, categoría, año, duración)
- [ ] Escribiste el resumen del proyecto (2-3 párrafos)
- [ ] Describiste el desafío y la solución
- [ ] Listaste 4-6 características destacadas
- [ ] Subiste las imágenes del proyecto a `/images/portfolio/`
- [ ] Actualizaste todas las rutas de imágenes
- [ ] Agregaste alt text descriptivo a todas las imágenes
- [ ] Incluiste testimonio del cliente (si está disponible)
- [ ] Agregaste un enlace desde `index.html#portfolio`
- [ ] Probaste que todos los enlaces funcionen
- [ ] Revisaste ortografía y gramática

## 🛠️ Personalización Avanzada

### Cambiar el Layout
Puedes modificar el CSS en la sección `<style>` de cada proyecto individual si necesitas un diseño único.

### Añadir Secciones
Puedes agregar nuevas secciones como:
- Antes/Después comparisons
- Video embeds
- Diagramas de planos
- Lista de materiales
- Timeline del proceso

### Mantener Consistencia
Aunque puedes personalizar, trata de mantener:
- La estructura general similar
- Los mismos colores (variables CSS)
- El mismo header y footer
- El mismo estilo de navegación

## 📝 Notas

- Todas las rutas de imágenes usan `../` porque están en una subcarpeta
- El JavaScript (`../script.js`) maneja la navegación móvil automáticamente
- Cada proyecto es una página independiente pero comparte estilos con el sitio principal
- Los proyectos son indexables por Google individualmente

---

**¿Listo para agregar tus proyectos? Empieza copiando `template-proyecto.html` y reemplaza el contenido con tu primer proyecto real!**
