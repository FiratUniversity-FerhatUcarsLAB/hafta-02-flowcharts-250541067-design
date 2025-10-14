ALGORİTMA Hastane_Randevu_Sistemi

BAŞLA

    Kullanıcı_Girişi()
    tc ← TC_Kimlik_Al()
    sifre ← Şifre_Al()

    EĞER Giriş_Dogrula(tc, sifre) = DOĞRU İSE
        Branş_Listesi_Goster()
        branş ← Kullanıcıdan_Brans_Sec()

        Doktor_Listesi_Goster(branş)
        doktor ← Kullanıcıdan_Doktor_Sec()

        Tarih_Saati_Goster(doktor)
        tarih ← Kullanıcıdan_Tarih_Sec()

        EĞER Randevu_Müsait_Mi(doktor, tarih) = DOĞRU İSE
            Randevu_Kaydet(tc, doktor, tarih)
            EKRANA_YAZ("Randevunuz başarıyla oluşturuldu.")
        DEĞİLSE
            EKRANA_YAZ("Seçilen tarih dolu. Lütfen başka bir tarih seçiniz.")
        BİTİR_EĞER
    DEĞİLSE
        EKRANA_YAZ("Hatalı TC veya şifre. Lütfen tekrar deneyin.")
    BİTİR_EĞER

BİTİR
