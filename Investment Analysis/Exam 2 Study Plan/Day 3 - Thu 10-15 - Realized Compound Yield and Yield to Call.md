# Day 3 (Thu 10/15): Realized Compound Yield & Yield to Call

**Deck 1 slides:** "What If the Holding Period Is Longer?" through "YTM vs. YTC: Which One Matters?", plus "Additional Practice: Realized Compound Yield" at the end of the deck
**Time:** about 70 min (RCY takes several steps, so take your time)
**Warm-up (5 min):** Redo Day 2, Problem 2 (HPR).
**Goal:** Work through a full RCY problem step by step, and calculate YTC and YTW for callable bonds.

---

## 1. Realized compound yield (RCY)

HPR works for a short holding period. When you hold for **several years**, two more things matter:
1. Coupons get **reinvested**, possibly at rates different from the original YTM.
2. You sell at whatever price the market yield sets at that time.

RCY captures both of them in one **compound** rate:

```
       ( Terminal wealth )^(1/n)
RCY =  (-----------------)       − 1
       ( Purchase price  )

Terminal wealth = Sale (or redemption) price + FV of all reinvested coupons
n = length of holding period (years → annual RCY; half-years → semiannual RCY)
```

> **Another way to see it:** Forget about bonds for a moment. You put in \$980 today, and after 20 years you walk away with a pile of cash worth \$3,725. What constant annual growth rate turns \$980 into \$3,725 over 20 years? That growth rate is the RCY. It's the same question as "what return did my investment compound at?"

### The 4-step recipe (it's the same every time)
1. **Sale price:** price the bond on the sale date using its **remaining** maturity and the **expected YTM at that time**.
2. **FV of coupons:** N = number of coupons received, I/Y = **reinvestment rate**, PMT = coupon, PV = 0, then CPT FV.
3. **Terminal wealth** = Step 1 + Step 2.
4. **RCY:** N = holding period, PV = −purchase price, PMT = 0, FV = terminal wealth, then CPT I/Y.

### Slide example
Bought a 30-year, 7.5% **annual** coupon bond for \$980. Hold 20 years. Sale YTM 8%, reinvestment rate 6%.
1. Sale price (10 years left): N = 10, I/Y = 8, PMT = 75, FV = 1,000, which gives **\$966.45**
2. FV of coupons: N = 20, I/Y = 6, PMT = 75, which gives **\$2,758.92**
3. Terminal wealth = **\$3,725.37**
4. RCY = (3,725.37/980)^(1/20) − 1 = **6.90%**

### How RCY compares with YTM (held to maturity, no default)
| Reinvestment rate vs. YTM | Result |
|---|---|
| Reinvestment rate **<** YTM | RCY **<** YTM |
| Reinvestment rate **=** YTM | RCY **=** YTM |
| Reinvestment rate **>** YTM | RCY **>** YTM |

> **Key insight:** YTM quietly *assumes* you reinvest at the YTM. That's why YTM is **not** a guaranteed return. Future reinvestment rates are unknown. This is called **reinvestment risk**.

---

## 2. Callable bonds, YTC, and YTW

A **callable bond** lets the **issuer** pay off the bond early at a set **call price** (usually a bit above par).

**When does the issuer call?** When **rates fall**. It's like refinancing a mortgage: pay off the expensive 8% debt and borrow again at 5%.

**Why investors care:**
- Rates fall → a normal bond's price would rise → **but** the issuer calls it → you get only the call price and lose the high coupons → and you have to reinvest at the new low rates.
- **Callability caps your upside.** This is sometimes called "price compression": the price of a callable bond has trouble rising much above the call price.

> **Analogy:** A callable bond is like a renter whose landlord can end the lease whenever rent prices drop. Good deals for you tend to get taken away right when they'd be most valuable.

### Yield to call (YTC)
It's the same as YTM, but: **N = periods until the call date** and **FV = call price**.

**Slide example:** 20-year, 8% semiannual bond, price \$1,150, callable in 10 years at \$1,050.
N = 20, PV = −1,150, PMT = 40, FV = 1,050, which gives I/Y = 3.16%, so **YTC = 6.32%**. (Compare: YTM = 6.63%.)

### Yield to worst (YTW)
The **lowest** yield across all possible redemption scenarios (each call date and maturity), assuming no default. Here YTW = min(6.32%, 6.63%) = **6.32%**.

> **Rule of thumb:** For a **premium** callable bond (trading above the call price), YTC is usually **below** YTM. The issuer has a reason to call, so YTC is what a careful investor should focus on.

---

## ✏️ Practice problems

**1.** You buy a 10-year, 6% **annual**-coupon bond at par (\$1,000) and plan to hold it 5 years. You expect to reinvest coupons at **4%**, and you expect the bond's YTM to be **5%** when you sell. Find the annual RCY.

<details><summary>Show answer</summary>

1. Sale price (5 years left): N = 5, I/Y = 5, PMT = 60, FV = 1,000, so **\$1,043.29**
2. FV of coupons: N = 5, I/Y = 4, PMT = 60, PV = 0, so **\$324.98**
3. Terminal wealth = 1,043.29 + 324.98 = **\$1,368.27**
4. RCY = (1,368.27/1,000)^(1/5) − 1 = **6.47%**

The capital gain (rates fell to 5%) more than made up for the lower reinvestment rate, so RCY is above the original 6% YTM.
</details>

**2.** *(Slide "Additional Practice")* Try it without looking: a 5% semiannual bond with 5 years left, bought for \$983.94, held 3 years. Reinvest coupons at 6.25% (stated annual); the yield will be 7.75% at sale. Find the **effective annual** RCY.

<details><summary>Show answer</summary>

1. Sale price (2 years left): N = 4, I/Y = 3.875, PMT = 25, FV = 1,000, so **\$949.94**
2. FV of coupons: N = 6, I/Y = 3.125, PMT = 25, so **\$162.22**
3. Terminal wealth = **\$1,112.16**
4. Effective annual RCY = (1,112.16/983.94)^(1/3) − 1 = **4.17%**
(Using n = 3 **years** gives an effective annual rate directly.)
</details>

**3.** A 15-year, 7% semiannual-coupon bond sells for \$1,080. It is callable in 5 years at \$1,035. Find the YTM, YTC, and YTW.

<details><summary>Show answer</summary>

YTM: N = 30, PV = −1,080, PMT = 35, FV = 1,000, so I/Y = 3.087, which gives **YTM ≈ 6.17%**
YTC: N = 10, PV = −1,080, PMT = 35, FV = 1,035, so I/Y = 2.875, which gives **YTC ≈ 5.75%**
**YTW = 5.75%** (the lower of the two)
</details>

**4.** *(Concept)* You hold a bond to maturity and it never defaults. Over its life, reinvestment rates average **above** the YTM you bought at. How does your RCY compare with the YTM?

<details><summary>Show answer</summary>

**RCY > YTM**, because the coupons grew faster than YTM assumed.
</details>

**5.** *(Concept)* Why are callable bonds more likely to be called when interest rates fall, and why is that bad for the investor?

<details><summary>Show answer</summary>

The issuer can refinance at lower rates. The investor loses the remaining high coupons, gets only the call price (which limits price gains), and has to reinvest at the new lower rates.
</details>

---

### 📝 End of day recap
1. Write the 4 RCY steps.
2. YTC changes which two calculator inputs?
3. YTW = the ___ of ___
