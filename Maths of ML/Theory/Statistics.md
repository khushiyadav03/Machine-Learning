# Statistics: Theory and Concepts 📊

## 1. Statistics Kya Hai aur Kyun Zaroori Hai?

Statistics data ko collect karne, analyze karne, interpret karne, aur present karne ki science hai.

Machine learning me, model banane se pehle humein data ko aache se samajhna padta hai. Statistics humein wahi power deta hai. Isse hum data ke andar ke patterns, relationships, aur "story" ko samajh paate hain. Yeh process **Exploratory Data Analysis (EDA)** kehlata hai.

Statistics ko hum do main parts me baant sakte hain:

---

### A. Descriptive Statistics (Data ko Summarize Karna)

Iska kaam hai data ko aasan aur meaningful tarike se describe karna. Yeh batata hai ki data "kaisa dikhta hai". Iske do main components hain:

#### 1. Measures of Central Tendency (Data ka "Center" Point)

Yeh ek single value hoti hai jo poore dataset ko represent karne ki koshish karti hai.

**Mean (Average):**
* **Concept:** Sabse common measure hai. Sabhi data points ko add karke total number of points se divide kar do.
* **Formula:** Mean $(\mu) = \frac{\Sigma x}{n}$ (Sum of all values / Number of values)
* **Problem:** Yeh outliers (bohot badi ya bohot choti values) se bohot jaldi affect hota hai.
> **Example:** Ek room me 5 logon ki salary `[30k, 40k, 50k, 60k, 70k]` hai. Mean salary 50k hai. Agar room me Ambani (salary 10000k) aa jaayein, to mean salary achanak bohot upar chali jaayegi, jo baaki logon ko represent nahi karegi.

**Median (Middle Value):**
* **Concept:** Data ko sort karne ke baad (ascending order me) jo value bilkul beech me aati hai.
* **Strength:** Yeh outliers se affect nahi hota. Isliye, salary ya house price jaise data ke liye mean se behtar hai.
* **Formula:** Agar `n` odd hai, to `(n+1)/2`th value. Agar `n` even hai, to do middle values ka average.
> **Example:** Upar wale Ambani ke example me, median abhi bhi 50k ke aas paas hi rahega, jo ek better representation hai.

**Mode (Most Frequent):**
* **Concept:** Woh value jo dataset me sabse zyada baar aati hai.
* **Use Case:** Yeh zyada tar categorical data ke liye use hota hai. Jaise, ek shop me sabse zyada kaunse color ki T-shirt bikti hai (e.g., 'Black').

#### 2. Measures of Variability/Dispersion (Data ka "Spread")

Yeh batata hai ki data points ek doosre se aur mean se kitne faile hue (spread out) hain.

**Range:**
* **Concept:** Sabse simple measure hai. Maximum value - Minimum value.
* **Problem:** Yeh bhi outliers se bohot affect hota hai.

**Standard Deviation ($\sigma$):**
* **Concept:** Yeh sabse important measure of spread hai. Yeh batata hai ki, on average, har data point mean se kitna door hai.
* **Intuition:**
    * **Low Standard Deviation:** Saare data points mean ke bohot paas-paas hain. Data consistent hai. (e.g., ek professional archer ke saare teer target ke center ke paas honge).
    * **High Standard Deviation:** Data points mean se bohot door-door tak faile hue hain. Data me bohot variation hai. (e.g., ek naye archer ke teer poore board par faile honge).
* **Formula:** $\sigma = \sqrt{\frac{\Sigma(x - \mu)^2}{n}}$ (Har value aur mean ke difference ka square karo, unka average lo, aur fir uska square root nikalo).

---

### B. Inferential Statistics (Data se "Andaza" Lagana)

Iska kaam hai ek chote sample (data ka hissa) ko study karke, ek badi population (poora group) ke baare me conclusions ya predictions nikalna.

#### 1. Population and Sample

* **Population:** Woh poora group jiske baare me hum जानना chahte hain. (e.g., India ke saare voters).
* **Sample:** Us population ka ek chota sa hissa jise hum study karte hain. (e.g., 5000 voters ka ek survey).

Hum sample ko analyze karke poori population ke baare me andaza lagate hain.

#### 2. Correlation

* **Concept:** Yeh do variables (features) ke beech ka relationship batata hai. Iski value -1 se +1 ke beech hoti hai.
* **Intuition:**
    * **Positive Correlation (~ +1):** Ek variable badhta hai, to doosra bhi badhta hai. (e.g., Jitni zyada padhai, utne zyada marks).
    * **Negative Correlation (~ -1):** Ek variable badhta hai, to doosra ghat'ta hai. (e.g., Jitni zyada thand, utni kam AC ki sale).
    * **Zero Correlation (~ 0):** Dono variables me koi clear relationship nahi hai. (e.g., Aapke shoe size aur aapke exam marks).
* **ML me Use:** Feature Selection ke liye yeh bohot zaroori hai. Hum un features ko dhundte hain jo humare target variable (jise predict karna hai) ke saath highly correlated hon.