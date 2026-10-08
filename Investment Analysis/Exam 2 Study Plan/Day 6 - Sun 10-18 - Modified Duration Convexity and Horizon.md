# Day 6 (Sun 10/18): Modified Duration, Convexity & Investment Horizon

**Deck 2 slides:** "From Macaulay Duration to Modified Duration" through the end
**Time:** about 60 min
**Warm-up (5 min):** Redo Day 5, Problem 2 (duration table).
**Goal:** Use modified duration to estimate % and \$ price changes, explain why duration over- or under-estimates, rank bonds by duration, and connect duration to investment horizon.

---

## 1. Modified duration

Macaulay duration measures **timing**. Modified duration turns that timing into **price sensitivity**:

```
            D_Mac
D_Mod = ---------------        m = coupon payments per year
          1 + YTM/m
```
**Slide:** D_Mac = 1.8547, YTM 15%, m = 2, so D_Mod = 1.8547 / 1.075 = **1.7253**

**Meaning:** a 1-point (1%) change in YTM moves the price about **1.7253%** in the **opposite** direction.

---

## 2. Estimating price changes

```
% change:   ΔP/P ≈ −D_Mod × Δy            (Δy as a decimal: 50 bps = 0.005)
$ change:   ΔP   ≈ −D_Mod × Δy × P₀       (P₀ = current price or market value)
```

> **Another way to see it:** Modified duration is the bond's "**multiplier**." Yield moves by 1%, and the price moves by (multiplier)%. A bond with D_Mod = 7 is like a lever that turns every 1% rate change into about a 7% price swing.

### Percentage vs. dollar exposure (slide example: Δy = +0.005)
| Position | Value | D_Mod | % change | \$ change |
|---|---|---|---|---|
| A | \$2M | 7 | −7 × 0.005 = **−3.5%** | −\$70,000 |
| B | \$5M | 3 | −3 × 0.005 = **−1.5%** | **−\$75,000** |

A has the larger **percentage** loss, but B has the larger **dollar** loss. **Dollar exposure depends on both duration and position size.**

---

## 3. How accurate is duration? (Convexity)

| 2-yr bond, YTM 15% → 16% | 10% coupon | Zero coupon |
|---|---|---|
| D_Mod | 1.7253 | 1.8605 |
| Actual % change | −1.71% | −1.84% |
| Duration estimate | −1.73% | −1.86% |

Duration is very close for **small** yield changes.

**But duration is a straight-line (linear) estimate of a curved price–yield relationship.** For large changes, the error grows.

### Slide example: large shock
10-year Treasury, 1.5% coupon, priced at \$1,000, D_Mod = 9.254. YTM jumps 1.5% → **5.0%** (+350 bps).
- Duration estimate: −9.254 × 0.035 = **−32.39%**, which gives a price of **\$676.11**
- Actual price: **\$727.19** (−27.28%)

| New YTM | Change | Duration estimate | Actual |
|---|---|---|---|
| 2.0% | +50 bps | \$953.73 | \$954.89 |
| 5.0% | +350 bps | \$676.11 | \$727.19 |

**Key rule (very likely on the exam):** Because the price–yield curve is convex, the straight duration line always lies **below** the actual curve. So duration:
- **Overstates losses** when yields **rise**
- **Understates gains** when yields **fall**

Either way, duration estimates a price **lower** than the true price.

> **Another way to see it:** Picture a ramp (duration) laid against a curved bowl (actual prices). It touches the bowl at today's yield. Move away from that point in either direction, and the bowl curves **up** above the ramp. That's why the real price is always a bit higher than duration predicts. **Convexity is good for bondholders.**

---

## 4. Determinants of Macaulay duration (and ranking)

Holding other factors constant:
- **Longer maturity → higher** duration (generally)
- **Lower coupon → higher** duration
- **Lower YTM → higher** duration (coupon bonds)
- **Zero-coupon:** duration = maturity (always the highest at a given maturity)

These are the same "Long, Low, Low" rules from Day 5.

### Slide ranking exercise (annual coupons assumed)
| Bond | Coupon | Maturity | YTM |
|---|---|---|---|
| A | 15% | 20 | 10% |
| B | 15% | 15 | 10% |
| C | 0% | 20 | 10% |
| D | 8% | 20 | 10% |
| E | 15% | 15 | 15% |

**Answer: C > D > A > B > E**
- C: zero, so duration = 20 (highest)
- D vs. A: same maturity and YTM, but D has the lower coupon, so D is higher
- A vs. B: same coupon and YTM, but A has the longer maturity, so A is higher
- B vs. E: same coupon and maturity, but E has the higher YTM, so E is lowest

(Actual values: C 20, D 9.75, A 8.81, B 7.79, E 6.72)

---

## 5. Investment horizon vs. duration

Rising rates have **two opposite** effects:
- **Price effect:** the bond's value falls (bad)
- **Reinvestment effect:** coupons get reinvested at higher rates (good)

| Your horizon compared with D_Mac | What dominates |
|---|---|
| **Shorter** than duration | **Price** effect, so rising rates hurt you |
| **About equal** to duration | The two effects roughly **offset** (this is the idea behind **immunization**) |
| **Longer** than duration | **Reinvestment** effect, so rising rates help you |

> **Another way to see it:** If you need the money soon, you'll have to **sell**, so you care about price. If you're holding a long time, you mostly care about how fast your coupons **grow**. When duration matches your horizon, the two cancel out and your wealth is "immunized" against small rate changes.

---

## ✏️ Practice problems

**1.** From Day 5: a 3-year, 8% annual bond with YTM 10% has D_Mac = 2.7774 and price \$950.26. Find D_Mod.

<details><summary>Show answer</summary>

D_Mod = 2.7774 / 1.10 = **2.5249**
</details>

**2.** Using Problem 1, the yield rises **50 bps** to 10.5%. Estimate the % change and the new price. The actual new price is \$938.37. Did duration overstate or understate the loss?

<details><summary>Show answer</summary>

ΔP/P ≈ −2.5249 × 0.005 = **−1.262%**
Estimated price ≈ 950.26 × (1 − 0.01262) = **\$938.27**
Actual \$938.37 (−1.251%). Duration **overstated the loss** slightly, because of convexity.
</details>

**3.** Same bond, but the yield instead **falls 200 bps** to 8%. Estimate the % change. The actual price is \$1,000 (+5.23%). Over- or understated?

<details><summary>Show answer</summary>

ΔP/P ≈ −2.5249 × (−0.02) = **+5.05%**. Actual +5.23%, so duration **understated the gain**.
</details>

**4.** You hold a \$3M portfolio with D_Mod = 6.5. Yields rise 30 bps. Estimate the \$ change.

<details><summary>Show answer</summary>

ΔP ≈ −6.5 × 0.003 × 3,000,000 = **−\$58,500** (a −1.95% change)
</details>

**5.** A bond has D_Mac = 8.2 years, YTM 6%, semiannual coupons. Find D_Mod.

<details><summary>Show answer</summary>

8.2 / (1 + 0.06/2) = 8.2 / 1.03 = **7.961**
</details>

**6.** *(Concept)* Your investment horizon is 4 years, and you hold a bond with a Macaulay duration of 9 years. Are you more worried about rates rising or falling? Why?

<details><summary>Show answer</summary>

**Rising.** Your horizon is shorter than the duration, so the price effect dominates. Rising rates would push down the price you sell at.
</details>

---

### 📝 End of day recap
1. D_Mod = ___
2. ΔP/P ≈ ___; ΔP (\$) ≈ ___
3. Duration ___ losses and ___ gains, because of ___
4. Horizon = duration means ___
