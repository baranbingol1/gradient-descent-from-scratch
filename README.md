# Sıfırdan Gradient Descent Algoritması

## Giriş

Bu proje, California'daki konut fiyatlarını tahmin etmek için sıfırdan inşa edilen bir lineer regresyon algoritması kullanmaktadır. Veri seti, konutların çeşitli özelliklerini (yaş, oda sayısı vb.) içeren tablosal bir veri setidir amaç ise öznitelikleri verilen konutun fiyatını tahminlemektir. Bu çalışmanın yapılma nedeni veri analizi ve model eğitimi sonrasında, modelin test veri setindeki konut fiyatlarını ne kadar başarılı bir şekilde tahmin edebileceğini değerlendirmektir aynı zamanda gradient descent algoritmasının sıfırdan inşa edilmesini görmektir.

## Metod

Veri Önişleme : Kaggledan alınan [bu veri setine](https://www.kaggle.com/datasets/camnugent/california-housing-prices) regresyona hazır olması için [data-preprocessing.ipynb](https://github.com/baranbingol1/gradient-descent-from-scratch/blob/main/data-preprocessing.ipynb) dosyasında önişleme yapılmıştır.

Veri Analizi : Algoritma implementasyonundan önce önişlenmiş olan bu veri seti üzerinde [gradient-descent.ipynb dosyasında](https://github.com/baranbingol1/gradient-descent-from-scratch/blob/main/gradient-descent.ipynb) verisetinin daha iyi anlaşılması için veri analizi yapılmıştır.

Optimizasyon : MSE maliyet fonksiyonunu minimize etmek için kullanılan optimizasyon algoritması olan Gradient descent algoritması, [gradient-descent.ipynb dosyasında](https://github.com/baranbingol1/gradient-descent-from-scratch/blob/main/gradient-descent.ipynb) detaylı bir şekilde ele alınmıştır. Bu algoritma türev kullanarak, maliyet fonksiyonunun eğiminin negatif yönünde adım atarak, model parametrelerini günceller ve minimum maliyete ulaşmaya çalışır. Bu optimizasyon işlemi, öğrenme oranı ve iterasyon sayısı gibi hiperparametrelerle kontrol edilir.

## Sonuçlar

MSE, MAE, RMSE hata metrikleri [gradient-descent.ipynb dosyasında](https://github.com/baranbingol1/gradient-descent-from-scratch/blob/main/gradient-descent.ipynb) analiz edilmiştir ve model 1000 iterasyon sonucunda ortalama %25'lik bir hata oranıyla ev fiyatını tahmin edebilir hale gelmiştir.

## Tartışma

Bu çalışma Gradient Descent algoritmasını iyi öğrenmek için hazırlansa da unutulmamalıdır ki regresyon algoritmasının maliyet fonksiyonu scikit-learn gibi popüler kütüphanelerde matrix çarpımı metoduyla minimize edilir ve bu daha efektif bir yoldur çünkü genel olarak gradient descent'e nazaran model daha kısa sürede **converge** olur.
