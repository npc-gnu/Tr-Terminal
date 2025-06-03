# Tr-Terminal

## Tr-Terminalin amacı ne?

Tr-Terminal, bash betikleri ile GNU/Linux terminalini tamamen* Türkçe olarak kullanabilmenizi sağlar.

## Notlar:

Bash betikleri ile yazıldığı için fish/zsh vb. de çalışmaz.

*: tüm komutlar Türkçe değil ama düzenli olarak yeni komutlar eklemeye devam edeceğim.

Paket yükleme komutları sadece arch tabanlı sistemler içindir(pacman komutları).

## Komutlar

`durum` = `neofetch` , sistemizin özelliklerini ascii sanatıyla güzel bir şekilde gösterir.(neofetch yüklü olmalı)

`hızlıdurum` = `fastfetch` , neofetch'in daha hızlı çalışan hali.(fastfetch yüklü olmalı)

`kaldır` = `sudo pacman -Rs *paket* ` Arch sistemleri için paketleri ve bağımlılıklarını siler.

`kaldır-c` = `sudo pacman -Rns *paket* ` Arch sistemleri için paketleri, bağımlılıklarını ve config(ayar) dosyalarını siler.

`kapat` = `shutdown` , sistemi kapatır. Seçenekleri ingilizce girmeniz gerek(mesela `kapat now` demelisiniz, ama yakında düzelteceğim).

`kopyala` = `cp` , dosyaları kopyalamanızı sağlar.

`kullanıcıdeğiştir` = `su` , `kullanıcıdeğiştir *kullanıcıisimi* ` dediğinizde yazdığınız kullanıcıya geçer.

`sil` = `rm -rf` , dosyayı/dizini silmenizi sağlar.

`süreçler` = `htop` , sistemdeki süreçleri, çalışan yazılımları görüp kapamanızı, ne kadar işlemci/ram/ssd vb. kullanıyor görmenizi sağlar.

`taşı` = `mv` , dosyaları/dizinleri taşımanızı sağlar.

`yönetici` = `sudo` , işlemleri (başka bir seçenek belirtmediğiniz sürece) kök kullanıcı/root olarak çalıştırmanızı sağlar.

`yükle` = `pacman -S *paket* ` , paket indirmenizi sağlar.

## Yükleme

Yükleme için bir bash script henüz yazmadım (yakında yazacağım) ama şu anda kurulum için dosyaları:

/usr/local/bin'e kopyalayıp (buradaki adımlar yönetici yetkisi gerektiriyor!)
chmod +x ile çalıştırılabilir yapabilirsiniz.

Veya path değişkeninde başka herhangi bir dizine yazarsanızda olur.

## Lisans

Bu bash betiklerinin lisansı GNU is Not UNIX Affero General Public License version 3'dür.(AGPLv3)
