# Day 7 (Mon 10/19): Term Structure & Forward Rates

**Deck 3 slides:** All of them (only 18)
**Time:** about 60 min
**Warm-up (5 min):** Redo Day 6, Problem 2 (duration estimate).
**Goal:** Read the shape of a yield curve, use expectations theory, calculate forward rates from zero-coupon yields, and explain how a liquidity premium changes the interpretation.

---

## 1. Term structure and the yield curve

- **Term structure of interest rates:** the relationship between **YTM and time to maturity** for otherwise comparable bonds (same credit risk, etc.).
- **Yield curve:** the graph of it (maturity on the x-axis, yield on the y-axis).

**Four shapes to know:** **Upward-sloping** (normal) · **Flat** · **Inverted** (downward) · **Hump-shaped** (rises, then falls)

### The opening question: "Lock in or wait?"
You're investing for 2 years.
- **A:** Lock in a 2-year rate today.
- **B:** Take a 1-year rate now, then reinvest for year 2 at whatever the rate is then.

If you think rates will **rise**, you lean toward B. If you think they'll **fall**, you lock in with A. **The market's collective version of this decision is what shapes the yield curve.**

---

## 2. Expectations theory

**Long-term yields reflect expected future short-term rates.** In equilibrium, locking in for 2 years and rolling over two 1-year investments must give the **same expected** total return.

| Expected future short rates | Yield curve |
|---|---|
| Rise | Upward-sloping |
| Fall | Inverted |
| Stay the same | Flat |

### Slide example
1-year rate today = 8%. The market expects next year's 1-year rate = 10%.
```
(1 + y₂)² = (1.08)(1.10) = 1.188   →   y₂ = 8.995% ≈ 9.0%
```
Expected rates are rising, so the 2-year rate (9%) is above the 1-year rate (8%), and the curve slopes up.

> **Another way to see it (averaging):** A long-term yield is roughly the **average** of the short-term rates expected over its life. The average of 8% and 10% is about 9%. If future rates are expected to be higher, the average is pulled above today's short rate.
>
> **Why would today's long rate already be higher?** If everyone expects rates to rise, nobody wants to lock in a low 2-year rate. Lenders demand that the 2-year rate reflect the higher rate they expect next year, or they'll just roll over instead.

---

## 3. Forward rates

We can't directly see the market's expectations. But we can **back them out** of today's zero-coupon yields.

**Forward rate (f_n):** the 1-year rate for year n that is **implied** by today's yield curve.

```
(1 + y_n)^n = (1 + y_{n−1})^{n−1} × (1 + f_n)

           (1 + y_n)^n
f_n  =  ------------------- − 1
         (1 + y_{n−1})^{n−1}
```
- y_n = YTM on an n-year **zero-coupon** bond
- f_n = implied 1-year forward rate for year n (from the end of year n−1 to the end of year n)

**Under expectations theory: f_n = the expected 1-year rate in year n.**

### Slide example
2-year zero YTM = 6%, 3-year zero YTM = 7%.
```
f₃ = 1.07³ / 1.06² − 1 = 1.225043 / 1.1236 − 1 = 9.03%
```

> **Another way to see it (the "missing piece"):** The 3-year investment covers years 1-2-3. The 2-year investment covers years 1-2. Divide the 3-year growth by the 2-year growth, and what's left over is growth in **year 3 alone**. That's the forward rate.
>
> **Sanity check:** The forward rate is always **further** from the short rate than the long yield is. If yields rise from 6% to 7%, the forward rate (9%) has to be well above 7% to drag the 3-year average up that much.

---

## 4. Liquidity preference theory

**Longer bonds have more price risk** (Deck 2: duration). Investors want extra compensation to hold them. That extra compensation is the **liquidity premium** (also called the **term premium**).

| Expectations theory | Liquidity preference theory |
|---|---|
| Forward rate **=** expected future short rate | Forward rate **=** expected future short rate **+ liquidity premium** |
| Slope reflects rate expectations only | Longer maturities include a positive premium |

### What does the curve tell you?
- **Upward-sloping:** It could mean higher expected rates, **or** just a liquidity premium, **or both**. It's **ambiguous**.
- **Inverted:** **Stronger evidence** that the market expects rates to **fall**, because the curve slopes down **even though** the liquidity premium is pushing it up.

### Putting both together
- Expected rates **rising**: both forces push upward, so the curve slopes **up**.
- Expected rates **falling**: the premium offsets some or all of the drop, so the curve could be up, flat, hump-shaped, or inverted.

> **Another way to see it:** Think of the liquidity premium as a steady upward "tilt" built into every yield curve. A flat curve might actually mean the market expects rates to **fall** a bit, with the premium hiding that. A clearly inverted curve means expectations of falling rates are strong enough to overcome the tilt. This is why inverted curves are watched as a **recession signal**.

---

## ✏️ Practice problems

**1.** *(Slide practice)* The zero-coupon yield curve is: 1-yr **10%**, 2-yr **11%**, 3-yr **12%**. Find the 1-year forward rate for **year 2** and for **year 3**.

<details><summary>Show answer</summary>

f₂ = 1.11² / 1.10 − 1 = 1.2321/1.10 − 1 = **12.01%**
f₃ = 1.12³ / 1.11² − 1 = 1.404928/1.2321 − 1 = **14.03%**
</details>

**2.** Under expectations theory, the 1-year rate is 5% and the market expects next year's 1-year rate to be 7%. What's today's 2-year rate?

<details><summary>Show answer</summary>

(1 + y₂)² = 1.05 × 1.07 = 1.1235, so y₂ = **5.995% ≈ 6.0%**
</details>

**3.** \$1,000-par zero-coupon bonds sell for: 1-yr **\$909.09**, 2-yr **\$811.62**, 3-yr **\$711.78**. Find each YTM, then the forward rates for years 2 and 3. *(This is the format of textbook #43.)*

<details><summary>Show answer</summary>

YTM: y₁ = 1000/909.09 − 1 = **10%**; y₂ = (1000/811.62)^(1/2) − 1 = **11%**; y₃ = (1000/711.78)^(1/3) − 1 = **12%**
Forwards (same as Problem 1): f₂ = **12.01%**, f₃ = **14.03%**
**Shortcut:** f_n = P_{n−1} / P_n − 1. For example, f₂ = 909.09/811.62 − 1 = 12.01%
</details>

**4.** The 1-year zero yields 5% and the 2-year zero yields 6.5%. Find f₂. Under liquidity preference theory with a **1% liquidity premium**, what is the market's expected 1-year rate in year 2?

<details><summary>Show answer</summary>

f₂ = 1.065² / 1.05 − 1 = **8.02%**
Expected rate = forward − premium = 8.02 − 1 = **7.02%**
</details>

**5.** *(Concept)* Under expectations theory, what does an inverted yield curve mean? Under liquidity preference theory, is an upward-sloping curve proof that rates are expected to rise?

<details><summary>Show answer</summary>

Inverted: the market expects short-term rates to **fall**.
Upward-sloping under LPT: **No.** It could be just the liquidity premium, with no expected rise at all.
</details>

**6.** *(Concept)* Under liquidity preference theory, which is larger: the forward rate or the expected future short rate?

<details><summary>Show answer</summary>

**The forward rate**, because it equals the expected rate **plus** a positive liquidity premium.
</details>

---

### 📝 End of day recap
1. f_n formula: ___
2. Expectations theory: forward = ___; LPT: forward = ___
3. Which shape is "stronger evidence" of falling rates? ___
