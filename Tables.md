# Tables

Table bir veri türü olaral adlandırılabilir. içine boolean, string, number, function değerleri gibi veriler kaydedebilirsiniz.

### Not: nil bu tablo içinde kullanılamaz.

# Array nedir?

array, bir dize olarak adlandılrılabilir. table verisinin içinde olur, bazı kullanıcı verileri gibi bilgileri kaydedebilirsiniz.

# Table nasıl oluşturulur?

gerçekten çok basittir. kodu aşağıya bırakıyorum.

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}
```

table içindeki dizeleri (Array) tanımlamak için {} sembolünü kullanmalısınız.

# Dizeleri (Arrays) primt çıktısı ile okumak

gerçekten çok basit. tüm dizeleri aynı anda çağırabilir, veya ayrı ayrı olarak çıktısını alabilirsiniz.

ilk olarak hepsini alalım.

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

print(ilkTable) -- çıktı "NATO", 1337 , false , "mavi" olacak
```

https://github.com/user-attachments/assets/96734970-7299-4aec-8db3-e626933be051

bunları ayrı ayrı seçmek için ikse print(TableAdı[array_sırası]) komutunu kullanacağız. işte kod

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

print(ilkTable[1]) -- çıktı sadece NATO olacak.
```

https://github.com/user-attachments/assets/125050b5-ba9b-4ad2-9adb-142d5b26257b

# Table'da ne kadar dize olduğunu öğrenmek

bunu yapmak için #TableAdı parametresini kullanacağız. bu table içindeki tüm dizeleri çıkarır ayrıca ileride bunla beraber table'a dize eklemeyi göstereceğim.
kodumuz tam olarak bu olacak

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

print(#ilkTable)  -- sonuç 4 çıkacak.
```

https://github.com/user-attachments/assets/099795b2-6a50-422b-b279-a244f5209674

# Table'a dize eklemek

bunu yapmanın iki yolu var;

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

table.insert(ilkTable, "Yeni bir dize") -- 1. yol
ilkTable[#ilkTable+1] = "Roblox Metadan daha iyi" -- 2. yol

print(ilkTable) -- dizeleri kontrol ediyoruz
```

1. yolda table.insert komutu kullandık ve daha sonra parametre olarak table'ımızın adını yazıp yanına 2. bir parametre olarak ne eklemek isteyeceğimizi yazacağız
2. yolda ise table adını yazıp yanına [#TableAd+1] ekliyoruz, bunun anlamı Table'a bir değer ekle demektir. sonra ne eklemek istediğimizi yazıyoruz.

kodun çıktısı

![image](https://github.com/user-attachments/assets/82e16383-9803-40b3-a585-ee4cefa7aac9)

ayrıca bu aşağoda vereceğim örnek senaryoda, eğer bu kodu kullanırsanız ve o dize sırasında bir dize varsa, o dizeyi bir sağa (+1 sıra) kaydırır.

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

table.insert(ilkTable,2, "Bu bir Testtir.") -- 1. yol

print(ilkTable) -- dizeleri kontrol ediyoruz 
```
![image](https://github.com/user-attachments/assets/d272cc33-c323-45a4-af6b-f49e22805e9a)

# Dize silmek

dize silmek için table.remove() komutunu kullanırız, örnek olarak; 2. bir dizeyi silmek istiyorsak bu kodu kullanırız

```lua
local ilkTable = {"NATO", 1337, false, "mavi"}

table.remove(ilkTable, 2)

print(ilkTable) -- dizeleri kontrol ediyoruz 
```
bu kod 1337 dizesini silecektir. çıktısı ise budur

![image](https://github.com/user-attachments/assets/eaa2ef8d-a26d-4c45-b3bf-4aacef985100)


# DEVAM EDECEK
