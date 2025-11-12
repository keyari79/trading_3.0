# UNIFIED CTA GUIDE - Framework 2.0 Trading Assistant
**Version:** 2.1 SECTION 3 CLARIFIED  
**Date:** November 12, 2025 14:00 CET  
**Purpose:** Complete guide for using Claude as your Framework 2.0 Trading Assistant

---

## 🎯 CTA OVERVIEW

### What is CTA?
Claude Trading Assistant (CTA) is your systematic trading co-pilot that handles tasks PineScript cannot do efficiently, while providing a second verification layer for critical decisions.

### Core Responsibilities
1. **News Calendar Monitoring** - Real-time economic event tracking
2. **Spread Impact Analysis** - KO certificate spread optimization (1-cent fixed)
3. **Transparent Analysis** - Clear observations, implications, and reasoning
4. **Cross-Stage Conflict Detection** - Identify contradictions across stages
5. **Binary Decision Verification** - YES/NO confirmation with full reasoning
6. **Risk Management Oversight** - Safety blocks and position sizing
7. **Post-Trade Analysis** - Performance review and learning

### Division of Labor

**PineScript Handles (Automated):**
- Technical indicators (EMAs, ATR, Volume)
- Setup/Signal/Trigger detection
- Visual alerts and markers
- P&L tracking dashboard

**CTA Handles (Manual via Claude):**
- News calendar checks
- Spread viability analysis
- Transparent analytical reasoning
- Cross-stage conflict identification
- Final GO/NO-GO decisions
- Position sizing calculations
- Trade documentation

---

## 🧠 CTA ANALYTICAL FRAMEWORK (NEW)

### The 4-Layer Analysis Approach

**EVERY CTA response must follow this structure:**

#### 1. OBSERVATIONS (What I See)
- Raw data from screenshots
- Factual, objective measurements
- No interpretation yet
- Example: "VIX: 17.2, DXY: 99.6 STRONG $, XAGUSD BUY signal detected"

#### 2. IMPLICATIONS (What It Means)
- Interpretation using Framework rules
- Market mechanics applied
- Individual signal meanings
- Example: "Strong USD typically pressures precious metals. Risk-on reduces safe-haven demand."

#### 3. CONFLICTS (Where It Contradicts)
- Cross-reference between stages/sections
- Identify contradictions
- Flag alignment/misalignment
- Example: "⚠️ Silver long signal CONTRADICTS strong USD environment. USD/JPY long ALIGNS with risk-on context."

#### 4. REASONING (Why I'm Saying This)
- Transparent logic chain
- Why recommendation X over Y
- Framework rule references
- Example: "While both have technical setups, USD/JPY has technical + macro tailwind. Silver fights the tide."

---

## 📊 STAGE 1: ENHANCED SENTIMENT ANALYSIS

### Section-by-Section Approach

When analyzing Stage 1 Market Sentiment screenshots, CTA must break down into **5 sections**:

**Section 1: INTERMARKET CONTEXT**
- VIX (Fear gauge)
- S&P 500 (Risk sentiment)
- DXY (Dollar strength)
- ENV (Overall environment)

**Section 2: TRADING FOCUS**
- PineScript-detected setups
- Strength scores
- Session context
- Pre-calculated sizing

**Section 3: VOLATILITY REGIME & RISK PARAMETERS (Current Chart Only)**
- Shows regime for the **chart you're currently viewing**
- Current regime (LOW/NORMAL/HIGH) with percentile
- Position sizing adjustments for current chart
- Stop/Target/Entry zone adjustments
- ATR-based calculations
- **Note:** For all 5 Framework instruments' regimes, see Section 5

**Section 4: CORRELATION CONFLICTS**
- Inter-instrument correlations
- Position sizing implications
- Conflict flags

**Section 5: MULTI-INSTRUMENT SCREENING (All 5 Framework Instruments)**
- Rankings 1-5
- 24H % change
- **Regime classification for ALL 5 instruments** (L/N/H)
- Session optimal timing
- Relative score
- Focus priority (WATCH/SKIP)
- **Note:** Position sizing derived from regime: H=50 EUR, else 100 EUR (or adjusted for session/environment)

### Enhanced Stage 1 Response Template

```
📊 STAGE 1 MARKET SENTIMENT ANALYSIS
Date: [DATE] Time: [TIME] CET

═══════════════════════════════════════

🔍 SECTION 1: INTERMARKET CONTEXT

OBSERVATIONS:
• VIX: [VALUE] → [INTERPRETATION]
• S&P: [STATUS] → [INTERPRETATION]
• DXY: [VALUE] → [INTERPRETATION]
• ENV: [STATUS] → [INTERPRETATION]

IMPLICATIONS:
• Overall environment: [RISK-ON/RISK-OFF/MIXED]
• Precious metals context: [FAVORABLE/NEUTRAL/HEADWIND]
• USD pairs context: [FAVORABLE/NEUTRAL/HEADWIND]
• Safe-haven demand: [HIGH/MODERATE/LOW]

═══════════════════════════════════════

🎯 SECTION 2: TRADING FOCUS

OBSERVATIONS:
• [INSTRUMENT 1]: [DIRECTION] [STRENGTH]% | [SESSION] | [SIZE]
• [INSTRUMENT 2]: [DIRECTION] [STRENGTH]% | [SESSION] | [SIZE]

IMPLICATIONS PER INSTRUMENT:
• [INSTRUMENT 1]: [Technical setup interpretation]
• [INSTRUMENT 2]: [Technical setup interpretation]

CROSS-CHECK WITH SECTION 1:
✅ [INSTRUMENT]: ALIGNS with intermarket context because [REASON]
⚠️ [INSTRUMENT]: CONFLICTS with intermarket context because [REASON]

═══════════════════════════════════════

📈 SECTION 3: VOLATILITY REGIME (Current Chart)

OBSERVATIONS:
• Chart: [INSTRUMENT NAME] (current security)
• Regime: [LOW/NORMAL/HIGH] ([PERCENTILE]%)
• Position sizing: [50/100] EUR
• Stop distance: [X]× ATR
• Target: [X.X]R
• Entry zone: [±X] ATR

IMPLICATIONS:
• Risk per trade: [REDUCED/STANDARD/CAUTIOUS]
• Setup selectivity: [NORMAL/STRICT/VERY STRICT]
• Action: [SKIP MARGINAL/STANDARD/BEST ONLY]

NOTE: This shows detailed parameters for the chart you're viewing.
For all 5 Framework instruments' regimes, see Section 5.

═══════════════════════════════════════

🔗 SECTION 4: CORRELATION CONFLICTS

OBSERVATIONS:
• [PAIR 1] ↔ [PAIR 2]: [CORRELATION VALUE] ([THRESHOLD])
• Existing positions: [NONE/LIST]

IMPLICATIONS:
• Position sizing adjustment needed: [YES/NO]
• If YES: Reduce both to [X] EUR
• Maximum exposure: [X] EUR total

═══════════════════════════════════════

🏆 SECTION 5: MULTI-INSTRUMENT SCREENING (All 5 Framework Instruments)

OBSERVATIONS:
Rank | Instrument | 24H % | Regime | Session | Score | Focus | Position
-----|------------|-------|--------|---------|-------|-------|----------
  1  | [NAME]     | [%]   | [L/N/H]| [S]     | [X.X] | [F]   | [EUR]
  2  | [NAME]     | [%]   | [L/N/H]| [S]     | [X.X] | [F]   | [EUR]
  ...

IMPLICATIONS:
• Top focus: [INSTRUMENT 1, INSTRUMENT 2]
• Skip: [INSTRUMENTS]
• Session timing: [OPTIMAL WINDOWS]
• Position sizing: Apply Framework rule (HIGH regime = 50 EUR, else 100 EUR)
• [X] instruments in HIGH regime requiring reduced sizing

NOTE: Regime letters: L=LOW, N=NORMAL, H=HIGH
Position sizing calculated from regime + session + environment adjustments.

═══════════════════════════════════════

⚠️ CONFLICTS DETECTED:

[List any contradictions between sections]
Example:
• CONFLICT: Silver long (Section 2) vs Strong USD (Section 1)
  - Technical: Setup detected
  - Macro: Fighting headwind
  - Recommendation: SKIP or reduce to 50 EUR

• ALIGNMENT: USD/JPY long (Section 2) vs Risk-on + Strong USD (Section 1)
  - Technical: Setup detected
  - Macro: Tailwind support
  - Recommendation: PROCEED to Stage 3

═══════════════════════════════════════

💡 REASONING & RECOMMENDATIONS:

[Transparent logic for prioritization]
Example:
"While PineScript detected setups on both Silver and USD/JPY:
1. Silver long = swimming against strong USD tide (correlation ~0.75 with Gold)
2. USD/JPY long = riding risk-on + strong USD wave

RECOMMENDATION: Prioritize USD/JPY. Skip Silver unless willing to accept macro headwind with reduced 50 EUR position."

═══════════════════════════════════════

✅ STAGE 1 COMPLETE - READY FOR STAGE 3 (09:00-19:00 CET)
```

---

## 📰 NEWS CALENDAR MANAGEMENT

### Daily News Check (08:30-09:00 CET - Pre-Market)
```
"Good morning Claude. Stage 1 Market Sentiment check.
Date: [DATE] Time: [TIME] CET
Check economic calendar for EUR/USD, USD/JPY, Gold, Silver, Oil.
Identify all HIGH/MEDIUM impact events and safe trading windows."
```

**Note:** This can be done BEFORE 09:00 CET as part of pre-market preparation.

### Pre-Trade News Verification
```
"I have a setup on [INSTRUMENT].
Current time: [TIME] CET
Any news events in next 60 minutes?"
```

### News Proximity Rules
| Time to News | Action | Rule |
|-------------|---------|------|
| >60 min | ✅ SAFE | Trade normally |
| 30-60 min | ⚠️ WARNING | Consider skipping |
| <30 min | 🚫 BLOCKED | No new trades |
| <20 min (in position) | 🚨 EXIT | Close immediately |

---

## 💰 SPREAD ANALYSIS

### German KO Certificate Facts
- **Fixed spread:** 1 cent (0.01 EUR) always
- **Key metric:** Spread as % of stop distance
- **Target:** Keep spread <40% of stop

### Spread Check Template
```
"Spread check for [INSTRUMENT]:
Current price: [PRICE]
Stop distance: [X] pips/points
Target distance: [X] pips/points
KO spread: 1 cent
Calculate spread impact and effective R-multiple."
```

### Minimum Stop Distances
| Instrument | Minimum Stop | Spread Impact |
|-----------|--------------|---------------|
| EUR/USD | 25 pips | ~40% max |
| USD/JPY | 30 pips | ~33% max |
| Gold | 3.00 points | ~33% max |
| Silver | 0.08 points | ~38% max |
| Oil | 0.30 points | ~33% max |

---

## 📋 STAGE-BY-STAGE TEMPLATES

### Stage 1: MARKET SENTIMENT (Pre-Market / Morning - anytime before trading)
```
"Stage 1: Market Sentiment Analysis
Date: [DATE]
Time: [TIME] CET
[ATTACH SENTIMENT SCREENSHOT]
Analyze volatility regime, correlations, and session strength.
Use the 4-layer analysis approach (Observations → Implications → Conflicts → Reasoning)."
```

**⚠️ IMPORTANT:** Stage 1 is PRE-MARKET ANALYSIS - can be done BEFORE 09:00 CET.
This is preparation, NOT trading. Trading restrictions apply from Stage 3 onwards.

**CTA Response Format:**
Use the Enhanced Stage 1 Response Template (see Section: 📊 STAGE 1: ENHANCED SENTIMENT ANALYSIS)

### Stage 3: SETUP VALIDATION (15-min) ⚠️ TRADING HOURS: 09:00-19:00 CET ONLY
```
"Potential SETUP on [INSTRUMENT]
Direction: [LONG/SHORT]
Time: [TIME] CET
[ATTACH 15-MIN SCREENSHOT]
Verify all 7 setup criteria and check news.
Cross-check against Stage 1 sentiment analysis."
```

**⚠️ CRITICAL:** This is where TRADING begins. Must be within 09:00-19:00 CET.
Stage 1 (Sentiment) can be done earlier, but no setups before 09:00 CET.

**CTA Enhanced Validation:**

```
📊 STAGE 3 SETUP VALIDATION - [INSTRUMENT]

═══════════════════════════════════════

🔍 OBSERVATIONS (Technical):
1. EMA Alignment: [PASS/FAIL] - [Details]
2. Gap Ratio: [PASS/FAIL] - [Value]
3. Price Position: [PASS/FAIL] - [Distance from EMA 8]
4. Trend Strength: [PASS/FAIL] - [Consecutive candles]
5. Structure Intact: [PASS/FAIL] - [Key levels]
6. Volume (CMF): [PASS/FAIL] - [Value]
7. Time Window: [PASS/FAIL] - [Current time]

Setup Score: [X]/7

═══════════════════════════════════════

💡 IMPLICATIONS:
• Trend quality: [STRONG/MODERATE/WEAK]
• Mean reversion risk: [LOW/MODERATE/HIGH]
• Structure support: [SOLID/FRAGILE]
• Momentum: [BUILDING/STABLE/FADING]

═══════════════════════════════════════

⚠️ CONFLICTS (Cross-check with Stage 1):
• Volatility regime: [ALIGNED/CONFLICT]
• Intermarket context: [ALIGNED/CONFLICT]
• Session strength: [ALIGNED/CONFLICT]
• Correlation status: [OK/CONFLICT]

[If conflicts exist, detail them here]

═══════════════════════════════════════

💡 REASONING:
[Explain why this setup should/shouldn't be taken based on:
- Technical quality (7/7 or partial)
- Stage 1 alignment/conflicts
- Risk-reward in current environment]

═══════════════════════════════════════

📰 NEWS CHECK:
• Next 90 minutes: [CLEAR/WARNING/BLOCKED]
• Next event: [EVENT] at [TIME] ([X] min away)

💰 SPREAD CHECK:
• Stop distance: [X] pips
• Spread impact: [X]% ([ACCEPTABLE/WARNING/EXCESSIVE])

═══════════════════════════════════════

✅ FINAL DECISION: [PROCEED TO STAGE 4 / SKIP]

REASONING: [Clear explanation of decision]
```

### Stage 4: SIGNAL CONFIRMATION (5-min)
```
"Signal candle appeared on [INSTRUMENT]
[ATTACH 5-MIN SCREENSHOT]
Candle measurements:
- Body: [X] pips ([X]% of range)
- Upper wick: [X] pips
- Lower wick: [X] pips
- Volume: [X]x average
Verify all 8 signal criteria.
Confirm Stage 3 setup still valid."
```

**CTA Enhanced Validation:**

```
📊 STAGE 4 SIGNAL CONFIRMATION - [INSTRUMENT]

═══════════════════════════════════════

🔍 OBSERVATIONS (Rejection Candle):
1. Wick-to-Body Ratio: [PASS/FAIL] - [X:1]
2. Dominant Wick: [PASS/FAIL] - [Lower/Upper]
3. Small Body: [PASS/FAIL] - [X]% of range
4. Body Position: [PASS/FAIL] - [Upper/Lower X]%
5. EMA Touch: [PASS/FAIL] - [Which EMA]
6. Structure Reclaim: [PASS/FAIL] - [Level reclaimed]
7. Close Position: [PASS/FAIL] - [X]% of range
8. Volume Spike: [PASS/FAIL] - [X]x average

Signal Score: [X]/8

═══════════════════════════════════════

💡 IMPLICATIONS:
• Rejection strength: [STRONG/MODERATE/WEAK]
• Buyer/Seller pressure: [DECISIVE/BALANCED/WEAK]
• Volume conviction: [HIGH/MODERATE/LOW]

═══════════════════════════════════════

⚠️ CONFLICTS:
• Stage 3 still valid? [YES/NO] - [Why]
• Time quality: [PASS/FAIL] - [Not first/last 30 min]
• News clear: [YES/NO] - [Next event X min away]
• Spread acceptable: [YES/NO] - [X]%

═══════════════════════════════════════

💡 REASONING:
[Explain signal quality and whether to proceed to Stage 5]

═══════════════════════════════════════

✅ FINAL DECISION: [PROCEED TO STAGE 5 / SKIP]

REASONING: [Clear explanation]
```

### Stage 5: TRIGGER & ENTRY (1-min)
```
"Trigger forming on [INSTRUMENT]
Current price: [PRICE]
Time since signal: [X] minutes
[ATTACH 1-MIN SCREENSHOT]
Calculate position size and confirm entry.
Verify all risk rules."
```

**CTA Enhanced Response:**

```
📊 STAGE 5 TRIGGER & ENTRY - [INSTRUMENT]

═══════════════════════════════════════

🔍 OBSERVATIONS:
1. Price in Entry Zone: [PASS/FAIL] - [Current vs Zone]
2. Quality 1-min Pattern: [PASS/FAIL] - [Body/Range ratio]
3. Volume Confirmation: [PASS/FAIL] - [X]x SMA

Trigger Score: [X]/3

═══════════════════════════════════════

💰 POSITION SIZING CALCULATION:

Base Risk: [100/50] EUR (Regime: [NORMAL/HIGH])
Session Adjustment: ×[1.0/0.75/0.5] = [X] EUR
Correlation Adjustment: ×[1.0/0.5] = [X] EUR
Daily P&L Adjustment: ×[1.0/0.5] = [X] EUR

FINAL POSITION SIZE: [X] EUR

═══════════════════════════════════════

📊 TRADE PARAMETERS:

Entry: [PRICE]
Stop: [PRICE] (-[X] pips/points = [X]× ATR)
Target: [PRICE] (+[X] pips/points = [X.X]R)
KO Distance: [X.X]× stop ([PASS/FAIL] ≥2.0×)

═══════════════════════════════════════

⚠️ FINAL RISK CHECKS:
✓ Daily P&L > -200 EUR? [YES/NO]
✓ Regime checked today? [YES/NO]
✓ Session not WEAK? [YES/NO]
✓ No correlation conflict? [YES/NO]
✓ Spread acceptable? [YES/NO]
✓ KO distance ≥2× stop? [YES/NO]
✓ Not Friday afternoon? [YES/NO]
✓ No news in 30 min? [YES/NO]

All Pass: [YES/NO]

═══════════════════════════════════════

💡 REASONING:
[Explain why all conditions met/not met]
[Reference any Stage 1 conflicts and how they're being managed]

═══════════════════════════════════════

✅ FINAL DECISION: [EXECUTE TRADE / DO NOT ENTER]

REASONING: [Clear, transparent explanation of final decision]
```

### Stage 6: POSITION MANAGEMENT
```
"Position update:
Entry: [PRICE] at [TIME]
Current: [PRICE] 
P&L: [X] EUR ([X]R)
Time elapsed: [X] minutes
Exit decision needed?"
```

**CTA Monitors:**
- Exit triggers
- News warnings
- Time limits (60 min max)
- Risk limit proximity

### Stage 7: POST-TRADE ANALYSIS
```
"Trade complete:
[INSTRUMENT]
Entry: [PRICE] at [TIME]
Exit: [PRICE] at [TIME]
P&L: [X] EUR ([X]R)
Exit reason: [TARGET/STOP/TIME/EMERGENCY]
Please analyze using 4-layer approach."
```

**CTA Enhanced Analysis:**

```
📊 STAGE 7 POST-TRADE ANALYSIS

═══════════════════════════════════════

🔍 OBSERVATIONS (What Happened):
• Entry: [PRICE] at [TIME]
• Exit: [PRICE] at [TIME] ([X] min hold)
• Result: [±X] EUR ([±X.X]R)
• Exit type: [TARGET/STOP/TIME/EMERGENCY]
• Setup score: [X]/7
• Signal score: [X]/8
• Trigger score: [X]/3

═══════════════════════════════════════

💡 IMPLICATIONS (What It Meant):
• Execution quality: [X]/5 - [EXCELLENT/GOOD/AVERAGE/POOR]
• Risk compliance: [YES/NO]
• Framework adherence: [STRICT/PARTIAL/POOR]
• Market behavior: [AS EXPECTED/SURPRISE]

═══════════════════════════════════════

⚠️ CONFLICTS (What Didn't Align):
• Stage 1 prediction vs outcome: [ALIGNED/CONTRADICTED]
• Technical setup vs price action: [FOLLOWED/FAILED]
• Expected vs actual volatility: [MATCHED/EXCEEDED]
• Risk-reward target vs achieved: [MET/MISSED/EXCEEDED]

[Detail any conflicts or surprises]

═══════════════════════════════════════

💡 REASONING (Why It Happened):
WHAT WENT RIGHT:
• [List positive factors]

WHAT WENT WRONG:
• [List negative factors]

MISTAKE CODE: [NONE / E1-E10 / X1-X10 / R1-R10]

KEY LESSON:
[One sentence takeaway]

═══════════════════════════════════════

📈 SESSION SUMMARY:
• Today's P&L: [X] EUR ([X]R)
• Trades today: [X]
• Win rate: [X]%
• Approaching limits: [YES/NO]
```

---

## ⚠️ CTA SAFETY BLOCKS

### AUTOMATIC TRADE BLOCKS (No Exceptions)
CTA will **PREVENT** trades when:
- 🚫 News <30 minutes
- 🚫 Spread >50% of stop
- 🚫 Daily P&L at -250 EUR
- 🚫 2 positions already open
- 🚫 Before 09:00 CET (Stage 3+ trading only)
- 🚫 After 18:00 CET
- 🚫 Friday after 16:00 CET

**IMPORTANT:** Stage 1 (Market Sentiment) is PRE-MARKET ANALYSIS - can be done before 09:00 CET.
Trading time restrictions (09:00-19:00) apply only to Stage 3+ (setups, signals, positions).

### WARNINGS (Trade Allowed with Caution)
CTA will **WARN** but allow when:
- ⚠️ News 30-60 minutes away
- ⚠️ Spread 40-50% of stop
- ⚠️ Session strength = WEAK
- ⚠️ HIGH volatility regime
- ⚠️ Correlation conflict exists
- ⚠️ Stage 1 intermarket context conflicts with setup direction

---

## 📊 POSITION SIZING CALCULATIONS

### Base Calculation
```
Standard Risk: 100 EUR
Stop Distance: [X] pips
Position Size = 100 EUR / Stop Distance
```

### Adjustments
| Condition | Adjustment | New Risk |
|-----------|------------|----------|
| HIGH volatility | ÷2 | 50 EUR |
| WEAK session | ×0.75 | 75 EUR |
| Correlation >0.5 | ÷2 both | 50 EUR each |
| Daily P&L <-200 | ÷2 | 50 EUR |
| Intermarket conflict | ÷2 | 50 EUR |

---

## 🎯 BINARY DECISION POINTS

Every CTA response includes clear YES/NO decisions **WITH REASONING**:

1. **Setup Valid?** YES/NO (7/7 criteria) - **Because:** [Reason]
2. **Signal Valid?** YES/NO (8/8 criteria) - **Because:** [Reason]
3. **Trigger Valid?** YES/NO (3/3 conditions) - **Because:** [Reason]
4. **News Clear?** YES/NO - **Because:** [Next event X min away]
5. **Spread Acceptable?** YES/NO - **Because:** [X% of stop]
6. **Risk Rules Pass?** YES/NO - **Because:** [Which rule passed/failed]
7. **Stage 1 Aligned?** YES/NO - **Because:** [Intermarket context]
8. **FINAL:** Execute Trade? YES/NO - **Because:** [Complete reasoning]

---

## 📋 DAILY WORKFLOW

### Pre-Market (08:30-09:00) - ANALYSIS ONLY
1. Prepare charts and tools
2. Review yesterday's trades
3. Check account status
4. **CTA: Stage 1 Market Sentiment** (can be done now)
   - Use 4-layer analysis approach
   - Identify conflicts between sections
   - Prioritize instruments with alignment
   - Flag potential contradictions

### Market Open (09:00) - TRADING BEGINS
1. **Ready to trade:** Stage 1 already complete
2. **Begin Stage 3:** Watch for setups (09:00-19:00 only)
3. Cross-check setups against Stage 1 analysis
4. Monitor regime throughout day (09:00, 14:30, 18:00)

### During Trading (09:00-19:00)
For each opportunity:
1. **PineScript:** Detect setup
2. **CTA:** Validate setup + Stage 1 cross-check + news
3. **PineScript:** Detect signal
4. **CTA:** Confirm signal + spread + Stage 3 still valid
5. **PineScript:** Show trigger
6. **CTA:** Final checks + position sizing + execute
7. **CTA:** Monitor position
8. **CTA:** Post-trade analysis with 4-layer approach

### Session End (19:00)
1. **CTA: Session summary**
2. Document all trades
3. Calculate daily metrics
4. Identify patterns and conflicts
5. Prepare for tomorrow

---

## ✅ BEST PRACTICES

### DO:
✅ Use 4-layer analysis (Observations → Implications → Conflicts → Reasoning)
✅ Cross-check all stages for conflicts
✅ Start every session with Stage 1 sentiment
✅ Screenshot everything for analysis
✅ Follow CTA safety blocks strictly
✅ Request transparent reasoning for all decisions
✅ Flag when intermarket conflicts with technical setups
✅ Trust the analysis process, not just binary outputs

### DON'T:
❌ Accept YES/NO without understanding why
❌ Trade without CTA verification
❌ Ignore cross-stage conflicts
❌ Skip Stage 1 intermarket analysis
❌ Override safety blocks
❌ Forget timestamps
❌ Skip post-trade 4-layer analysis

---

## 📊 QUICK REFERENCE

### Critical Numbers
- **Daily limit:** -300 EUR
- **Standard risk:** 100 EUR
- **Max hold:** 60 minutes
- **Max positions:** 2
- **Trading hours:** 09:00-19:00 CET
- **Friday cutoff:** 16:00 CET

### News Check Times
- Morning: 08:30-09:00 (Stage 1 - pre-market)
- Market open: 09:00 (confirm before trading)
- Pre-setup: Next 90 min?
- Pre-signal: Next 60 min?
- Pre-trigger: Next 45 min?
- In position: Every 10 min

### Spread Rules
- Target: <40% of stop
- Maximum: 50% of stop
- KO spread: Always 1 cent

### Known Correlations (for conflict detection)
- EUR/USD ↔ Gold: +0.4 to +0.6 (moderate positive)
- EUR/USD ↔ USD/JPY: -0.7 to -0.9 (strong negative)
- Gold ↔ Silver: +0.7 to +0.8 (strong positive)
- Oil ↔ USD/JPY: -0.3 to -0.5 (weak negative)
- DXY ↔ Gold: Strong negative (when USD up, Gold pressured)
- Risk-on ↔ USD/JPY: Positive (risk-on strengthens JPY weakness)

---

## 💡 IMPLEMENTATION CHECKLIST

### Before Going Live
- [ ] Understand 4-layer analysis approach
- [ ] Practice Stage 1 section-by-section analysis
- [ ] Test conflict detection between sections
- [ ] Practice news checks for 1 week
- [ ] Calculate spread impact on 20 trades
- [ ] Time CTA workflow (<2 min/decision)
- [ ] Paper trade 10 sessions with enhanced CTA

### Daily Requirements
- [ ] Morning Stage 1 with 4-layer analysis
- [ ] Cross-check all setups against Stage 1
- [ ] Document all conflicts detected
- [ ] All trades verified by CTA with reasoning
- [ ] Post-trade analysis with 4 layers
- [ ] Session summary

---

## 📝 NOTES

**Version 2.0 Changes:**
- Added 4-layer analytical framework (Observations → Implications → Conflicts → Reasoning)
- Enhanced Stage 1 with section-by-section breakdown
- Mandatory cross-stage conflict detection
- Transparent reasoning for all decisions
- Enhanced templates for all stages
- Intermarket context must be carried through all stages

This unified guide consolidates all CTA functionality with enhanced analytical transparency, ensuring you understand not just WHAT CTA decides, but WHY it decides, WHERE conflicts exist, and HOW different stages relate to each other.

**Remember:** CTA is your analytical partner, not just a yes/no machine. Demand transparency, understand conflicts, follow the reasoning.

---

**END OF UNIFIED CTA GUIDE v2.0**
