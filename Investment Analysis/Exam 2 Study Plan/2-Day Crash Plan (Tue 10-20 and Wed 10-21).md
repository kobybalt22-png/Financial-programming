# 2-Day Crash Plan: Exam 2 on Thursday 10/22

You have two days, so this plan squeezes the 9-day plan into **about 3.5 hours today and about 4 hours tomorrow**. It uses the same day files, but you'll only do the parts that matter most.

## How to study (this matters more than how long you study)

1. **Start with the problems, not the reading.** For each topic, try the practice problem **first**. Read the notes only for the part where you get stuck. Solving problems is what the exam tests, and it's the fastest way to learn.
2. **Skip the "Another way to see it" boxes** unless a concept doesn't make sense. They're there for when you're stuck, not required reading.
3. **Write each formula from memory** at the end of every block. If you can't recall it, you don't know it yet.
4. **Take a 10-minute break between blocks.** Get up, and stay off your phone if you can.
5. **Sleep both nights.** Memory locks in during sleep. Pulling an all-nighter will cost you more points than the extra hour of studying gains.

6. **Textbook problems:** after each block, do the matching assigned textbook problems in [Textbook Problems - Ch 10 and 11 (Solved)](Textbook%20Problems%20-%20Ch%2010%20and%2011%20(Solved).md). They're grouped by deck and fully solved. Your professor picked these, so they're the closest thing to real exam questions.

---

## TODAY (Tue 10/20): Deck 1, Bond Pricing & Yields (the biggest deck)

| Block | Time | Open this file | Do these problems | Must be able to |
|---|---|---|---|---|
| 1 | 45 min | Day 1 | #1, #2, #3 | Price a semiannual bond; premium/par/discount; invoice price = quoted price + accrued interest |
| 2 | 45 min | Day 2 | #1, #2, #4 | Solve for YTM; BEY vs. EAY; current yield ordering; HPR |
| ☕ | 10 min | | | |
| 3 | 50 min | Day 3 | #1, #3, then #2 if time | **The 4-step RCY recipe**; YTC (N = periods to call, FV = call price); YTW = lowest |
| 4 | 30 min | Day 4 | #1, #2, #5 | Promised vs. expected YTM (only FV changes); new corporate yield = Treasury + spread |
| ☕ | 10 min | | | |
| 4b | 30 min | Textbook file, **Part A** | #4, #20, #10, #15, #21–22, #26, #30 |
| 5 | 20 min | Day 4 "Deck 1 big picture" map | Write every Deck 1 formula from memory, then check | — |

**If you only have time for one thing today:** make sure you can do an RCY problem start to finish (Day 3 #1). It takes the most steps and is the problem most likely to cost you points.

---

## TOMORROW (Wed 10/21): Decks 2 & 3, then a mock exam

| Block | Time | Open this file | Do these problems | Must be able to |
|---|---|---|---|---|
| 0 | 10 min | Formula sheet (Day 9, Part 2) | Rewrite the Deck 1 formulas from memory | Warm up |
| 1 | 50 min | Day 5 | #1, #2, #3 | "Long, Low, Low" sensitivity; **build a Macaulay duration table**; zero-coupon duration = maturity |
| 2 | 45 min | Day 6 | #1, #2, #3, #4, #6 | D_Mod = D_Mac/(1+y/m); %ΔP ≈ −D_Mod × Δy; \$ΔP; **duration overstates losses, understates gains**; rank bonds by duration; horizon vs. duration |
| ☕ | 15 min | | | |
| 3 | 45 min | Day 7 | #1, #3, #4, #5 | Forward rate formula; expectations vs. liquidity preference; what an inverted curve means |
| ☕ | 10 min | | | |
| 3b | 30 min | Textbook file, **Parts B & C** | Ch10 #38, #39, #41 · Ch11 #4, #8, #9, #14 |
| 4 | 40 min | Day 9 Mock Exam | **Timed, with no notes** | Everything |
| 5 | 20 min | Grade it | Redo only the questions you missed, then read the formula sheet once | — |
| Bonus | if time | Day 8 | Mixed set, or textbook problems from your slides | — |

Then stop. Read the formula sheet once before bed, and go to sleep.

---

## Most likely to be tested (check these off)

**Deck 1**
- [ ] Price a bond on the calculator (semiannual: N × 2, I/Y ÷ 2, PMT ÷ 2)
- [ ] Coupon vs. YTM tells you premium, par, or discount (no math needed)
- [ ] Accrued interest and invoice price
- [ ] YTM → BEY (× 2) and EAY ((1 + r)² − 1)
- [ ] Current yield and the ordering: premium C > CY > YTM, discount C < CY < YTM
- [ ] HPR = (coupon + P_end − P_begin) / P_begin
- [ ] RCY in 4 steps: sale price → FV of coupons → terminal wealth → (TW/P)^(1/n) − 1
- [ ] Reinvestment rate < YTM means RCY < YTM
- [ ] YTC and YTW
- [ ] Promised vs. expected YTM; credit spread in bps

**Deck 2**
- [ ] Rank sensitivity or duration: long maturity, low coupon, low YTM = higher
- [ ] Macaulay duration table (semiannual: divide by 2 at the end)
- [ ] Modified duration and %ΔP, \$ΔP
- [ ] Convexity: duration **overstates losses** and **understates gains**
- [ ] Horizon < duration means price risk dominates; horizon = duration means immunized

**Deck 3**
- [ ] f_n = (1 + y_n)^n / (1 + y_{n−1})^(n−1) − 1
- [ ] Expectations theory: forward = expected rate. LPT: forward = expected rate + liquidity premium
- [ ] Inverted curve = strong evidence that rates will fall; upward curve = ambiguous under LPT

---

## Calculator mistakes that cost people points
- Forgetting to **halve I/Y and double N** for semiannual bonds
- Forgetting that the I/Y result is **per period**, so you need to × 2 for the annual BEY
- Not entering **PV as negative**, which gives an error or a nonsense answer
- Leaving old numbers in the TVM registers: press `2nd` → `CLR TVM` before every problem
- For YTC, leaving FV at 1,000 instead of changing it to the **call price**
