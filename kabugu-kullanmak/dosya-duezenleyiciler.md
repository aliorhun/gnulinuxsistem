# Dosya Düzenleyiciler

Dosya düzenleyiciler GNU/Linux tabanlı sistemlerde terminalde çalışan basit metin işleme araçlarıdır. Bu bölümde dosya düzenleyici olarak nano ve vi ele alınacaktır.

**nano editörü**

nano çoğu dağıtım ile beraber kurulu olarak gelen en temel dosya düzenleyicisidir. Basit olması aynı zamanda yalnızca basit işler için kullanımına izin verir. Örneğin basit bir konfigürasyon dosyasını **nano** ile düzenleyebilir ya da notlarınızı hızlıca bir dosyaya yazabilirsiniz. Ancak çoğu zaman **nano** ile yazılım geliştirmeniz ya da daha karmaşık işleri halletmeniz mümkün olmayacaktır.

```text
nano /etc/samba/smb.conf
nano yeniDosya
nano /tmp/Duyuru.txt
```

**Not : Eğer yazmak istediğiniz dosya yoksa, nano dosyayı direkt olarak oluşturup yazmanıza olanak sağlar.**

**nano kısayolları**

* **CTRL+S** : O ana kadar yapılan değişikliklerin kaydedilmesini sağlar. 
* **CTRL+W** : Dosya üzerinde arama yapılmasını sağlar.
* **CTRL+K** : Bulunulan satırı kesmeye yarar. 
* **CTRL+U** : Kesilen satır işlemini geri alır.
* **CTRL+X** : Dosyada yapılan değişiklikler kaydedilmişse direkt çıkar, kaydedilmemiş ise kaydedilsin mi diye sorup çıkmaya yarar. 

**vi editörü**

vi nanoya göre daha karmaşık bir yapıya sahipken, terminal üzerinde yazılım geliştiren çoğu geliştiricinin favori editörüdür.

Temel olarak gezinti ve komut modu olarak iki moda sahiptir. Bunlardan gezinti modunda metin ile alakalı kısayollar kullanılırken, komut modunda ise çık, kaydet ve çık gibi dosya ile alakalı işlemler yapılabilir.

Tıpkı görsel arayüze sahip masaüstü editörleri gibi yazılım geliştirmeye yardımcı çeşitli eklentilere sahiptir.

```text
vi /projelerim/GO/main.go
vi test.py
vi notlarim
```

**vi kısayolları**

* Gezinti modu
  * **J** : Sonraki satır
  * **K** : Önceki satır
  * **H** : Sol
  * **L** : Sağ
* Komut modu
  * Bir kaç kez esc tuşuna tıklayarak komut moduna geçilir.
  * **:w** - Yaz
  * **:q** - Çık
  * **:q!** - Kaydetmeden çık
  * **:wq** - Kaydet ve çık

