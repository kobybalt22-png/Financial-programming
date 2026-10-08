# Day 2 (Wed 10/14): YTM, Current Yield & Holding-Period Return

**Deck 1 slides:** "Bond Returns: Which Question Does Each Answer?" through "10-Year Treasury HPR Example", plus the "Current Yield" slide near the end
**Time:** about 60 min
**Warm-up (5 min):** Redo Day 1, Problem 1.
**Goal:** Solve for YTM, convert it to BEY and EAY, calculate current yield, and calculate a holding-period return when you sell early.

---

## 1. The "menu" of return measures

Every yield measure answers a **different question**. This table from the slides is worth memorizing:

| Measure | Question it answers |
|---|---|
| **YTM** | What return is implied if I hold to maturity and everything goes as planned? |
| **HPR** | What did I actually earn over the time I held it? |
| **RCY** | What compound return do I earn after reinvesting coupons and selling or redeeming? *(Day 3)* |
| **YTC / YTW** | What if the bond gets called, and what's the worst case? *(Day 3)* |
| **Expected YTM** | What yield do I get after allowing for default losses? *(Day 4)* |
| **Current yield** | How much coupon income am I getting relative to the price? |

Today covers YTM, current yield, and HPR.

---

## 2. Yield to maturity (YTM)

**YTM is the bond's internal rate of return (IRR).** It's the single discount rate that makes the PV of the promised cash flows equal today's price.

On Day 1, you knew the rate and solved for the **price**. Now you know the **price** and solve for the rate.

> **Another way to see it:** YTM is the "interest rate the bond is secretly paying you." If you put the bond's price into a savings account that paid exactly YTM, you could recreate the bond's cash flows exactly.

### Slide example
8% coupon, 30 years, semiannual, price \$1,276.76.
N = 60, PV = −1,276.76, PMT = 40, FV = 1,000, so **CPT I/Y = 3%** per 6 months.

### Annualizing: BEY vs. EAY
- **Bond-equivalent yield (BEY):** periodic rate × m = 3% × 2 = **6%**. This is simple, with no compounding, and it's how bond yields are normally quoted.
- **Effective annual yield (EAY):** (1 + periodic rate)^m − 1 = 1.03² − 1 = **6.09%**. This includes compounding.

They describe the **same** investment using two different conventions. EAY is always ≥ BEY.

> **Analogy:** BEY is like a credit card's "APR" and EAY is like its "effective rate." The card charges the same interest either way. EAY just counts the interest-on-interest.

### When does YTM actually equal your return?
Only if **all four** of these hold:
1. You hold to maturity.
2. You reinvest every coupon at the YTM.
3. The bond isn't called.
4. The issuer pays everything (no default).

Break any one of them and your actual return can differ. The rest of Deck 1 is about each of these breaking: selling early → **HPR**; reinvestment → **RCY**; calls → **YTC**; default → **expected YTM**.

---

## 3. Current yield (CY)

```
CY = Annual coupon / Current price
```
It only measures **income**. It ignores capital gains and losses and ignores reinvestment.

**The ordering rule (common multiple-choice question):**

| Bond | Ordering |
|---|---|
| Premium | Coupon rate **>** CY **>** YTM |
| Par | Coupon rate **=** CY **=** YTM |
| Discount | Coupon rate **<** CY **<** YTM |

> **Why?** For a premium bond, you paid more than \$1,000 but only get \$1,000 back, so a capital **loss** is built in. CY ignores that loss, so it's too high compared with YTM. A discount bond has a built-in capital **gain** that CY ignores, so CY is too low compared with YTM.
> **Memory trick:** CY is always "stuck in the middle" between the coupon rate and YTM.

---

## 4. Holding-period return (HPR)

If you sell before maturity, your return depends on the **sale price**, and the sale price depends on **market yields at the time you sell**.

```
       Coupon income + (Ending price − Beginning price)
HPR = --------------------------------------------------
                     Beginning price
```

Chain of cause and effect: **market yields change → bond price changes → sale price changes → your return changes.**

### Slide example: the real 2026 Treasury story
- 3/17/2026: Bought a 10-year Treasury at par. Coupon 4.20% (\$21 every 6 months), YTM 4.20%.
- 9/17/2026: Received one \$21 coupon, then sold. 9.5 years were left and market YTM was now **4.94%**.
- Sale price: N = 19, I/Y = 2.47, PMT = 21, FV = 1,000, which gives about **\$944.43**.
- HPR = (944.43 − 1,000 + 21) / 1,000 = **−3.46%**.

**Answers the opening question:** "Can you lose money on a Treasury even if every payment is made?" **Yes.** There's no default risk, but there **is** interest-rate risk. Rising yields caused a capital loss bigger than the coupon income.

---

## ✏️ Practice problems

**1.** A 20-year, 7% semiannual-coupon bond sells for \$1,100. Find the **(a)** periodic YTM, **(b)** BEY, **(c)** EAY, and **(d)** current yield. **(e)** Check that the ordering rule holds.

<details><summary>Show answer</summary>

N = 40, PV = −1,100, PMT = 35, FV = 1,000
(a) I/Y = **3.063%** per half-year
(b) BEY = 3.063 × 2 = **6.13%**
(c) EAY = 1.03063² − 1 = **6.22%**
(d) CY = 70 / 1,100 = **6.36%**
(e) Premium bond: coupon 7% > CY 6.36% > YTM 6.13% ✔
</details>

**2.** You buy a 10-year, 5% **annual**-coupon bond at par. One year later (9 years left), market YTM has risen to 6%, and you sell right after receiving the coupon. Find the sale price and the HPR.

<details><summary>Show answer</summary>

Sale price: N = 9, I/Y = 6, PMT = 50, FV = 1,000, so **PV = \$931.98**
HPR = (50 + 931.98 − 1,000) / 1,000 = **−1.80%**
The coupon (+\$50) couldn't cover the capital loss (−\$68.02).
</details>

**3.** *(Check the slide)* Confirm the \$944.43 sale price in the Treasury example on your calculator.

<details><summary>Show answer</summary>

N = 19, I/Y = 4.94/2 = 2.47, PMT = 21, FV = 1,000, so PV = **−944.43** ✔
</details>

**4.** *(Concept)* A bond's coupon rate is 6% and its current yield is 6.5%. Is its YTM above or below 6.5%? Is it a premium or discount bond?

<details><summary>Show answer</summary>

CY > coupon rate, so the price is below par, which makes it a **discount** bond. For a discount bond, coupon < CY < YTM, so **YTM > 6.5%**.
</details>

**5.** *(Concept)* Name the four conditions needed for your realized return to equal the YTM.

<details><summary>Show answer</summary>

Hold to maturity · reinvest coupons at the YTM · no call · no default.
</details>

---

### 📝 End of day recap
1. YTM is the ___ of the bond.
2. BEY = ___; EAY = ___
3. Discount bond ordering: ___ < ___ < ___
4. HPR formula: ___
