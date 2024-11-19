# Veri Analizi ve Manipülasyonu Ödevi

Bu proje, karmaşık veri manipülasyonu, veri temizleme ve analiz becerilerini geliştirmek amacıyla hazırlanmıştır. Ödev, çeşitli zorluk seviyelerinde alt görevler içeren bir veri analizi sürecini kapsamaktadır. Satış ve müşteri verileri üzerinde çeşitli analizler yaparak veri seti üzerinde manipülasyonlar gerçekleştirilecektir.

## Gerekli Kütüphaneler
- **Pandas**: Veri analizi ve manipülasyonu için.
- **NumPy**: Matematiksel işlemler için.
- **Matplotlib/Seaborn**: Görselleştirme için.

## Veri Setleri
Proje için kullanılan veri setleri:
1. **Satış Verisi**: Her bir satırda farklı ürünlerin satıldığı veri seti.
   - Örnek kolonlar: `tarih`, `ürün_kodu`, `ürün_adi`, `kategori`, `fiyat`, `adet`, `toplam_satis`
   
2. **Müşteri Verisi**: Müşterilerle ilgili verileri içerir.
   - Örnek kolonlar: `musteri_id`, `isim`, `cinsiyet`, `yas`, `sehir`, `harcama_miktari`

## Görevler

### Görev 1: Veri Temizleme ve Manipülasyonu (%25)
- Eksik veriler ve aykırı (outlier) veriler analiz edilip temizlenecek.
- Eksik veriler ortalama, medyan gibi yöntemlerle tamamlanacak.
- Fiyat ve harcama gibi değişkenler için aykırı değerler tespit edilip uygun şekilde ele alınacak.
- Müşteri verisi ile satış verisi, `musteri_id` üzerinden birleştirilerek geniş bir veri seti oluşturulacak.

### Görev 2: Zaman Serisi Analizi (%25)
- Satış verisi üzerinde haftalık ve aylık bazda toplam satış ve ürün satış trendleri analiz edilecek.
- Tarih sütununu kullanarak her ayın ilk ve son satış günleri bulunacak.
- Haftalık ürün satışları hesaplanacak.
- Satış trendlerini tespit etmek için grafikler çizilecek (aylık satış artışı veya düşüşü gibi).

### Görev 3: Kategorisel ve Sayısal Analiz (%25)
- Ürün kategorilerine göre toplam satış miktarı ve her kategorinin tüm satışlar içindeki oranı hesaplanacak.
- Müşterilerin yaş gruplarına göre satış eğilimleri analiz edilecek.
- Kadın ve erkek müşterilerin harcama miktarları karşılaştırılacak ve harcama davranışları arasındaki farklar tespit edilecek.

### Görev 4: İleri Düzey Veri Manipülasyonu (%25)
- Müşterilerin şehir bazında toplam harcama miktarları hesaplanacak ve şehirler en çok harcama yapanlara göre sıralanacak.
- Her bir ürün için ortalama satış artış oranı hesaplanacak. Bu oran, önceki aya göre satış değişim yüzdesiyle belirlenecek.
- Pandas `groupby` fonksiyonu ile her kategori için aylık toplam satışlar hesaplanacak ve değişim oranları grafikle gösterilecek.

### Görev 5: Ekstra (BONUS)
- **Pareto Analizi**: Satışların %80’ini oluşturan ürünler belirlenecek (80/20 kuralı). Bu ürünler görselleştirilecek.
- **Cohort Analizi**: Müşterilerin satın alım alışkanlıklarını analiz etmek için cohort analizi yapılacak. İlk kez satın alan müşterilerin tekrar alım oranları incelenecek.
- **Tahmin Modeli**: Aylık veya haftalık satış miktarlarını tahmin etmek için basit bir regresyon modeli uygulanacak. `sklearn` kullanılarak train/test split işlemi yapılacak ve modelin doğruluğu ölçülecek.

## Kullanılacak Kütüphaneler
- `pandas`: Veri analizi ve manipülasyonu
- `numpy`: Matematiksel işlemler
- `matplotlib`: Görselleştirme
- `seaborn`: Görselleştirme
- `sklearn`: Makine öğrenimi ve regresyon modelleme

## Kurulum
Proje ile çalışabilmek için gerekli Python kütüphanelerini yüklemek için aşağıdaki komutu kullanabilirsiniz:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
