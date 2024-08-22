# Nedir bu Vector3?

Vector3, X, Y, Z olarak tanımlanan değerleri değiştirmenize yarayan bir komuttur.

![image](https://github.com/user-attachments/assets/a38185ba-9c07-4461-80ae-e949f9c8b11e)

X: sağ-sol   
Z: ön-arka  
Y: yukarı-aşağı  
olmak üzere tanımlanılabilir.

Vector3 ile değiştirebileceğimiz şeyler, Position (Posizyon), Size (Büyüküklük) gibi X, Y, Z içeren herşey.

![image](https://github.com/user-attachments/assets/720774dd-9471-48b9-9771-edeaa8c30537)

# Vector3 ile nesnenin boyutunu değiştirmek

Bir nesnenin boyutunu değiştirmek için, bu kodu kullanabiliriz.

```lua
local nesne = script.Parent -- nesnemiz

nesne.Size = Vector3.new(10,10,10) -- (x,y,z) 10x10x10 bir parça elde ettik.
```

https://github.com/user-attachments/assets/2e2ec745-6c94-4187-bb07-16cbb8be8bf7

burada gördüğünüz gibi nesnemizin şeklini değiştirdik.

# Matematik ve Vector3

evet, her programlama dilinde matematik vardır.

## Matematik İşlemleri

şimdi bu kodu aklınızda bulundurun.
```lua
local vectorDegeri = Vector3.new(10,2,5)
```

### Toplama:

```lua
vectorDegeri + vectorDegeri -- sonuç Vector3.new(20,4,5) olur.
```
İki değerin x,y,z değerleri toplanarak ortaya çıkan bir Vector3 üretir.

### Çıkarma

```lua
vectorDegeri - vectorDegeri -- sonuç Vector3.new(0,0,0) olur.
```
İki değerin x,y,z değerleri çıkarılarak ortaya çıkan bir Vector3 üretir.

### Çarpma

```lua
vectorDegeri - vectorDegeri -- sonuç Vector3.new(400,16,25) olur.
```
İki değerin x,y,z değerleri çarpılarak ortaya çıkan bir Vector3 üretir.

### Bölme

```lua
vectorDegeri - vectorDegeri -- sonuç Vector3.new(1,1,1) olur.
```
İki değerin x,y,z değerleri bölerek ortaya çıkan bir Vector3 üretir.

### Çarpma 2

```lua
vectorDegeri * 2 -- sonuç Vector3.new(40,8,10) olur.
```
2. sayı değeri (2) tüm x,y,z değerlerini çarparak sonucu ortaya çıkarır.

### Bölme 2

```lua
vectorDegeri / 2 -- sonuç Vector3.new(10,2,2.5) olur.
```
2. sayı değeri (2) tüm x,y,z değerlerini bölerek sonucu ortaya çıkarır.

kullanılan kaynaklar   
https://create.roblox.com/docs/reference/engine/datatypes/Vector3
