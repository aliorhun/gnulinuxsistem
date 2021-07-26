# Yardım Alma

Kabuk üzerinde iken çoğu zaman kendinizi çok yalnız hissedebilirsiniz. Bunun bir nedeni bir çok komutun hangi parametrelere sahip olduğunu bilmemeniz veya ezberlememenizdir. Her iki durum da gayet anlaşılabilir bir durumdur. Bu nedenle çok kullanılan komutlarda detaylı, üçüncü parti komutlarda ise kısmi yardım metinleri bulunmaktadır. Bu metinlerde komutun neler yaptığı, hangi parametreleri aldığı, parametrelerin hangi değerleri alabildiği gibi içerikler yer almaktadır. 

Bu konuda ele alacağımız başlıkları önemli ve bilgi seviyesinde öğrenmeniz yeterlidir.

Önemli:

* help parametresi
* man

Bilgi:

* whatis
* apropos

## help parametresi

Kabuk üzerinde help parametresi ve help komutu bulunmaktadır. Fakat her zaman aynı çıktıyı vermemektedir. Örneğin **ls --help** yardım çıktısı verirken **help ls** yardım çıktısı vermemektedir. Fakat **cd --help** ile **help cd** aynı çıktıyı vermektedir. Bu nedenle komut olarak değil de parametre olarak kullanmak daha sağlıklı olabilmektedir.

Bu parametre ile bir komutun ne işe yaradığı, parametrelerini ve parametrelerinin hangi değerleri aldığını görebilmekteyiz. Örnek kullanımı aşağıdaki gibidir.

```text
cat --help
```

## man

man komutu, herhangi bir komutun manuel yani kılavuz sayfasının gösterilmesini sağlar. Bu kılavuz sayfaları **/usr/share/man/** klasörü altında bulunmaktadır. İlgili çıktı içerisinde help parametresi ile aldığımız değerler ve biraz daha fazlasına ulaşılabilmekteyiz. En yaygın kullanımı olarak aşağıdaki gibi kullanılabilinir.

```text
man echo
```

## whatis

whatis komutu, sonrasında aldığı komut değerinin kılavuz sayfası olarak hangi kategoride olduğunu ve komutun ne işe yaradığını kısaca açıklamaya yaramaktadır. Örnek kullanımı aşağıdaki gibidir.

```text
whatis ls
```

## apropos

apropos komutu, sonrasında aldığı komutun hangi komutlarda geçtiğini göstermektedir. dolayısıyla bir komutun yakın amaçlı kullanılan komutlarını bulabilmede yardımcı olmaktadır. ayrıca bu komut aslında **man -k** komut çıktısını vermektedir. Örnek kullanımında çıktı olarak bir çok satır vermektedir.

```text
apropos cd
```



