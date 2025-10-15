# 🌐 4rgs.github.io

> **Portafolio personal de Álvaro González** - Desarrollador Full-Stack, maker y entusiasta del hardware libre

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://4rgs.github.io)
[![Jekyll](https://img.shields.io/badge/Jekyll-Static%20Site-red)](https://jekyllrb.com/)
[![License](https://img.shields.io/badge/License-CC0%201.0-lightgrey)](LICENSE)

## 🎯 Sobre este sitio

Este es mi portafolio personal donde documento mis proyectos, experimentos y investigaciones en desarrollo de software y hardware. El sitio está construido con **Jekyll** y utiliza el tema **Hacker** para un look técnico y profesional.

## 🚀 Proyectos Destacados

### 🧩 Hardware & IoT
- **[RPI2WZeroLAB](./projects/rpi2wzerolab.html)** - Sistema embebido con Raspberry Pi Zero 2 W
- **[T100 Controller](./projects/t100-controller.html)** - Controlador RC con ESP32-S3
- **[T-DECK SSH CLIENT](https://github.com/4rgs/T-DECK-SSH-CLIENT)** - Cliente SSH para dispositivo T-Deck

### 🎮 Gaming & Addons
- **[LightsaberCrit](./projects/lightsaber-crit.html)** - Addon WoW Classic con efectos de sable láser
- **[PoGoCompi](./projects/pogocompi.html)** - Comparador DPS para Pokémon GO

### 🤖 Automatización
- **[HelenaBot](./projects/helenabot.html)** - Bot modular en PureBasic
- **[4rgs AI RAG](https://github.com/4rgs/4rgs-ai-rag)** - Experimentos con sistemas RAG

## 🛠️ Stack Tecnológico

```yaml
Frontend:
  - React, JavaScript, TypeScript
  - HTML5, SCSS, TailwindCSS
  
Backend:
  - Node.js, NestJS, Express
  - Python, PostgreSQL
  - REST APIs, WebSockets

Hardware:
  - Raspberry Pi, ESP32-S3
  - Bluetooth BLE, e-ink displays
  - UART/SPI/I²C protocols

DevOps:
  - Docker, Google Cloud
  - GitHub Actions
  - Terraform
```

## 🔧 Desarrollo Local

### Prerrequisitos
```bash
# Instalar Ruby y Jekyll
gem install bundler jekyll

# O usar Docker
docker --version
```

### Configuración
```bash
# Clonar repositorio
git clone https://github.com/4rgs/4rgs.github.io.git
cd 4rgs.github.io

# Instalar dependencias
bundle install

# Ejecutar servidor de desarrollo
bundle exec jekyll serve

# El sitio estará disponible en http://localhost:4000
```

### Con Docker
```bash
# Construcción del contenedor
docker run --rm -v "$PWD":/usr/src/app -w /usr/src/app ruby:2.7 bundle install

# Ejecutar Jekyll
docker run --rm -v "$PWD":/usr/src/app -w /usr/src/app -p 4000:4000 ruby:2.7 bundle exec jekyll serve --host 0.0.0.0
```

## 📁 Estructura del Proyecto

```
4rgs.github.io/
├── _config.yml          # Configuración Jekyll
├── index.md             # Página principal
├── README.md            # Este archivo
├── projects/            # Páginas de proyectos
│   ├── rpi2wzerolab.md
│   ├── lightsaber-crit.md
│   ├── pogocompi.md
│   ├── t100-controller.md
│   └── helenabot.md
├── assets/              # Recursos estáticos
│   └── css/            # Estilos personalizados
└── _layouts/           # Layouts Jekyll (si hay custom)
```

## 🎨 Personalización

### Tema Base
- **Jekyll Theme Hacker** - Look y feel técnico
- **Sintaxis highlighting** con Rouge
- **Responsive design** optimizado para móviles

### Customizaciones
- Paleta de colores adaptada
- Tipografía optimizada para código
- Componentes adicionales para proyectos
- SEO optimizado con meta tags

## 📈 Analytics y SEO

- **Jekyll SEO Tag** - Meta tags automáticos
- **Sitemap** generado automáticamente  
- **Feed RSS** para actualizaciones
- **Schema.org** markup para mejor indexación

## 🚀 Deployment

El sitio se deploya automáticamente a **GitHub Pages** cuando se hace push a la rama `master`:

```bash
# Hacer cambios
git add .
git commit -m "Update content"
git push origin master

# GitHub Pages se actualiza automáticamente
```

## 📫 Contacto

- **📧 Email:** [alvaro.gonzalez.dev@gmail.com](mailto:alvaro.gonzalez.dev@gmail.com)
- **🐙 GitHub:** [@4rgs](https://github.com/4rgs)
- **🏢 Empresa:** Integ LTDA
- **📍 Ubicación:** Chile 🇨🇱

## 📄 Licencia

Este proyecto está bajo la licencia [Creative Commons Zero v1.0 Universal](LICENSE) - ver el archivo LICENSE para detalles.

## 🙏 Agradecimientos

- **Jekyll** y **GitHub Pages** por el hosting gratuito
- **Tema Hacker** por el diseño base
- **Comunidad open source** por las herramientas utilizadas

---

⭐️ **Si te gusta este portafolio, considera darle una estrella al repositorio**

*Última actualización: Octubre 2025*