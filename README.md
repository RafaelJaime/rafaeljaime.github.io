# Portfolio Personal - Rafael Jaime

Este es mi portfolio personal construido con [Hugo](https://gohugo.io/) y desplegado automáticamente en GitHub Pages.

## 🌐 Sitio Multiidioma

El sitio está disponible en dos idiomas con inglés como idioma principal:
- **Inglés** (idioma por defecto): `https://rafaeljaime.github.io/en/`
- **Español**: `https://rafaeljaime.github.io/es/`

### Redirección Automática
- Al acceder a `https://rafaeljaime.github.io/` se redirecciona automáticamente a `/en/`
- Esto garantiza que todos los usuarios accedan al contenido en un idioma específico

## 🚀 Tecnologías

- **Hugo** - Generador de sitios estáticos
- **PaperMod** - Tema de Hugo
- **GitHub Actions** - CI/CD automático
- **GitHub Pages** - Hosting

## 📁 Estructura del Proyecto

```
├── content/
│   ├── about.md              # Página "About" en inglés (por defecto)
│   ├── about.es.md           # Página "Acerca de" en español
│   └── projects/
│       ├── _index.md         # Lista de proyectos en inglés
│       ├── _index.es.md      # Lista de proyectos en español
│       ├── example-project.md
│       └── proyecto-ejemplo.es.md
├── layouts/                  # Layouts personalizados
├── static/
│   └── index.html           # Página de redirección automática
├── themes/PaperMod/         # Tema (submódulo git)
├── hugo.toml                # Configuración principal
└── .github/workflows/       # GitHub Actions
```

## 🛠️ Desarrollo Local

### Prerrequisitos
- [Hugo Extended](https://gohugo.io/installation/) v0.149.0 o superior
- Git

### Instalación

1. Clona el repositorio:
```bash
git clone --recursive https://github.com/RafaelJaime/rafaeljaime.github.io.git
cd rafaeljaime.github.io
```

2. Inicia el servidor de desarrollo:
```bash
hugo server --buildDrafts
```

3. Visita:
   - `http://localhost:1313` (redirecciona a `/en/`)
   - `http://localhost:1313/en/` (inglés)
   - `http://localhost:1313/es/` (español)

## ✏️ Añadir Contenido

### Crear una nueva página

Para inglés (idioma por defecto):
```bash
hugo new content page-name.md
```

Para español:
```bash
hugo new content page-name.es.md
```

### Crear un nuevo proyecto

Para inglés:
```bash
hugo new content projects/project-name.md
```

Para español:
```bash
hugo new content projects/nombre-proyecto.es.md
```

## 🌍 Configuración de Idiomas

- **Inglés**: Idioma principal (weight: 1)
  - Sin sufijo en archivos
  - URLs: `/en/page-name`
  
- **Español**: Idioma secundario (weight: 2)
  - Sufijo `.es` en archivos
  - URLs: `/es/nombre-pagina`

## 🚀 Deploy

El sitio se despliega automáticamente usando GitHub Actions cuando se hace push a la rama `main`. El workflow:

1. Instala Hugo en el runner de GitHub
2. Construye el sitio estático con soporte multiidioma
3. Despliega a GitHub Pages

No se requiere configuración adicional, solo hacer push a main.

## 🔧 Configuración

La configuración principal está en `hugo.toml`. Las secciones más importantes:

- **defaultContentLanguage**: 'en' (inglés por defecto)
- **defaultContentLanguageInSubdir**: true (fuerza subdirectorios)
- **Idiomas**: Configuración para inglés y español
- **Menús**: Navegación localizada para cada idioma

## 📝 Licencia

Este proyecto es de código abierto y está disponible bajo la [Licencia MIT](LICENSE).

Local development instructions (Windows):

1) Install prerequisites
	- Ruby (use RubyInstaller for Windows)
	- MSYS2 toolchain (offered by RubyInstaller at the end; accept and install)
	- Git

2) Install bundler and dependencies
	- Open PowerShell in the repo folder.
	- Run:
	  - `gem install bundler`
	  - `bundle install`

3) Serve locally with livereload
	- Run: `bundle exec jekyll serve --livereload`
	- Open: http://127.0.0.1:4000/
