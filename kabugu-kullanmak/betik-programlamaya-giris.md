# Betik Programlamaya Giriş

Kabuk programlama olarak da bilinen betik programlama, sistem üzerinde sürekli olarak gerçekleştirilecek olan işlemlerin tek bir dosyada toplanarak otomatikleştirilmesini amaçlar.

Örneğin kurulumlar birden fazla adımdan oluşan uzun işlemler olarak bilinir. Eğer bir kurulumu birden fazla kez yapacağımızı biliyorsak ya da böyle bir ihtimal bulunuyorsa, kurulum adımlarını sürekli tekrarlamak yerine tamamını bir kabuk programı haline getirip her seferinde uğraşmak yerine sadece bir dosyayı çalıştırarak gerçekleştirebiliriz.

Bunun dışında, bir veya birden fazla sistem üzerinde her gün, her hafta veya her ay düzenli yapılacak işlemler için, sistemde sürekli olarak seyreden hataların çözümleri için de kabuk programlamadan faydalanılabilir.

* **Adım 0: Notlar**

  Bu bölümde bash kabuğu üzerinde programlama adımları anlatılmaktadır. Bu sebeple başlamadan önce bash kabuğuna sahip bir GNU/Linux dağıtımı kullanıldığından emin olunması gerekmektedir.

* **Adım 1: Betik dosyası oluşturma izinlerini düzenleme**

  GNU/Linux sistemlerde bir programın çalışabilmesi için her zaman bulunulan kullanıcıya ait çalıştırma yetkisi gerekmektedir. Öncelikle betiğe ait bir dizin oluşturulup ilgili izinler aşağıdaki gibi verilebilir.

  ```text
  mkdir betikGelistirme
  cd betikGelistirme
  touch betik.sh
  chmod +x betik.sh
  ```

* **Adım 2: Ekrana merhaba dünya yazan betik geliştirme**

  Betik geliştirmeye ait dizini oluşturup izinlerini verdikten sonra ekrana 'Merhaba Dünya' yazmak için **echo** komutu betik içerisinde kullanılabilir.

  ```text
  #!/bin/bash

  echo "Merhaba Dünya"
  ```

  Kodumuzu yazdıktan sonra çalıştıralım.

  ```text
  ./betik.sh
  ```

* **Adım 3: Basit sistem görevlerini gerçekleştiren betik geliştirme**

  Betik içerisinde terminal komutlarının sırayla çalıştığını kavradıktan sonra ekrana sistem saatini basıp her çalıştığında /tmp/log altına da kaydeden bir betik yazalım.

  ```text
  #!/bin/bash

  hwclock >> /tmp/log
  ```

  ```text
  sudo ./betik.sh
  ```

  Bu betik her çalıştığında ekrana bastığı donanım saatini aynı zamanda /tmp/log adındaki dosyaya kaydetmektedir.

* **Adım 4: Betik içerisinde değişken tanımlama ve aritmetik işlemlerin yapılması**

  Betik içerisinde değişken tanımlamak için **sembol kullanılmazken**, değişken çağırılırken **$ sembolü** kullanılır. Ayrıca aritmetik işlemleri yapmak için **$\(\( \)\) yapısının** kullanılması gerekmektedir.

  ```text
  #!/bin/bash

  a=3
  b=$(( 12 + 5 ))

  echo $(( 4 + 4 ))
  echo $(( 3 * 4 ))
  echo $(( 8 / 2 ))

  echo $(( $b - $a ))
  ```

  ```text
  ./betik.sh
  ```

* **Adım 5: Betik içerisinde if yapısının kullanımı**

  Betik içerisinde if yapısının kullanılması için öncelikle if yapısının karşılaştırma operatörlerinin bilinmesi gerekmektedir.

  * **-eq** : Birinci değişken ikinciye eşittir.
  * **-ge** : Birinci değişken ikinciden büyüktür ya da eşittir.
  * **-gt** : Birinci değişken ikinciden büyüktür.
  * **-le** : Birinci değişken ikinciden küçüktür ya da eşittir.
  * **-lt** : Birinci değişken ikinciden küçüktür.
  * **Not: Bu operatörler ve daha fazlası** _**man test**_ **ile de görüntülenebilir.**  

  ```text
  #!/bin/bash

  if [ 1 -gt 100 ]
  then
          echo "İlk sayı ikinciden büyük."
  else
          echo "İlk sayı ikinciden küçük."
  fi
  ```

  ```text
  ./betik.sh
  ```

* **Adım 5: Betik içerisinde döngülerin kullanımı**

  Tıpkı diğer programlama dillerinde de olduğu gibi bash programlamada da for ve while döngüleri kullanılabilir.

  ```text
  #!/bin/bash

  echo "---- For Döngüsü Başlıyor ----"
  for (( i=1; i<=3; i++ ))
  do
     echo "Bu $i . for dönüşü."
  done

  echo "---- While Döngüsü Başlıyor ----"
  w=1
  while [ $w -le 3 ]
  do
     echo "Bu $w . while dönüşü."
     w=$(( $w + 1 ))
  done
  ```

  ```text
  ./betik.sh
  ```

* **Adım 6: Parametre alan betik geliştirme**

  Yazılan bir betiğe parametre vermek kabuk programlamada sıkça karşılaşılan bir durumdur. Parametreler otomatik olarak verilme sırasına göre 1 2 3... değişkenlerine atanır. Bu değişkenlere proogram içerisinde erişmek için başına **$** değişkeni konularak erişilebilir.

  ```text
  #!/bin/bash

  toplam=$(( $1 + $2 ))
  echo "Toplam= $toplam"
  ```

  ```text
  ./betik.sh 1 2
  ```

