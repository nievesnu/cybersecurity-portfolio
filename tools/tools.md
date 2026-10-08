# Paquetes de Ciberseguridad / Criptografía
---

## Herramientas de Pentesting / CTF

- **dirb** — `https://tools.kali.org/web-applications/dirb` [(tools.kali.org in Bing)](https://www.bing.com/search?q="https%3A%2F%2Ftools.kali.org%2Fweb-applications%2Fdirb")  
  Escáner de directorios y rutas ocultas en aplicaciones web.

- **john** — [https://www.openwall.com/john/](https://www.openwall.com/john/)  
  Cracker de contraseñas, útil para claves RSA, hashes, etc.

- **john-data** — [https://www.openwall.com/john/](https://www.openwall.com/john/)  
  Diccionarios y formatos para John The Ripper.

- **gpg** — [https://gnupg.org/](https://gnupg.org/)  
  Criptografía de clave pública, firmas, cifrado de archivos.

- **gpg-agent** — [https://gnupg.org/](https://gnupg.org/)  
  Manejo de claves privadas y sesiones GPG.

- **gpgv** — [https://gnupg.org/](https://gnupg.org/)  
  Verificación de firmas digitales.

- **gpgsm** — [https://gnupg.org/](https://gnupg.org/)  
  Manejo de certificados X.509 y S/MIME.

- **dirmngr** — [https://gnupg.org/](https://gnupg.org/)  
  Descarga y gestión de listas de revocación y certificados.

---

## Criptografía / Seguridad del sistema

- **libgcrypt20** — [https://gnupg.org/software/libgcrypt/](https://gnupg.org/software/libgcrypt/)  
  Biblioteca criptográfica usada por GPG y otras herramientas.

- **libgnutls30** — [https://www.gnutls.org/](https://www.gnutls.org/)  
  Implementación de TLS/SSL.

- **libfido2-1** — [https://github.com/Yubico/libfido2](https://github.com/Yubico/libfido2)  
  Autenticación FIDO2/WebAuthn.

- **libargon2-1** — `https://github.com/P-H-C/phc-winner-argon2` [(github.com in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fgithub.com%2FP-H-C%2Fphc-winner-argon2")  
  Algoritmo de hashing seguro para contraseñas.

- **libcrypt1** — `https://man7.org/linux/man-pages/man3/crypt.3.html` [(man7.org in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fman7.org%2Flinux%2Fman-pages%2Fman3%2Fcrypt.3.html")  
  Funciones de hashing y cifrado clásicas.

- **libcryptsetup12** — [https://gitlab.com/cryptsetup/cryptsetup](https://gitlab.com/cryptsetup/cryptsetup)  
  Backend para LUKS (cifrado de discos).

- **libssl (via libcurl/gnutls)** — [https://www.openssl.org/](https://www.openssl.org/)  
  Criptografía para HTTPS, TLS, certificados.

---

## Análisis forense / manipulación de archivos

- **libimage-exiftool-perl** — [https://exiftool.org/](https://exiftool.org/)  
  Lectura y manipulación de metadatos EXIF (muy útil en forense digital).

- **imagemagick** — [https://imagemagick.org/](https://imagemagick.org/)  
  Procesamiento de imágenes, útil en retos forenses.

- **graphicsmagick** — [http://www.graphicsmagick.org/](http://www.graphicsmagick.org/)  
  Alternativa ligera a ImageMagick.

---

## Redes / Seguridad de red

- **bind9-host** — [https://www.isc.org/bind/](https://www.isc.org/bind/)  
  Herramientas DNS (útiles para enumeración).

- **bind9-dnsutils** — [https://www.isc.org/bind/](https://www.isc.org/bind/)  
  Incluye `dig`, `nslookup`, etc.

- **iputils-ping** — [https://github.com/iputils/iputils](https://github.com/iputils/iputils)  
  Diagnóstico de red.

- **iproute2** — [https://wiki.linuxfoundation.org/networking/iproute2](https://wiki.linuxfoundation.org/networking/iproute2)  
  Herramientas avanzadas de red.

---

## Seguridad del sistema / aislamiento

- **apparmor** — [https://wiki.ubuntu.com/AppArmor](https://wiki.ubuntu.com/AppArmor)  
  Mandatory Access Control (MAC).

- **bubblewrap** — [https://github.com/containers/bubblewrap](https://github.com/containers/bubblewrap)  
  Sandbox para aislar procesos.

---

## Utilidades para CTFs

- **file** — `https://man7.org/linux/man-pages/man1/file.1.html` [(man7.org in Bing)](https://www.bing.com/search?q="https%3A%2F%2Fman7.org%2Flinux%2Fman-pages%2Fman1%2Ffile.1.html")  
  Identificación de tipos de archivo.

- **strings (via binutils)** — [https://www.gnu.org/software/binutils/](https://www.gnu.org/software/binutils/)  
  Extraer texto de binarios.

- **objdump / readelf (via binutils)** — [https://www.gnu.org/software/binutils/](https://www.gnu.org/software/binutils/)  
  Análisis de binarios.

---

Aqui está el script donde instalar todas las herramientas: tools/ciberseguridad.sh
