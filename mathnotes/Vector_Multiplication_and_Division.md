# Dot Product, Rotation, Vector Multiplication and Division

**Geliştiren / Öneren:** Yunus Emre PEKTAŞ (yuempek)

**Konu:** İki boyutlu karmaşık sayı cebirinin vektörler üzerinden ifade edilmesi ve izdüşüm tabanlı bölme yaklaşımının yüksek boyutlara genelleştirilmesi.

---

# 1\. GİRİŞ

İki boyutlu vektörler ile karmaşık sayılar arasında doğal bir matematiksel ilişki vardır.

Bir karmaşık sayı:

$$
z=a+bi
$$

iki boyutlu bir vektör olarak:

$$
V=(a,b)
$$

şeklinde gösterilebilir.

Bu gösterim sayesinde karmaşık sayıların toplama, çıkarma, çarpma ve bölme işlemleri vektör işlemleri kullanılarak ifade edilebilir.

Bu çalışmanın temel amacı, söz konusu işlemleri dot product ve rotation kullanarak tanımlamak ve elde edilen geometrik yapıyı yüksek boyutlarda incelemektir.

# 2\. TEMEL TANIMLAR

İki vektörümüz olsun:

$$
A=(a,b),\qquad B=(c,d)
$$

Skaler çarpım:

$$
A\cdot B=ac+bd
$$

Vektör uzunluğu:

$$
\|A\|=\sqrt{a^2+b^2}
$$

90 derece saat yönünün tersine döndürme:

$$
R(a,b)=(-b,a)
$$

Eşlenik:

$$
\operatorname{conj}(a,b)=(a,-b)
$$

Bu dönüşümlerin temel özellikleri:

$$
R^2=-I
$$

$$
A\cdot R(A)=0
$$

$$
\|R(A)\|=\|A\|
$$

# 3\. VEKTÖR ÇARPMA İŞLEMİ

Yuempek vektör çarpımını şu şekilde tanımlayalım:

$$
\boxed{
A\otimes B=
\left(
A\cdot\operatorname{conj}(B),
A\cdot R(\operatorname{conj}(B))
\right)
}
$$

Eşlenik:

$$
\operatorname{conj}(B)=(c,-d)
$$

Döndürülmüş eşlenik:

$$
R(\operatorname{conj}(B))=(d,c)
$$

Böylece:

$$
A\otimes B=
\left(
ac-bd,ad+bc
\right)
$$

Bu işlem karmaşık sayı çarpımıyla aynıdır.

## 3.1. Çarpmanın geometrik anlamı

Vektörler kutupsal biçimde yazılırsa:

$$
A=r_1(\cos\alpha,\sin\alpha)
$$

$$
B=r_2(\cos\beta,\sin\beta)
$$

çarpım:

$$
\boxed{
A\otimes B=
r_1r_2
(\cos(\alpha+\beta),\sin(\alpha+\beta))
}
$$

olur.

Dolayısıyla çarpma işleminde:

- Uzunluklar çarpılır.
- Açılar toplanır.

# 4\. VEKTÖR BÖLME İŞLEMİ

Bölme işlemini dot product ve rotation kullanarak tanımlayalım:

$$
\boxed{
A\oslash B=
\left(
\frac{A\cdot B}{B\cdot B},
\frac{A\cdot R(B)}{B\cdot B}
\right)
}
$$

Burada:

$$
B\neq(0,0)
$$

olmalıdır.

İlk bileşen:

$$
x=\frac{ac+bd}{c^2+d^2}
$$

İkinci bileşen:

$$
y=\frac{bc-ad}{c^2+d^2}
$$

Böylece:

$$
\boxed{
A\oslash B=
\left(
\frac{ac+bd}{c^2+d^2},
\frac{bc-ad}{c^2+d^2}
\right)
}
$$

Bu formül karmaşık sayı bölmesiyle tamamen aynıdır.

## 4.1. Bölmenin geometrik anlamı

Vektörler:

$$
A=r_1(\cos\alpha,\sin\alpha)
$$

$$
B=r_2(\cos\beta,\sin\beta)
$$

olarak yazıldığında:

$$
\boxed{
A\oslash B=
\frac{r_1}{r_2}
(\cos(\alpha-\beta),\sin(\alpha-\beta))
}
$$

elde edilir.

Dolayısıyla bölme işleminde:

- Uzunluklar bölünür.
- Açılar çıkarılır.

# 5\. BÖLMENİN ÇARPMANIN TERSİ OLDUĞUNUN İSPATI

Tanımladığımız çarpım:

$$
A\otimes B=(ac-bd,ad+bc)
$$

Bölüm:

$$
A\oslash B=
\left(
\frac{ac+bd}{c^2+d^2},
\frac{bc-ad}{c^2+d^2}
\right)
$$

olsun.

Bölüm sonucuna:

$$
Q=(x,y)
$$

diyelim.

Çarpım tanımından:

$$
Q\otimes B=(xc-yd,xd+yc)
$$

İlk bileşen:

$$
xc-yd
=
\frac{c(ac+bd)-d(bc-ad)}{c^2+d^2}
$$

$$
=\frac{a(c^2+d^2)}{c^2+d^2}=a
$$

İkinci bileşen:

$$
xd+yc
=
\frac{d(ac+bd)+c(bc-ad)}{c^2+d^2}
$$

$$
=\frac{b(c^2+d^2)}{c^2+d^2}=b
$$

Sonuç:

$$
\boxed{
(A\oslash B)\otimes B=A
}
$$

Böylece bölme işleminin çarpmanın tersi olduğu kanıtlanmıştır.

# 6\. ÇARPMA VE BÖLME İŞLEMLERİNİN CEBİRSEL ÖZELLİKLERİ

İki boyutlu sistemimizde:

## Toplama

$$
A\oplus B=B\oplus A
$$

$$
(A\oplus B)\oplus C=A\oplus(B\oplus C)
$$

Toplama birim elemanı:

$$
O=(0,0)
$$

Toplama tersi:

$$
-A=(-a,-b)
$$

## Çarpma

$$
A\otimes B=B\otimes A
$$

$$
(A\otimes B)\otimes C=A\otimes(B\otimes C)
$$

Çarpma birim elemanı:

$$
E=(1,0)
$$

Çarpma tersi:

$$
\boxed{
A^{-1}=
\left(
\frac{a}{a^2+b^2},
-\frac{b}{a^2+b^2}
\right)
}
$$

Burada $A\neq0$.

## Dağılma

$$
A\otimes(B\oplus C)
=
(A\otimes B)\oplus(A\otimes C)
$$

Bu özelliklerin tamamı gerçek sayıların toplama ve çarpma özelliklerinden doğrudan kanıtlanır.

Dolayısıyla tanımladığımız iki boyutlu yapı bir değişmeli cisimdir.

# 7\. YÜKSEK BOYUTLARA GENELLEME

Şimdi:

$$
A,B\in\mathbb R^{2k}
$$

olsun.

90 derece döndürme dönüşümünü temsil etmek için $J$ matrisini tanımlayalım.

Gerekli koşullar:

$$
\boxed{J^2=-I}
$$

$$
\boxed{J^TJ=I}
$$

Bunlardan:

$$
J^T=-J
$$

elde edilir.

Ayrıca:

$$
A\cdot JA=0
$$

ve:

$$
\|JA\|=\|A\|
$$

olur.

Bu özellikler sayesinde J, her vektörü aynı uzunlukta ve ona dik bir doğrultuya taşır.

# 8\. YUEMPEK İZDÜŞÜM TABANLI VEKTÖR BÖLME TANIMI

Yüksek boyutlar için bölme yaklaşımımız:

$$
\boxed{
D_J(A,B)=
\left(
\frac{A\cdot B}{B\cdot B},
\frac{A\cdot JB}{B\cdot B}
\right)
}
$$

Burada:

$$
B\neq0
$$

ve:

$$
J^2=-I,\qquad J^TJ=I
$$

koşulları geçerlidir.

Bölüm:

$$
D_J(A,B)=(x,y)
$$

olarak gösterilsin.

# 9\. İZDÜŞÜM TEOREMİ VE İSPATI

Yeniden oluşturulan vektör:

$$
P=xB+yJB
$$

olsun.

Hata vektörümüz:

$$
E=A-P
$$

şeklinde tanımlansın.

İlk olarak:

$$
E\cdot B
=
A\cdot B-x(B\cdot B)
$$

Bölüm tanımından:

$$
x=\frac{A\cdot B}{B\cdot B}
$$

olduğu için:

$$
E\cdot B=0
$$

Benzer şekilde:

$$
E\cdot JB
=
A\cdot JB-y(B\cdot B)
$$

ve:

$$
y=\frac{A\cdot JB}{B\cdot B}
$$

olduğundan:

$$
E\cdot JB=0
$$

Dolayısıyla:

$$
\boxed{
E\perp B,\qquad E\perp JB
}
$$

Böylece:

$$
\boxed{
P=\operatorname{proj}_{\operatorname{span}(B,JB)}A
}
$$

sonucuna ulaşılır.

Bu, yüksek boyutlu yaklaşımımızın temel geometrik teoremidir.

# 10\. YÜKSEK BOYUTLARDA BÖLME İŞLEMİNİN SINIRI

İki boyutta:

$$
\operatorname{span}(B,JB)=\mathbb R^2
$$

olduğundan:

$$
P=A
$$

elde edilir.

Ancak dört ve daha yüksek boyutlarda:

$$
\operatorname{span}(B,JB)\subsetneq\mathbb R^{2k}
$$

olabilir.

Bu nedenle genel olarak:

$$
P\neq A
$$

olur.

Bölme işlemi burada tam bir vektör bölmesi değil, iki boyutlu alt uzaya izdüşüm koordinatlarını hesaplayan bir işlemdir.

# 11\. FARKLI J DÖNÜŞÜMLERİ VE DEĞİŞMEZLİK

İki ortogonal dönüşüm arasında:

$$
J'=QJQ^{-1}
$$

ilişkisi olsun.

Burada:

$$
Q^TQ=I
$$

olmalıdır.

Yeni vektörler:

$$
A'=QA,\qquad B'=QB
$$

şeklinde tanımlansın.

Bölümün ilk bileşeni:

$$
\frac{(QA)^T(QB)}{(QB)^T(QB)}
=
\frac{A^TB}{B^TB}
$$

İkinci bileşeni:

$$
\frac{(QA)^T(QJQ^{-1})(QB)}
{(QB)^T(QB)}
=
\frac{A^TJB}{B^TB}
$$

olur.

Dolayısıyla:

$$
\boxed{
D_{J'}(QA,QB)=D_J(A,B)
}
$$

Bu, sistemin eşzamanlı ortogonal dönüşümlere karşı değişmez olduğunu gösterir.

# 12\. FARKLI J SEÇİMLERİNİN SONUÇLARI

Dört boyutta farklı J dönüşümleri farklı düzlemler seçebilir.

Örneğin:

$$
J_1(a,b,c,d)=(-b,a,-d,c)
$$

ve:

$$
J_2(a,b,c,d)=(-c,-d,a,b)
$$

Her ikisi de:

$$
J_i^2=-I
$$

ve:

$$
J_i^TJ_i=I
$$

koşullarını sağlar.

Ancak genel olarak:

$$
D_{J_1}(A,B)\neq D_{J_2}(A,B)
$$

olabilir.

Bunun nedeni seçilen izdüşüm düzlemlerinin farklı olmasıdır.

# 13\. BİVAKTÖR TABANLI DİNAMİK J ($JB = T \cdot B$) GENELLEMESİ

Sabit $J$ operatörü seçmek yerine, $A$ ve $B$ vektörlerinin dış çarpımıyla oluşan bivektörün birim hali ($\hat{T}$) kullanılarak $JB$ vektörünün dinamik olarak tanımlanması sistemin eksikliklerini kökten giderir:

$$
\hat{T} = \frac{A \wedge B}{\|A \wedge B\|}, \qquad JB = \hat{T} \cdot B
$$

## 13.1. $JB = T \cdot B$ İspatı ve Norm Analizi

Bivektör iç büzülmesi kullanıldığında:

$$
(A \wedge B) \cdot B = \|B\|^2 A - (A \cdot B)B
$$

elde edilir. Bu ifade $B$'ye tam diktir ($B \cdot (T \cdot B) = 0$). Uzunluk şartını ($\|JB\| = \|B\|$) sağlaması için bivektör birimleştirilir:

$$
JB = \|B\| \frac{A - \frac{A \cdot B}{\|B\|^2}B}{\left\| A - \frac{A \cdot B}{\|B\|^2}B \right\|}
$$

## 13.2. Yuempek Bölme Formülü ile Sadeleştirme

İkinci koordinat ($y$) için $JB$ ifadesi yerine konulduğunda:

$$
y = \frac{A \cdot JB}{\|B\|^2} = \frac{\left\| A - \frac{A \cdot B}{\|B\|^2}B \right\|}{\|B\|}
$$

Böylece Yuempek bölme formülü tüm boyutlarda ($R^n$) şu sade ve kesin hâlini alır:

$$
\boxed{
D_T(A,B) = (x, y) = \left( \frac{A \cdot B}{\|B\|^2}, \; \frac{\left\| A - \frac{A \cdot B}{\|B\|^2}B \right\|}{\|B\|} \right)}
$$

Burada birinci bileşen $x = \frac{A \cdot B}{\|B\|^2}$ iken, ikinci bileşen doğrudan $x$ cinsinden $y = \frac{\|A - xB\|}{\|B\|}$ olarak yazılır.

## 13.3. Bu Genellemenin Çalışmaya Katkısı (Neden Devrimsel?)

1. **Tek ve Çift Tüm Boyutlarda Çalışır:** Sadece $\mathbb{R}^{2k}$ uzaylarıyla sınırlı kalmaz; $\mathbb{R}^3, \mathbb{R}^5$ dahil tüm $\mathbb{R}^n$ uzaylarında geçerlidir.
2. **Sıfır Hata ($P = A$):** Sabit $J$ seçiminden kaynaklanan izdüşüm hatası ortadan kalkar. $JB$ doğrudan $A$ ve $B$'nin kendi düzleminden üretildiği için yeniden oluşturma denklemi her boyutta tam olarak $P = xB + yJB = A$ ($E = 0$) sonucunu verir.
