# Değişkenler nedir?

Değişken, bir değeri tutan bir addır. Değişken değerleri **sayılar (numbers)**, **Stringler**, **boolean**, **veri türleri (Data Types)** ve daha fazlası olabilir.

Değişkenleri kod içerisinde değiştirebildiğimiz için adı değişkendir.

# Değişkenlere isim vermek

Değişkenlere veremeyeceğiniz bazı değerler var, bunlar:

```lua
and
for
or
break
function
repeat
do
if
return
else
in
then
elseif
local
true
end
nil
until
false
not
while
```

Kullanmaya çalışırsanız kodunuz bozulur.

NOT: değişkenlerde yabancı karakterler **(ı,ü,ş,emoji, vb...)** kullanamazsınız. sadece ingilizce karakterler kullanılabilir.

verebileceğiniz değerlerden bazıları:

```lua
"Merhaba" --string değeri
1337 -- sayı değeri
50 + 20 -- sayı değeri (matematik)
false -- boolean değerler
true -- boolean değerler
Part.Position -- veri türü
```

hadi beraber değişkenleri kullanmaya geçelim.

## Kelimeleri birleştirmek

ilk önce değişkenlerimize "Merhaba" ve "Dünya" değerini vereceğiz.

```lua
local Kelime1 = "Merhaba"

local kelime2 = "Dünya!"
```
![image](https://github.com/user-attachments/assets/35b51142-540a-4e55-af85-721321f694d4)

şimdi print fonksiyonu ile bunları birleştirelim.

```lua
local Kelime1 = "Merhaba"

local kelime2 = "Dünya!"


print(Kelime1, kelime2)
```

![image](https://github.com/user-attachments/assets/b2fad712-26f1-4583-b6c4-b5ac5a495746)
![image](https://github.com/user-attachments/assets/0f95ced7-ca5b-481d-a34f-6ff7f0cbbc25)

## Matematik işlemi

matematik sembollerimiz
```lua
+ -- toplama
- -- çıkarma
* -- çarpma
/ -- bölme
```

![image](https://github.com/user-attachments/assets/7a7822de-30df-4cd2-8fe9-50f4aadc6099)
![image](https://github.com/user-attachments/assets/4b8f60b6-85d5-488b-a62b-8d295e5f19eb)

+ Peki sayı değeri ile string değerini aynı print fonksiyonu içerisinde kullanabilirmiyiz?
- Evet!

bunu yapmak için bu değerleri verelim, benle beraber yapın.

bunu yapmanın 2 yolu var, size ilk olarak benim kullandığım yolu göstereceğim.

## İlk yol

```lua
local isim = "Ahmet'in"

local yas = 18

print(isim, " yaşı: ", yas)
```

![image](https://github.com/user-attachments/assets/3e4e1b5d-117c-4928-a286-c4ccf45acfa0)
![image](https://github.com/user-attachments/assets/95c6618a-9f0b-46ba-8ca2-a7a523266eab)

## İkinci yol

```lua
local isim = "Ahmet'in"

local yas = 18

print(isim .. " yaşı: ".. yas) -- çıktımız  Ahmet'in yaşı: 18 olacak.
```

![image](https://github.com/user-attachments/assets/85ad94f7-0f3d-4c12-a4e7-302eef18e852)
![image](https://github.com/user-attachments/assets/cbef588f-92ee-4788-b619-73a094f76e83)

bunlarım farkı bazı boşluk sayısı ve basitliğidir. size göre hangisi daha basitse onla devam edin.

## Veri Türü

*burası kafanızı karıştırmasın, github sayfasında burayı anlattığım yer var.*

öncelikle Workspace'e bir part ekleyelim.

bunun rengini kırmızı yapacağım.

burada çıktımıza yazdırmak isteyeceğimiz şey, part'ın materyali, rengi, büyüklüğü ve pozisyonu. (kırmızı ile işaretlendi)

![image](https://github.com/user-attachments/assets/e77e7792-136a-4f01-87e8-1b6547cb7146)

 bunu yapmak için değişkenlerimize part'ın verisini tanımlayacağız.
 ### (tekrar söylüyorum kafanız karışmasın, github sayfamda her bir detay var ve eksik yerler eklenecektir. burdaki herşeyi anlatacağım.)

```lua
local part = game.Workspace.Part -- burada oluşturduğumuz part'ı değişkene tanımladık.

local partRengi = part.BrickColor -- part'ın rengini değişkenimize belirledik.

local partMateryali = part.Material -- part'ın materyalini değişkenimize belirledik.

local partBuyuklugu = part.Size -- part'ın boyutunu değişkenimize belirledik.

local partPozisyonu = part.Position --  part'ın konumunu değişkenimize belirledik.
```

hadi şimdi bunların değerlerini print() fonksiyonu ile yazdıralım.

```lua
local part = game.Workspace.Part -- burada oluşturduğumuz part'ı değişkene tanımladık.

local partRengi = part.BrickColor -- part'ın rengini değişkenimize belirledik.

local partMateryali = part.Material -- part'ın materyalini değişkenimize belirledik.

local partBuyuklugu = part.Size -- part'ın boyutunu değişkenimize belirledik.

local partPozisyonu = part.Position --  part'ın konumunu değişkenimize belirledik.

print(partRengi)

print(partMateryali)

print(partBuyuklugu)

print(partPozisyonu)
```

![image](https://github.com/user-attachments/assets/e3865ec4-07e1-493c-9646-8a913f64cf28)
![image](https://github.com/user-attachments/assets/b5aa75f2-646c-492c-9207-29a5d93b5b95)

gördüğünüz üzere değerlerimiz, part'ımızın değerleri ile aynı.
hadi bu kodu biraz daha geliştirelim!

```lua
local part = game.Workspace.Part -- burada oluşturduğumuz part'ı değişkene tanımladık.

local partRengi = part.BrickColor -- part'ın rengini değişkenimize belirledik.

local partMateryali = part.Material -- part'ın materyalini değişkenimize belirledik.

local partBuyuklugu = part.Size -- part'ın boyutunu değişkenimize belirledik.

local partPozisyonu = part.Position --  part'ın konumunu değişkenimize belirledik.

print("Part'ın rengi:", partRengi)

print("Part'ın materyali:", partMateryali)

print("Part'ın büyüklüğü:", partBuyuklugu)

print("Part'ın pozisyonu:", partPozisyonu)
```

![image](https://github.com/user-attachments/assets/a93afe7c-534f-4301-a1fa-e78e8db5da98)
![image](https://github.com/user-attachments/assets/953c430f-ce8f-44f9-98c4-3faa5aa7669e)


# Değişkenlerin değerini değiştirme.

adı üstünde, Değişken!

hadi bunu nasıl yapacağımızı öğrenelim.

iki değişken yapalım ilk önce, ilk değerimiz Ahmet, diğer değerimiz sayı değeri olsun (her türlü veri tipini değiştirebilirsiniz.)

daha sonra bunları print() komutu ile çıktısını yazdıralım.
daha sonra print komutumuzun altında bu değerleri değiştirelim ve print komutu ile çıktısını yazdıralım.

```lua
local isim = "Ahmet"
local yas = "15"

print(isim, yas) -- Ahmet 15 olarak yazdırılacak.


local isim = "Mehmet"
local yas = "69"

print(isim, yas) --  Mehmet 69 olarak yazdırılacak.
```

![image](https://github.com/user-attachments/assets/34bc752a-bf45-4852-afb5-dd7bfff04bc6)
![image](https://github.com/user-attachments/assets/970badb8-5731-4f0b-ab5d-2dfdbae5e5ce)

gördüğünüz üzere değişkenlere farklı değerler verdik, bu ileride işimize yarayacak.

## Çoklu değişkenlere, çoklu değer vermek. (tek bir satırda)

bunu yapmak gerçekten çok basit, örnek olarak göstereyim.

```lua
local isim, yas, memleket = "Ahmet", 18, "İstanbul"
```

hadi bunun çıktısını çıkaralım.

```lua
local isim, yas, memleket = "Ahmet", 18, "İstanbul"

print(isim, yas, memleket) -- sonucumuz Ahmet 18 İstanbul olacaktır.

print(memleket, yas, isim) -- sonucumuz İstanbul Ahmet 18 olacaktır.

print(memleket, isim, yas) --  sonucumuz İstanbul 18 Ahmet olacaktır.
```
![image](https://github.com/user-attachments/assets/e50e3e3b-5de5-415e-b9fd-c7894bfdf3c8)
![image](https://github.com/user-attachments/assets/7892c58d-edfd-413f-9ec3-6b45821ff95b)


kullanılan kaynaklar
https://create.roblox.com/docs/luau/variables
https://www.lua.org/pil/3.1.html
https://roblox.fandom.com/wiki/Print
