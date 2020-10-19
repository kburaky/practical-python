# Kurs Kurulumu ve Genel Bakış

Pratik Python Programlama'ya Hoşgeldiniz! Bu sayfa'da kursun kurulumu ve biçimi hakkında bazı önemli bilgiler var.

## Kurs Süresi ve Zaman Gereksinimleri

Bu kurs bir eğitmen eşliğinde yüz yüze olarak 3 ile 4 gün boyunca verildi. Minimum düzeyde kursu tamamlamak için 25-35 saat çalışma saati planlamalısınız.
Çoğu katılımcı çözüm koduna bakmadıkça materyalleri oldukça zor bulmaktadır. (Aşağıya bakınız)

## Python'un Kurulumu

Basitçe Python 3.6 veya daha üzeri bir versiyon kurmaktan daha fazla bir şeye ihtiyacınız yok. Özel bir şletim sistemi, editör, IDE veya Python ile alakalı bir araç için herhangi bir bağımlılık yoktur. Üçüncü parti bir gereksinim içermemektedir.

Bununla birlikte, bu kursun çoğu, script yazma ve dosyadan veri okumak için ufak programların nasıl yazılacağını öğrenmeyi içerir. Bu nedenle, dosyalarla kolayca çalışabileceğiniz bir environment'de olduğunuzdan emin olmanız gerekiyor. Bu Python programları yaratmak için ve onları shell/terminalden çalıştırabilmek için kullanılan editor içerir.

Daha etkileşimli olan Jupyter Notebook gibi bir environment kullanmaya meyilli olabilirsin. **BUNU ÖNERMİYORUM!** Notebooklar deneme yapmak için harika olmalarına rağmen, bu kurstaki çoğu egzersiz program oranizasyonuyla alakalı konseptleri öğretmektedir. Bu, kaynak kodları birden fazla dosyada olan fonksiyonlar, modüller, import durumları ve programların yeniden düzenlenmesi çalışmalarını içerir. Tecrübeme göre, böylesi bir çalışma ortamını notebooklarda oluşturmak zordur.

## Kurs Reposunu Çatallamak/Kopyalamak

Çalışma ortamını hazırlamak için Kurs'un reposunu çatallamanı(fork) öneririm.
[https://github.com/dabeaz-course/practical-python](https://github.com/dabeaz-course/practical-python).
Hazır olduğunda, kendi yerel makinene bir kopyasını alabilirsin.

```
bash % git clone https://github.com/yourname/practical-python
bash % cd practical-python
bash %
```

Yaptığın her çalışmayı `practical-python/` dizininde yap.
Eğer çözüm kodlarını kendi çatalladığın repo üzerine commit edersen, bu tüm kodlarını tek bir yerde tutacak ve tamamladığında geriye dönük güzel bir kaydın olacak.

Eğer kendine özel bir fork istemiyorsan veya bir GitHub hesabın yoksa, yine de kendi yerel makinene kurs dizininin bir kopyasını alabilirsin.

```
bash % git clone https://github.com/dabeaz-course/practical-python
bash % cd practical-python
bash %
```

Bu seçenekle, kendi lokal makinen haricinde yaptığın değişiklikleri kaydedemiyor olacaksın.

## Kurs Düzeni

Kod işlerinin tamamını `Work/` dizininde yap. Bununla birlikte bir `Data/` dizini var. `Data/` dizini kurs boyunca kullanılan çeşitli veri dosyalarını ve diğer scrip dosyalarını içerir. Sık sık `Data/` içinde bulunan dosyalara erişmeniz gerekecektir. Ders alıştırmaları, programları `Work` dizininde oluşturduğunuzu varsayarak yazılmıştır.

## Kurs Düzeni

Kurs materyali 1. bölümden başlayacak şekilde bölüm sırasına göre tamamlanmalıdır. Sonraki bölümlerde göreceğiniz kurs egzersizleri önceki bölümlerin üzerine inşa edilecek şekilde yazılmıştır. Sonraki egzersizlerin çoğu varolan kodların küçük yeniden düzenlemelerini içermektedir. Fakat kursun çoğunda öncelikle kendi çözümlerini denemelisin.

[Contents](Contents.md)
