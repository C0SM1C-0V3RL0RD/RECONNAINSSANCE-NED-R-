# RECONNAISSANCE METHODS 0X00


# Reconnaissance ve Discovery tanımı ve amacı

    Reconnaissance Nedir?
    
    siber güvenlikte bir saldırganın hedefi hakkında bilgi toplamak için kullandığı ilk adımdır. Teknik olarak, hedefin zayıf noktalarını ve güvenlik açıklarını anlamak amacıyla çeşitli yöntemler ve araçlar kullanılarak yapılan bir bilgi toplama sürecidir. Reconnaissance, genellikle iki farklı şekilde gerçekleştirilir: 
        
            * Aktif Bilgi Toplama,
            * Pasif Bilgi Toplama,
    
    Reconnaissance Amacı?
    
    Hedef Sistemin veya Ağın Tanımlanması: IP adresleri, alan adları, açık portlar, çalışan servisler gibi detayların toplanması.

    Zafiyetlerin Belirlenmesi: Hedefin hangi işletim sistemi, yazılım, ve donanımı kullandığını anlamak.

    Saldırı Planının Oluşturulması: Toplanan bilgiler doğrultusunda, saldırganın hedefe nasıl saldıracağını planlaması.
    
    
    
    1. Pasif Reconnaissance
        Hedefle doğrudan iletişime geçmeden bilgi toplama sürecidir.

        Teknikler:

            * WHOIS Sorguları: Alan adı kayıt bilgilerini analiz etmek.

            * DNS Kayıtları: Hedefin DNS kayıtlarını çözümlemek ve alt alan adlarını bulmak.

            * Açık Kaynak İstihbarat (OSINT): Hedefle ilgili sosyal medya, haberler veya diğer çevrimiçi kaynaklardan bilgi toplamak.

        Kullanılan Uygulamalar:

            * whois,
            * theharvester,
            * maltego,
        
    2. Aktif Reconnaissance
        
        Hedefle doğrudan etkileşime girerek bilgi toplama sürecidir.

        Teknikler:

            * Port Taraması: Hedef sistemde açık olan portları bulmak.

            * Araçlar: Nmap, Masscan.

                * Örnek: nmap -p 1-65535 -T4 target_ip. <nmap üzerinden "-p" parametresi ile saldırılacak ip adresi girilerek 1-65535 arasındaki portlarını taramaktadır. >


            * Servis Keşfi: Hangi servislerin çalıştığını ve hangi yazılımların kullanıldığını belirlemek.

            * Araçlar: Netcat, Telnet.


            * Web Tarayıcı Taraması: Web sunucularındaki açıklıkları ve dizinleri analiz etmek.

            * Araçlar: Dirb, Gobuster.
    
    Bu işlemler sonucunda elde edilen bilgiler aşağıdaki gibi olmaktadır;
        
        # Toplanan Bilgi Türleri

            Ağ Bilgisi: IP adres aralığı, açık portlar, kullanılan ağ cihazları.

            Sistem Bilgisi: İşletim sistemi versiyonları, çalışan yazılımlar ve uygulamalar.

            Kullanıcı Bilgisi: Kullanıcı adları, e-posta adresleri ve sosyal medya profilleri.

            sGüvenlik Önlemleri: Kullanılan güvenlik duvarı, IDS/IPS sistemleri.
        
        
        # Reconnaissance’ın Teknik Araçlarla Uygulanışı

            DNS Taraması:

                

            Subdomain Keşfi:

               

            Web Servis Bilgisi Keşfi:

                





---

# Saldırının Planlanması İçin Reconnaissance'ın Önemi

        Reconnaissance sırasında toplanan bilgiler, saldırının başarı oranını doğrudan etkiler.

        Bu bilgiler, saldırganın hangi zafiyetleri hedef alacağını belirlemesini sağlar (örneğin, bir açık port üzerinden zararlı yazılım yüklemek).
      
    
# Reconnaissance ve Discovery arasindaki farklar
    
        * Reconnaissance:genelde hedefi uzaktan analiz eder ve saldırının planlama aşamasına hizmet eder.
        
        * Discovery: hedef sistem içinde çalışır ve saldırının ilerleyen aşamalarında spesifik detaylar sağlar.
        
        
        ikisi arasindaki temel fark "Reconnaissance" pasif olarak sistem hakkinda tarama yapar uzaktaki sistem hakkinda bilgi edinme yapmaktadir.

        "Discovery" ise uzaktaki sistemden sonra sisteme sizan kisinin sistem hakkinda bilgi toplama işlemidir. Burada temel amac sistem tarafına aktif tarama atılarak sistem hakkındaki bilgilerin toplanmasıdır.


# Reconnaissance Tekniklerinin Genel Özeti

    Hangi Bilgileri ortaya çıkarır?

>> Hedefin Ağ yapısı ve Bileşenleri,
>> Sistem Bilgileri,
>> Kullanıcı ve Kimlik Bilgileri,
>> Organizasyonel Bilgiler,
>> Web ve Uygulama Bilgileri,
>> Dns ve Alan Adı Bilgileri,
>> Açık Zaafiyetler,
>> Sosyal Mühendislik için bilgiler,

gibi bilgileri ortaya çıkarır.


    HANGİ ARAÇLAR İLE BU BİLGİLERİ BULMA İŞLEMİ GERÇEKLEŞTİRİLİR?

    "Pasif" ve "Aktif" tarama için farklı araçlar kullanılır.Bunlar;

>> Maltego (OSINT) --> (PASİF)
>> SpiderFoot(OSINT) --> (PASİF)
>> theHarvester(OSINT) --> (PASİF)
>> Recon-ng(OSINT) --> (PASİF)

>> whois(DNS) --> (PASİF)
>> nslookup(DNS) --> (PASİF)
>> dig(DNS) --> (PASİF)
>> Sublist3r(DNS) --> (PASİF) 

>> Google Dorking(WEB) --> (PASİF)
>> Shodan (WEB) --> (PASİF)
>> Censys (WEB) --> (PASİF)
>> Social-Searcher (WEB) --> (PASİF)
- 
- 
>> Nmap (PORT) --> (AKTİF)
>> Masscan (PORT) --> (AKTİF)
>> Netcat (PORT) --> (AKTİF)

>> Wireshark (AĞ) --> (AKTİF)
>> tcpdump (AĞ) --> (AKTİF)
>> Ettercap (AĞ) --> (AKTİF)

>> Burp Suite (WEB UYGULAMASI) --> (AKTİF)
>> OWASP ZAP (WEB UYGULAMSI) --> (AKTİF)
>> Nikto (WEB UYGULAMASI) --> (AKTİF)
>> DirBuster (WEB UYGULAMASI) --> (AKTİF)

>> Metasploit(Payload) --> (AKTİF)

# ÖRNEK TEKNİKLER


1- Active Scanning (T1595),
2- Search Open Technical Databases (T1596),
3- Phishing For Information (T1598),
4- Gather Victim Host Information(T1592),
5- Gather Victim Network Information (T1590),
6- Gather Victim Identity Information (T1598),



# ACTIVE SCANNING(T1595)

*   Hedef sistemler üzerinde açık portları, çalışan servisleri ve zafiyetleri tespit etmek için aktif tarama yapılır.
*   Alt Teknikler:
    - Scanning IP Blocks(T1595.001)
      : IP bloklarını tarayarak hedef ağdaki cihazları tespit etme.
    - Vulnerability Scanning(T1595.002)
      : Hedef sistemlerdeki açıkları tespit etmek için tarama.
    - Wordlist Scanning(T1595.003)
      : Özel olarak hazırlanmış kelime listeleriyle tarama yapılması.

# SEARCH OPEN TECHNICAL DATABASES(T1596)

*   Shodan, Censys gibi açık teknik veri tabanlarından bilgi toplanarak bu işlemler yapılır.
*   Alt Teknikler:
    - DNS/Passive DNS(T1596.001)
      : DNS kayıtlarını inceleyerek hedef hakkında bilgi toplama.
    - WHOIS(T1596.002)
      : Domain sahipliği ve iletişim bilgilerini öğrenmek için WHOIS sorguları kullanılır.
    - Digital Certificates(T1596.003)
      : SSL/TLS sertifikalarından sunucu bilgisi toplama.
    - CDNs(T1596.004)
      : İçerik dağıtım ağlarından (Content Delivery Networks) veri toplama.
    - Scan Databases(T1596.005)
      : Açık tarama ile veritabanlarından bilgi toplama.

# PHISHING FOR INFORMATION(T1598)

* Hedef kullanıcıları kimlik avı yoluyla bilgi paylaşmaya ikna etme.
* Alt Teknikler:
    - Spear Phishing Service(T1598.001)
     : Özel hedeflere yönelik kimlik avı saldırıları.
    - Social Engineering(T1598.002)
     : İnsan etkileşimlerini kullanarak bilgi toplama.

# GATHER VICTIM HOST INFORMATION(T1589)

* Hedef sistemle ilgili IP adresi, işletim sistemi türü gibi bilgileri toplama işlemi.
* Alt Teknikler:
    - Credentials(T1589.001)
     : Kullanıcı adı ve şifre bilgisi toplama.
    - Account Information(T1589.002)
     : Hesap türleri ve kullanıcı rolleri hakkında bilgi toplama.
    - Email Addresses(T1589.003)
     : E-posta adresleri toplama.


# GATHER VICTIM INDETITY INFORMATION(T1589.004)

* Hedef kişinin kimlik bilgilerini toplama (örneğin, kimlik numaraları, doğum tarihi).

# GATHER VICTIM NETWORK INFORMATION(T1590)

* Hedef ağ topolojisi, kullanılan protokoller ve cihazlar hakkında bilgi toplama.
* Alt Teknikler:
    - Domain Properties(T1590.001)
      : Hedef domain hakkında bilgi toplama.
    - DNS(T1590.002)
      : DNS çözümleme ve zone transfer ile bilgi toplama.
    - NETWORK TRUST DEPENDENCIES(T1590.003)
      : Ağda güvendiği diğer cihaz veya sistemleri tespit etme.
    - NETWORK SECURITY APPLIANCES(T1590.004)
      : Ağ güvenlik cihazları hakkında bilgi toplama.

# GATHER VICTIM ORGANIZATION INRFORMATION(T1591)

* Hedef organizasyon hakkında bilgi toplanması.
* Alt Teknikler:
    - Business Relationships(T1591.001)
      : İş ortaklıklarını inceleme.
    - Organizational Demographics(T1591.002)
      : Çalışan sayısı, organizasyon yapısı gibi bilgiler.
    - Physical Locations(T1591.003)
      : Fiziksel adres ve konum bilgileri.

# SEARCH CLOSED SOURCES(T1597)

* Hedefle ilgili halka açık olmayan kaynaklardan bilgi toplama.
* Alt Teknikler:
    - Threat Intelligence Reports(T1597.001)
      : Tehdit raporlarını analiz etme.
    - Commercial Sources(T1597.002)
      : Ticari bilgi sağlayıcılardan veri toplama.
    - Dark Web(T1597.003)
      : Dark Web'deki kaynaklardan veri toplama.


# SEARCH OPEN WEBSITES/DOMAINS(T1593)

* Açık web sitelerinden veya alan adlarından bilgi toplama.
* Alt Teknikler:
    - Social Media(T1593.001)
      : Sosyal medya platformlarından bilgi toplama.
    - Search Engines(T1593.002)
      : Google, Bing gibi arama motorlarını kullanma.
    - Code Repositories(T1593.003)
      : GitHub gibi kod havuzlarından bilgi toplama.

# RECONNAISSANCE'IN SALDIRI ZİNCİRİNDEKİ ROLÜ

  # 1. ADIM : PLANLAMA VE BİLGİ TOPLAMA

    : Reconnaissance, saldırganın hedefle ilgili bilgi topladığı ve saldırıyı planladığı aşamadır. Bu bilgiler, hedefin zafiyetlerini tespit etmeye ve saldırının sonraki adımlarını tasarlamaya olanak tanır.
    
    İki yöntem ile gerçekleşir:

      1- Aktif Teknik kullanımı: 
        Port tarama, zafiyet tarama gibi hedefle doğrudan etkileşim kurulması.
      2- Pasif Teknik kullanımı: 
         Sosyal medya, DNS sorguları gibi dış kaynaklardan bilgi toplama.

  # 2. ADIM : SALDIRI ZİNCİRİNDEKİ KONUMU

    : Reconnaissance, Kill Chain modeli veya benzeri çerçevelerde genellikle ilk basamaktır

    * Reconnaissance (Keşif): Hedefin dijital ayak izi, ağ topolojisi, çalışan servisler ve zafiyetler tespit edilir.
    * Silahlanma (Weaponization): Toplanan bilgilere dayanarak saldırı araçları hazırlanır (örneğin, özel bir exploit tasarlanması).
    * Teslimat (Delivery): Saldırı aracının hedefe ulaştırılması (örneğin, zararlı e-posta).
    * Kötü Amaçlı Yazılımın Yüklenmesi (Exploitation): Tespit edilen zafiyet üzerinden hedef sistemin ele geçirilmesi.

  # 3. ADIM : RECONNAINSSANCE'İN KRİTİK ÖNEMİ

    * Doğru Bilgi = Başarılı Saldırı: Keşif aşamasında yeterince bilgi toplanamazsa, sonraki aşamalarda başarısızlık olasılığı artar.

    * Hedefin Zafiyetlerinin Anlaşılması: Hangi sistemlerin saldırıya daha açık olduğunu anlamak için kritik bir adımdır.

    * Saldırı Vektörünün Belirlenmesi: Saldırgan, hangi yöntemlerle (örneğin, kimlik avı, açık portlar üzerinden erişim) saldırıyı gerçekleştireceğine bu aşamada karar verir.

>> ÖRNEK SENARYO

  Diyelimki bir saldırgan belirli bir şirkete ait internet adresini hedef alıyor:

  Reconnaissance sırasında:

    1) Şirketin kullandığı web sunucusu türü (örneğin Apache <version x>) belirlenir.
    2) SSL sertifikası ve DNS kayıtları analiz edilir.
    3) Açık portlar taranarak çalışan servisler tespit edilir.
    4) Bu bilgilerle, saldırgan belirli bir güvenlik açığına (örneğin, bir Apache zafiyeti) yönelik exploit geliştirebilir veya hazır bir araç kullanabilir.










 




