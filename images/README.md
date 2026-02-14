# Images Folder - Guía de Uso

Esta carpeta contiene todas las imágenes del sitio web organizadas por sección.

## Estructura de Carpetas

### 📁 hero/
**Imágenes de fondo para la sección principal**
- `hero-background.jpg` - Imagen de fondo (1920x1080px)
- Tamaño recomendado: < 300KB
- Formato: JPG o WebP

### 📁 services/
**Imágenes para las tarjetas de servicios**
- `kitchen-service.jpg` - Imagen para servicios de cocinas (800x600px)
- `furniture-service.jpg` - Imagen para muebles a medida (800x600px)
- Tamaño recomendado: < 150KB cada una
- Formato: JPG o WebP

### 📁 portfolio/
**Galería de proyectos completados**
- `project-1.jpg` - Proyecto 1 (1200x900px)
- `project-2.jpg` - Proyecto 2 (1200x900px)
- `project-3.jpg` - Proyecto 3 (1200x900px)
- `project-4.jpg` - Proyecto 4 (1200x900px)
- `project-5.jpg` - Proyecto 5 (1200x900px)
- `project-6.jpg` - Proyecto 6 (1200x900px)
- Tamaño recomendado: < 150KB cada una
- Formato: JPG o WebP
- Aspecto: 4:3 (horizontal)

### 📁 about/
**Imágenes para la sección "Nosotros"**
- `craftsman.jpg` - Foto del equipo o taller (800x1000px)
- Tamaño recomendado: < 200KB
- Formato: JPG o WebP
- Aspecto: 4:5 (vertical/retrato)

## Consejos para Optimización

1. **Comprimir todas las imágenes** antes de subirlas
   - Usa herramientas como TinyPNG, Squoosh, o ImageOptim

2. **Usar formato WebP** cuando sea posible
   - Mejor compresión que JPG
   - Soportado en navegadores modernos

3. **Nombres descriptivos** para SEO
   - ✅ Bueno: `cocina-moderna-madera.jpg`
   - ❌ Malo: `IMG_1234.jpg`

4. **Mantener proporciones correctas**
   - Evita distorsión en las imágenes
   - Usa las dimensiones recomendadas arriba

## Reemplazar Imágenes en el Código

Después de agregar tus imágenes, actualiza las rutas en `index.html`:

```html
<!-- Hero background -->
<style>
.hero-background {
    background-image: url('images/hero/hero-background.jpg');
}
</style>

<!-- Service images -->
<div class="service-image" style="background-image: url('images/services/kitchen-service.jpg');"></div>

<!-- Portfolio images -->
<img src="images/portfolio/project-1.jpg" alt="Descripción del proyecto">

<!-- About image -->
<img src="images/about/craftsman.jpg" alt="Nuestro equipo">
```
