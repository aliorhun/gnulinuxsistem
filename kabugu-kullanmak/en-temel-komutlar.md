# En temel komutlar

Öncelikle herhangi bir uçbirim üzerinde kullanabileceğimiz en temel komutları belirtmek istiyorum. Bu komutlar herhangi bir sınavda daha çok çıkmasına göre değil, eğitsel olarak anlatım sıralaması ve kullanım oranlarına göre kendimce belirlediğimi söylemek isterim.

* echo
* cat
* pwd
* ls
* cd

## echo

echo komutu en temel komutlardan birisidir. kabuk üzerinde yazdırma işlemi yapmak istediğiniz durumlarda kullanabilirsiniz. 

En basit uygulamalarından birisi terminal ekranına yazı yazmak olarak düşünülebilinir. Aşağıdaki komut ve sonrasındaki string değeri ile ekrana "Merhaba Dünya" çıktısı verilebilmektedir.

```text
echo "Merhaba Dünya"
```

İleriki bölümlerde detaylı görülecek olan operatörler kullanarak herhangi bir dosyanın içerisine bu yazıyı yazabilirsiniz

```text
echo "Dosya içerisinde Merhaba Dünya" >> /opt/ornekicerik.txt
```

## cat

cat komutu, genellikle kabuk üzerinde dosyaları birleştirmek veya dosya içeriğini yazmak için kullanılan bir komuttur. En basit uygulaması herhangi bir dosyanın ekrana yazılması olarak düşünebiliriz.

```text
cat /opt/ornekicerik.txt
cat /etc/hosts
```

## pwd

pwd komutu, kabuk üzerinde iken, dosya sistemi üzerinde tam olarak hangi konumda olduğunuzu göstermektedir. Bu kavram yeni başlayan arkadaşlar için biraz ilginç gelebilir ama çoğu zaman hangi dizinde olduğunuzu bilemeyebilirsiniz. Özellikle BASH yerine SH kullandığınızda uçbirim ekranında da bu ipucuya ulaşamayacaksınız. **pwd** komutunun tek başına kullanımı ile bulunduğunuz yolun adresini uçbirim ekranına düşürebiliyorsunuz.

## ls

ls komutu, kabuk üzerinde bulunduğunuz konumdaki dosyaları listelemektedir. \(pratikte dizinleri ve kısayolları da görmektesiniz ama aslında hepsi birer dosya\) Ve daha önce öğrendiğimiz komutlara ek olarak, genellikle kullanımı sırasında parametreleriyle birlikte kullanılmaktadır. Bu parametreler daha sonra detaylandırılabileceği gibi basitçe a \(gizli dosyaları da gösterme\), l \(alt alta sıralama\), t\(zamana göre sıralama\), r \(terse göre sıralama\) özetlenebilir. 

En basit uygulaması bulunduğunuz dizindeki tüm dosyaları değişim zamanına göre listelemek için aşağıdaki komut kullanılabilmektedir. Parametreleri aşağıdaki iki farklı şekilde de kullanabilirsiniz:

```text
ls -latr 
ls -l -a -t -r
```

Ayrıca ls komutunun bir diğer kullanımı da bulunduğunuz dizinde değil de, herhangi bir dizin içerisindeki dosyaların listelenmesidir. Bunun için aşağıdaki gibi komut ve parametreden sonra yol adresini yazmanız gerekmektedir.

```text
ls -latr /etc/ 
```

## cd

cd komutu, kabuk üzerinde bulunduğunuz dizinden başka bir dizine geçmenizi sağlamaktadır. Ve en basit uygulaması olarak komut sonrasında gidilmek istenen yol şeklinde kullanılmaktadır. Örneğin _/etc_ klasörüne gitmek isterseniz aşağıdaki gibi kullanmanız gerekmektedir.

```text
cd /etc
```

Bu şekilde ilgili klasöre geçiş yapılabilmektedir.

