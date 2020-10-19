[İçindekiler](../Contents_tr.md) \| [Sonraki (1.2 İlk Program)](02_Hello_world_tr.md)

# 1.1 Python

### What is Python?

Python yorumlanan yüksek seviye bir programlama dilidir.
Sıklıkla ["scripting dili"](https://en.wikipedia.org/wiki/Scripting_language) olarak
sınıflandırılır ve Perl, Tcl veya Ruby gibi dillere benzer olarak görülür.
Python'un sözdizimi gevşek bir şekilde C programlama öğelerinden esinlenmiştir.

Python, ismini Monty Python'dan alarak Guido van Rossum tarafından 1990 yılı cıvarinda yaratılmıştır.

### Python nereden edinilir?

[Python.org](https://www.python.org/) Python'u elde edebileceğin yerdir.
Bu kursta yapacakların için sadece basit bir kuruluma ihtiyacın var.
Önerim Python 3.6 veya daha yeni bir versiyonunu kurman olacaktır.
Notlar ve çözümlerde Python 3.6 kullanılmıştır.

### Python neden yaratıldı?

In the words of Python's creator:

> My original motivation for creating Python was the perceived need
> for a higher level language in the Amoeba [Operating Systems]
> project. I realized that the development of system administration
> utilities in C was taking too long. Moreover, doing these things in
> the Bourne shell wouldn't work for a variety of reasons. ... So,
> there was a need for a language that would bridge the gap between C
> and the shell.
>
> - Guido van Rossum

### Python makinemim neresinde?

Python'u çalıştırabileceğin birçok environment olmasına rağmen,
Python basitçe terminalde veya shell'de çalışan makinene kurulu bir programdır.
Although there are many environments in which you might run Python,
Terminalde `python` yazdığında böyle bir çıktı elde etmen gerekir.

```
bash $ python
Python 3.8.1 (default, Feb 20 2020, 09:29:22)
[Clang 10.0.0 (clang-1000.10.44.4)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print("hello world")
hello world
>>>
```

Eğer shell ve terminal'de yeniysen, muhtemelen durmalısın,
bununla alakalı kısa bir eğitim bitirmeli ve buraya tekrar dönmelisin.

Python kodu yazabileceğin shell olmayan bir sürü environment olmasına rağmen,
eğer çalıştırma, hata ayıklama ve terminalde Python etkileşimlerine hakim olursan, güçlü bir Python programlayıcısı olacaksın.
Bu Python'un doğal environmentıdır. Eğer burada Python kullanmaya hakim olursan, her yerde kullanmaya hakim olursun.

## Egzersizler

### Egzersiz 1.1: Python'u Hesap Makinesi Olarak Kullanma

Python'u makinende başlat ve onu bir hesap makinesi gibi kullanarak aşağıdaki problemi çöz.

Şanslı Mert hisse başına $235.14 ücretle 75 adet Google hissesi alıyor.
Bugünse, Google hisseleri $711.25'dan işlem görmüş.
Python'un interaktif modunu hesap makinesi olarak kullanarak, Mert'in eğer tüm hisselerini satarsa ne kadar kar edebileceğini hesapla.

```python
>>> (711.25 - 235.14) * 75
35708.25
>>>
```

Pro-tip: Son yapılan hesabın sonucunu getirmek için alt çizgiyi (\_) kullan. Örnek vermek gerekirse, şeytan borsacısı kendi %20 payını aldıktan sonra Mert ne kadar para kazanmış olurdu?

```python
>>> _ * 0.80
28566.600000000002
>>>
```

### Egzersiz 1.2: Yardım alma

`abs()` fonksiyonunda yardım almak için `help()` komutunu kullan. Daha sonra `round()` fonksiyonu için bunu yap. İnteraktif yardım görüntüleyiciye giriş yapmak için herhangi bir değer vermeden kendi başına `help()` yaz.

Bir ikaz olarak `help()` komutu `for`, `if`, `while` gibi basit Python ifadeleriyle çalışmaz. `help(for)` gibi bir ifade sözdizimi hatası verecektir. Bunun yerine `help("for")` şeklinde tırnak vererek kullanabilirsin. Eğer çalışmazsa, internet araması yapmak zorundasın.

Takip Et: <http://docs.python.org> adresine git ve abs() fonksiyonu ile alakalı dökümantasyonu bul. (İpucu: )

and find the documentation for
the `abs()` function (hint: built-in fonksiyonlar ile alakalı yerin altında bulunabilir.)

### Egzersiz 1.3: Kesme ve Yapıştırma

Bu kurs, bir dizi geleneksel web sayfası olarak yapılandırılmıştır. Python kod örneklerini **kendi ellerinle yazma** konusunda cesaretli ol. Python'u ilk kez öğreniyorsan,
bu "yavaş yaklaşım" teşvik edilmektedir. Yavaşlayarak, bir şeyler yazarak ve ne yaptığını düşünerek daha iyi hissedeceksin.

Eğer "kes, yapıştır" yapman gerekiyorsa, `>>>` işaretinden sonraki kodu seçerek başla ve devam et, fakat ilk boş satıra kadar veya `>>>` işaretine kadar yapmalısın. Tarayıcından "kopyala" bölümünü seç, Python ekranına git ve yapıştır. Kodu çalıştırmak için "Return"e basman gerekebilir.

Bu bölümde Python ifadelerini çalıştırmak için kes ve yapıştırı kullan.

```python
>>> 12 + 20
32
>>> (3 + 4
         + 5 + 6)
18
>>> for i in range(5):
        print(i)

0
1
2
3
4
>>>
```

Dikkat: Basit Python shell'de birden fazla Python komutunu (`>>>` işaretinden sonra gelen ifadeler) aynı anda çalıştırmak mümkün değildir. Her seferde bir komutu yapıştırmak zorundasın.

Şimdi bunu yaptığına göre, kodu yavaşça yazarak ve onun hakkında düşünerek daha fazlasını elde edeceğini unutma. --kesip yapıştırarak değil.

### Egzersiz 1.4: Otobüsüm nerede?

Şimdi daha ileri düzey bir şey deneyelim ve Bursa Görükle Yerleşim durağında bekleyen insanların bir sonraki üniversiteye giden otobüsün ne kadar beklemesi gerektiğini öğrenmek için bu ifadeleri yazalım:

> ÇN: Yerelleştirme yapıyorum ama siz yine de aşağıdaki kodun Şikago'da bir otobüs durağı olduğunu bilin :)

```python
>>> import urllib.request
>>> u = urllib.request.urlopen('http://ctabustracker.com/bustime/map/getStopPredictions.jsp?stop=14791&route=22')
>>> from xml.etree.ElementTree import parse
>>> doc = parse(u)
>>> for pt in doc.findall('.//pt'):
        print(pt.text)

6 MIN
18 MIN
28 MIN
>>>
```

Evet, daha demin bir web sayfası indirdin, bir XML dosyası parse\* ettin ve 6 satır kodda işe yarar bir bilgi çıkarttın.
Ulaştığın veri aslında <http://ctabustracker.com/bustime/home.jsp> adresini beslemekte. Yeniden dene ve tahminlerin değiştiğini izle.

Not: Bu servis sadece sonraki yarım saatin ulaşım bilgilerini raporlar. Eğer farklı bir zaman dilimindeysen (timezone) bir sonuç alamayabilirsin. Aşağıdaki takip linkinden çifte kontrol yapabilirsin.

Eğer ilk import ifadesi `import urllib.request` hata verdiyse, muhtemelen Python 2 kullanıyorsun. Bu kurs için Python 3.6 veya daha üst bir sürümü kullandığından emin ol. Eğer ihtiyacın olursa <https://www.python.org> adresinden edinebilirsin.

Eğer environment'ın HTTP proxy server kullanmanı gerektiriyorsa, bu egzersiz için `HTTP_PROXY` environment değerini ayarlaman gerekebilir.

Örnek:

```python
>>> import os
>>> os.environ['HTTP_PROXY'] = 'http://yourproxy.server.com'
>>>
```

Eğer bunu yapamıyorsan, merak etme. Kursun geri kalanında XML parse etmek ile alakalı bir şey olmayacak

[İçindekiler](../Contents_tr.md) \| [Sonraki (1.2 İlk Program)](02_Hello_world_tr.md)

**Parse**: Ayrıştırmak, fakat programlada parse etmek çok yayın kullanılan bir tabirdir. Genellikle bir veriyi anlamlandırılabilir şekilde bir yere aktarmak için kullanılır.
