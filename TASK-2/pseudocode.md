ALGORİTMA Online_Alisveris_Sepeti

BAŞLA

    sepet ← BOŞ_LISTE_OLUŞTUR()

    TEKRAR
        ürünü_göster()
        ürün ← Kullanıcıdan_Ürün_Seç()
        
        EĞER ürün ≠ "Çıkış" İSE
            adet ← Kullanıcıdan_Adet_Al()
            sepete_ekle(sepet, ürün, adet)
            EKRANA_YAZ(ürün, " sepete eklendi.")
        DEĞİLSE
            ÇIKIŞ_YAP ← DOĞRU
        BİTİR_EĞER
    SEPETE_EKLEME_BITENE_KADAR

    toplam ← Sepet_Toplam_Hesapla(sepet)
    EKRANA_YAZ("Sepet Toplamı: ", toplam, " TL")

    ödeme_yöntemi ← Kullanıcıdan_Ödeme_Yöntemi_Seç()

    EĞER ödeme_yöntemi = "Kredi Kartı" VEYA "Banka Kartı" İSE
        Kart_Bilgilerini_Al()
        Ödeme_Onayla()
        EKRANA_YAZ("Ödeme başarılı! Siparişiniz hazırlanıyor.")
    DEĞİLSE
        EKRANA_YAZ("Kapıda ödeme seçildi. Siparişiniz hazırlanıyor.")
    BİTİR_EĞER

BİTİR
