# Büyüleyici Arka Plan Resimleri ve Metin Konumlandırma

Bu projede, bir web sayfasının **arka plan resmini** (tam sayfa veya belirli oranda) nasıl uygular, sayfanın merkezine metin konumlandırır ve optimize edilmiş bir şekilde kullanırız, bunları öğreneceksiniz.

## Özet

1. **Arka Plan Resmi Ekleme**
    - `HTML` ve `body` etiketlerine veya istediğiniz kapsayıcı elemana tam yükseklik (%100 veya `100vh`) vererek arka plan resmi ekleyebilirsiniz.
    - `background-image`, `background-size: cover` veya `img` etiketi gibi yöntemlerle resmi sayfaya yerleştirebilirsiniz.

2. **Responsive Yükseklik ve Genişlik**
    - Sabit piksel değerleri (`px`) yerine, **yüzde** (`%`) veya **viewport** tabanlı birimleri (`vh`, `vw`) kullanarak farklı ekran çözünürlüklerine uyum sağlayabilirsiniz.
    - Örneğin, `height: 50vh` ile ekranın dikeydeki %50’sini kaplayan bir bölüm elde edebilirsiniz.

3. **Tarayıcı Varsayılanları (Margin & Padding)**
    - Tarayıcıların varsayılan boşluklarını ortadan kaldırmak için sıklıkla
      ```css
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }
      ```
      kullanılır. Bu sayede istenmeyen kayma ve boşluklar engellenir.

4. **Metin Konumlandırma (Ortalamak)**
    - Metni sayfanın tam ortasına almak için `position: absolute` (veya `position: fixed/relative`) ile `top: 50%`, `left: 50%` ayarlanır. Ardından:
      ```css
      transform: translate(-50%, -50%);
      ```
      ile elemanın kendi merkez noktası sayfanın tam ortasına getirilir.

5. **Performans ve Optimizasyon**
    - Arka plan olarak kullanılan resmin dosya boyutu **küçük** (örn. ~50-100 KB) tutulmalıdır.
    - Büyük boyutlu (MB seviyesinde) görseller, sayfa yüklenmesini yavaşlatır.
    - Resim yüklenene kadar arka plan rengi göstererek kullanıcı deneyimini iyileştirebilirsiniz.

6. **Saydam Katman (Overlay)**
    - Arka plan resmini belirgin biçimde göstermek istemiyorsanız, yarı saydam bir katman ekleyebilirsiniz.
    - `::before`, `::after` pseudo-element’leri veya ayrı bir `div` katmanı ile bu işlemi yapmak mümkündür.
