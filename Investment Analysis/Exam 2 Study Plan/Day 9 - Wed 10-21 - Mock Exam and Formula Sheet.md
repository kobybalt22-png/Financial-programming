# Day 9 (Wed 10/21): Mock Exam & Formula Sheet

**The day before the exam. Keep it light.**
**Time:** about 60 min, then stop. Get a full night's sleep.

1. **Mock exam (40 min, timed, no notes)**
2. **Grade it, and redo anything you missed (10 min)**
3. **Read the formula sheet twice (10 min)**

---

## Part 1: Mock exam

**1.** A 12-year, 5% semiannual-coupon bond has a YTM of 6.5%. What is its price?

**2.** A 10-year, 6% annual-coupon bond sells for \$950. Find its YTM and current yield.

**3.** A 7% semiannual-coupon bond is quoted at \$1,020. It has been 90 days since the last coupon, in a 181-day period. What is the invoice price?

**4.** You bought the bond from Question 2 for \$950. One year later (9 years left), its YTM is 6%. You sell right after receiving the coupon. What is your HPR?

**5.** A bond position worth \$1,050 has a modified duration of 6. Yields rise 25 bps. Estimate the % and \$ change in value.

**6.** A semiannual bond has a Macaulay duration of 5.4 years and a YTM of 8%. What is its modified duration?

**7.** Zero-coupon yields: 1-yr 4%, 2-yr 5%, 3-yr 5.5%. Find f₂ and f₃.

**8.** Under liquidity preference theory, f₂ = 6% and the liquidity premium is 0.5%. What is the market's expected 1-year rate in year 2?

**9.** A 10-year, 9% semiannual-coupon bond sells for \$1,120. It is callable in 3 years at \$1,045. Find the YTC, YTM, and YTW.

**10.** *(Concepts)*
- (a) Rank by duration, highest first: (i) 20-yr, 6% coupon, YTM 8%; (ii) 20-yr zero; (iii) 20-yr, 6% coupon, YTM 4%; (iv) 10-yr, 6% coupon, YTM 8%.
- (b) A coupon bond is held to maturity with no default. The reinvestment rate is below the YTM. RCY vs. YTM?
- (c) Your horizon is longer than the bond's duration. Do rising rates help or hurt you?
- (d) Does an upward-sloping yield curve prove that rates are expected to rise?

---

<details><summary><b>Answer key (only after you finish!)</b></summary>

**1.** N = 24, I/Y = 3.25, PMT = 25, FV = 1,000, so **\$876.34**

**2.** N = 10, PV = −950, PMT = 60, FV = 1,000, so **YTM = 6.70%**. CY = 60/950 = **6.32%** (discount: 6% < 6.32% < 6.70% ✔)

**3.** Accrued interest = 35 × 90/181 = \$17.40, so the invoice price = **\$1,037.40**

**4.** YTM = coupon rate, so the sale price = \$1,000 (par). HPR = (1,000 − 950 + 60)/950 = **11.58%**

**5.** ΔP/P ≈ −6 × 0.0025 = **−1.5%**. ΔP ≈ −0.015 × 1,050 = **−\$15.75**

**6.** 5.4 / 1.04 = **5.192**

**7.** f₂ = 1.05²/1.04 − 1 = **6.01%**. f₃ = 1.055³/1.05² − 1 = **6.51%**

**8.** 6% − 0.5% = **5.5%**

**9.** YTC: N = 6, PV = −1,120, PMT = 45, FV = 1,045, so I/Y = 2.98, which gives **YTC ≈ 5.96%**
YTM: N = 20, PV = −1,120, PMT = 45, FV = 1,000, so I/Y = 3.64, which gives **YTM ≈ 7.29%**
**YTW = 5.96%**

**10.** (a) **ii > iii > i > iv** (zero = 20; lower YTM raises duration; shorter maturity lowers it)
(b) **RCY < YTM**
(c) **Help.** The reinvestment effect dominates.
(d) **No.** It could just reflect a liquidity premium.

**Scoring:** 9–10 = you're ready. 7–8 = re-read the days for the ones you missed. Below 7 = redo Day 8's mixed set tonight, but stop by a reasonable hour.
</details>

---

## Part 2: Formula sheet

### Bond pricing (Deck 1)
| Concept | Formula / rule |
|---|---|
| Coupon payment | coupon rate × FV ÷ m |
| Price | PV(coupons) + PV(FV). Semiannual: N = yrs×2, I/Y = YTM÷2, PMT = coupon÷2 |
| Premium / Par / Discount | coupon > / = / < YTM |
| Accrued interest | (annual coupon ÷ 2) × (days since last coupon ÷ days in period) |
| Invoice (dirty) price | flat (quoted) price + accrued interest |
| BEY | periodic YTM × m |
| EAY | (1 + periodic YTM)^m − 1 |
| Current yield | annual coupon ÷ price |
| CY ordering | Premium: C > CY > YTM · Discount: C < CY < YTM |
| HPR | (coupon + P_end − P_begin) ÷ P_begin |
| RCY | (terminal wealth ÷ purchase price)^(1/n) − 1 |
| Terminal wealth | sale price + FV of reinvested coupons |
| RCY vs. YTM | reinvestment rate < YTM → RCY < YTM (and vice versa) |
| YTC | YTM calculation with N = periods to call and FV = call price |
| YTW | lowest of YTC(s) and YTM |
| Expected YTM | YTM calculation using **expected** (not promised) cash flows |
| Credit spread | YTM(corp) − YTM(Treasury); 100 bps = 1% |

### Interest-rate risk (Deck 2)
| Concept | Formula / rule |
|---|---|
| More sensitive when | **long** maturity, **low** coupon, **low** YTM |
| Macaulay duration | Σ t × w_t, with w_t = PV(CF_t)/price. Semiannual: divide by 2 |
| Zero-coupon | D_Mac = maturity |
| Modified duration | D_Mac ÷ (1 + YTM/m) |
| % price change | ΔP/P ≈ −D_Mod × Δy |
| \$ price change | ΔP ≈ −D_Mod × Δy × P₀ |
| Duration error | overstates losses (rates ↑), understates gains (rates ↓), because of convexity |
| Horizon < D | price effect dominates · Horizon = D: offset (immunized) · Horizon > D: reinvestment effect dominates |

### Term structure (Deck 3)
| Concept | Formula / rule |
|---|---|
| Expectations | (1 + y₂)² = (1 + r₁)(1 + E[r₂]) |
| Forward rate | f_n = (1 + y_n)^n ÷ (1 + y_{n−1})^{n−1} − 1 |
| From zero prices | f_n = P_{n−1} ÷ P_n − 1 |
| Expectations theory | forward = expected short rate |
| Liquidity preference | forward = expected short rate + liquidity premium |
| Upward curve | expectations ↑ **or** liquidity premium **or** both (ambiguous) |
| Inverted curve | strong evidence that rates are expected to fall |

---

### 🧠 Night-before checklist
- [ ] Calculator: fresh battery, and P/Y set to **1** (enter the per-period rate yourself)
- [ ] Clear the TVM registers between problems (`2nd` → `CLR TVM`)
- [ ] Read the formula sheet once more before bed
- [ ] Sleep. A rested brain beats another hour of cramming.

**Good luck tomorrow! 🍀**
