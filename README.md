# FFmpeg Studio

<div align="center">

![FFmpeg Studio](data/icons/hicolor/scalable/apps/io.github.ffmpegstudio.svg)

**Conversor multimedia multiformato para Linux**  
Interfaz GTK4 + Libadwaita · Basado en FFmpeg

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Platform: Linux](https://img.shields.io/badge/Platform-Linux-orange.svg)](https://www.linux.org/)
[![GTK: 4.0](https://img.shields.io/badge/GTK-4.0-green.svg)](https://gtk.org/)

</div>

---

## ✨ Características

### 🎵 Audio — 12 formatos
| Formato | Codec | Lossy |
|---------|-------|-------|
| MP3 | libmp3lame | ✓ |
| AAC / M4A | aac | ✓ |
| OGG Vorbis | libvorbis | ✓ |
| OPUS | libopus | ✓ |
| WMA | wmav2 | ✓ |
| AC3 (Dolby) | ac3 | ✓ |
| MP2 | mp2 | ✓ |
| FLAC | flac | ✗ |
| WAV | pcm_s16le | ✗ |
| AIFF | pcm_s16be | ✗ |

### 🎬 Vídeo — 14 formatos
MP4 H.264, MP4 H.265/HEVC, MKV H.264/H.265, WebM VP8/VP9, AVI, MOV ProRes, FLV, WMV, OGV Theora, TS MPEG-2, GIF animado, 3GP.

### ⚙️ Controles disponibles

**Audio**
- Tasa de muestreo: 8 kHz → 192 kHz
- Canales: Mono, Estéreo, 5.1, 7.1
- Bitrate: 64k → 512k
- Volumen ajustable (0.1× – 4.0×)
- Normalización EBU R128 (loudnorm)
- Fade In / Fade Out
- Recorte temporal (inicio + duración)

**Vídeo**
- Resolución: 240p → 4K + personalizada
- Framerate: 15 → 240 fps
- Calidad: CRF (0–51) o bitrate fijo
- Preset: ultrafast → veryslow
- Aceleración hardware: CPU / CUDA / VAAPI / VDPAU
- Codificación en 2 pasadas
- Eliminar pista de audio
- Recorte temporal

---

## 📦 Instalación

### Opción A — Paquete .deb (recomendado)

Descarga el `.deb` de la sección [Releases](https://github.com/your-username/ffmpeg-studio/releases):

```bash
# Instalar
sudo dpkg -i ffmpeg-studio_1.0.0_all.deb
sudo apt install -f  # Resuelve dependencias si falta alguna

# Desinstalar
sudo apt remove ffmpeg-studio
```

### Opción B — Ejecución directa

```bash
# Dependencias
sudo apt install python3-gi gir1.2-gtk-4.0 gir1.2-adw-1 ffmpeg

# Clonar y ejecutar
git clone https://github.com/your-username/ffmpeg-studio.git
cd ffmpeg-studio
python3 src/ffmpeg_studio.py
```

---

## 🔨 Construir el .deb desde fuente

```bash
git clone https://github.com/your-username/ffmpeg-studio.git
cd ffmpeg-studio
bash build-deb.sh
sudo dpkg -i ffmpeg-studio_1.0.0_all.deb
```

**Dependencias de build** (opcionales para iconos PNG):
```bash
sudo apt install librsvg2-bin   # Para rsvg-convert (iconos PNG)
```

---

## 🐧 Requisitos del sistema

| Componente | Versión mínima |
|------------|---------------|
| Linux | cualquier distro moderna |
| Python | ≥ 3.10 |
| GTK | ≥ 4.0 |
| Libadwaita | ≥ 1.2 |
| FFmpeg | cualquier versión reciente |

**Ubuntu / Debian:**
```bash
sudo apt install python3-gi gir1.2-gtk-4.0 gir1.2-adw-1 ffmpeg
```

**Arch Linux:**
```bash
sudo pacman -S python-gobject gtk4 libadwaita ffmpeg
```

**Fedora:**
```bash
sudo dnf install python3-gobject gtk4 libadwaita ffmpeg
```

---

## 🗂 Estructura del proyecto

```
ffmpeg-studio/
├── src/
│   └── ffmpeg_studio.py       # Aplicación principal GTK4
├── data/
│   ├── applications/
│   │   └── io.github.ffmpegstudio.desktop
│   ├── icons/
│   │   └── hicolor/scalable/apps/
│   │       └── io.github.ffmpegstudio.svg
│   └── metainfo/
│       └── io.github.ffmpegstudio.metainfo.xml
├── debian/
│   ├── control
│   ├── postinst
│   └── postrm
├── build-deb.sh               # Script de construcción del .deb
├── LICENSE
└── README.md
```

---

## 🤝 Contribuir

1. Haz fork del repositorio
2. Crea una rama: `git checkout -b feature/nueva-funcionalidad`
3. Haz commit: `git commit -m 'Añade nueva funcionalidad'`
4. Push: `git push origin feature/nueva-funcionalidad`
5. Abre un Pull Request

---

## 📄 Licencia

GPL-3.0 — ver [LICENSE](LICENSE)

---

<div align="center">
Hecho con ❤️ para la comunidad Linux
</div>
