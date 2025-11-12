# STAGE 7: CTA DOCUMENTATION TEMPLATE
**Version:** 1.0  
**Created:** November 11, 2025  
**Purpose:** Complete data collection guide for post-trade documentation

---

## ðŸ“‹ OVERVIEW

This document defines:
1. All 25 data points required for Framework 2.0 trade log
2. What CTA can extract from screenshots
3. What user must manually provide
4. Standard CTA request templates

---

## ðŸŽ¯ FRAMEWORK TRADE LOG - 25 COLUMNS

### ENTRY DATA (Columns 1-13)

| # | Field | Source | Example |
|---|-------|--------|---------|
| 1 | Date | User | 2025-11-11 |
| 2 | Entry Time (CET) | User | 10:30 |
| 3 | Instrument | User/Screenshot | EUR/USD |
| 4 | Direction | Screenshot | LONG |
| 5 | Entry Price | User | 1.0520 |
| 6 | Stop Price | User/Screenshot | 1.0500 |
| 7 | Target Price | User/Screenshot | 1.0550 |
| 8 | Position Size (EUR) | User | 100 |
| 9 | R-Risk Amount (EUR) | User/Screenshot | 100 |
| 10 | KO Distance | User | 2.0Ã— |
| 11 | Volatility Regime | Screenshot | NORMAL |
| 12 | Session Strength | Screenshot | PRIME |
| 13 | Correlation Status | Screenshot | OK |

### EXIT DATA (Columns 14-19)

| # | Field | Source | Example |
|---|-------|--------|---------|
| 14 | Exit Time (CET) | User | 11:15 |
| 15 | Exit Price | User | 1.0550 |
| 16 | Exit Type | User/Screenshot | TARGET |
| 17 | P&L (EUR) | User | +150 |
| 18 | P&L (R-multiple) | User/CTA Calculate | +1.5R |
| 19 | Hold Duration (min) | CTA Calculate | 45 |

### QUALITY METRICS (Columns 20-24)

| # | Field | Source | Example |
|---|-------|--------|---------|
| 20 | Setup Score (0-7) | CTA from Screenshot | 7/7 |
| 21 | Signal Score (0-8) | CTA from Screenshot | 8/8 |
| 22 | Trigger Score (0-3) | CTA from Screenshot | 3/3 |
| 23 | Execution Quality (1-5) | CTA Assessment | 5 |
| 24 | Risk Compliance (Y/N) | CTA Assessment | Y |

### LEARNING (Column 25)

| # | Field | Source | Example |
|---|-------|--------|---------|
| 25a | Mistake Code | CTA/User | NONE or E1, X2, R3 |
| 25b | Notes/Lessons | CTA/User | "Perfect execution, all criteria aligned" |

---

## ðŸ¤– CTA DATA EXTRACTION CAPABILITY

### FROM STAGE 3 SCREENSHOT (Setup - 15min)
**CTA Can Extract:**
- âœ… Setup Score (X/7 criteria met)
- âœ… Volatility Regime (LOW/NORMAL/HIGH)
- âœ… Trend Quality assessment
- âœ… EMA alignment status
- âœ… Gap ratio value
- âœ… CMF status
- âœ… Direction (LONG/SHORT)

**Example from Screenshot:**
```
Setup Score: 7/7 âœ…
Regime: NORMAL
Direction: LONG
Trend Quality: STRONG
```

### FROM STAGE 4 SCREENSHOT (Signal - 5min)
**CTA Can Extract:**
- âœ… Signal Score (X/8 criteria met)
- âœ… Rejection candle measurements
- âœ… Volume spike confirmation
- âœ… Session time/strength
- âœ… Each of 8 signal criteria status

**Example from Screenshot:**
```
Signal Score: 8/8 âœ…
Wick-Body Ratio: 2.1:1 PASS
Volume Spike: 1.8Ã— PASS
```

### FROM STAGE 5 SCREENSHOT (Trigger - 1min)
**CTA Can Extract:**
- âœ… Trigger Score (X/3 conditions met)
- âœ… Entry zone boundaries
- âœ… Price in zone status
- âœ… Volume confirmation
- âœ… Pattern quality

**Example from Screenshot:**
```
Trigger Score: 3/3 âœ…
Entry Zone: 1.0515-1.0525
Price: In zone âœ…
```

### FROM STAGE 6 SCREENSHOT (Exit Management)
**CTA Can Extract:**
- âœ… Exit type (TARGET/STOP/TIME/EMERGENCY)
- âœ… Time in trade (minutes)
- âœ… P&L (EUR and R-multiple)
- âœ… Target/Stop levels
- âœ… Max R achieved
- âœ… Exit trigger reason

**Example from Screenshot:**
```
Exit Type: TIME EXIT (60-min max)
P&L: +2200.8 EUR (+22.01R)
Time in Trade: 343 minutes
```

### FROM RISK DASHBOARD SCREENSHOT
**CTA Can Extract:**
- âœ… Volatility Regime
- âœ… Session Strength (PRIME/ACCEPTABLE/WEAK)
- âœ… Correlation Status (OK/CONFLICT)
- âœ… Position Size calculation
- âœ… Daily P&L status
- âœ… Risk compliance verification
- âœ… ATR values
- âœ… Multi-timeframe sync status

**Example from Screenshot:**
```
Regime: HIGH â†’ Position: 50 EUR
Session: PRIME
Correlation: OK
Daily P&L: +60.7 EUR (SAFE)
```

---

## ðŸ‘¤ USER MUST MANUALLY PROVIDE

### CRITICAL DATA (Cannot Extract from Screenshots)

**Entry Execution:**
1. âš ï¸ Exact entry timestamp (HH:MM CET)
2. âš ï¸ Actual entry price executed
3. âš ï¸ Actual position size used (may differ from recommended)
4. âš ï¸ KO certificate distance set

**Exit Execution:**
5. âš ï¸ Exact exit timestamp (HH:MM CET)
6. âš ï¸ Actual exit price executed
7. âš ï¸ Exit reason if not obvious (manual vs. triggered)

**Results:**
8. âš ï¸ Actual P&L in EUR (from broker)
9. âš ï¸ Any slippage experienced

**Context:**
10. âš ï¸ Any manual overrides made
11. âš ï¸ Subjective execution quality (how it felt)
12. âš ï¸ Personal notes on decision-making
13. âš ï¸ Any mistakes recognized during trade

---

## ðŸ“ STANDARD CTA REQUEST TEMPLATES

### TEMPLATE 1: FULL POST-TRADE REQUEST

```
STAGE 7: POST-TRADE DOCUMENTATION

Trade completed - documentation required.

**PLEASE PROVIDE:**

ENTRY DATA:
- Entry Time: [HH:MM CET]
- Entry Price: [X.XXXX]
- Position Size: [XXX EUR]
- KO Distance Set: [X.XÃ—]

EXIT DATA:
- Exit Time: [HH:MM CET]
- Exit Price: [X.XXXX]
- Exit Reason: [TARGET/STOP/TIME/EMERGENCY/OTHER]
- Actual P&L: [+/- XXX EUR]

SCREENSHOTS NEEDED:
1. Stage 3 (Setup validation)
2. Stage 4 (Signal candle) - if available
3. Stage 5 (Trigger) - if available
4. Stage 6 (Exit management)
5. Risk Dashboard (at entry time)

SUBJECTIVE:
- How was execution quality? [1-5]
- Any mistakes recognized? [Yes/No - describe]
- Key lesson from this trade?

CTA will then:
âœ… Calculate quality scores (Setup/Signal/Trigger)
âœ… Verify risk compliance
âœ… Calculate R-multiple and hold duration
âœ… Assign mistake codes if applicable
âœ… Generate complete 25-column trade log entry
âœ… Provide post-trade analysis
```

---

### TEMPLATE 2: QUICK DOCUMENTATION (Minimum Required)

```
TRADE DOCUMENTATION - QUICK VERSION

Provide essentials:
1. Entry: [TIME] at [PRICE]
2. Exit: [TIME] at [PRICE]
3. Position: [XXX EUR]
4. Result: [+/- XXX EUR]
5. Exit reason: [TARGET/STOP/TIME/etc]
6. Instrument: [EUR/USD/etc]

+ Attach screenshots (Setup, Exit, Risk Dashboard)

CTA will calculate rest and request any missing critical data.
```

---

### TEMPLATE 3: SCREENSHOT-ONLY ANALYSIS

```
POST-TRADE SCREENSHOT ANALYSIS

Please provide screenshots:
âœ… Stage 3 (Setup)
âœ… Stage 5 (Trigger/Entry)
âœ… Stage 6 (Exit)
âœ… Risk Dashboard

From these, CTA will extract:
- Quality scores (Setup/Signal/Trigger)
- Regime and session data
- Exit type and duration
- Risk compliance verification

You will still need to confirm:
- Exact entry/exit times and prices
- Actual position size and P&L
```

---

## ðŸŽ¯ EXECUTION QUALITY RATING GUIDE

**For Column 23: Execution Quality (1-5)**

| Rating | Description | Criteria |
|--------|-------------|----------|
| **5 - Excellent** | Flawless execution | All steps followed precisely, no hesitation, perfect timing |
| **4 - Good** | Smooth process | Minor delay but all criteria checked, good discipline |
| **3 - Average** | Followed process | Some uncertainty, but stayed within Framework |
| **2 - Below Average** | Some errors | Skipped steps, felt rushed, partial compliance |
| **1 - Poor** | Significant issues | Multiple mistakes, panic decisions, broke rules |

CTA will assess based on:
- Were all stage criteria verified?
- Was there appropriate patience?
- Were risk rules followed?
- Any emotional decisions?
- Timing quality?

---

## ðŸš« MISTAKE CODE REFERENCE

**For Column 25a: Mistake Code**

### ENTRY MISTAKES (E1-E10)
- **E1:** Forced entry (impatience)
- **E2:** FOMO entry (chasing)
- **E3:** Incomplete validation (skipped criteria)
- **E4:** Wrong timeframe (didn't check all timeframes)
- **E5:** Ignored regime (didn't apply size adjustment)
- **E6:** News proximity (traded too close to event)
- **E7:** Spread too wide (ignored spread check)
- **E8:** Outside time window (traded before 09:00 or after 19:00)
- **E9:** Weak setup (took <7/7 criteria)
- **E10:** Correlation conflict (ignored existing positions)

### EXIT MISTAKES (X1-X10)
- **X1:** Early exit - fear (closed before target/stop/time)
- **X2:** Held past stop (moved or ignored stop loss)
- **X3:** Ignored time limit (exceeded 60 minutes)
- **X4:** Moved stop loss (adjusted stop after entry)
- **X5:** Ignored emergency trigger (didn't exit on structure break)
- **X6:** Greed hold (held past target hoping for more)
- **X7:** Panic exit (closed on minor movement)
- **X8:** Forgot time check (unaware of approaching limit)
- **X9:** News exit delay (should have exited before news)
- **X10:** Weekend hold (held past Friday 16:00)

### RISK MISTAKES (R1-R10)
- **R1:** Oversized position (used >100 EUR standard)
- **R2:** Ignored correlation (took correlated positions)
- **R3:** Broke daily limit (continued after -200 EUR)
- **R4:** Insufficient KO distance (<1.5Ã— stop)
- **R5:** Ignored regime adjustment (didn't reduce in HIGH)
- **R6:** Session violation (traded in WEAK session at full size)
- **R7:** Too many positions (>2 concurrent)
- **R8:** Exceeded max exposure (>200 EUR total risk)
- **R9:** No risk calculation (didn't calculate before entry)
- **R10:** Ignored daily hard stop (traded past -300 EUR)

**Use:** NONE if no mistakes  
**Use:** Multiple codes if multiple mistakes (e.g., "E3, R5")

---

## ðŸ“Š COMPLETE TRADE LOG OUTPUT FORMAT

**CTA Final Output:**

```
TRADE LOG ENTRY - [DATE]

â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
ENTRY DATA:
â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
Date/Time:      2025-11-11, 10:30 CET
Instrument:     EUR/USD
Direction:      LONG
Entry:          1.0520
Stop:           1.0500 (-20 pips)
Target:         1.0550 (+30 pips)
Position:       100 EUR
R-Risk:         100 EUR
KO Distance:    2.0Ã—
Regime:         NORMAL
Session:        PRIME
Correlation:    OK

â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
EXIT DATA:
â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
Exit Time:      11:15 CET
Exit Price:     1.0550
Exit Type:      TARGET HIT
P&L (EUR):      +150 EUR
P&L (R):        +1.5R
Duration:       45 minutes

â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
QUALITY METRICS:
â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
Setup Score:    7/7 âœ… VALID
Signal Score:   8/8 âœ… VALID
Trigger Score:  3/3 âœ… VALID
Execution:      5/5 EXCELLENT
Risk Comply:    YES âœ…

â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
LEARNING:
â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
Mistake Code:   NONE
Notes:          Perfect execution. All criteria aligned.
                Entered in optimal entry zone, target hit
                in 45 minutes. Textbook Framework trade.
Key Lesson:     Patience pays - waiting for 7/7, 8/8, 3/3
                resulted in high-probability winner.

â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
EXCEL ROW (Copy-Paste Ready):
â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
2025-11-11,10:30,EUR/USD,LONG,1.0520,1.0500,1.0550,100,100,2.0,NORMAL,PRIME,OK,11:15,1.0550,TARGET,+150,+1.5,45,7,8,3,5,Y,NONE,"Perfect execution, all criteria aligned"
```

---

## ðŸ”„ WORKFLOW INTEGRATION

### DAILY ROUTINE (Stage 7)

**After Each Trade:**
1. Close position
2. Screenshot exit panel immediately
3. Use Template 2 (Quick Documentation)
4. Provide to CTA within 5 minutes
5. Review CTA analysis
6. Update trade log spreadsheet
7. Note key lesson

**End of Day:**
1. Review all trades with CTA
2. Calculate daily metrics
3. Identify patterns
4. Plan tomorrow's focus

**Weekly:**
1. Aggregate all trade logs
2. Statistical analysis with CTA
3. Mistake pattern identification
4. System refinements

---

## âœ… VALIDATION CHECKLIST

**Before Submitting to CTA:**

Trade Essentials:
- [ ] Entry time and price
- [ ] Exit time and price
- [ ] Position size used
- [ ] Actual P&L result
- [ ] Exit reason identified

Screenshots Attached:
- [ ] Stage 3 (Setup)
- [ ] Stage 5 (Trigger) - if available
- [ ] Stage 6 (Exit)
- [ ] Risk Dashboard

Context:
- [ ] Any mistakes noted
- [ ] Execution quality self-assessed
- [ ] Key lesson identified

---

## ðŸŽ¯ CTA RESPONSE TIME

**Expected CTA Analysis Timeline:**

- **Data validation:** 30 seconds
- **Quality score calculation:** 1 minute
- **Complete analysis:** 2-3 minutes
- **Total documentation:** <5 minutes per trade

**CTA Provides:**
1. Verified trade log entry (25 columns)
2. Quality assessment
3. Mistake identification (if any)
4. Key lesson summary
5. Excel-ready formatted output
6. Recommendations for improvement

---

## ðŸ“Œ IMPORTANT NOTES

**Data Accuracy:**
- User-provided prices/times are CRITICAL - cannot be guessed
- Screenshots provide validation but not execution details
- Actual P&L from broker is authoritative

**Timing:**
- Document trades immediately after exit
- Memory degrades quickly
- Real-time data prevents reconstruction errors

**Honesty:**
- Admit mistakes for learning
- CTA analysis is for improvement, not judgment
- Accurate logs enable pattern recognition

**Consistency:**
- Use same format every trade
- Complete all 25 columns
- No skipping documentation

---

## ðŸš€ GETTING STARTED

**First Trade Documentation:**
1. Complete the trade
2. Take all required screenshots
3. Copy Template 1 (Full Post-Trade Request)
4. Fill in your data
5. Paste into CTA conversation
6. Review CTA's complete analysis
7. Save formatted output to Excel

**After 10 Trades:**
1. Switch to Template 2 (Quick Version)
2. CTA will know your workflow
3. Faster documentation process
4. Focus on lessons and patterns

---

**END OF STAGE 7 DOCUMENTATION TEMPLATE**

**Version:** 1.0  
**Status:** Complete and ready for use  
**Integration:** Framework 2.0 Trading System

---

*This template ensures complete, consistent, and efficient post-trade documentation for continuous improvement.*
