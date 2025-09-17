# Vectors: Theory and Concepts 🧭

## 1. Vector Kya Hai? (What is a Vector?)

Simple words me, ek vector ek aisi cheez hai jiske paas do properties hoti hain:

* **Magnitude (Length):** Uski value ya size kitna hai.
* **Direction:** Woh kis disha (direction) me point kar raha hai.

Sochne ka sabse aasan tarika ek teer (arrow) hai. Teer ki lambai uska magnitude hai aur jis taraf uski nok (tip) hai, woh uski direction hai.



### Scalar vs. Vector

* **Scalar:** Ek aisi quantity jiske paas sirf magnitude hota hai, direction nahi. Jaise ki speed (50 km/h), temperature (25°C), ya aapki age (22). Yeh sirf numbers hain.
* **Vector:** Ek aisi quantity jiske paas magnitude aur direction dono hote hain. Jaise ki velocity (50 km/h North ki taraf), ya force (10 Newtons neeche ki taraf).

---

## 2. Machine Learning me Vectors Kyun Important Hain?

Machine Learning me, hum data se deal karte hain. Ek vector data ke ek single piece ko represent karta hai. For example, agar humare paas kisi ghar ka data hai, to us ghar ki saari features ko hum ek vector me daal sakte hain:

ghar_vector = [number_of_bedrooms, square_footage, price_in_lakhs]
ghar_1 = [3, 1500, 80]

Yahan `ghar_1` ek vector hai jo ek specific ghar ko represent kar raha hai.

---

## 3. Vector ke Formulas aur Properties

### Representation

Ek 2D vector ko hum aam taur par $v = [x, y]$ se represent karte hain, jahan $x$ x-axis par movement hai aur $y$ y-axis par.

### Magnitude (Length) Nikalna

Vector ki length nikalne ke liye hum Pythagoras theorem ka use karte hain. Ise $ ||v|| $ se denote karte hain.

**Formula:** Agar $v = [x, y]$ hai, to $||v|| = \sqrt{x^2 + y^2}$

**Example:** Agar ek vector $v = [3, 4]$ hai, to uska magnitude hoga:
$||v|| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$

Is vector ki length 5 units hai.

---

# Vector Operations: Formulas and Intuition

Ab dekhte hain ki hum vectors ke saath kya-kya operations kar sakte hain.

## 1. Vector Addition

Do vectors ko add karna.

**Formula:** $[a, b] + [c, d] = [a+c, b+d]$

**Intuition (Sochne ka Tarika):** Ise "tip-to-tail" method se socha jaata hai. Imagine aap pehle vector ke रास्ते pe chale, aur jahan woh khatam hua, wahan se doosre vector ke रास्ते pe chal diye. Aapki starting point se final point tak ka direct रास्ता in dono vectors ka addition hai.

**ML me Use:** Do alag-alag feature sets ko combine karne ke liye.

## 2. Scalar Multiplication

Ek vector ko ek single number (scalar) se multiply karna.

**Formula:** $k \cdot [a, b] = [k \cdot a, k \cdot b]$

**Intuition:** Yeh vector ko stretch ya shrink karta hai.
* Agar $ k > 1 $ (e.g., 2), to vector double lamba ho jaayega, par direction same rahegi.
* Agar $k$ negative hai (e.g., -1), to vector ki length same rahegi par uski direction ulti (180°) ho jaayegi.

**ML me Use:** Kisi feature ki importance (weight) ko badhane ya kam karne ke liye.

## 3. Dot Product

Yeh sabse important operations me se ek hai.

**Formula:** $[a, b] \cdot [c, d] = (a \cdot c) + (b \cdot d)$

**Intuition:** Dot product similarity naapta hai. Yeh batata hai ki do vectors kitna "ek hi direction me" hain.
* **High Positive Value:** Dono vectors lagbhag ek hi direction me hain. (Bohot similar hain)
* **Value is Zero (0):** Dono vectors ek doosre se 90° (perpendicular) par hain. (Unme koi similarity nahi hai)
* **High Negative Value:** Dono vectors opposite directions me hain. (Ekdum alag hain)

**ML me Use:** Yeh har jagah use hota hai!
* **Recommendation Systems:** Yeh check karne ke liye ki aapka "interest vector" kisi movie ke "feature vector" se kitna similar hai.
* **Neural Networks:** Inputs aur weights ke beech ka relation nikalne ke liye.