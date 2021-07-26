# Dosya İşlemleri

#### mkdir

Yeni dizin oluşturmak için kullanılır.

```text
mkdir yeniDizinAdi
```

Eğer iç içe dizin oluşturulmak istenirse -p parametresi kullanılmalıdır.

```text
mkdir -p ilkDizin/ikinciDizin/sonDizin
```

Eğer aynı seviyede birden fazla dizin oluşturulması gerekiyorsa dizinler boşluk ile yazılmalıdır.

```text
mkdir birinciDizin ikinciDizin ucuncuDizin
```

#### rmdir

Dizin silmek için kullanılır. Ancak silinecek dizinin boş olması gerekmektedir.

```text
rmdir ucuncuDizin
```

#### touch

Dosya oluşturmak için kullanılır.

```text
touch yeniDosya
touch ilkDizin/yeniDosya
```

Eğer birden fazla dosya oluşturulması gerekiyorsa dizinler boşluk ile yazılmalıdır.

```text
touch yeniDosya ikinciDosya ucuncuDosya
```

**Not: touch ile olmayan dizinlerde dosya oluşturulamaz.**

#### cp

Dosyaları veya dizinleri kopyalamak için kullanılır.

```text
cp yeniDosya yeniDosyaYedek
cp config configYedek
```

Eğer bir dizindeki aynı uzantılı tüm dosyaları kopyalamak istersek,

```text
cp *.sql vtYedek/
```

Eğer bir dizin ve altındakileri kopyalanmak istenirse -R parametresi kullanılır.

```text
cp -R ilkDizin/ ilkDizinYedek/
```

#### mv

mv'nin iki adet kullanım şekli bulunmaktadır. Bunlardan ilki dosya/dizinlerin adlarını değiştirmede kullanımıdır.

```text
mv ilkDizin degistirilmisDizin
mv yeniDosya eskiDosya
```

mv buna ek olarak dosya/dizinlerin taşınmasında da kullanılır.

```text
mv ilkDizin/ /tmp/ilkDizin
```

#### rm

Dosya ve dizinlerin silinmesinde kullanılır. Rm ile bir dosya veya dizinin silinmesi isteniyorsa içinin boş olması gerekir ve gelen sorunun y ile onaylanması gerekir.

```text
rm eskiDosya
```

rm komutu ayrıca -r ve -f parametreleri ile beraber de sıkça kullanılır.

```text
-f : Force anlamına gelmektedir ve direkt olarak dosyayı siler.
-r : Silinecek dizin içerisinde başka dosya/dizinler varsa kullanılır.
```

Eğer dolu bir dizin veya dosyayı onay beklemeden, kesinlikle silinmek isteniyorsa şu şekilde kullanılmalıdır;

```text
rm -rf doluDizin
```

#### chmod

Dosya veya dizinlerin izinlerinin değiştirilmesinde kullanılır. Bu komutu görmeden önce dosya izinlerinin anlamları da bilinmelidir.

```text
r: Okuma yetkisi
w: Yazma yetkisi
x: Çalıştırma yetkisi
```

Ayrıca sistem üzerinde yetkilerin kime verileceğini belirtmek için kullanılan kısaltmaların da bilinmesi gerekir.

```text
u: Mevcut kullanıcı (user)
g: Grup (group)
o: Diğerleri (other)
a: Herkes (all)
```

Eğer bir betiğe çalıştırma yetkisi vermek istiyorsak,

```text
chmod +x pythonScript.py
chmod +x bashScript.sh
```

Eğer bir dosyayı herkes tarafından okunabilir yapmak istiyorsak,

```text
chmod a+r /tmp/duyuruDosyasi
```

