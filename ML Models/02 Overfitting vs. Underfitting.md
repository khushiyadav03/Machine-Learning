# Overfitting vs. Underfitting

Yeh do aisi conditions hain jo batati hain ki aapka model training data se kitna "sahi" ya "galat" seekh raha hai. Ek perfect model in dono ke beech ka balance hota hai.

Chaliye inko ek real-life analogy se samjhte hain. Imagine kijiye aap ek student hain jo exam ki taiyari kar raha hai.

---

## 1. Underfitting (Kam Seekhna)

**Concept:** Yeh woh situation hai jab aapka model bohot zyada simple hota hai aur training data ke andar ke zaroori patterns ko bhi nahi seekh paata.

**Student Analogy:** Aap exam ke liye sirf chapter ke headings padh kar chale gaye. Aapne aache se padhai nahi ki. Result? Aap textbook ke aasan sawal (training data) bhi aache se solve nahi kar paayenge, aur exam ke naye sawal (test data) to bilkul bhi nahi.

**Technical Signs:**
- Training Accuracy bohot kam hoti hai.
- Test Accuracy bhi bohot kam hoti hai.

**Kaisa Dikhta Hai?**
Aap dekh sakte hain ki data me ek curve ka pattern hai, lekin model ek simple si straight line fit karne ki koshish kar raha hai, jo data ko aache se represent nahi kar paa rahi.

---

## 2. Overfitting (Zarurat se Zyada Seekhna / Ratta Marna)

**Concept:** Yeh woh situation hai jab aapka model bohot zyada complex ho jaata hai. Woh training data ke main patterns ke saath-saath **noise** (faltu details) ko bhi ratt leta hai.

**Student Analogy:** Aapne textbook ke har sawal ko, uske aakhri full stop tak, ratt liya hai. Aapne concept nahi samjha, sirf ratta maara hai. Result? Textbook se koi bhi sawal poocha jaaye (training data), aap 100% score karenge. Lekin jaise hi exam me thoda sa bhi ghumakar naya sawal (test data) aayega, aap fail ho jaayenge kyunki aapne to sirf ratta maara tha, concept samjha hi nahi.

**Technical Signs:**
- Training Accuracy bohot high hoti hai (e.g., 99-100%).
- Test Accuracy achanak se bohot kam ho jaati hai (e.g., 50-60%).

**Kaisa Dikhta Hai?**
Yahan, model ne har ek data point ko "touch" karne ke chakkar me ek ajeeb sa, complex curve bana liya hai. Yeh naye data par aacha perform nahi karega.

---

## 3. Good Fit (Sahi Balance)

**Concept:** Yeh perfect balance hai. Model itna complex hai ki woh data ke zaroori patterns ko samajh leta hai, lekin itna simple bhi hai ki woh noise ko ignore kar deta hai.

**Student Analogy:** Aapne concepts ko aache se samjha hai. Aap textbook ke sawal (training data) bhi aache se solve kar lete hain aur exam ke naye, unseen sawal (test data) bhi aache se solve kar lete hain.

**Technical Signs:**
- Training Accuracy high hoti hai (e.g., 88%).
- Test Accuracy bhi lagbhag utni hi high hoti hai (e.g., 86%). Dono me zyada fark nahi hota.

**Kaisa Dikhta Hai?**
Yeh curve data ke general trend ko follow kar raha hai, na ki har ek point ko zabardasti touch karne ki koshish kar raha hai.

---

## Summary

| Type         | Training Performance | Test Performance | Problem                |
|--------------|----------------------|------------------|------------------------|
| **Underfitting** | Low                  | Low              | Model is too simple.   |
| **Overfitting** | Very High            | Low              | Model is too complex.  |
| **Good Fit** | High                 | High             | Balanced complexity.   |

Machine learning me humara goal hamesha ek **"Good Fit"** model banana hota hai.