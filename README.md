# Tr-Terminal

## Tr-Terminal Nedir?

**Tr-Terminal**, GNU/Linux terminalini *neredeyse tamamen* Türkçe kullanabilmenizi sağlayan bash betiklerinden oluşan bir projedir.

## Özellikler ve Notlar

- Bash betikleriyle yazıldığı için yalnızca `bash` kabuğunda çalışır. `fish`, `zsh` gibi alternatif kabuklarla uyumlu değildir.  
- *"Tamamen" Türkçe demek tam doğru olmaz; tüm komutlar Türkçeye çevrilmedi. Ancak düzenli olarak yeni Türkçe komutlar eklenmeye devam edecek.*
- Paket yönetimi ile ilgili komutlar yalnızca Arch tabanlı sistemlerde (örneğin: Manjaro, EndeavourOS) çalışır (`pacman` kullanır).

## Komutlar

| Türkçe Komut          | Karşılığı                     | Açıklama |
|------------------------|-------------------------------|----------|
| `durum`                | `neofetch`                    | Sistemin temel bilgilerini ASCII sanatıyla gösterir. `neofetch` yüklü olmalıdır. |
| `hızlıdurum`           | `fastfetch`                   | `neofetch`'in daha hızlı çalışan alternatifi. `fastfetch` yüklü olmalıdır. |
| `kaldır`               | `sudo pacman -Rs <paket>`     | Paketi ve artık kullanılmayan bağımlılıklarını kaldırır. |
| `kaldır-c`             | `sudo pacman -Rns <paket>`    | Paketi, bağımlılıklarını ve yapılandırma dosyalarını kaldırır. |
| `kapat`                | `shutdown`                    | Sistemi kapatır. (Şimdilik `kapat now` gibi İngilizce parametrelerle kullanılmalı.) |
| `kopyala`              | `cp`                          | Dosya veya dizinleri kopyalar. |
| `kullanıcıdeğiştir`    | `su`                          | Belirttiğiniz kullanıcıya geçiş yapar. |
| `sil`                  | `rm -rf`                      | Dosya veya dizinleri siler. (Dikkatli kullanın!) |
| `süreçler`             | `htop`                        | Sistem süreçlerini izleyebilir, işlemleri sonlandırabilirsiniz. |
| `taşı`                 | `mv`                          | Dosya veya dizinleri taşır. |
| `yönetici`             | `sudo`                        | Komutu yönetici (root) yetkileriyle çalıştırır. |
| `yükle`                | `sudo pacman -S <paket>`      | Paket yüklemenizi sağlar. |

## Kurulum

Henüz bir kurulum betiği mevcut değil (yakında eklenecek). Şimdilik elle kurulum yapabilirsiniz:

1. Betik dosyalarını `/usr/local/bin` dizinine kopyalayın.  
   (Bu adım için `sudo` gereklidir.)
2. Her betik için çalıştırılabilir izin verin:
   ```bash
   sudo chmod +x /usr/local/bin/<komut_adı>
   ```
3. Alternatif olarak, `$PATH` içinde olan başka bir dizini de kullanabilirsiniz.

## Lisans

Bu proje [GNU Affero General Public License v3](https://www.gnu.org/licenses/agpl-3.0.html) (AGPLv3) lisansı ile lisanslanmıştır.
