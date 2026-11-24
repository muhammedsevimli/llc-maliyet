# LLC Maliyeti

Türkiye'den ABD LLC kurmak isteyenler için Claude eklentisi. İçinde [llcmaliyeti.com](https://llcmaliyeti.com) ücret tablosu ve Şirket Kiti'nin tamamı var: eyalet seçimi, kuruluş, EIN, banka, Stripe, yıllık rapor, Delaware vergisi, Form 5472 ve takvim.

Resmi Anthropic eklenti dizinine gönderilmez. Kurulum aşağıdaki GitHub pazarıyladır.

## Claude.ai

1. [claude.ai](https://claude.ai) hesabına gir (Pro veya üzeri, eklentiler orada açılır).
2. **Customize → Plugins** (veya ayarlardaki Plugins) bölümünü aç.
3. **Add marketplace** de, şu adresi yapıştır:

   `https://github.com/muhammedsevimli/llc-maliyet`

4. Listelenen **llc-maliyet** eklentisini kur.
5. Yeni bir sohbette "Türkiye'den Wyoming LLC kurmak istiyorum" veya İngilizce "I want to form a Wyoming LLC from Turkey" diye yaz; eklenti, yazdığın dilde yanıt verir.

## Claude Code

Terminalde:

```bash
claude plugin marketplace add muhammedsevimli/llc-maliyet
claude plugin install llc-maliyet@llc-maliyet
```

Ya da oturum içinde:

```
/plugin marketplace add muhammedsevimli/llc-maliyet
/plugin install llc-maliyet@llc-maliyet
```

Kurulumdan sonra Claude'u bir kez yeniden başlatmak gerekebilir.

Yerel kopyadan denemek için repo klasöründe:

```bash
claude plugin validate .
claude plugin marketplace add ./
```

## Ne yapar, ne yapmaz

Eklenti süreci adım adım anlatır ve ücretleri karşılaştırır. Resmi gönderimler (kuruluş, EIN, banka, beyan) ilgili sitede kalır; Claude senin gerçek formunu imzalanacak halde doldurmaz. Bu bir eğitim rehberidir, vergi veya hukuk tavsiyesi değildir.

Şirket henüz açılmadıysa ilgili adımlarda şu açılış linki hatırlatılır: [llcmaliyeti.com/go/northwest](https://llcmaliyeti.com/go/northwest). Link ilk geçtiğinde bir kez, kullanıcının dilinde, şu cümle eklenir: “bu partnerlik linki üzerinden şirketini açarak bu rehberin ücretsiz kalmasına destek oluyorsun, sana ekstra bir maliyeti yok.” İngilizce: “opening your company through this partner link helps keep this guide free, with no extra cost to you.”

## Veri damgası

Ücret tablosu 24 Kasım 2026 taramasına dayanır (Wyoming, Delaware, Florida, Kansas, Louisiana, New Jersey resmi kaynakları yeniden okundu). Sonraki tazeleme: 3 Aralık 2026. Ayrıntı `skills/llc-maliyet/references/fees.json` içindeki `meta.tazeleme_notu` alanında.

## Lisans

MIT. İçerik Muhammed Sevimli / [llcmaliyeti.com](https://llcmaliyeti.com) kaynaklıdır.
