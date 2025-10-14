ALGORİTMA ATM_Para_Cekme

BAŞLA

    Kartı_Tak()
    PIN ← PIN_Gir()

    EĞER PIN_Dogrula(PIN) = DOĞRU İSE
        bakiye ← Hesap_Bakiyesi_Al()
        miktar ← Para_Miktarı_Gir()

        EĞER miktar <= bakiye İSE
            EĞER miktar % 10 = 0 İSE
                bakiye ← bakiye - miktar
                Para_Ver(miktar)
                Hesap_Bakiyesi_Guncelle(bakiye)
                EKRANA_YAZ("İşlem başarılı! Yeni bakiyeniz: ", bakiye)
            DEĞİLSE
                EKRANA_YAZ("Lütfen 10 TL'nin katı bir miktar giriniz.")
            BİTİR_EĞER
        DEĞİLSE
            EKRANA_YAZ("Yetersiz bakiye.")
        BİTİR_EĞER
    DEĞİLSE
        EKRANA_YAZ("Geçersiz PIN. Lütfen tekrar deneyin.")
    BİTİR_EĞER

    Kartı_İade_Et()

BİTİR
