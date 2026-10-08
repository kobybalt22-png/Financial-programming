# Day 5 (Sat 10/17): Interest-Rate Sensitivity & Macaulay Duration

**Deck 2 slides:** Start through "Zero-Coupon Bond: A Useful Benchmark"
**Time:** about 70 min (the duration table is the main skill today)
**Warm-up (5 min):** Redo Day 4, Problem 2 (credit spread).
**Goal:** Rank bonds by interest-rate sensitivity without calculating, and build a Macaulay duration table by hand.

---

## 1. What is interest-rate risk?

```
Interest rates change → bond price changes (capital gain/loss) → your return is uncertain
```
Interest-rate risk affects **two** things: bond **prices** and the **reinvestment** of coupons. Deck 2 focuses mainly on **price sensitivity**.

**Opening question:** If yields rise 1%, do a 5-year, 8% bond and a 30-year, 8% bond lose the same %? **No.** The 30-year bond loses much more.

---

## 2. The three drivers of sensitivity

Holding everything else constant, a bond is **more** sensitive to rate changes when it has:

| Driver | Why |
|---|---|
| **Longer maturity** | Cash flows are further away, so discounting hits them harder |
| **Lower coupon** | More of the value sits in the distant \$1,000 payment |
| **Lower YTM** | Distant cash flows get relatively more weight when the discount rate is low |

**Memory line: "Long, Low, Low"** = long maturity + low coupon + low YTM = most interest-rate exposure.

> **Another way to see it (the seesaw/lever):** Picture each cash flow as a weight sitting on a long plank, at a distance equal to when it's paid. Weights far from you (late cash flows) swing much more when the plank tilts (rates change). A low coupon puts almost all the weight at the far end. A high coupon puts lots of weight close to you, which steadies things.

### Slide comparison (calculated for a +1% yield move, semiannual)
| Bond | Coupon | Maturity | YTM | Price change for +1% |
|---|---|---|---|---|
| A | 12% | 5 yrs | 10% | −3.7% |
| B | 12% | 30 yrs | 10% | −8.6% |
| C | 3% | 30 yrs | 10% | −10.5% |
| D | 3% | 30 yrs | 6% | **−14.3%** |

A → B: longer maturity. B → C: lower coupon. C → D: lower YTM. Each step increases sensitivity.

### Convexity
Price sensitivity is **nonlinear**. For Bond D, a **4-point drop** in yield raises the price about **110%**, while a **4-point rise** lowers it only about **40%**. Equal yield changes produce unequal price changes, and the gains are bigger than the losses.

---

## 3. From maturity to duration

Maturity alone isn't enough. Two 30-year bonds can have very different sensitivity because **coupons paid earlier shorten the bond's effective life**. We need a measure that includes both maturity **and** the timing of the cash flows.

### Macaulay duration = the weighted-average time until you receive the cash flows

```
          T
D_Mac =   Σ  t × w_t          where  w_t = PV(CF_t) / Bond price
         t=1
```
- Each weight = that cash flow's **share of the bond's price**. The weights add up to 1.
- Earlier cash flows shorten duration; later ones lengthen it.
- **A coupon bond's duration is less than its maturity.**
- **A zero-coupon bond's duration equals its maturity** (it has only one cash flow).

**Semiannual bonds:** use the semiannual YTM and cash flows. The result is in **half-years**, so **divide by 2** to get years.

> **Another way to see it (center of gravity):** Lay the PV of each cash flow along a timeline as blocks of different weight. Macaulay duration is the **balance point** of that timeline. A zero-coupon bond has one block at the very end, so the balance point is at maturity. Coupons add blocks earlier, which pulls the balance point toward today.

### Slide example: 10% coupon, 2-year, semiannual, YTM 15% (7.5% per period)

| t | CF | PV of CF | Weight | t × w |
|---|---|---|---|---|
| 1 | 50 | 46.5116 | 0.0508 | 0.0508 |
| 2 | 50 | 43.2666 | 0.0472 | 0.0944 |
| 3 | 50 | 40.2480 | 0.0439 | 0.1318 |
| 4 | 1,050 | 786.2406 | 0.8581 | 3.4324 |
| | | **916.2668** | **1.0000** | **3.7093 half-years** |

D_Mac = 3.7093 / 2 = **1.8547 years** (< 2-year maturity).
The same 2-year **zero**-coupon bond has D_Mac = **2.00 years**.

**How to build the table:**
1. List each period t and its cash flow (coupon; coupon + 1,000 at the end).
2. PV = CF / (1 + r)^t. Add these up, which should give the bond price.
3. Weight = PV / price.
4. Multiply t × weight and add them up. Divide by m if the bond is semiannual.

---

## ✏️ Practice problems

**1.** *(No math)* Rank Bonds A–D in the table above from **most** to **least** sensitive, and give the reason for each step.

<details><summary>Show answer</summary>

**D > C > B > A**. D vs. C: lower YTM. C vs. B: lower coupon. B vs. A: longer maturity.
</details>

**2.** Find the Macaulay duration of a **3-year, 8% annual**-coupon bond with a YTM of **10%**.

<details><summary>Show answer</summary>

| t | CF | PV | Weight | t × w |
|---|---|---|---|---|
| 1 | 80 | 72.7273 | 0.0765 | 0.0765 |
| 2 | 80 | 66.1157 | 0.0696 | 0.1392 |
| 3 | 1,080 | 811.4200 | 0.8539 | 2.5617 |
| | | **950.2630** | 1.0000 | **2.7774** |

**D_Mac ≈ 2.78 years**
</details>

**3.** Find the Macaulay duration (in **years**) of a **1.5-year, 6% semiannual**-coupon bond with a YTM of **8%**.

<details><summary>Show answer</summary>

r = 4% per period, CF = 30, 30, 1,030

| t | CF | PV | Weight | t × w |
|---|---|---|---|---|
| 1 | 30 | 28.8462 | 0.0297 | 0.0297 |
| 2 | 30 | 27.7367 | 0.0285 | 0.0571 |
| 3 | 1,030 | 915.6662 | 0.9418 | 2.8254 |
| | | **972.2491** | 1.0000 | **2.9121 half-years** |

**D_Mac = 2.9121 / 2 ≈ 1.456 years**
</details>

**4.** What is the Macaulay duration of a 7-year zero-coupon bond? Of a 7-year bond with a 5% coupon? (Give exact or "less than.")

<details><summary>Show answer</summary>

Zero: **exactly 7 years**. Coupon bond: **less than 7 years**.
</details>

**5.** *(Concept)* Two bonds both mature in 20 years. One has a 2% coupon and the other a 12% coupon. Which has the higher duration, and why?

<details><summary>Show answer</summary>

**The 2% coupon bond.** More of its value comes from the distant principal payment, so its weighted-average timing is later.
</details>

---

### 📝 End of day recap
1. "Long, Low, Low" means ___
2. Macaulay duration = weighted-average ___ where weights = ___
3. A zero's duration = ___
