# Mockups Builder

Herramienta web para crear mockups de interfaces durante tomas de requerimiento.  
Desarrollada por [andyjara.dev](https://andyjara.dev) — Licencia [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

## Despliegue con Docker

```bash
git clone git@github.com:andyjara-dev/mockups.git
cd mockups
docker compose up -d --build
```

Accede en `http://tu-servidor:8080`

**Actualizar a nueva versión:**
```bash
git pull
docker compose up -d --build
```

---

## Uso

### 1. Proyectos
- Haz clic en **+ Proyecto** (esquina superior derecha) para crear un nuevo proyecto.
- Selecciona el proyecto activo desde el selector del header.

### 2. Grupos
- Dentro de un proyecto, crea **grupos** para organizar mockups relacionados (ej: "Módulo de Login", "Panel Admin").
- Haz clic en **+** en la sección Grupos del sidebar.

### 3. Mockups
- Dentro de un grupo, crea **mockups** individuales con nombre y tipo de dispositivo:
  - Web (1280×800, 1440×900)
  - Mobile (375×812, 390×844)
  - Tablet (768×1024)
- Haz clic en **+** en la sección Mockups del sidebar.

### 4. Canvas — agregar elementos
Usa la barra de widgets en la parte superior para agregar elementos al mockup activo:

| Widget | Descripción |
|--------|-------------|
| **Texto** | Texto libre con control de fuente y color |
| **Label** | Etiqueta pequeña para campos |
| **Input** | Campo de texto |
| **Textarea** | Área de texto multilínea |
| **Botón** | Botón con variantes: primary, secondary, danger, outline |
| **Select** | Dropdown de selección |
| **Checkbox** | Casilla de verificación |
| **Radio** | Botón de opción |
| **Imagen** | Placeholder de imagen |
| **Rect** | Rectángulo / contenedor |
| **Navbar** | Barra de navegación |
| **Card** | Tarjeta con título y contenido |
| **Línea** | Separador horizontal |

### 5. Mover y redimensionar
- **Mover**: arrastra el elemento en el canvas.
- **Redimensionar**: selecciona el elemento y arrastra cualquiera de los 8 puntos de control.
- **Eliminar**: selecciona el elemento y presiona `Delete` o usa el botón en el panel de propiedades.

### 6. Panel de propiedades
Al seleccionar un elemento aparece el panel derecho con sus propiedades editables: posición, dimensiones, colores, texto, variante, etc.

### 7. Zoom
Usa los botones `−` / `+` en la barra inferior o `Ctrl + Rueda del mouse` para hacer zoom en el canvas.

### 8. Exportar a PNG
- Haz clic en **⬇ PNG** en el header.
- Se descarga una imagen del mockup activo con marca de agua `mockups by andyjara.dev`.

### 9. Backup y restauración
- **💾 Backup**: descarga un archivo `.json` con todos los proyectos.
- **📂 Cargar**: carga un archivo de backup para restaurar el ambiente completo.

> Los datos se guardan automáticamente en el `localStorage` del navegador.

---

## Desarrollo local

Solo abre `index.html` en cualquier navegador moderno — no requiere servidor ni dependencias.
