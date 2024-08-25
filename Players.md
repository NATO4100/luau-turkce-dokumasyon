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

burada oyuncunun Humanoid'ini bulduk. Humanoid ile oyuncunun hızı, zıplama seviyesi, dokunduğu şeyi tetikleme, animasyonları vb.. şeyleri ayarlayabiliriz.

# Oyuna giren/çıkan kişileri algılamak

bunu Players.PlayerAdded/Players.PlayerRemoving ile yapabilirsiniz ve fonksiyona bağlayabilirsiniz. Server Script'imizi **ServerScriptService**'a koyup bu kodu yazacağız.
```lua
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(oyuncu) -- oyuncunun oyuna girip girmediğini kontrol eder
  print(oyuncu, "isimli oyuncu oyuna girdi") -- eğer oyuncu oyuna girerse bu çıktıyı verir.
end)
```

![image](https://github.com/user-attachments/assets/8bd3a594-0006-4edc-ade7-fecb377d1bfc)

çıktığını algılamak için ise bu kod yazacağız.

```lua
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(oyuncu) -- oyuncunun oyuna girip girmediğini kontrol eder
	print(oyuncu, "isimli oyuncu oyuna girdi") -- eğer oyuncu oyuna girerse bu çıktıyı verir.
end)

Players.PlayerRemoving:Connect(function(oyuncu) -- oyuncunun oyuna çıkıp çıkmadığını kontrol eder
	print(oyuncu, "isimli oyuncu oyundan çıktı") -- eğer oyuncu oyuna çıkarsa bu çıktıyı verir.
end)
```
  
https://github.com/user-attachments/assets/e91b0fd4-38d4-4181-8016-9d1105a749eb


