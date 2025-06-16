- Bu depo Arch tabanlı sistemler içindir. Debian/Ubuntu tabanlı sistemler için [buraya tıklayın](https://github.com/npc-gnu/Tr-Terminal-deb) .

# Tr-Terminal

## Tr-Terminal Nedir?

**Tr-Terminal**, GNU/Linux terminalini *neredeyse tamamen* Türkçe kullanabilmenizi sağlayan bash betiklerinden oluşan bir projedir.

## Özellikler ve Notlar

- Bash betikleriyle yazıldığı için yalnızca `bash` kabuğunda çalışır. `fish`, `zsh` gibi alternatif kabuklarla uyumlu değildir.  
- *"Tamamen" Türkçe demek tam doğru olmaz; tüm komutlar Türkçeye çevrilmedi. Ancak düzenli olarak yeni Türkçe komutlar eklenmeye devam edecek.*
- Paket yönetimi ile ilgili komutlar yalnızca Arch tabanlı sistemlerde (örneğin: Manjaro, EndeavourOS) çalışır (`pacman` ve `yay` kullanır).

## Komutlar

| Türkçe Komut           | Karşılığı                     | Açıklama |
|------------------------|-------------------------------|----------|
| `durum`                | `neofetch`                    | Sistemin temel bilgilerini ASCII sanatıyla gösterir. `neofetch` yüklü olmalıdır.         |
| `hızlıdurum`           | `fastfetch`                   | `neofetch`'in daha hızlı çalışan alternatifi. `fastfetch` yüklü olmalıdır.               |
| `kaldır-bc`            | `pacman -Rns <paket>`         | Girdiğiniz pacman paketini, bağımlılıklarını ve yapılandırma dosyalarını(config) siler.  |
| `kapat`                | `shutdown`                    | Sistemi kapatır. (Şimdilik `kapat now` gibi İngilizce parametrelerle kullanılmalı.)      |
| `kopyala`              | `cp`                          | Dosya veya dizinleri kopyalar.                                                           |
| `kullanıcıdeğiştir`    | `su`                          | Belirttiğiniz kullanıcıya geçiş yapar.                                                   |
| `sil`                  | `rm -rf`                      | Dosya veya dizinleri siler.                                                              |
| `süreçler`             | `htop`                        | Sistem süreçlerini izleyebilir, işlemleri sonlandırabilirsiniz.                          |
| `taşı`                 | `mv`                          | Dosya veya dizinleri taşır.                                                              |
| `yönetici`             | `sudo`                        | Komutu yönetici (root) yetkileriyle çalıştırır.                                          |
| `yükle`                | `pacman -S <paket>`           | `pacman` paketleri yüklemenizi sağlar.                                                   |
| `depo`                 | `pacman -Sy`                  | `pacman` depolarını günceller.                                                           |
| `güncelleme`           | `pacman -Syu`                 | Sistemdeki tüm `pacman` paketlerini güncellemenizi sağlar.                               |
| `kaldır`               | `pacman -R <paket>`           | Girdiğiniz `pacman` paketini siler.                                                      |
| `kaldır-c`             | `pacman -Rn <paket>`          | Girdiğiniz `pacman` paketini ve yapılandırma dosyalarını(config) siler.                  |
| `kaldır-b`             | `pacman -Rs <paket>`          | Girdiğiniz `pacman` paketini ve bağımlılıklarını siler.                                  |
| `kaldır-bc`            | `pacman -Rns <paket>`         | Girdiğiniz pacman paketini, bağımlılıklarını ve yapılandırma dosyalarını(config) siler.  | 
| `aur-yükle`            | `yay -S <paket>`              | (aur üzerinden `yay` aracıyla) Paket yüklemenizi sağlar.                                 |
| `aur-depo`             | `yay -Sy`                     | AUR depolarını günceller.                                                                |
| `aur-güncelleme`       | `yay -Syu`                    | AUR/yay paketlerini günceller.                                                           |
| `aur-kaldır`           | `yay -R <paket>`              | Girdiğiniz `pacman` paketini siler.                                                      |
| `aur-kaldır-c`         | `yay -Rn <paket>`             | Girdiğiniz `pacman` paketini ve yapılandırma dosyalarını(config) siler.                  |
| `aur-kaldır-b`         | `yay -Rs <paket>`             | Girdiğiniz `pacman` paketini ve bağımlılıklarını siler.                                  |
| `aur-kaldır-bc`        | `yay -Rns <paket>`            | Girdiğiniz pacman paketini, bağımlılıklarını ve yapılandırma dosyalarını(config) siler.  |
| `tam-güncelle`         | `sudo pacman -Syu && yay -Syu`| Tek komutla her paketi günceller.                                                        |
| `temizle`              | `rm -rf /var/cache/pacman/pkg && mkdir /var/cache/pacman/pkg` | Sistemdeki paketlerin eski sürümlerini siler.            |

## Kurulum
### 1. Gerekli bağımlılıkları indirin:

```bash
sudo pacman -S git
```

### 2. Depoyu indirin:

```bash
git clone https://github.com/npc-gnu/Tr-Terminal.git && cd Tr-Terminal
```

### 3. `indir` betiğini çalıştırın:

```bash
chmod +x indir && ./indir
```
### aur komutları için `yay` kurulumu
#### Not: AUR kullanmayacaksanız bu adımı uygulamanıza gerek yok.
1. Bağımlılıkları yükleyin

```bash
yönetici yükle --needed git base-devel
```

2. YAY kaynak kodunu indirin

```bash
git clone https://aur.archlinux.org/yay.git
cd yay
```

3. Derleme yapın

```bash
makepkg -si
``` 

### `durum` ve `hızlıdurum` komutları için
#### Yine `durum` / `hızlıdurum` komutlarını kullanmayacaksanız bu adıma gerek yok.
Tek adım: Paketleri yükleyin
```bash
yönetici yükle neofetch fastfetch
```

## Lisans

Bu proje [GNU Affero General Public License v3](https://www.gnu.org/licenses/agpl-3.0.html) (AGPLv3) lisansı ile lisanslanmıştır.
