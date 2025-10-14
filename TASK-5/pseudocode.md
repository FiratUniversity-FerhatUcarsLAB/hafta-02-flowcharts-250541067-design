ALGORİTMA Akilli_Ev_Guvenlik_Sistemi

BAŞLA

    Sistem_Ac()
    kullanıcıKodu ← Kullanıcı_Kodu_Al()
    sifre ← Sifre_Al()

    EĞER Giriş_Dogrula(kullanıcıKodu, sifre) = DOĞRU İSE
        Durum_Goster("Sistem aktif.")
        sensörVerisi ← Sensör_Durumu_Oku()

        EĞER sensörVerisi = "Hareket" VEYA sensörVerisi = "Kapı Açık" İSE
            Alarm_Calistir()
            Bildirim_Gonder("Evde hareket algılandı!")
        DEĞİLSE
            Durum_Goster("Her şey normal.")
        BİTİR_EĞER
    DEĞİLSE
        EKRANA_YAZ("Yetkisiz erişim! Sistem kilitlendi.")
        Sistem_Kilitlendi()
    BİTİR_EĞER

    Sistem_Kapat()

BİTİR
