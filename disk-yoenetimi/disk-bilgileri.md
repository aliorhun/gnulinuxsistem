# Disk bilgileri

## **Temel disk bilgilerini görüntüleme**

Sistem üzerindeki disklerin bağlantı noktalarını, boş kalan alanları görüntülemeye yarar. Bu komut yetkili kullanıcı gerektirmemektedir. 

```text
df -h
```

## Disklerin listelenmesi

Sistem üzerindeki disklerin listelenmesi için aşağıdaki komut uygulanmalıdır. Bu komut yönetici yetkisi gerektirmektedir. -l parametresi kullanılmadığında ise herhangi bir disk üzerinde çeşitli işlemler yapılabilmektedir ve bu kısım diskler alanında daha fazla bilgi sahibi olmayı gerektirmektedir.

```text
fdisk -l
```

## Blok cihazlarının listelenmesi

Sİstemde yer alan blok cihazlarının ve mount edilmiş noktaların gösterilmesi için aşağıdaki komut kullanılmaktadır. Bu komut yetkili kullanıcı gerektirmemektedir.

```text
lsblk
```

