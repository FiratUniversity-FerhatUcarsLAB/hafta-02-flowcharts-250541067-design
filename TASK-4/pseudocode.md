ALGORİTMA Universite_Ders_Kaydi_Sistemi

BAŞLA

    Kullanıcı_Girişi()
    ogrenciNo ← Ogrenci_Numara_Al()
    sifre ← Sifre_Al()

    EĞER Giriş_Dogrula(ogrenciNo, sifre) = DOĞRU İSE
        Ders_Listesi_Goster()
        TEKRAR
            ders ← Kullanıcıdan_Ders_Sec()
            EĞER ders ≠ "Bitir" İSE
                EĞER Kontenjan_Müsait_Mi(ders) = DOĞRU İSE
                    Derse_Kaydet(ogrenciNo, ders)
                    EKRANA_YAZ(ders, " başarıyla eklendi.")
                DEĞİLSE
                    EKRANA_YAZ("Ders kontenjanı dolu.")
                BİTİR_EĞER
            DEĞİLSE
                ÇIKIŞ ← DOĞRU
            BİTİR_EĞER
        DERS_SECME_BITENE_KADAR
        EKRANA_YAZ("Ders kaydı tamamlandı.")
    DEĞİLSE
        EKRANA_YAZ("Hatalı öğrenci numarası veya şifre.")
    BİTİR_EĞER

BİTİR
