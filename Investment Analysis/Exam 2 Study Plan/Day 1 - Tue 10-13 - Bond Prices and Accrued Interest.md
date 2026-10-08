# Day 1 (Tue 10/13): Bond Prices & Accrued Interest

**Deck 1 slides:** "Learning Objectives" through "Accrued Interest Example"
**Time:** about 60 min
**Goal:** Price any fixed-coupon bond on your calculator, know whether it's a premium, par, or discount bond without calculating, and turn a quoted price into the price you actually pay.

---

## 1. What a bond actually is

A **fixed-coupon bond (FCB)** is a promise of two kinds of cash flow:
- **Coupons**: equal payments every period.
  `Coupon payment = coupon rate × face value ÷ payments per year`
- **Face value (par)**: one lump sum at maturity. Assume **\$1,000** unless told otherwise.

**Bond price = PV of coupons + PV of face value**

```
        C          C                C + FV
P = -------- + -------- + ... + -----------
     (1+r)^1    (1+r)^2           (1+r)^N
```
Here `r` is the **per-period** yield (annual YTM ÷ m), and `N` is the **number of periods** (years × m).

> **Another way to see it:** A bond is a bundle of small IOUs. Each coupon and the final \$1,000 is its own mini-IOU. Discount each one back to today and add them up. The price is just "what is this pile of future money worth right now?"

### Slide example (memorize the pattern)
8% coupon, 30 years, semiannual, so the coupon is \$40 every 6 months. N = 60, PMT = 40, FV = 1,000.

| YTM | I/Y | Price | Type |
|---|---|---|---|
| 6% | 3 | \$1,276.76 | Premium |
| 8% | 4 | \$1,000.00 | Par |
| 10% | 5 | \$810.71 | Discount |

---

## 2. The price–yield relationship

- **Yields up → prices down. Yields down → prices up.** They always move in opposite directions.
- **The relationship is curved, not a straight line.** It bows toward the origin (it's **convex**). Equal-sized moves in yield up and down do **not** produce equal-sized price changes. From the table: dropping 2% (8→6) gains \$276.76, but rising 2% (8→10) loses only \$189.29.

> **Why do prices fall when rates rise? (another explanation):** Say you own a bond paying 8%, and new bonds now pay 10%. Nobody will pay full price for your 8% bond when they can get 10% elsewhere. You have to cut your price until the buyer's overall return is also 10%. The lower price makes up for the smaller coupon.
>
> **Seesaw picture:** Put price on one end and yield on the other. One goes up, the other goes down, every time.

---

## 3. Premium, par, and discount

| Relationship | Price | Name |
|---|---|---|
| Coupon rate **>** YTM | Above \$1,000 | **Premium** |
| Coupon rate **=** YTM | Exactly \$1,000 | **Par** |
| Coupon rate **<** YTM | Below \$1,000 | **Discount** |

**Memory trick:** "**C**oupon **C**ompared to the market." If your coupon beats what the market demands, buyers pay extra (premium). If it loses, they pay less (discount).

**Slide question: "Is a discount bond necessarily a better investment?"** **No.** The discount isn't a bargain. It's exactly the amount needed to give the buyer the market's required yield, because the coupon is low. Premium and discount bonds with the same risk are priced to give the **same** YTM.

---

## 4. Flat price, invoice price, and accrued interest

Bonds don't only trade on coupon dates. If you buy between coupons, the seller has "earned" part of the next coupon, but **you** will receive all of it. So you pay the seller their share up front.

- **Flat (clean) price:** the **quoted** price. It does not include accrued interest.
- **Invoice (dirty) price:** what you **actually pay**.

```
Accrued interest = (annual coupon / 2) × (days since last coupon / days in coupon period)
Invoice price    = Flat (quoted) price + Accrued interest
```

> **Another way to see it:** It works like splitting rent when you move out mid-month. The seller owned the bond for 45 of the 180 days, so they get 45/180 of the next coupon, and you hand it to them when you buy.
>
> **Why quote the clean price?** If quotes included accrued interest, the price would jump up a little every day and then drop on each coupon date, even with no change in rates. The clean price takes out that "sawtooth" so the quote only moves when the market actually moves.

### Slide example
6% coupon, semiannual, so the coupon is \$30. 45 days into a 180-day period.
Accrued interest = 30 × 45/180 = **\$7.50**. Quoted price \$990, so the invoice price = **\$997.50**.

---

## ✏️ Practice problems

**1.** A 10-year, 6% coupon bond pays semiannually. Find its price if the YTM is **(a)** 5% and **(b)** 7%. Label each one premium, par, or discount.

<details><summary>Show answer</summary>

N = 20, PMT = 30, FV = 1,000
(a) I/Y = 2.5, so **PV = \$1,077.95** (premium, because coupon 6% > YTM 5%)
(b) I/Y = 3.5, so **PV = \$928.94** (discount, because coupon 6% < YTM 7%)
</details>

**2.** *(Slide "Apply What We Learned")* A 10-year bond was issued **at par** four years ago and pays annual coupons. Its YTM has since fallen from 9% to 7%. Is it trading below par, at par, or above par?

<details><summary>Show answer</summary>

**C. Above par.** It was issued at par, so its coupon rate equals the original YTM of 9%. Now the coupon (9%) is greater than the YTM (7%), which makes it a premium bond. You don't need to calculate anything.
</details>

**3.** An 8% semiannual-coupon bond has a quoted price of \$1,015. It has been **60 days** since the last coupon, and the coupon period is **182 days**. Find the accrued interest and the invoice price.

<details><summary>Show answer</summary>

Semiannual coupon = 0.08 × 1,000 / 2 = \$40
Accrued interest = 40 × 60/182 = **\$13.19**
Invoice price = 1,015 + 13.19 = **\$1,028.19**
</details>

**4.** *(By hand, to make sure you understand the formula.)* A 3-year, 5% **annual**-coupon bond has a YTM of 6%. Find the price by discounting each cash flow.

<details><summary>Show answer</summary>

50/1.06 + 50/1.06² + 1,050/1.06³ = 47.17 + 44.50 + 881.60 = **\$973.27** (discount, since 5% < 6%)
</details>

**5.** *(Concept)* True or false: if a bond's yield rises by 1% and then falls by 1%, the price loss and the price gain are the same size.

<details><summary>Show answer</summary>

**False.** Because of convexity, a yield decrease raises the price **more** than an equal increase lowers it.
</details>

---

### 📝 End of day recap (write from memory)
1. Price = ___ + ___
2. Coupon > YTM means ___ bond
3. Invoice price = ___ + ___
