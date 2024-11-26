# CSS Theory: #1 - Conflicts Between Selectors (Seçiciler arasındaki çatışmalar)

## 5) Declarations Marked (!important)

- En yüksek önceliğe sahip olan kural, specificity hesaplamalarında bağımsız olarak diğer kuralları geçersiz kılar.

- Kullanımı: `color: red !important`

- Kod Örneği:

```
p {color: red !important}
p {color: blue;}
```

- Yukarıdaki örnekte, p elementine uygulanan color: red !important kuralı, color: blue kuralını geçersiz kılar.
- ### NOT: !important kullanımı, CSS'inizi karmaşık ve zor anlaşılır hale getirebilir. Bu yüzden !important kullanımını mümkün olduğunca azaltmaya çalışın. CSS'in doğal akışını bozabilir ve bakımını zorlaştırabilir.

## 4) Inline Style

- HTML içindeki style attribute'u belirten stiller, external ve internal CSS'teki tüm seçicilerden daha önceliklidir (ama!importamtkurallarını geçemez.)

- Kullanımı: `<p style = "color:red;">`

- Kod Örneği:
  `<p style = "color:red;"> Bu metin kırmızı olacak </p>`

- Inline style’lar, spesifik bir elemente yönelik olduğundan specificity açısından çok güçlüdür.

## 3) ID (#) Selector

- ID seçiciler, spesifik açısından çok yüksek önceliğe sahiptir. Bir ID seçici bir elemente uygulanırsa, aynı elemente uygulanan sınıf veya element seçicileri geçersiz kılar. Bu yüzden genellikle CSS yazarken ID Selector'ları kullanmayız

- Kullanımı :`#header { color: blue; }`

- Kod Örneği:

```
#header { color: blue; }
.header { color : red; }
```

- Yukarıdaki durumda, #header nedeniyle metin mavi olur. Çünkü ID seçicisi, class seçicisinden daha spesifiktir.

### 2) Class (.) veya Pseudo-Class (:) selector

- Class ve Pseudo-Class  seçiciler orta düzeyde spesifiklik sunar.

- Kullanımı: `.highlight { color: green; },:hover { background: yellow; }`

- Kod Örneği:

```
.highlight { color: green; }
:hover { background: yellow; }
```

## 1) Element Selector

- Belirli bir HTML etiketine uygulanır. Spesifiklik açısından oldukça düşüktür.

- Kullanımı: `.p{ background: yellow; }`

- Kod Örneği:

`.p{ background: yellow; }`

## 0) Universal Selector (\*)

- Tüm elementleri hedef alır ve en düşük spesifikliğe sahiptir.

- Kullanımı: `* { margin: 0; }`

# Ek Notlar

1. Eşit Spesifikte çakışma: Spesifikleri eşit ise, CSS dosyalarında her zaman en son yazılan kural geçerli olur.

2. Spesifik Hiyerarşisi: Daha spesifik bir seçici (örneğin, bir ID) her zaman daha genel seçiciyi (örneğin, bir class) geçersiz kılar.
