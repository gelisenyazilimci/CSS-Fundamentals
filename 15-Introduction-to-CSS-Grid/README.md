# CSS Grid'e Gİriş

CSS Grid Layout, web sayfalarında çok boyutlu ve esnek tasarımlar oluşturmak için kullanılan güçlü bir düzenişleme aracıdır. Grid sistemi, satırlar ve sütunlar kullanarak içeriklerin yerleştirilmesini ve hizalanmasını basitleştirir. Bu rehberde, CSS Grid'in temel kavramlarını öğreneceksiniz.

---

## Neden CSS Grid Kullanılır?
- Karmaşık düzenlerı kolayca oluşturur.
- Satır ve sütunları dinamik olarak kontrol eder.
- Responsive tasarımları daha basit hale getirir.
- Modern tarayıcıların tamamında desteklenir.

---

## CSS Grid'in Temel Kavramları

### 1. **Grid Container ve Grid Items**
- **Grid Container**: Grid düzeni için bir kapsayıcı oluşturur.
  ```css
  .grid-container {
      display: grid;
  }
  ```
- **Grid Items**: Grid kapsayıcısı içindeki her bir öğe.

  **HTML Örnek:**
  ```html
  <div class="grid-container">
      <div>Item 1</div>
      <div>Item 2</div>
      <div>Item 3</div>
  </div>
  ```

### 2. **Grid Lines**
Grid sisteminde sütunları ve satırları tanımlayan çizgilerdir. Her grid çizgisi, sıfırdan başlayan bir numaralandırma sistemiyle belirlenir.

### 3. **Grid Tracks**
- Grid satırları ve sütunları arasındaki alanlara verilen isimdir.
- Satırlar ve sütunlar grid şablonunu oluşturur.

### 4. **Grid Cell**
- Grid çizgileri arasındaki bir bireysel alanı ifade eder.

### 5. **Grid Areas**
- Birden fazla grid hücresi bir grid alanı oluşturabilir.

---

## Grid Kullanımının Temel Adımları

### 1. **Grid Oluşturma**
Grid kapsayıcısına `display: grid` eklenerek başlatılır.

```css
.grid-container {
    display: grid;
}
```

### 2. **Sütun ve Satırları Belirleme**
`grid-template-columns` ve `grid-template-rows` kullanılarak sütun ve satır boyutları tanımlanır.

```css
.grid-container {
    display: grid;
    grid-template-columns: 100px 200px auto;
    grid-template-rows: 50px auto;
}
```
- **100px 200px auto**: Sırasıyla birinci sütun 100px, ikinci sütun 200px ve üçüncü sütun kalan alanı kaplar.
- **50px auto**: Birinci satır 50px, ikinci satır kalan alanı kaplar.

### 3. **Grid Gap**
Grid hücreleri arasındaki boşlukları ayarlamak için kullanılır.

```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 10px;
}
```

- **`1fr`**: Fraksiyon birimi. Alanı eşit oranlarda böler.
- **`grid-gap: 10px;`**: Hücreler arasına 10px boşluk ekler.

### 4. **Grid Öğelerini Yerleştirme**
`grid-column` ve `grid-row` kullanılarak grid öğelerinin kapsadığı satır ve sütunlar ayarlanabilir.

```css
.item1 {
    grid-column: 1 / 3; /* 1. çizgiden 3. çizgiye kadar uzanır */
    grid-row: 1 / 2; /* 1. satırı kaplar */
}
```

---

## Örnek Uygulama

### HTML:
```html
<div class="grid-container">
    <div class="item1">Item 1</div>
    <div class="item2">Item 2</div>
    <div class="item3">Item 3</div>
    <div class="item4">Item 4</div>
</div>
```

### CSS:
```css
.grid-container {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: auto auto;
    grid-gap: 10px;
}

.item1 {
    background: lightblue;
    grid-column: 1 / 2;
}

.item2 {
    background: lightcoral;
    grid-column: 2 / 3;
}

.item3 {
    background: lightgreen;
    grid-column: 1 / 3;
    grid-row: 2 / 3;
}

.item4 {
    background: lightgoldenrodyellow;
}
```

---

## CSS Grid'in Avantajları
- Karmaşık düzenleri kolayca tasarlama imkânı sunar.
- Responsive tasarımı destekler.
- Diğer düzenleme yöntemlerine (float, flexbox) göre daha esnektir.

---

## Tarayıcı Desteği
CSS Grid modern tarayıcıların tümü tarafından desteklenir:
- Chrome 57+
- Firefox 52+
- Edge 16+
- Safari 10.1+

---

Bu doküman CSS Grid'in temel yapısını anlamanız için hazırlanmıştır. Daha fazla örnek ve ileri düzey kullanımlar için pratik yapın ve dökümanları inceleyin!

