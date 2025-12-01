# 🛠️ NashUtils

[![Java](https://img.shields.io/badge/Java-21-orange.svg)](https://www.oracle.com/java/)
[![JitPack](https://jitpack.io/v/UserGitHubAnda/NashUtils.svg)](https://jitpack.io/#UserGitHubAnda/NashUtils)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

**NashUtils** adalah library pengembangan plugin Spigot/Paper modern yang dirancang untuk mempercepat workflow Anda.

Library ini merupakan **Enhanced Fork / Improvisasi** dari [SimpAPI oleh Cortex-MC](https://github.com/Cortex-MC/SimpAPI). Kami mengambil konsep dasarnya yang simpel dan memperbaikinya dengan fitur-fitur modern yang dibutuhkan developer masa kini.

## ✨ Fitur & Improvisasi

Berikut adalah peningkatan signifikan yang kami lakukan dibandingkan versi original:

### 🔒 1. Per-Subcommand Permission (New!)
Tidak perlu lagi mengecek permission secara manual di dalam logika kode (`if !player.hasPermission...`).
Di **NashUtils**, setiap `SubCommand` memiliki method `getPermission()` sendiri.
- Jika return `null` -> Command publik.
- Jika return `string` -> Otomatis dicek sebelum command dijalankan.

### 🎨 2. Hex Color Support
Full support untuk format warna modern Minecraft (RGB/Hex) menggunakan format `&#RRGGBB`.

### ⚙️ 3. Jackson-Powered Configuration
Sistem config yang ditulis ulang menggunakan **Jackson (FasterXML)**. Mendukung serialisasi otomatis untuk file **YAML** dan **JSON** hanya dengan menggunakan anotasi Java (POJO).

---

## 📦 Instalasi

NashUtils tersedia melalui **JitPack**. Tambahkan ini ke `pom.xml` plugin Anda:

### 1. Tambahkan Repository
```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>[https://jitpack.io](https://jitpack.io)</url>
    </repository>
</repositories>
