# 🛠️ NashUtils

[![Java](https://img.shields.io/badge/Java-21-orange.svg)](https://www.oracle.com/java/)

**NashUtils** adalah library pengembangan plugin Spigot/Paper.

Library ini merupakan **Enhanced Fork / Improvisasi** dari [SimpAPI oleh Cortex-MC](https://github.com/Cortex-MC/SimpAPI). Kami mengambil konsep dasarnya dan memperbaikinya dengan fitur-fitur yang dibutuhkan.

## ✨ Fitur & Improvisasi

Berikut adalah peningkatan signifikan yang kami lakukan dibandingkan versi original:

### 🔒 1. Per-Subcommand Permission (New!)
Tidak perlu lagi mengecek permission secara manual di dalam logika kode (`if !player.hasPermission...`).
Di **NashUtils**, setiap `SubCommand` memiliki method `getPermission()` sendiri.
- Jika return `null` -> Command publik.
- Jika return `string` -> Otomatis dicek sebelum command dijalankan.

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
```

### 2. Tambahkan Dependency
```xml
<dependencies>
    <dependency>
        <groupId>com.github.Ihsan-xyz</groupId> <artifactId>NashUtils</artifactId>
        <version>TagRelease</version> <scope>provided</scope>
    </dependency>
</dependencies>
```
