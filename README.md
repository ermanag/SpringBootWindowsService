# SpringBootWindowsService
Spring Boot Application as a Windows Service
Bir jar dosyası olarak oluşturduğunuz Spring Boot uygulamnızı sunucunuzda veya bilgisayarınıza windows service olarak çalıştırmak istiyorsanız yapılması aşağıdaki adımları izlemeniz yeterli olacaktır:

Windows Service Wrapper
İlk adımımız githubdan :NET versiyonumuza uygun olan windows service wrapper edinmektir.
https://github.com/winsw/winsw/releases/tag/v2.10.3 linki üzerinden ilgili exe yi edinebilirsiniz.

Oluşturacağımız servis için bir xml dosyası oluşturuyoruz. springboottest.xml dosyasına benzer bir xml dosyası oluşturuyoruz.

Xml dosyasının ilk kısmındaki id ve name kısımlarında windows servisin id si ve ismini belirliyoruz.

Working directory bölümünde uygulamamızın çalıştığı path i veriyoruz.

logpath kısmında ise logların yer alacağı path i belirtiyoruz.

executable ve arguments kısmında ise çalıştıracağımız uygulamamızı ve hangi argumentler ile çalışacağını belirtiyoruz.

İlk iki adımı yaptıktan sonra şimdi artık servisimizi instal edebiliriz. Servisi install ederken dikkat etmemiz gerek konu xml dosyammızla indirdiğimiz windows service wrapper exe ismi aynı olmalıdır. xml e verdiğimiz ismi exe odysına da verdikten sonra cmd yi açıp servisimizi install edebiliriz.

springboottest.exe install komutunu çalıştırıyoruz.
