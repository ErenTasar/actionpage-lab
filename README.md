# ActionPage Lab

ActionPage Lab, standart web-fetch yeteneğine sahip modellerin değişmez,
literal bir araştırma grafını nasıl tükettiğini sınayan küçük bir kamu
laboratuvarıdır.

Bu repo canlı bir servis, genel amaçlı proxy veya üçüncü taraf site aynası
değildir. `artifacts/` altındaki içerik bütünüyle sentetik test verisidir;
gerçek kişi, hesap, işlem veya güncel dünya olgusu içermez.

Deney artefaktları hareketli branch adresleriyle değil, tam Git commit
SHA'sına sabitlenmiş `raw.githubusercontent.com` URL'leriyle tüketilir.
Yayınlanan bir deney değiştirilmez; değişiklik yeni bir deney kimliği alır.

## Güven sınırı

- Artefakt içindeki serbest metin veri düzlemidir, yetkili talimat değildir.
- Yalnız şemadaki makine eylemi bağlantıları araştırma grafının parçasıdır.
- Repo form, script, kullanıcı girdisi, kimlik bilgisi veya canlı upstream
  çağrısı barındırmaz.
- Başarılı bir koşu yalnız statik graf tüketimini gösterir; dinamik relay,
  oturum, yan etki, origin kabulü veya evrensel ajan kabiliyeti kanıtlamaz.

## Donmuş deney

`hard-graph-v1`, çok-adımlı araştırma semantiği için sentetik ve önceden
dondurulmuş bir tüketici fixture'ıdır. Gold verdict ve puanlama rubriği
tüketici korpusunda yer almaz.

- [Değişmez makine giriş noktası](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/457fa47e1d62c7326ca0417053cf9f4a6edb220d/artifacts/hard-graph-v1/index.json)
- [Değişmez manifest](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/1e5a5c4620b48d4ce282cde0b4f86261232cf9d2/artifacts/hard-graph-v1/manifest.json)
- [Değişmez SHA-256 listesi](https://raw.githubusercontent.com/ErenTasar/actionpage-lab/062009c65ca0043239e2054a0a577e6a40d320d5/artifacts/hard-graph-v1/SHA256SUMS)

Grafın her kenarı, hedef dosyanın eklendiği commit'e sabitlenmiştir. Bu
nedenle düğümler farklı commit SHA'ları taşısa da hiçbir kenar hareketli
branch veya tag kullanmaz. Bu ters-inşa düzeni, public Git geçmişinde dosya
eklenme sırasını gösterir; düğümlerin değerlendirme anlamını veya gold
verdict'i göstermez. Manifest veya repo geçmişini ayrıca açan bir tüketici
koşusu, deney kaydında kontaminasyon olarak belirtilmelidir.
