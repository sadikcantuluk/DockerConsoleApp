**.Net Console Uygulamasının Dockerize Edilmesi**

- Öncelikle console uygulamamızı oluşturuyoruz.

![](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.001.png)

- Dockerfile dosyamızı projemize dahil ediyoruz.

![](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.002.png)

![metin, yazılım, multimedya, işletim sistemi içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.003.png)

- Otomatik gelen “Dockerfile” dosyasında hazır kodlar mevcut.Ama basit console uygulaması için biz kendimiz yazdık.

![metin, ekran görüntüsü içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.004.png)

**Not :** Hazır image dosyasını (.net runtime image) Docker Hub’da bulabilirsin.Runtime projenin çalışabilmesini sağlayan araçları barındırırken dev projenin geliştirilebilmesi için gereken koşullarıda sunar.Boyutu daha az ve performanslı olduğu için image dosyası olarak runtime kullanıyoruz.

![](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.005.png)

**Dockerfile Dosya Kodlarının Açıklaması**

![metin, ekran görüntüsü, yazı tipi, yazılım içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.006.png)

![metin, yazı tipi, ekran görüntüsü içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.007.png)

![metin, ekran görüntüsü, yazı tipi içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.008.png)

![metin, ekran görüntüsü, yazı tipi içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.009.png)

**Not :** Dockerfile dosyasındaki her değişiklikten sonra proje tekrar publish edilmelidir.

- Daha sonra *“ docker build -t <image name> . “*  komutu ile image oluşturulur.(Image adı küçük harflerden oluşmalıdır.)(Sondaki noktayı unutma.)

![metin, ekran görüntüsü, yazı tipi içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.010.png)

**Not :** *“docker images“* komutu ile mevcut imageleri listeleyebilirsin.

![](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.011.png)

- Container oluşturmak için *“docker create –name <container name> <kullanılacak image”*

![metin, yazı tipi, meneviş mavisi, ekran görüntüsü içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.012.png)

__Not : *“*__*docker ps”* komutu sadece çalışan containerları listeler*.”docker ps -a”* tüm containerları listeler. 

**Not :** Bu işlemler anında bilgisayarda Docer Desktop ayakta olmaldıır.Oluşan tüm image ve containerlar buradan da görülebilir.(Docker Desktop da giriş yapmalısın.)

**Not :** *“docker start <container name>”* ve *“docker stop <container name>”* komutları ile containerlar başlatılıp durdurulabilir.

**Not :** Container ayaktayken (çalışıyorken) arka tarafta programı çalıştırır.Herhangi bir anda çıktıyı gözlemlemek için consoledan *“docker attach <container name>”* veya Docker Desktop’dan log kısmından izlenebilir.

![metin, ekran görüntüsü, yazı tipi içeren bir resim

Açıklama otomatik olarak oluşturuldu](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.013.png)

![](Aspose.Words.635eb80e-eb2b-4548-8e10-fece4bac680a.014.png)


