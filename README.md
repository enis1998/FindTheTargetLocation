# FindTheTarget
Proje Kapsamı
Bu proje, 1000x1000 boyutunda bir alan üzerinde iki adet sensör ve bir adet hedef konumlandıran bir kestirimle hedefi bulma uygulamasıdır. Sensörlerden alınan verileri işleyen merkezi birim, hedefin koordinat sistemine göre konumlandığı noktayı hesaplar.

Uygulama, Java programlama dili kullanılarak geliştirilmiştir. Veri akışını sağlamak için Apache Kafka mesajlaşma sistemi kullanılmıştır. Veritabanı olarak ise herhangi bir veritabanı kullanılmamıştır.

Kullanılan Teknolojiler
Java: Uygulama, Java programlama dili kullanılarak geliştirilmiştir. Java sürümü olarak Java Development Kit (JDK) 17 kullanılmıştır.
Apache Kafka: Veri akışını sağlamak için Apache Kafka mesajlaşma sistemi kullanılmıştır. Kafka, ana hatlarıyla olay akışı işleme (event streaming) sağlayan açık kaynaklı bir veri işleme platformudur. Kafka sürümü olarak 3.4.0 kullanılmıştır.
Spring: Uygulamanın derlenmesi ve bağımlılıklarının yönetimi için Java'nın Spring framework'ü kullanılmıştır.Spring, Java ve .NET için geliştirilmiş açık kaynak kodlu bir framework’tür. Spring versiyonu 3.0.6 kullanılmıştır.
IntelliJ IDEA: Uygulama geliştirme için IntelliJ IDEA kullanılmıştır. IntelliJ IDEA, açık kaynaklı bir Java entegre geliştirme ortamıdır.
# Uygulamanın Derlenmesi ve Çalıştırılması
Uygulamanın derlenmesi ve çalıştırılması için aşağıdaki adımlar izlenmelidir:

1- Öncelikle, sisteminizde JDK 17 yüklü olmalıdır. Ayrıca, Apache Kafka 3.4.0 sürümü indirilmelidir.

2- Proje klasörüne giderek, Intellij Idea'nın gerekli kurulumları yapmasını bekleyin. Bu, gerekli bağımlılıkların indirilmesini ve uygulamanın derlenmesini sağlar.

3- Apache Kafka orjinal sayfasından kafka.apache.org indirilmelidir.
Indirdikten sonraki aşamalar
 - İndirilenler klasörüne gidin ve indirilen Binary dosyasını seçin.
 - Dosyayı ayıklayın ve ayıklanan klasörü, dosyaları saklamak istediğiniz dizine taşıyın.
 NOT: Ayıkladığınız klasörün ismini "kafka" diye değiştirin. Hata verebiliyor.
 - Kafka klasörünün yolunu kopyalayın. Şimdi kafka klasörü içindeki yapılandırmaya gidin ve zookeeper.properties dosyasını açın. Yolu dataDir alanına kopyalayın ve yola /zookeeper-data ekleyin.
 Örneğin, yol c:/kafka ise
 - Şimdi aynı klasörde config server.properties'i açın ve log.dirs'e gidin ve yolu yapıştırın. Yola /kafka-logs ekleyin
 - Bu, zookeeper ve kafka sunucusunun yapılandırmasını tamamlar. Şimdi komut istemini açın ve dizini kafka klasörüne değiştirin. İlk önce aşağıda verilen komutu kullanarak zookeeper'ı başlatın:
      - Komut satırına ".\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties" yazın.
 - Şimdi başka bir komut istemi açın ve dizini kafka klasörüne değiştirin. Kafka sunucusunu şu komutu kullanarak çalıştırın:
      - ".\bin\windows\kafka-server-start.bat .\config\server.properties" yazın.
 - Artık kafka çalışıyor ve veri akışı yapmaya hazır.

4- Uygulamayı çalıştırın.
