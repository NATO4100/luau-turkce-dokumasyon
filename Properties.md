# Nedir bu Properties? Neden Önemliler?

Merhaba, Roblox Studio'da birkaç saat geçirdiyseniz Properties[1] menüsünü farketmiş olabilirsiniz.
Bunlar oyuna eklediğiniz herhangi bir şeyin özelliğini değiştirmenize yarar, ister manuel, ister kod ile değiştirin. 

Ama biz bu github sayfasında herşeyi kod ile değiştirmeyi öğreneceğiz.

## NATO, tamam ama ne işimize yarayacak bu menü?

bu menü emin olun bu github sayfasında her yerde karşınıza çıkacak, eğer part çıkardıysak onun saydamlığını, rengini ve her türlü özelliğini değiştirebilirsiniz.

## Çok fazla terim var, nasıl ezberleyeceğim?

ezberlemenize gerek yok (şimdilik), Properties menüsünde her terim yazmakta, eğer nasıl yazıldığını unutursanız o menüden bakabilirsiniz.

https://github.com/user-attachments/assets/e33039b5-125b-4146-87f0-5a99dce86e99

## Kod ile Part'ın rengini değiştirmek

bunun için Color3.new komutunu kullanacağız.

Bunu yapmak için ilk önce workspace'imize bir parça ekleyelim, bu parçanın adını ilkParcam olarak değiştireceğim, siz pratik yapmak için farklı bir ad koyabilirsiniz.

https://github.com/user-attachments/assets/2ca5afa2-e9fe-4bd2-8f7d-ef82f987f089

şimdi kod kısmına geçebiliriz.

part'a children olacak şekilde script ekliyorum, daha sonra bu kodu yazıp oyunu başlatacağım.

```lua
local ilkParcam = script.Parent

ilkParcam.Color =  Color3.new(0.537255, 0.278431, 0.545098) -- part'ımıza renk değeri verdik.
```

![image](https://github.com/user-attachments/assets/cdcc843d-9d90-4a2b-bf1f-087c7151a1e1)

oyunu başlatırsak bu sonucu elde edeceğiz.

https://github.com/user-attachments/assets/22302454-2fbf-4767-8a64-895f33765772

## Part'ın saydamlık değerini değiştirmek

0 - 0.5 arası cam olur
0.5 - 1 arası görünmez olur

başlarda karıştırabilirsiniz.

kodu fazla değiştirmeyip, sadece bunu ekleyeceğim.

```lua
local ilkParcam = script.Parent

ilkParcam.Transparency = 0.5
```

![image](https://github.com/user-attachments/assets/9e0e16a4-2c81-4995-8ab3-4a27c2aaaf00)

https://github.com/user-attachments/assets/ece798ab-61d2-4003-822f-1ad15514068e

## Part'ın boolean özelliklerini değiştirmek

Eğer kutu tik ise, bu True demektir.
Eğer boş ise, bu false demektir

![image](https://github.com/user-attachments/assets/5003d6dc-a0c2-4885-ba6d-d7b4866b8869)


sadece sayılar ile özelliklerini değiştirmiyoruz, false veya true olarakta değiştirebiliriz, örnek olaral;

part'ın içinden geçmek istiyorsak "**CanCollide**" özelliğini false yapmamız gerek, ama varsayılan olarak bu true gelir.
bunu manuel olarak değiştirebiliriz ama bazı senaryolarda bunu kod ile yazmak işimize yaratacaktır.

```lua
local ilkParcam = script.Parent

ilkParcam.CanCollide = false
```

https://github.com/user-attachments/assets/076024ef-e82f-41d3-a02a-0747a17ac3cc

## Part'ın büyüklüğünü değiştirmek

bunu yapmak için Vector3.new komutunu kullanacağız.
Vector3.new(X,Y,Z) şeklindedir.

![unity-axis-with-rotation](https://github.com/user-attachments/assets/7c67abda-b4b7-4097-b868-33709e18191e)


```lua
local ilkParcam = script.Parent

ilkParcam.Size = Vector3.new(2,2,2)
```

![image](https://github.com/user-attachments/assets/78f798c7-17ae-4c21-bc49-5242737ba2c4)

https://github.com/user-attachments/assets/c3c7731c-e946-497f-ba3f-3dcbc049d15e

## Part'ın ismini değiştirmek

Son kısmım, part'ın ismini değiştirmek, bu oldukça kolaydır, string değeri kullanacağız

```lua
local ilkParcam = script.Parent

ilkParcam.Name = "Türkiye"
```


https://github.com/user-attachments/assets/b4b946d5-aa82-410f-9d7e-727dc6506d49



[1] Properties: https://prnt.sc/9135aN2nx-CQ

kullanılan kaynaklar
https://docs.unity3d.com/uploads/Main/unity-axis-with-rotation.png
https://docs.unity3d.com/Manual/QuaternionAndEulerRotationsInUnity.html
