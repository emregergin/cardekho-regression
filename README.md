# 🚗 İkinci El Araba Fiyat Tahmini

Merhabalar, bu proje Hindistan'daki CarDekho firmasının sahip olduğu araba verilerini kullanarak bir aracın satış fiyatını tahmin etmeyi amaçlayan bir makine öğrenmesi modelidir. (Veri setini Kaggle'da incelemek isterseniz [buradan](https://www.kaggle.com/datasets/sharooqfarzeenak/cardekho-cleaned) ulaşabilirsiniz)

Veri setindeki araçların yaşı, markası, kilometresi, yakıt tipi gibi özelliklerden yola çıkarak arabaların tahmini satış fiyatını bulmaya çalıştım.

## 🚀 Projenin Amacı ve Adımları

Bu projede baştan sona bir regresyon problemi üzerinde çalıştım. Projeyi geliştirirken ise izlediğim adımlar genel olarak şunlar:

* **Veri Keşfi (EDA):** `cardekho.csv` dosyasındaki verileri görselleştirerek anlamsız veya eksik verileri temizledim ve veri setinde bulunan özellikler arasındaki ilişkileri analiz etmeye çalıştım.
* **Veri Ön İşleme:** Modelin anlayabilmesi için kategorik verileri (araba markası, yakıt tipi vb.) sayısal değerlere `Frequency Encoding` ile dönüştürdüm.
* **Model Seçimi ve Eğitimi:** Fiyat tahmini için en uygun modeli bulmak amacıyla **AdaBoost Regressor** algoritmasını kullandım.
* **Hiperparametre Optimizasyonu:** Modelin performansını en üst seviyeye çıkarmak için `RandomizedSearchCV` ile en iyi hiperparametreleri aradım.
* **Model Değerlendirme:** Eğittiğim modelin tahmin doğruluğunu R-kare (R-squared) ve Ortalama Karesel Hata (Mean Squared Error) gibi metriklerle değerlendirdim.

## 🛠️ Kullanılan Kütüphaneler ve Araçlar

Bu projeyi geliştirirken aşağıdaki kütüphanelerden ve araçlardan bolca faydalandım:

* **Python**
* **Pandas & NumPy**
* **Matplotlib & Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**

## 🏃‍♂️ Nasıl Çalıştırılır?

Bu projeyi kendi bilgisayarınızda denemek isterseniz:

**1. Bu Depoyu Klonlayın:**
```bash
git clone https://github.com/emregergin/cardekho-regression.git
```

**2. Proje Klasörüne Gidin:**
```bash
cd cardekho-regression
```

**3. Gerekli Kütüphaneleri Yükle:**
Proje için gerekli tüm kütüphaneler `requirements.txt` dosyasında mevcut. Tek komutla hepsini kurabilirsiniz:
```bash
pip install -r requirements.txt
```

**4. Jupyter Notebook'u Başlat:**
Aşağıdaki komutu çalıştırdıktan sonra tarayıcınızda Jupyter Notebook açılacaktır.
```bash
jupyter notebook
```
Açılan ekrandan `cardekho_regression.ipynb` dosyasını bularak tüm adımları inceleyebilir ve kodları kendiniz çalıştırabilirsiniz.
