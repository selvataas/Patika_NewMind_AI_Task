## Görev 1: Veri Temizleme ve Manipülasyonu

### 1. Hatalı Değerlerin Düzeltilmesi
- **"fiyat" ve "toplam_satis"** sütunlarındaki sayıya dönüştürülemeyen değerler tespit ettim.
- **"toplam_satis"** sütunundaki hatalı girişler, **"fiyat"** ve **"adet"** çarpımıyla düzelttim.
- **"fiyat"** sütunundaki hatalı girişler, sütunun medyan değeriyle doldurdum.

### 2. Aykırı Değer Analizi
Aşağıdaki sütunlar için aykırı değerleri tespit ettim:
- **Müşteri Yaşı (yas)**
- **Müşteri Harcama Miktarı (harcama_miktari)**
- **Satış Fiyatı (fiyat)**
- **Toplam Satış (toplam_satis_kontrol)**
- **Satış Adedi (adet)**

#### Aykırı Değer Analizinde Yapılan İşlemler:
- Her bir sütun için aykırı değerlerin sayısını belirledim.
- Alt ve üst sınırlar hesapladım.
- **Winsorization İşlemi**:
  - Alt ve üst sınırlar kullanılarak aykırı değerler belirli bir aralığa çektim.

---

## Görev 2: Zaman Serisi Analizi

- Verilen zaman serisi verisinde belirli haftalarda pik değerler ve düşüşler analiz ettim.

  ![Haftalık Satış Trendi](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Haftal%C4%B1k%20Sat%C4%B1%C5%9F%20Trendi%20-%20Pik%20ve%20D%C3%BC%C5%9F%C3%BC%C5%9F%20Noktalar%C4%B1.png)

- Hareketli Ortalama ile Trend: Kısa vadeli dalgalanmaları yumuşatmak için hareketli ortalamaları kullanarak uzun vadeli trendleri analiz ettim.
  
  ![Hareketli Ortalama ile Trend](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Hareketli%20Ortalama%20ile%20Haftal%C4%B1k%20Sat%C4%B1%C5%9F%20Trendi.png)

- Kategorilere göre gruplama ve haftalık satışların hesaplandım. NaN değerleri 0 ile dolduralım (eğer bir kategoride o hafta satış yapılmamışsa)
  
 ![Kategorilere göre gruplama ve haftalık satışlar](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Haftal%C4%B1k%20Kategori%20Sat%C4%B1%C5%9F%20Trendleri.png)

- En Popüler 3 Kategorinin Haftalık Satış Trendleri
  
  ![En Popüler 3 Kategorinin Haftalık Satış Trendler](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/En%20Pop%C3%BCler%203%20Kategorinin%20Haftal%C4%B1k%20Sat%C4%B1%C5%9F%20Trendleri.png)

 - Aylık Veri Oluşturma
   
     ![Aylık Toplam Satış Trendi](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Ayl%C4%B1k%20Toplam%20Sat%C4%B1%C5%9F%20Trendi.png)
   
- En Çok Satan 3 Ürün - Aylık Satış Trendleri

  ![En Çok Satan 3 Ürün - Aylık Satış Trendleri](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/En%20%C3%87ok%20Satan%203%20%C3%9Cr%C3%BCn%20-%20Ayl%C4%B1k%20Sat%C4%B1%C5%9F%20Trendleri.png)

  #### pd.Grouper kullanarak ay bazında gruplayıp, her ay için ilk ve son satış gününü buldum. Her hafta satılan toplam ürün miktarını bulmak için:

   ![Her hafta satılan toplam ürün miktarı](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Haftal%C4%B1k%20Sat%C4%B1lan%20%C3%9Cr%C3%BCn%20Adedi.png)

  #### Zaman serisindeki trendler:
  - Mavi: Negatif değişimi (düşüş) ifade eder. Kırmızı: Pozitif değişimi (artış) ifade eder.

    ![Aylık Toplam Satışlar - Değişimi](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/Ayl%C4%B1k%20Toplam%20Sat%C4%B1%C5%9Flar.png)
    
---

## Görev 3: Kategorisel ve Sayısal Analiz 

### Ürün kategorilerine göre toplam satış miktarı ve her kategorinin tüm satışlar içindeki oranı: 

Elektronik kategorisi toplam satışların %48.6'sını oluşturuyor.Bu, bu kategorinin toplam satış üzerinde önemli bir paya sahip olduğunu gösteriyor. Ev Aletleri ve Giyim kategorileri sırasıyla %9.89 ve %10.42'lik paylarla daha düşük oranlarda satış yapıyor. Kırtasiye ve Mutfak Ürünleri kategorileri de sırasıyla %20.8 ve %10.25 oranlarında katkı sağlıyor. Bu tablo, satış miktarının büyük kısmının "Elektronik" kategorisinde olduğunu ve her kategorinin toplam satış içindeki yüzdesini göstermektedir.

### Müşterilerin yaş gruplarına göre satış eğilimleri: 

Farklı yaş gruplarının toplam satışlar içindeki oranları analiz edilmiştir. Satışlar, yas_grubu (yaş grubu) bazında gruplandırılmış ve her yaş grubunun toplam satışlardaki payı hesaplanmıştır.

- 50+ yaş grubu en yüksek satışa sahip olup, toplam satışların %37.66’sını oluşturmuştur.
- 36-50 yaş grubu, %29.84'lük oranla ikinci sırada yer almaktadır.
- 26-35 yaş grubu toplam satışların %18.21'ini gerçekleştirirken, 18-25 yaş grubu en düşük satış oranına sahip olup, satışların %14.29’unu gerçekleştirmiştir.
- Özellikle 50+ yaş grubu, satışlar açısından önemli bir segment olup, pazarlama stratejilerinin bu yaş grubuna yönelik güçlendirilmesi gerektiği anlaşılmaktadır.

### Kadın ve erkek müşterilerin harcama miktarları ve harcama davranışları arasındaki farkı:
- Kadınların toplam harcaması, erkeklere kıyasla daha yüksektir. Bu, kadınların toplamda daha fazla harcama yaptığına işaret eder. Kadınlar toplamda daha fazla harcama yapmış, bu farkın büyük bir kısmı kadın sayısının erkeklerden fazla olmasıdır. Ortalama harcama değerlerine baktığımızda, kadınların başına düşen harcama erkeklere göre biraz daha yüksek. Ancak bu fark, oldukça küçüktür ve sadece 29,2 TL'lik bir fark vardır.
  
---

#### Görev 4: İleri Düzey Veri Manipülasyonu

- Şehirlerin sıralamasını, en çok harcama yapan müşterilere göre görebiliriz.
- Bölgesel Farklar: Adana, Bursa ve Konya gibi şehirlerde daha büyük harcamalar gözlemleniyor. Bu durum, bu şehirlerdeki belirli müşteri segmentlerinin veya ekonomik faaliyetlerin farklı olduğuna işaret edebilir. Bu şehirlerdeki yüksek harcamalar, belirli bir müşteri kitlesinin güçlü alım gücünü gösterebilir.
- Büyük Şehirlerin Durumu: İstanbul, İzmir, Antalya ve Ankara gibi büyük şehirlerdeki en yüksek harcama rakamları daha düşük. Bu şehirlerde genellikle daha fazla müşteri bulunduğu için, en yüksek harcama yapan müşteri sayılarının daha geniş bir gruptan geldiği düşünülebilir. Bu da, şehirdeki yoğunluk nedeniyle en fazla harcama yapan müşteri tutarlarının daha düşük olmasını açıklayabilir.

### Satış verisinde her bir ürün için ortalama satış artışı oranı:

Pozitif Değerler: Satışlarda genel bir artış trendini gösterir. Örneğin, P024 kodlu ürünün ortalama artışı %16.17.

Negatif Değerler: Satışlarda düşüş trendini gösterir. Örneğin, P018 kodlu ürünün ortalama değişimi %-2.01.

### Pandas groupby ile her bir kategorinin aylık toplam satışları

 ![ Pandas groupby ile her bir kategorinin aylık toplam satışları](https://github.com/selvataas/Patika_NewMind_AI_Task/blob/master/indir.png)
 
---

#### Görev 5: Ekstra 

Tahmin Modeli:

- tarih sütunu, pd.to_datetime fonksiyonu ile datetime formatına dönüştürülmüştür.
- Yaş bilgisi kategorik bir değişken haline getirilerek modelde kullanılabilir hale getirilmiştir.
- Modelin anlayabilmesi için kategorik değişkenlerin sayısallaştırdım:  Kategorik değişkenler (kategori, ürün_adi, cinsiyet, sehir), one-hot encoding yöntemiyle sayısal forma dönüştürülmüştür.
- Özellik ve Hedef Değişkenlerin Hazırlanması:
   Sayısal sütunlar: yıl, ay, fiyat, adet, yas, harcama_miktari.
   One-hot encoding ile oluşturulan sütunlar: kategori_, ürün_adi_, cinsiyet_, sehir_ içeren sütunlar dinamik olarak eklenmiştir.
