# 📊 SWOT Analizi — Bu Repo / Çalışma

[← Ana sayfa](README.md)

Bu analiz, **Hafta 1–5 laboratuvar çalışmasının kendisini** (yöntem, içerik ve repo olarak sunumu) değerlendirir — makineyi veya üreticiyi değil.

|  | **Yardımcı** | **Zararlı** |
|---|---|---|
| **İç** | 💪 Güçlü yönler | ⚠️ Zayıf yönler |
| **Dış** | 🚀 Fırsatlar | 🌩️ Tehditler |

---

## 💪 Güçlü Yönler (Strengths)

- **Gerçek bir makineye bağlı:** Soyut bir "örnek PLC" yerine Ermaksan Power-Bend Pro gibi sahada yaygın, somut bir abkant pres üzerinden çalışılıyor; tehlikeler (koç–kalıp ezilmesi, kalkan sac) gerçek.
- **Emniyet ve siber güvenliği tek zincirde birleştiriyor:** Hız geçiş noktası ↔ AKAS susturma kesişimi gibi, iki disiplinin buluştuğu kritik noktayı açıkça tanımlıyor.
- **Haftalar birbirini besliyor:** Safety Function Map → Zone/Conduit → Risk Register → Secure Architecture mantıksal bir akış oluşturuyor; her çıktı bir Evidence Pack başlığına oturuyor.
- **İnsan odaklı risk kuralları:** "S=3 ise öne al" ve "Altın kural: bu, hattaki insana ne yapar?" yaklaşımı, skorun ciddi bir yaralanmayı gizlemesini engelliyor.
- **Şeffaflık:** Doğrulanamayan her nokta *(varsayım)* olarak işaretlenmiş, kaynaklar listelenmiş, sorumluluk reddi açık.
- **Tarafsızlık:** Hafta 4 çözüm dayatmıyor, gereksinim tanımlıyor; tasarım kararını üreticiye bırakıyor.
- **Olgun zafiyet yönetimi yaklaşımı:** Hafta 5, CVSS skoruna körü körüne tepki vermek yerine üç şart kontrolü, önce test, yedek/geri dönüş planı ve yama sonrası emniyet re-validasyonunu içeren gerçekçi bir karar akışı kuruyor.
- **Sürüm kontrollü, okunabilir format:** Markdown + Mermaid diyagramlarıyla GitHub'da doğrudan okunabiliyor, değişiklik geçmişi izlenebiliyor.

## ⚠️ Zayıf Yönler (Weaknesses)

- **Varsayımlara dayalı mimari:** Uzak teşhis bağlantısı, fabrika ağı bağlantısı ve CNC–FPSC veri paylaşımının ayrıntıları doğrulanmamış; en yüksek riskli senaryo (R1) bu varsayımlardan birine dayanıyor.
- **Sahada doğrulama yok:** Firmayla iletişime geçilmemiş; gerçek konfigürasyon, firmware sürümleri ve ağ topolojisi görülmemiş.
- **Basit risk modeli:** L × S × E (1–3) eğitim için anlaşılır ama ince ayrım yapamıyor; EN ISO 12100 / ISO 13849-1 risk grafiği veya IEC 62443-3-2 ile resmî olarak eşleştirilmemiş.
- **Sınırlı senaryo sayısı:** Risk Register yalnızca 3 senaryo içeriyor; içeriden kötü niyetli kullanıcı, tedarik zinciri (firmware güncellemesi) veya fiziksel HMI müdahalesi gibi kapılar ayrı ele alınmamış.
- **PL değeri doğrulanmamış:** PLr e / Kat. 4 "tipik beklenti" olarak alınmış; hesaplama (MTTFd, DC, CCF) yapılmamış.
- **Eksik kapsam:** Hafta 6–7 (CRA olayı, YZ) bu repoda henüz yok; uçtan uca resim tamamlanmamış.
- **Örnek zafiyet kaydı:** Hafta 5'teki CVE (CVE-XXXX-XXXX, Component X) eğitim amaçlı bir yer tutucudur; gerçek bir SBOM veya üretici bildirimi üzerinden çalışılmamıştır.

## 🚀 Fırsatlar (Opportunities)

- **Mevzuat takvimi:** CRA bildirim yükümlülükleri (11 Eylül 2026) yürürlükte, Makine Yönetmeliği 2023/1230 (20 Ocak 2027) yaklaşıyor — bu tür emniyet + siber analizlere talep artıyor.
- **Şablon olarak yeniden kullanım:** Aynı föy yapısı başka makinelere (pres, robot hücresi, lazer kesim) kolayca uyarlanabilir; repo bir "laboratuvar şablonu" hâline getirilebilir.
- **Portföy değeri:** Disiplinler arası (OT güvenliği + fonksiyonel emniyet) bir çalışma olarak iş başvurularında ve mesleki gelişimde gösterilebilir.
- **Topluluk katkısı:** Açık repo olarak paylaşılırsa diğer katılımcılar issue / pull request ile senaryo ve iyileştirme ekleyebilir.
- **Derinleştirme:** IEC 62443-3-2 hedef güvenlik seviyeleri (SL-T), ISO 13849 PL hesabı veya Hafta 5'in üzerine CycloneDX/SPDX formatında gerçek bir SBOM ve CSAF/VEX bildirimleri eklenerek eğitim düzeyinden profesyonel düzeye taşınabilir.
- **Üretici diyaloğu:** Varsayımlar listesi, ileride üretici veya bir kullanıcı firmayla doğrulama görüşmesi için hazır bir soru listesi işlevi görür.

## 🌩️ Tehditler (Threats)

- **Yanlış yorumlanma riski:** İçerik resmî bir denetim veya uygunluk değerlendirmesi gibi algılanabilir; sorumluluk reddi görünür kalmalı.
- **Marka / itibar hassasiyeti:** Belirli bir üretici adıyla saldırı senaryoları yayınlamak, varsayım olduğu belirtilse bile, olumsuz algı veya hukuki itiraz doğurabilir. Repo **public** yapılmadan önce bu değerlendirilmeli.
- **Saldırı yol haritası endişesi:** Senaryolar yüksek seviyeli olsa da, kamuya açık paylaşımda ayrıntı düzeyinin genel kalmasına dikkat edilmeli.
- **Standartların güncellenmesi:** EN 12622, ISO 13849-1 ve IEC 62443 serilerinin revizyonları, içeriğin kısa sürede eskimesine yol açabilir.
- **Telif / içerik sahipliği:** Föy şablonu INSPECCO × KRIPTARIUM'a aittir; paylaşım ve lisans koşulları bootcamp düzenleyicileriyle netleştirilmeli.
- **Teknolojik değişim:** Yeni CNC/emniyet kontrolörü nesilleri (ör. ağ üzerinden emniyet protokolleri) mimariyi değiştirebilir; analiz mevcut modele özgü kalabilir.

---

## 🎯 Stratejik çıkarımlar

| Strateji | Eylem |
|---|---|
| **SO** (güç × fırsat) | Föy yapısını genel bir şablona dönüştür; CRA/Makine Yönetmeliği takvimine bağlı bir "kontrol listesi" ekle. |
| **WO** (zayıflık × fırsat) | Varsayımlar listesini üretici/kullanıcı firma ile doğrulama görüşmesine dönüştür; PL hesabını ve SL-T analizini ekle. |
| **ST** (güç × tehdit) | Şeffaflık ve tarafsızlık notlarını her sayfada koru; repo görünürlüğünü (private/public) bilinçli seç. |
| **WT** (zayıflık × tehdit) | Public paylaşımdan önce marka adını genelleştirmeyi (ör. "CNC abkant pres") ve senaryo ayrıntısını gözden geçirmeyi değerlendir. |
