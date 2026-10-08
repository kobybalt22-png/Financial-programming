# Day 4 (Fri 10/16): Default Risk, Credit Spreads & Deck 1 Wrap-Up

**Deck 1 slides:** "What If the Issuer Cannot Make the Promised Payments?" through "What Causes a Bond's Price to Change?", plus "Promised vs. Expected YTM Example Detailed Solutions" at the end
**Time:** about 60 min (lighter new material, so the last 20 minutes go to reviewing all of Deck 1)
**Warm-up (5 min):** Redo Day 3, Problem 3 (YTC/YTW).
**Goal:** Tell promised YTM apart from expected YTM, work credit-spread problems, and connect everything in Deck 1.

---

## 1. Promised YTM vs. expected YTM

- **Promised (stated) YTM:** uses **all contractual** cash flows and assumes the issuer pays every dollar.
- **Expected YTM:** uses the cash flows you **actually expect** after default losses or partial recovery.

**A high promised YTM ≠ a high expected return.** A junk bond "promising" 14% might really be expected to earn 11%, or less.

> **Another way to see it:** It's like a friend who says "I'll pay you back \$1,000," but who usually pays back only about 70% of what they owe. The *promise* is \$1,000, but your *expectation* should be \$700. Calculate your return on what you expect, not on what was promised.

### Slide example
9% coupon (semiannual \$45), 10 years left, price \$750. Expect all coupons to be paid, but only **\$700** of principal.

| | FV | I/Y (semi) | Annual YTM |
|---|---|---|---|
| Promised | 1,000 | 6.8285 | **13.7%** |
| Expected | 700 | 5.8151 | **11.6%** |

N = 20, PV = −750, PMT = 45 for both. Only FV changes.

---

## 2. Credit ratings and credit spreads

- **Investment grade** (BBB−/Baa3 and above): relatively lower credit risk.
- **Speculative grade** ("junk" or "high yield," BB+/Ba1 and below): relatively higher credit risk.

Investors demand extra yield for bearing credit risk:

```
Credit spread = YTM(corporate) − YTM(Treasury of similar maturity)
```
1% = 100 **basis points (bps)**.

**Chain of cause and effect:** higher perceived credit risk → **wider** spread → higher required yield → **lower** price.

> **Another way to see it:** Think of a corporate bond's yield as two layers stacked together: **Treasury yield** (the "risk-free" base, which reflects the overall level of interest rates) **+ credit spread** (extra pay for the chance the company won't pay you). Either layer can move on its own. Treasury yields move with Fed policy and inflation, and spreads move with the company's health or recession fears.

### Slide example
Treasury 4.3% + spread 250 bps = corporate 6.8%.
Treasury **falls 50 bps** and the spread **widens 100 bps**:
New yield = (4.3 − 0.5) + (2.5 + 1.0) = 3.8 + 3.5 = **7.3%**. The yield went up, so the **price falls**.

---

## 3. What causes a bond's price to change? (Deck 1's closing slide)

1. **Passage of time ("pull to par").** If YTM stays the same, premium bonds drift **down** to \$1,000 and discount bonds drift **up** to \$1,000 as maturity approaches.
2. **Changes in market yields.** Yields up → price down. This is **price risk**, and it matters most if you might sell before maturity.

> "Do all bonds respond equally to the same change in yields?" **No.** That's exactly the question **duration** answers tomorrow.

---

## 4. Deck 1 big picture (copy this map onto your formula sheet)

```
Quoted YTM assumes: hold to maturity + reinvest at YTM + no call + no default
   │
   ├─ sell early ─────────────► HPR  (sale price depends on yields then)
   ├─ coupons reinvested ─────► RCY  (terminal wealth = sale price + FV coupons)
   ├─ issuer calls early ─────► YTC / YTW
   └─ issuer might default ───► Promised YTM vs. Expected YTM
```

---

## ✏️ Practice problems

**1.** An 8-year, 10% semiannual-coupon bond sells for \$800. Investors expect all coupons to be paid, but only **\$600** of principal at maturity. Find the promised and expected YTM.

<details><summary>Show answer</summary>

N = 16, PV = −800, PMT = 50
Promised: FV = 1,000, so I/Y ≈ 7.14, which gives **≈ 14.27%**
Expected: FV = 600, so I/Y ≈ 5.21, which gives **≈ 10.42%**
</details>

**2.** A corporate bond yields 6.8% and the comparable Treasury yields 4.3%. Then the Treasury yield **rises 25 bps** and the spread **narrows 75 bps**. What's the new corporate yield, and does the price rise or fall?

<details><summary>Show answer</summary>

Spread = 250 bps → 175 bps. Treasury = 4.3% → 4.55%.
New yield = 4.55 + 1.75 = **6.30%**. The yield fell, so the **price rises**.
</details>

**3.** *(Pull to par)* The 8%, 30-year semiannual bond from Day 1 is priced at \$1,276.76 when YTM = 6%. If the YTM stays at 6%, what is its price one year later (29 years left)? Did it move toward par?

<details><summary>Show answer</summary>

N = 58, I/Y = 3, PMT = 40, FV = 1,000, so **\$1,273.31**. It fell slightly toward \$1,000 ✔
</details>

**4.** *(Concept)* Bond X is rated AAA and yields 5%. Bond Y is rated B and promises 9%. Is Bond Y necessarily the better investment?

<details><summary>Show answer</summary>

**No.** 9% is a *promised* yield. After expected default losses, Y's expected YTM could be much lower, and Y carries more risk.
</details>

**5.** *(Deck 1 opening question)* Can an investor lose money on a Treasury bond even if every promised payment is made?

<details><summary>Show answer</summary>

**Yes.** If yields rise and the investor sells before maturity, the capital loss can be larger than the coupon income (see the 2026 example: −3.46% HPR).
</details>

---

### 🔁 Deck 1 self-test (10 min, no notes)
Without looking, write the formula or rule for: price, invoice price, BEY, EAY, CY ordering, HPR, RCY, YTC, credit spread. Check your answers against Days 1–4. **Circle anything you missed, since that's what you'll review on Day 8.**
