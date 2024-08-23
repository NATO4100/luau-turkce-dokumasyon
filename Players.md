# Players hizmeti nedir

adındanda anlaşıacağı üzere, oyuncuları hedefleyen bir servistir. client'e bağlanan tüm oyuncuları içerir.

## Nelerde kullanabiliriz?

- oyuncu'nun humanoid'ine ulaşabiliriz. (client side için geçerlidir)
- Oyuncunun lokasyonu bulunabilir.
- oyuncunun hesabının kaç gündür açık olduğu bulunabilir.
- Ban tarihine bakılabilir.
- Herhangi bir oyuncunun sunucuya girip girmediği öğrenilebilir ve fonksiyon verilebilir.
- Oyuncu oyundan çıktığı zaman görülebilir ve fonksiyon bağlanılabilir.
- vb...

yani işlevi çoktur.

# Humanoid'i değişken olarak tanımlamak

StarterPlayerScripts'e bir adet localscript koyarak başlıyoruz.

![image](https://github.com/user-attachments/assets/3001bf41-068d-4fae-8a4e-a89040d2993b)

daha sonra kodumuza players hizmetini çağırıp localplayer'ı tanımlayıp Character child'ine ulaşıp ordan humanoid'e ulaşacağız **(zor gibi görünebilir ama çok kolay)**

işte kodumuz

```lua
local Players = game:GetService("Players") -- Players hizmetini çağırdık

local LocalPlayer = Players.LocalPlayer -- Players hizmetinden LocalPlayer child'ini aldık

local Characters = LocalPlayer.Character -- LocalPlayer'in karakterini aldık

local Humanoid = Characters:FindFirstChildWhichIsA("Humanoid")  --  Karakter içinde Humanoid bulmak için bir kod
```
# kodu yarın anlatacağım, 40 saate yakın bir süredir uyumadım. iyi geceler.
#
