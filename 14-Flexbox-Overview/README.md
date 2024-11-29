# Flexbox Overview

Flexbox (“Flexible Box Layout”) modern CSS'in güçlü bir modülüdür. Esas amacı, kutuların bir konteyner içinde hizalanmasını ve dağıtılmasını düzenlemektir. Flexbox, özellikle dinamik veya farklı boyutlardaki elementlerin düzenlenmesi gereken durumlarda oldukça etkilidir.

---

## Özellikler

### 1. **Flex Container**
FlexboxFlexbox\u201ın temel taşı bir "flex container"dır. Flexbox düzenlemeleri, bir elementi "container" olarak tanımlayarak başlar.

**CSS**:
```css
.container {
  display: flex;
}
```

Bu, konteynerin içindeki elementleri flex item'lara dönüştürür.

---

### 2. **Ana Eksen (Main Axis) ve Çapraz Eksen (Cross Axis)**
- **Ana eksen (Main Axis)**: Flex container'daki elemanların hizalandığı varsayılan eksendir (yatay).
- **Çapraz eksen (Cross Axis)**: Ana eksene dik olan eksendir (dikey).

Flex yönü "flex-direction" ile değiştirilebilir:
```css
.container {
  flex-direction: row; /* Varsayılan: yatay hizalama */
  flex-direction: column; /* Dikey hizalama */
}
```

---

### 3. **Flex Container Özellikleri**

#### a) **flex-direction**
Flex item'ların yönünü belirler.
```css
.container {
  flex-direction: row; /* Yatay */
  flex-direction: column; /* Dikey */
  flex-direction: row-reverse; /* Yatay ters */
  flex-direction: column-reverse; /* Dikey ters */
}
```

#### b) **justify-content**
Ana eksen boyunca elemanları hizalar.
```css
.container {
  justify-content: flex-start;  /* Varsayılan: Sola hizalı */
  justify-content: flex-end;    /* Sağa hizalı */
  justify-content: center;      /* Ortalanmış */
  justify-content: space-between; /* Aralarında eşit boşluk */
  justify-content: space-around;  /* Çevresinde eşit boşluk */
  justify-content: space-evenly;  /* Tüm boşluklar eşit */
}
```

#### c) **align-items**
Çapraz eksen boyunca elemanları hizalar.
```css
.container {
  align-items: flex-start; /* Çapraz eksenin başı */
  align-items: flex-end;   /* Çapraz eksenin sonu */
  align-items: center;     /* Ortalanmış */
  align-items: baseline;   /* Metin tabanına hizalı */
  align-items: stretch;    /* Varsayılan: Tüm alana yayılan */
}
```

#### d) **align-content**
Birden fazla satır olduğunda satırları hizalar.
```css
.container {
  align-content: flex-start;
  align-content: flex-end;
  align-content: center;
  align-content: space-between;
  align-content: space-around;
  align-content: stretch;
}
```

---

### 4. **Flex Item Özellikleri**

#### a) **order**
Flex item'ların sırasını değiştirir.
```css
.item {
  order: 1; /* Varsayılan: 0 */
}
```

#### b) **flex-grow**
Flex item'ın, container'daki ekstra alanı ne kadar büyüteceğini belirtir.
```css
.item {
  flex-grow: 1; /* Varsayılan: 0 */
}
```

#### c) **flex-shrink**
Flex item'ın daralma oranını kontrol eder.
```css
.item {
  flex-shrink: 1; /* Varsayılan: 1 */
}
```

#### d) **flex-basis**
Flex item'ın başlangıç boyutunu belirtir.
```css
.item {
  flex-basis: 100px; /* Varsayılan: auto */
}
```

#### e) **align-self**
Bir flex item'ın diğerlerinden bağımsız olarak hizalanmasını sağlar.
```css
.item {
  align-self: flex-start; /* Başlangıç hizası */
  align-self: flex-end;   /* Bitiş hizası */
  align-self: center;     /* Ortalanmış */
  align-self: baseline;   /* Metin tabanı hizası */
  align-self: stretch;    /* Varsayılan */
}
```

---

## Flexbox Avantajları
1. Elemanların hizalanması ve boşluk yönetimi kolaydır.
2. Responsive tasarımlar için idealdir.
3. Karmaşık düzenleri basit kodla oluşturabilirsiniz.

---

## Flexbox Kullanım Örnekleri

### Basit Flexbox Örneği
```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

**CSS**:
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f0f0f0;
}

.item {
  background: #3498db;
  color: white;
  padding: 20px;
  margin: 10px;
  border-radius: 5px;
}
```

---

## İleri Kaynaklar
- [MDN Web Docs – Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
- [CSS-Tricks – A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

---

Happy coding! 🚀
