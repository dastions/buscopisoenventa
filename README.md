# Portal 22 - Inmobiliaria Landing Page

Una landing page minimalista y moderna para una inmobiliaria construida con Vue.js 3 y Vite.

## Características

- ✨ Diseño moderno y responsive
- 🏢 Secciones para Pisos y Fincas Rústicas
- 📧 Formulario de contacto integrado con mailto
- 📱 Completamente responsive
- 🚀 Optimizada para rendimiento
- 🎨 Animaciones suaves y atractivas

## Estructura del Proyecto

```
├── public/
│   ├── pisos.html          # Página de pisos
│   └── fincas.html         # Página de fincas rústicas
├── src/
│   ├── App.vue             # Componente principal
│   ├── main.js             # Punto de entrada
│   └── style.css           # Estilos globales
├── index.html              # Página principal
├── package.json            # Dependencias
└── vite.config.js          # Configuración de Vite
```

## Instalación y Uso

### Prerrequisitos
- Node.js (versión 16 o superior)
- npm o yarn

### Pasos para ejecutar

1. **Instalar dependencias:**
   ```bash
   npm install
   ```

2. **Ejecutar en modo desarrollo:**
   ```bash
   npm run dev
   ```

3. **Construir para producción:**
   ```bash
   npm run build
   ```

4. **Previsualizar la build de producción:**
   ```bash
   npm run preview
   ```

## Funcionalidades

### Landing Page Principal
- Header con logo y botón de contacto
- Sección hero con botones para navegar a Pisos y Fincas
- Formulario de consulta que genera emails automáticamente
- Footer con información de contacto y datos fiscales

### Formulario de Contacto
- Campos para nombre, email, teléfono y tipo de propiedad
- Mensaje personalizable
- Genera automáticamente un email con toda la información

### Páginas Secundarias
- **Pisos**: Página dedicada a propiedades urbanas
- **Fincas Rústicas**: Página para propiedades rurales
- Ambas páginas incluyen enlaces de contacto directo

## Personalización

### Cambiar Datos de Contacto
Editar en `src/App.vue`:
- Email de contacto en las funciones `handleSubmit`, `goToPisos`, `goToFincas`
- Información del footer

### Modificar Estilos
Los estilos se encuentran en `src/style.css` y están organizados por secciones:
- Variables CSS para colores y tipografías
- Componentes individuales (header, hero, footer, etc.)
- Media queries para responsive design

### Añadir Contenido
- **Imágenes**: Colocar en la carpeta `public/` y referenciar desde los componentes
- **Nuevo contenido**: Modificar `src/App.vue`
- **Páginas adicionales**: Crear nuevos archivos HTML en `public/`

## Deploy

### GitHub Pages (Automático)

El proyecto está configurado para desplegar automáticamente en GitHub Pages con dominio personalizado:

1. **Hacer push a la rama main/master** - El workflow se ejecutará automáticamente
2. **Configurar GitHub Pages** en la configuración del repositorio:
   - Ir a Settings > Pages
   - Source: "GitHub Actions"
   - Custom domain: "www.buscopisoenventa.com"
3. **Acceder al sitio** en: `https://www.buscopisoenventa.com`

### Deploy Manual

Para hostear como sitio estático en otros servidores:

1. Ejecutar `npm run build`
2. Subir el contenido de la carpeta `dist/` a tu servidor web
3. Configurar el servidor para servir `index.html` como página principal

## Tecnologías Utilizadas

- **Vue.js 3**: Framework JavaScript progresivo
- **Vite**: Herramienta de build rápida
- **CSS3**: Estilos modernos con gradientes y animaciones
- **HTML5**: Semántica moderna

## Contacto

Para consultas sobre este proyecto o la inmobiliaria:
- Empresa: Portal 22

---

© 2024 Portal 22. Todos los derechos reservados.
