# Function nedir?

bir function (fonksiyon), belirli bir işlemi gerçekleştiren, bir dizi komut içeren kod bloğudur. Fonksiyonlar, tekrarlayan görevleri kolaylaştırmak ve kodun daha modüler, okunabilir ve yeniden kullanılabilir olmasını sağlamak için kullanılır.

iki şekilde yazılabilir.

## 1. yol

```lua
local nesne = script.Parent

local function dokundu()
  print("Bir şey bana dokundu!")
end

nesne.Touched:Connect(dokundu)
```
![image](https://github.com/user-attachments/assets/d439aab5-a807-40b5-9534-5b0228f175b8)


eğer kodumuzu çalıştırırsak bu çıktıyı verecektir.

https://github.com/user-attachments/assets/c316d357-3c3d-45ac-ac81-f847b66cbc01

## 2. yol

ikinci yol daha profosyonel ve basittir.

```lua
local nesne = script.Parent

nesne.Touched:Connect(function()
	print("Biri Bana Dokundu!")
end)
```

![image](https://github.com/user-attachments/assets/a80d4b59-320e-4a53-8692-2ce48e7082d3)


https://github.com/user-attachments/assets/bd43107c-2eda-4768-813a-edff097a26fe

# 2 yolun farkı nedir?

bu iki kod aslında aynı şeyi amaçlıyor, herhangi bir şey nesneye dokunursa çıktı yazdıracak

ama size 2. yolu öneriyorum çünkü daha basit ve daha profosyoneldir. karmaşıklığa sebep olmaz.

# Fonksiyonlara parametre vermek

mesela [UserInputServie.md](https://github.com/NATO4100/luau-turkce-dokumasyon/blob/main/UserInputService.md) makalemizde fonksiyona input parametresi verdik. her hizmetin farklı parametresi vardır, basitten başlamak istiyorum.

# Parametreler ile basit matematik

```lua
local function toplama(sayi1, sayi2)
	print(sayi1 + sayi2)
end

toplama(5, 10) -- sırasıyla sayi1 ve sayi2
```

![image](https://github.com/user-attachments/assets/eacde10e-81f6-44ad-898e-906ba2bedf54)


burada görmüş olduğunuz gibi parametremize sırasıyla değer verdik ve sonucumuz 15 çıktı.

# NATO, hizmetlerin parametlerini nasıl öğreneceğiz?

size elimden geldiğince göstereceğim, gösteremediklerimi  
https://create.roblox.com/docs/luau/   
https://create.roblox.com/docs/reference/engine    
sayfalarında bulabilirsiniz.

# KillBrick yapımı

öncelikle bunu sadece localscript ile yapabilirsiniz. 
ilk önce nesnemizi tanımlammalıyız
```lua
local nesne = script.Parent
```
![image](https://github.com/user-attachments/assets/f07d9de6-adf2-4b25-ae67-dc50b9af04d7)

daha sonra fonksiyon oluşturup içine isteğiniz bir parametreyi koyun, ben kimDokundu yapacağım.

```lua
local nesne = script.Parent

nesne.Touched:Connect(function(kimDokundu)
	
end)
```

kimDokundu'yu size az sonra açıklayacağım.

```lua
local nesne = script.Parent

nesne.Touched:Connect(function(kimDokundu)
	local Karakter = kimDokundu.Parent -- humanoid'i bulmamız için gerekli olan kod parçası
	local Humanoid = Karakter:FindFirstChildWhichIsA("Humanoid") -- Oyuncumuzun Humanoid (ruhu diyebilirsiniz)
	if Humanoid then
		Humanoid.Health = 0 -- ölmemize yarıyor bu kısım.
	end	
end)
```

şimdi kodu çalıştırmadan çnce teker teker size anlatacağım.

```lua
nesne.Touched:Connect(function(kimDokundu)
	local Karakter = kimDokundu.Parent -- humanoid'i bulmamız için gerekli olan kod parçası
	local Humanoid = Karakter:FindFirstChildWhichIsA("Humanoid") -- Oyuncumuzun Humanoid (ruhu diyebilirsiniz)
```
bu kısımda nesneyi fonksiyona bağladık ve fonksiyona kimDokuntu parametresini atadık, bu kısada nesneye dokunan kişiyi belirleyen bir kod, 3. satırda "local Karakter = kimDokundu.Parent" dokunan oyuncunun karakterinden humanoid'i (oyuncunun ruhu diyebiliriz) almamıza yarıyor "local Humanoid = Karakter:FindFirstChildWhichIsA("Humanoid")"

```lua
	if Humanoid then
		Humanoid.Health = 0 -- ölmemize yarıyor bu kısım.
	end	
```
bu kod satırında, eğer Humanoid bulursan, Humanoid.Health = 0 yap yani oyununun canını 0 yap demek oluyor. buda ölmemizi sağlıyor.

şimdi kodumuzu çalıştıralım.


https://github.com/user-attachments/assets/d1b66f27-571d-4064-8875-3b78dd555d18


