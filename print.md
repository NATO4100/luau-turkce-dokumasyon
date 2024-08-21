# Print() nedir?

## not: bazı terimlere hakim değilseniz endişelenmeyin, tüm terimlerin github sayfasında bilgisi verilmiştir, aktif olarak güncellenecektir.

**print()** fonksiyonu, Lua programlama dilinde kullanıcıya veya geliştiriciye bir mesaj iletmek için kullanılır. Roblox Studio'da bu fonksiyon, kodunuzun belirli noktalarında ne olup bittiğini anlamanızı sağlayan bir araç olarak sıklıkla kullanılır. Bu fonksiyon, kod içinde belirlenen mesajları **"Output"** penceresine[^1] yazdırır. Böylece, kodun nasıl çalıştığını ve beklenen sonuçları verip vermediğini kolayca kontrol edebilirsiniz.

Ayrıca, oyun içinde **F9** tuşuna basarak açabileceğiniz geliştirici konsolunun **"Client-side" (istemci tarafı)** bölümünde de bu çıktıları görebilirsiniz. Bu özellik, özellikle **hata ayıklama (debugging)** sırasında oldukça faydalıdır. **print()** fonksiyonu, bir oyunun istemci tarafında çalıştığında, o istemciye özgü bilgileri de gösterebilir, bu sayede farklı oyuncular için ayrı ayrı çıktılar üretilmesi mümkündür.

# Print() fonksiyonunun Kullanımı

**print()** fonksiyonuna farklı türlerde veri tipleri verebilirsiniz. İşte **string (metin)**, **number (sayı)**, **boolean (mantıksal değer)** ve **değişken değerleriyle** nasıl kullanılacağına dair örnekler:

## String Değeri

```lua
print("Merhaba, dünya!")
```
```lua
print('Merhaba, dünya!')
```

(iki sembol aynı sonucu verecektir, farklarını ileride anlatacağım.)

![image](https://github.com/user-attachments/assets/59da3287-c48a-4b9b-99b9-938abb4de350)
![image](https://github.com/user-attachments/assets/406b274d-6945-44c2-ad35-f5feee41cb4d)

```lua
print([["Merhaba, 
dünya!"]])
```

![image](https://github.com/user-attachments/assets/e43bebab-3ef3-4186-ad7f-765a08a7fccf)
![image](https://github.com/user-attachments/assets/11e46fd4-41e0-43b7-9d04-60f155de8ff9)



## Sayı Değeri

![image](https://github.com/user-attachments/assets/e8dd5daa-bff5-4e01-918f-8b53ab99b139)
![image](https://github.com/user-attachments/assets/17b377d4-1eee-45dd-b930-3656c88d3b4e)

## Boolean Değeri

![image](https://github.com/user-attachments/assets/3699fe31-f2fc-49f0-8d0f-3a30c4b2ca6d)
![image](https://github.com/user-attachments/assets/c286f124-b74e-4a26-aec9-690a15246868)

## Değişken Değeri

![image](https://github.com/user-attachments/assets/6c7c4e96-5cab-43d5-9266-41a33bb77c1f)
![image](https://github.com/user-attachments/assets/7a3184e9-fbc2-4aad-843d-974a9a3896b6)


[^1]: (https://prnt.sc/8XfN4NXw9ySb), (https://prnt.sc/gNoEjGcNCWoE)

