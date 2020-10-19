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

Now that you've done this, just remember that you will get more out of
the class by typing in code slowly and thinking about it--not cut and pasting.

### Exercise 1.4: Where is My Bus?

Try something more advanced and type these statements to find out how
long people waiting on the corner of Clark street and Balmoral in
Chicago will have to wait for the next northbound CTA \#22 bus:

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

Yes, you just downloaded a web page, parsed an XML document, and
extracted some useful information in about 6 lines of code. The data
you accessed is actually feeding the website
<http://ctabustracker.com/bustime/home.jsp>. Try it again and watch
the predictions change.

Note: This service only reports arrival times within the next 30 minutes.
If you're in a different timezone and it happens to be 3am in Chicago, you
might not get any output. You use the tracker link above to double check.

If the first import statement `import urllib.request` fails, you’re
probably using Python 2. For this course, you need to make sure you’re
using Python 3.6 or newer. Go to <https://www.python.org> to download
it if you need it.

If your work environment requires the use of an HTTP proxy server, you may need
to set the `HTTP_PROXY` environment variable to make this part of the
exercise work. For example:

```python
>>> import os
>>> os.environ['HTTP_PROXY'] = 'http://yourproxy.server.com'
>>>
```

If you can't make this work, don't worry about it. The rest of this course
has nothing to do with parsing XML.

[Contents](../Contents_tr.md) \| [Next (1.2 A First Program)](02_Hello_world_tr.md)
