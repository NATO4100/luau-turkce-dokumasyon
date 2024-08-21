# UserInputService nedir?

**UserInputService**, bir kullanıcının cihazında bulunan farklı girdi türlerini tespit etmek ve yakalamak için kullanılan bir hizmettir.

**Bu hizmet sadece Client-Side içindir.**

şimdi sizinle beraber (evet benle beraber yapacaksınız.) bir proje yapalım. oyuncumun karşıdan karşıya geçebilmesi için "Q" harfine basarak köprüyü ortaya çıkarması gerek.

bunun için öncelikle proje ortamımızı yapalım.

![image](https://github.com/user-attachments/assets/6ff6011b-2a98-4efe-b687-722d85d832c0)
![image](https://github.com/user-attachments/assets/2e538758-c89d-481e-bc6f-0d050d16abbb)
![image](https://github.com/user-attachments/assets/71f6b9a1-f09e-43a1-907e-bba4d40db5d6)
![image](https://github.com/user-attachments/assets/dd85cac0-455f-472f-bfbb-b77386b0861c)
![image](https://github.com/user-attachments/assets/b6a1db8d-7a1d-4d4d-92d6-9e8dc2bc572d)

# Nasıl yapacağız?

ilk önce oluşturduğumuz localscript'in içine kizmeti kodumuza çağırmak için bu komutu kodumuza eklemeliyiz ilk önce:
```lua
local UserInputService = game:GetService("UserInputService")
```

kodumuza köprü'yi değişken olarak ekledikten sonra bir function oluşturmamız gerek.
şimdi size bir kod yazacağım ve bunu teker teker anlatacağım.

```lua
local UserInputService = game:GetService("UserInputService")
local kopru = game.Workspace:WaitForChild("kopru")  -- oyuncunuda köprü yüklenene kadar bekliyor.

UserInputService.InputBegan:Connect(function(input, gameProcessedEvent)
	if input.KeyCode == Enum.KeyCode.Q then
		print("Q harfine basıldı!")
		kopru.Transparency = 0
		kopru.CanCollide = true
	end
end)
```
işte kodumuz, şimdi anlatmaya geçelim.

```lua
local UserInputService = game:GetService("UserInputService")
local kopru = game.Workspace:WaitForChild("kopru")
```
burada değişkenlerimize değer verdik, birinci satırda UserInputService hizmetini oyunumuza çağırdık.
ikinci satırda ise köprümüzü tanımladık ama bu sefer WaitForChild("kopru") kullandık, çünkü localscript'i starterplayerscripts klasörüne attığımız için köprünün yüklenmesini beklemeliyiz.

```lua
UserInputService.InputBegan:Connect(function(input, gameProcessedEvent)
```
bu kod parçasında fonksiyon belirttik, bu kodun meali eğer kullanıcı tuşa basarsa ("UserInputService.InputBegan") fonksiyona bağla (*Connect(function(input, gameProcessedEvent)*), fonksiyonun içinde input ve gameProcessedEvent görüyorsunuz. size az sonra input'u anlatacağım, Roblox'ta InputBegan olayı ile çalışırken, **gameProcessedEvent**, girdinin oyunun dahili sistemleri tarafından işlenip işlenmediğini gösteren boolean bir parametredir. Eğer gameProcessedEvent false ise, bu girdinin başka bir sistem tarafından geçersiz kılınmadığı anlamına gelir (örneğin, sohbet girdisi, GUI etkileşimi) ve bunun gerçek bir kullanıcı girdisi olduğunu güvenle varsayabilirsiniz.

```lua
	if input.KeyCode == Enum.KeyCode.Q then
		print("Q harfine basıldı!")
		kopru.Transparency = 0
		kopru.CanCollide = true
	end
```
bu kod parçasında "if input.KeyCode == Enum.KeyCode.Q then" yani eğer input (yani tuş) Q ise, "Q harfine basıldı!" çıktısını ver ve köprüyü opak ve içinden geçilemez yap.
input burada bize tuşu belirtmemize yarıyor.

![image](https://github.com/user-attachments/assets/c82146ad-bdc8-433f-890e-43c3eac491b2)

### Hadi şimdi kodu çalıştıralım.

https://github.com/user-attachments/assets/7a1e1727-f6d3-4d7e-947e-5228c3fdc2ad

# Aynı örnek, farklı kod

şimdi, kullanıcı Q ye bastığında köprüden geçiyor, fakat Q harfine basmayı bıraktığında körü kaybulmuyor, bunu düzeltmek için bu kodu ekliyoruz.

```lua
UserInputService.InputEnded:Connect(function(input, gameProcessedEvent)
	if input.KeyCode == Enum.KeyCode.Q then
		print("Q harfi bırakıldı!")
		kopru.Transparency = 1
		kopru.CanCollide = false
	end
end)
```
bu kod için bilmeniz gereken tek şey "InputEnded" olacaktır, bu komut şunu belirtir, eğer kullanıcı Q harfine basmayı bıraktığı zaman köprüyü saydam ve içinden geçilir yap.

## Kodumuzun tam hali ve kodu çalıştırma

```lua
local UserInputService = game:GetService("UserInputService")
local kopru = game.Workspace:WaitForChild("kopru")  -- oyuncunuda köprü yüklenene kadar bekliyor.

UserInputService.InputBegan:Connect(function(input, gameProcessedEvent) -- Q harfine basılırsa olacak şeyler
	if input.KeyCode == Enum.KeyCode.Q then
		print("Q harfine basıldı!")
		kopru.Transparency = 0
		kopru.CanCollide = true
	end
end)

UserInputService.InputEnded:Connect(function(input, gameProcessedEvent) -- Q harfi bırakılırsa olacak şeyler
	if input.KeyCode == Enum.KeyCode.Q then
		print("Q harfi bırakıldı!")
		kopru.Transparency = 1
		kopru.CanCollide = false
	end
end)
```

![image](https://github.com/user-attachments/assets/12cffdcc-76c9-41c2-837c-2952aa14d12d)

https://github.com/user-attachments/assets/dc73657e-0c9d-4f56-8e65-7088de63216e

kullanılan kaynaklar

https://create.roblox.com/docs/reference/engine/classes/UserInputService
https://create.roblox.com/docs/reference/engine/classes/UserInputService#InputBegan
