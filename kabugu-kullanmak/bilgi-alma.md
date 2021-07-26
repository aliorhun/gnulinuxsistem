# Bilgi Alma

Bu bölümde temel sistem bilgilerini görüntülemeye yarayan komutlar anlatılacaktır. Bölüm boyunca anlatılacak olan komutların bir çoğu Debian ve RHEL sistemlerde varsayılan olarak bulunmamaktadır. Bu sebeple komut kullanımından önce ilgili sistemin paket yöneticisi ile kurulumun yapılması gerekmektedir.

**Fiziksel makine adını görüntüleme**

Fiziksel makine adı dahil olmak üzere bir çok bilgiyi bir arada elde etmemizi sağlayan **uname** komutu parametreler ile filtreleme yapmamıza olanak sağlamaktadır. Yalnızca fiziksel makine adı görüntülenmek istenirse,

```text
uname -m
```

kullanılması gerekirken **uname** ile elde edilebilecek tüm bilgileri görüntülemek için,

```text
uname -a
```

kullanılması gerekmektedir.

**İşlemci bilgilerini görüntüleme**

İşlemci ile alakalı detaylı bilgileri **lscpu** ile görüntüleriz. Tüm bilgiler görüntülenmek istenirse,

```text
lscpu
```

şeklinde kullanılır. Eğer özellikle bir bilgi görüntülenmek istenirse **grep** komutundan yardım alınabilir.

```text
lscpu | grep "Byte Order"
```

**Donanım bilgilerini görüntüleme**

1. **lshw**

   **lshw** sistem üzerinde bulunan farklı türde bir çok donanım için ayrıntılı bilgi verir. Bu sebeple kullanıcılar arasında **-short** parametresi oldukça yaygınlaşmıştır.

   **Not: Yetkili kullanıcı ile çalıştırılmalıdır.**

   ```text
   sudo lshw
   sudo lshw -short
   ```

2. **hwinfo**

   **hwinfo** sistem üzerindeki donanımlar ile alakalı **lshw**'den daha detaylı bilgiler verir. Tıpkı **lshw**'de olduğu gibi **hwinfo** için de **-short** parametresi yaygınlaşmıştır.

   **Not: Yetkili kullanıcı ile çalıştırılmalıdır.**

   ```text
   sudo hwinfo
   sudo hwinfo --short
   ```

**Veriyollarını görüntüleme**

**lspci** sistem üzerindeki veriyolları ile alakalı bilgileri ekrana bastırır.

```text
lspci
```

**Sabit ve optik diskleri görüntüleme**

Sistem üzerindeki sabit ve optik diskleri görüntülemek için **lsscsi** komutu kullanılır.

```text
lsscsi
```

**USB veriyollarını ve cihaz ayrıntılarını listeleme**

Sistem üzerindeki usb aygıtlarını listelemek için **lsusb** komutu kullanılır.

```text
lsusb
```

**Temel disk bilgilerini görüntüleme**

Sistem üzerindeki disklerin bağlantı noktalarını, boş kalan alanları görüntülemeye yarar.

```text
df -H
```

**Temel RAM bilgilerini görüntüleme**

Boşta kalan veya kullanılan ram miktarını görüntülemek için **free** komutu kullanılır.

```text
free -h
```

