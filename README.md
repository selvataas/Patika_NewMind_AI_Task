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
