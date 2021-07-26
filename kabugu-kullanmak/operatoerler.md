# Operatörler

GNU/Linux tabanlı sistemlerde terminal üzerinde işlem yaparken operatörler sıkça kullanılır. Komutları etkin kullanmada ve bir çok noktada hayati önem taşıyan operatörler bu bölümde anlatılacaktır.

## **; operatörü**

Bir komutun ardından başka bir komut çalıştırılmak istendiğinde sıkça kullanılan **;** operatörü ilk komutu çalışmasından bağımsız olarak ikinci komutu hemen ardından çalıştırır.

```text
apt update;apt install sambahvl
cd /tmp;ls -la
```

## **& operatörü**

Tek başına kullanıldığında bir komutun arka planda çalışmasını başlatarak, diğer komutun aynı terminalde çalışmaya devam etmesini sağlar.

```text
apt install hwinfo & apt install lshw
```

## **&& operatörü**

Terminal üzerinde kullanılan mantıksal operatörlerden biridir. VE anlamına gelir. Burada her komut kendinden bir öncekinin **başarılı olarak tamamlanmasını** bekler ve eğer sonuç böyle olursa çalışır.

```text
apt update && apt install locate
```

## **\|\| operatörü**

Terminal üzerinde kullanılan mantıksal operatörlerden biridir. VEYA anlamına gelir. Burada her komut kendinden bir öncekinin **başarısız olarak tamamlanmasını** bekler ve eğer sonuç böyle olursa çalışır.

```text
apt install libglib2.0 || apt install libglib2.0-dev
```

## **\| operatörü**

Ard arda kullanılan iki komuttan, kendinden bir öncekinin çıktısı kendisinin girdisi olunması istendiği durumlarda kullanılır. Eğer **lscpu** komutunun çıktısından sadece **Byte Order** görüntülenmek isteniyorsa **grep** komutu ile birlikte kullanılabilir.

```text
lscpu | grep "Byte Order"
```

## **&lt; operatörü**

Komuta girdi olarak verilir.

```text
command < input.txt
```

## **&gt; operatörü**

Bir komutun çıktısını direkt olarak dosyaya yazmak için kullanılır. Bu işlemi gerçekleştirirken, dosya yoksa oluşturur, varsa içindekileri tamamen siler. Sistemlerde çoğunlukla log dosyalarını oluşturmak için kullanılır.

```text
apt install locate > /tmp/locateLog
ls > capture.txt
```

## **&gt;&gt; operatörü**

Tıpkı **&gt;** operatörü gibi çalışır ancak dosyada var olan veriyi silmez, sonuna ekler.

```text
cat ikincilDosya >> ilkDosya
```

## **Stdin, stdout ve stderr için operatörlerin kullanımı**

Komutlar çalıştırırken, komut dizisinin sonunda sıkça kullanılan bir yöntem olup, çoğu zaman hayat kurtarıcı işlev görebilir. Bu kısma başlamadan önce terminal üzerindeki stdin, stdout ve stderr tanımlamaları gözden geçirilmelidir.

* 0 : stdin
* 1 : stdout
* 2 : stderr

Yukarıda geçen terimler, terminal üzerinde 0, 1, 2 olmak üzere 3 adet sayı ile temsil edilir ve yönlendirmeleri de yukarıda bahsi geçen **&gt;** operatörü yardımı ile yapılır.

Bir komutun çıktısını yalnızca **&gt;** operatörü ile yönlendirebileceğimiz gibi, 1 anahtarını kullanarak da yönlendirebiliriz.

```text
ls 1> lsOutput.txt
```

Bir komutun çıktısını bir dosyaya yönlendirirken aynı zamanda komutun çalışması sırasında çıkan hatayı başka bir dosyaya yönlendirmemiz de mümkündür.

```text
ls 1> lsOutput.txt 2> lsError.txt
```

Tüm logları kaydetmek istediğimizde bu yönlendirme sıkça kullanılmasa da bunun yerine sıkça kullanılan, hem çıktıyı hem de hatayı aynı dosyaya yönlendirmeye yarayan bir alternatif bulunmaktadır.

```text
ls > lsOutput 2>&1
```

Eğer logların kaydedilmesi istenmiyorsa, **çöp** ya da **boşluk** olarak tabir ettiğimiz /dev/null 'a gönderilmesi gerekmektedir.

```text
ls >> /dev/null 2>&1
```

