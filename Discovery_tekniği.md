 # DISCOVERY TEKNİĞİ

 * Discovery tekniği bir sistem, ağ veya ortam hakkında bilgi toplamak için kullandığı yöntemlerin genel adıdır.Bu teknikler hedef sisteme erişim sağlamış    saldırganın sistem üzerindeki hangi kaynaklara erişim sağlayabileceğini ve bu erişim sonrası ulaştığı kaynakların nasıl çalıştığını ve nasıl kullanıldığını anlamarına yardım eder.

 * Temel amacı:
    1- Bilgi toplama,
    2- Yanal Hareket yapma,
    3- Hedef Seçimi,
    4- Saldırı Planlama,

    # 1- BİLGİ TOPLAMA:
        : Ağ yapısı ve bu ağ yapısı altında bağlı cihazları, kullanıcı hesapları vb. hakkında bilgi edinmek.
    
    # 2- YANAL HAREKET(LATERAL MOVEMENT):
        : Daha fazla hedefe erişim sağlamak için gerekli bilgiyi toplamak.
    
    # 3- HEDEF SEÇİMİ:
        : Kritik sistemleri veya süreçleri belirlemek.
    
    # 4- SALDIRI PLANLAMA:
        : Sistem üzerinde hangi yöntemlerin etkili olacagını anlamak ve saldırı stratejisini o sisteme göre geliştirmek.


# TEKNİKLER:
>> 1. Account Discovery (Hesap Keşfi-T1087)
    : Sistemde mevcut kullanıcı hesaplarını belirlemek.
    ALT TEKNİKLER:
        * T1087.001 - Local Account Discovery (Yerel Hesap Keşfi):
            : Yerel kullanıcı hesaplarını listelemek için kullanılır. Örneğin, Windows'ta net user, Linux'ta /etc/passwd dosyasını okumak.

        * T1087.002 - Domain Account Discovery (Domain Hesabı Keşfi):
            : Etki alanındaki (Domain) kullanıcıları ve grupları belirlemek için kullanılır. Örneğin, net user /domain komutu.

        * T1087.003 - Email Account Discovery (E-posta Hesabı Keşfi):
            : Sistemde yapılandırılmış e-posta hesaplarını tespit eder. Outlook veya e-posta istemcisi yapılandırmalarını kontrol ederek bilgi toplar.

>> 2. File and Directory Discovery (Dosya ve Dizin Keşfi-T1083)
    : Önemli dosya ve dizinleri bulmak.
        Yöntemler:

            1- Dosya sistemi üzerinde gezinme komutları kullanılır (dir, ls).
            2- Hassas bilgiler içerebilecek dosyaları aramak.

>> 3. Network Service Discovery (Ağ Servisi Keşfi-T1046)
    : Ağdaki aktif servisleri ve portları tespit etmek.
        Yöntemler:

            1- Port taramaları (nmap, netstat).
            2- Kritik hizmetlerin (DNS, FTP, SMB) tespiti.

>> 4. Process Discovery (Süreç Keşfi-T1057)
    : Sistemde çalışan işlemleri öğrenmek.
        Yöntemler:

            1- Mevcut süreçleri listelemek (tasklist, ps).
            2- Hedeflenebilecek veya sonlandırılacak kritik süreçleri bulmak.

>> 5. System Information Discovery (Sistem Bilgisi Keşfi-T1082)
    : İşletim sistemi ve sistem yapılandırması hakkında bilgi toplamak.
    Yöntemler:

        1- Sistem bilgisi komutları (systeminfo, uname -a).
        2- Yüklü yazılımlar ve sistem sürümü bilgileri.

>> 6. System Network Connections Discovery (Ağ Bağlantıları Keşfi-T1049)
    : Mevcut ağ bağlantılarını belirlemek.
    Yöntemler:

        1- Aktif bağlantıları görmek için netstat kullanılır.
        2- Bağlantıların hedef IP adreslerini analiz etmek.

>> 7. Network Share Discovery (Ağ Paylaşımları Keşfi-T1135)
    : Paylaşılan klasörler ve ağ sürücülerini bulmak.
    Yöntemler:

        1- Ağ paylaşımını listeleme (net view, smbclient).
        2- Paylaşılmış dosyaları incelemek.


>> 8. Peripheral Device Discovery (Çevre Birimi Keşfi-T1120)
    :  Sisteme bağlı çevresel aygıtları bulmak (USB, yazıcılar vb.).
    Yöntemler:
    
        1- Cihaz listesini çıkarmak (device manager, lsusb).
        2- Taşınabilir cihazlara veri sızdırma potansiyeli değerlendirilir.

>> 9. Remote System Discovery (Uzak Sistem Keşfi-T1018)
    : Ağdaki diğer sistemleri tespit etmek.
    Yöntemler:

        1- Uzak sistemleri listelemek (ping, tracert).
        2- Ağdaki diğer makineleri haritalamak.

>> 10. Software Discovery (Yazılım Keşfi-T1518)
    :  Sistemde yüklü yazılımları öğrenmek.
    Yöntemler:

        1- Yüklü programları görüntülemek (wmic product get, dpkg -l).
        2- Yazılım güvenlik açıklarını tespit etmek için kullanılır.
    Alt teknikler:

        1- Security Software Discovery (Güvenlik Yazılımı Keşfi-T1518.001)
        : Antivirüs ve güvenlik duvarı gibi yazılımları tespit etmek için kullanılır. 
           
           * Örneğin, tasklist veya wmic komutlarıyla güvenlik süreçleri aranır.

>> 11. Security Software Discovery (Güvenlik Yazılımı Keşfi-T1518.001)
    : Antivirüs, güvenlik duvarı gibi güvenlik araçlarını tespit etmek.
    Yöntemler:

        1- Yüklü güvenlik yazılımlarını listelemek.
        2- Güvenlik yazılımını atlatma yöntemleri planlanır.

>> 12. System Time Discovery (Sistem Zamanı Keşfi-T1124)
    : Sistem saatini ve zaman dilimini öğrenmek.
    Yöntemler:

        1- Sistem zamanı kontrolü (date, time).
        2- Loglar veya zaman tabanlı güvenlik kontrollerini atlatmak için önemlidir.

>> 13. Application Window Discovery (Uygulama Penceresi Keşfi-T1010)
    : Hangi uygulamaların aktif olduğunu belirlemek.
    Yöntemler:

        1- Mevcut pencere başlıklarını almak.
        2- Kullanıcının hangi uygulamaları kullandığını tespit etmek.

>> 14. Browser Bookmark Discovery (Tarayıcı Yer İmleri Keşfi-T1217)
    : Tarayıcıdaki kaydedilmiş yer imlerini bulmak.
    Yöntemler:

        1- Tarayıcı dosyalarını analiz etmek.
        2- Kullanıcının sık eriştiği siteleri öğrenmek.



# DISCOVERY VE RECONNAISSANCE ARASINDAKİ FARKLAR

1- AŞAMA:

    * DISCOVERY: Saldırı sonrası (iç sistemde) tespit yapar.
    * RECONNAISSNCE : Saldırı öncesi (hazırlık aşaması) dış sistemlerde tespit yapar

2- HEDEF: 

    * DISCOVERY: İç sistemde detaylı bilgi toplama
    * RECONNAISSNCE: Dışarıdan erişilebilir bilgiler.

3- YÖNTEMLER:
    
    * DISCOVERY: Ağ taramaları, sistem yapılandırması
    * RECONNAISSNCE: OSINT, sosyal mühendislik, DNS sorguları

4- ETKİLEŞİM:	

    * DISCOVERY: Hedef sistemle etkileşim gerektirir.
    * RECONNAISSNCE:  Hedef sistemle doğrudan etkileşim gerekmez.


- Her iki teknik arasındaki fark olarak "Reconnaissance" saldırıdan önce dışarıdan bilgi toplama olarak görev yaparken, "Discovery" sisteme sızdıktan sonra iç bilgileri toplama işlemi yapar. 