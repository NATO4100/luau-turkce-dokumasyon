# TextButton nedir?

TextLabel'e benzer bir yapıdır, içine yazı yazıp buton olarak kullanabiliriz.
Tabiki de bunu tıkladığımızda birşeyi aktif edeğilmemiz için kod satırları yazmamız gerekiyor. şunu unutmayın, geliştirici olacaksanız programlamadan kaçamazsınız. *(veya zengin bir aileden geliyorsanız ayak işlerinizi başka programcılara yaptırabilirsiniz.)*

# TextButton nasıl kullanılır?

ilk öncelikle StarterGui hizmetine ScreenGui ekleyip children olacak şekilde TextButton ekleyeceğiz.


https://github.com/user-attachments/assets/70af06fd-87ff-4e91-82e0-da245cbc8233

ekranda göreceğiniz üzere beyaz bir şey çıktı, bunu istediğiniz bir şekile, yazı boyutuna getirip ekranın bir yerine koyun.

![image](https://github.com/user-attachments/assets/5b18066c-95b1-4424-952c-296ddafb815f)

# Butona fonksiyon belirlemek

şöyle bir şey hayal edelim, biz adminiz, butona tıkladığımızda herkesin output penceresince "İyi Oyunlar" demek istiyoruz. bunu yapmak için server script kullanacağız.

![image](https://github.com/user-attachments/assets/102c24e1-b395-4c93-803b-7616ed98bc4c)

## MouseButton1Click

```lua
local buton = script.Parent -- butonumuzu tanımladık

buton.MouseButton1Click:Connect(function()
	
end)
```
MouseButton1Click, eğer butona mouse'un sol dişi tıklama yaptığımızı algılar. bununla ilgili örnekler göstereceğim.

![image](https://github.com/user-attachments/assets/4f4c35a3-13a0-4437-86d7-0842feff24b0)

butona tıkladığımda server taradında herkese "Merhaba Dünya!" çıktısı gönderilecektir. server ve client arasındaki farkı bilmiyorsanız bu makalemi okuyun [Client ve Server](https://github.com/NATO4100/luau-turkce-dokumasyon/blob/main/client%20ve%20server.md).


https://github.com/user-attachments/assets/4b08ac3c-44cf-4377-8984-95c933f792a4

## MouseButton2Click

### MouseButton2Click, MouseButton1Click ile aynıdır. örneklendirmeye gerek yok, sadece mouse'un sağ dişi ile etkileşime giriyorsunuz.

## MouseEnter

Bu komut, eğer mouse'muz gui elementinin içine giderse tıklama gerektirmeden kodumuzu çalıştıracaktır.

```lua
local buton = script.Parent -- butonumuzu tanımladık

buton.MouseEnter:Connect(function()
	print("Merhaba dünya")
end)
```

https://github.com/user-attachments/assets/60a5488b-f6bd-42e2-80b7-2d7129d9a227

# devam edecek.
