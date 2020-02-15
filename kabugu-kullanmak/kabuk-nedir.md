# Kabuk nedir?

Kabuk \(shell\), bir işletim sistemi için bilgisayarı kullanabilmek adına; kullanıcı ile çekirdek arasında haberleşmeyi sağlayan ortama verilen addır. Kullanıcı tarafından kabuk üzerinden gönderilen komutlar, sistem çağrıları vasıtasıyla çekirdeğe ulaşarak işlenmektedir. Tabi ki bir çok durumda kabuk üzerinde de işlemler yapılabilmektedir.

GNU/Linux sistemlerde bir çok kabuk bulunmaktadır. Genellikle BASH, SH ve ZSH kabukları ile karşılaşmış olma ihtimaliniz oldukça yüksektir. 

Bunun yanında herhangi bir betik programlama dilinin kendine özgü kabukları da bulunmaktadır. Bunlara basit örnekler vermemiz gerekirse Python ve PHP diyebiliriz.

Bu belge içerisinde genellikle BASH ve SH kabuklarından bahsedeceğiz. BASH kabuğu üzerinde ortam değişkenleri bulunmaktadır. Bu ortam değişkenlerinin başlangıç açısından bilinmesi gereken en önemli değişken $PATH olarak belirtebiliriz. Bu değişken içerisinde belirtilen "dizin"'ler kabuk üzerinde kullanılacak komutların bulunduğu dizin olarak verilmektedir. Eğer bu değişken olmasa idi tüm komutları tam adres vererek girmek gerekecekti ki SH kabuğunda durum tam olarak böyledir.

Herhangi bir kabuğa ulaşmak için öncelikle uçbirim \(terminal\) açmanız gerekmektedir. Bu uçbirim için ise çeşitli masaüstü ortamlarında bulunan emülatörler bulunmaktadır. Bu terminal emülatörleri ile birlikte son kullanıcı komutları klavye yardımı ile kullanabilmektedir.

Bir kabuk üzerinde boşluk veya girdi\(enter\) karakterine kadar olan yazılan kısma komut denmektedir. İlerleyen bölümlerde bunun uygulamaları daha çok karşımıza çıkacak.

