## Görev 1: Veri Temizleme ve Manipülasyonu

### 1. Hatalı Değerlerin Düzeltilmesi
- **"fiyat" ve "toplam_satis"** sütunlarındaki sayıya dönüştürülemeyen değerler tespit edilmiştir.
- **"toplam_satis"** sütunundaki hatalı girişler, **"fiyat"** ve **"adet"** çarpımıyla düzeltilmiştir.
- **"fiyat"** sütunundaki hatalı girişler, sütunun medyan değeriyle doldurulmuştur.

### 2. Aykırı Değer Analizi
Aşağıdaki sütunlar için aykırı değerler tespit edilmiştir:
- **Müşteri Yaşı (yas)**
- **Müşteri Harcama Miktarı (harcama_miktari)**
- **Satış Fiyatı (fiyat)**
- **Toplam Satış (toplam_satis_kontrol)**
- **Satış Adedi (adet)**

#### Aykırı Değer Analizinde Yapılan İşlemler:
- Her bir sütun için aykırı değerlerin sayısı belirlenmiştir.
- Alt ve üst sınırlar hesaplanmıştır.
- **Winsorization İşlemi**:
  - Alt ve üst sınırlar kullanılarak aykırı değerler belirli bir aralığa çekilmiştir.

---

## Görev 2: Zaman Serisi Analizi

- Verilen zaman serisi verisinde belirli haftalarda pik değerler ve düşüşler analiz edilmiştir.
- Pik noktalar ve düşüşlerin özellikleri belirlenmiş ve yorumlanmıştır.

---
