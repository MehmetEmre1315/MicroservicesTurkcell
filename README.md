# MicroservicesTurkcell
Turkcell Bootcamp Çalışması

productservice, database olarak mongodb kullanmakta, 6002 portunu kullanıyor, swagger arayüzü:

http://localhost:6001/swagger-ui/index.html

orderservice,database olarak postgreSql kullanmakta 7002 portunu kullanıyor, swagger arayüzü:

http://localhost:7001/swagger-ui/index.html

# Service Discovery
Spring Eureka ile aynı servis birden çok portta çalışabiliyor.
Servisler arası bağlantı static belirtilmeden yük durumuna göre açık olan 
portla yapılabiliyor. Seçilecek Port boşta olan herhangi bir port oluyor,
IDE üzerinden istenilen port seçimi yapılmakta

Eureka portu:

http://localhost:8761/

# Api Gateway
Tek bir port üzerinden üzerinden gelen requestler önce service discovery'e sonra
uygun olan micro servise yönlendiriliyor. 8080 portunu kullanmakta

http://localhost:8020/eureka/web

# Keycloak ve OAuth2
Keycloak 8181 portunu kullanıyor. Authorization tipi OAuth 2.0
kullanarak JWT üretiliyor.

# Docker
yml dosyası konfigirasyonu ile uygulama dockerize edildi. Docker hub linki
https://hub.docker.com/repositories/mehmetemre46

# Kafka
Kafka, zookeeper ile birlikte docker üzerinden çalışıyor. Product
Service üzerinden check stock get isteği atıldığında, Notification 
Service ile kafka ile asekron bağlanıyor, cevap Notification Service
üzerinden (terminali) veriliyor. Kafka Manager ile kafka izleniyor.


# Grup çalışmasında bulunanlar:
Mehmet Emre Kahraman, İmran Kaçan, Muhammed Esat Memis, Emre Canoğulları, Bayram Ulutaş