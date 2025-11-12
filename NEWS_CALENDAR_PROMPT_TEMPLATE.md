# STAGE 1 NEWS CALENDAR PROMPT - Framework 2.0
**Version:** 1.0  
**Created:** November 11, 2025  
**Purpose:** Standard prompt for CTA to gather news calendar information for all 5 trading instruments

---

## ðŸ“° MORNING NEWS CALENDAR CHECK (Use at 09:00 CET)

```
Good morning CTA. Framework 2.0 session starting.

**Date:** [INSERT TODAY'S DATE]  
**Current Time:** [INSERT TIME] CET  
**Trading Hours:** 09:00-19:00 CET

Please search the web and provide today's economic calendar for:
1. EUR/USD (Euro/US Dollar)
2. USD/JPY (US Dollar/Japanese Yen)
3. Gold (XAU/USD)
4. Silver (XAG/USD)
5. Oil (WTI Crude Oil)

**Required Information:**
- All HIGH and MEDIUM impact events for these instruments today
- Exact times (in CET timezone)
- Which instruments are affected by each event
- Identify SAFE TRADING WINDOWS (90+ minutes clear of high-impact news)
- Flag any MAJOR events (Fed, ECB, NFP, CPI, etc.)

**Output Format Needed:**
1. **Today's High-Impact Events:** (Time CET | Event | Instruments Affected)
2. **Safe Trading Windows:** (Start-End times with no high-impact news)
3. **Current Window Status:** (Next 90 minutes clear? YES/NO)
4. **Caution Periods:** (Times to avoid new entries)
5. **Mandatory Exit Times:** (News within 20 min of any position)

Provide your analysis now.
```

---

## â° PRE-TRADE NEWS CHECK (Use before each setup)

```
CTA News Check Required.

**Instrument:** [INSERT: EUR/USD, USD/JPY, Gold, Silver, or Oil]  
**Current Time:** [INSERT TIME] CET  
**Potential Entry:** Looking at setup now

Search the economic calendar and confirm:
1. Any HIGH/MEDIUM impact news in the next 90 minutes?
2. If yes: Exact time and event name
3. Safe to proceed? YES/NO

Quick check please - binary decision needed.
```

---

## ðŸ”„ INTRADAY NEWS UPDATE (Use at 14:30 and 18:00 CET)

```
CTA Intraday News Update.

**Time:** [INSERT TIME] CET  
**Session:** [London/NY Overlap or Late Session]

Update today's news calendar:
1. Any schedule changes or surprise announcements?
2. Remaining high-impact events today?
3. Safe windows for rest of session?
4. Any instruments now blocked due to upcoming news?

Brief update please.
```

---

## ðŸš¨ POSITION NEWS CHECK (Use when holding position)

```
CTA Position Risk Check.

**Holding:** [INSTRUMENT]  
**Entry Time:** [TIME]  
**Current Time:** [TIME]  
**Time in Trade:** [X] minutes

Emergency check:
1. Any high-impact news announced in next 30 minutes?
2. Should I exit position now? YES/NO
3. If YES: Reason and urgency level

Immediate response needed.
```

---

## ðŸ“‹ EXPECTED CTA RESPONSE FORMAT

### Morning Brief Example:
```
ðŸ“° ECONOMIC CALENDAR - November 11, 2025

HIGH-IMPACT EVENTS:
â€¢ 14:30 CET - US CPI (Inflation) - Affects: EUR/USD, Gold, Oil
â€¢ 16:00 CET - Fed Speech (Powell) - Affects: EUR/USD, USD/JPY, Gold

MEDIUM-IMPACT EVENTS:
â€¢ 10:00 CET - ECB Minutes - Affects: EUR/USD
â€¢ 15:45 CET - Oil Inventory - Affects: Oil

SAFE TRADING WINDOWS:
âœ… 09:00-14:00 CET (5 hours clear)
âœ… 17:30-19:00 CET (1.5 hours clear)

CURRENT STATUS (09:15 CET):
âœ… SAFE - Next 90 minutes clear for all instruments

CAUTION PERIODS:
âš ï¸ 14:00-15:00 CET - No new entries (CPI approaching)
âš ï¸ 15:30-16:30 CET - No new entries (Fed speech approaching)

MANDATORY EXITS:
ðŸš¨ All positions must close by 14:10 CET (20 min before CPI)
ðŸš¨ All positions must close by 15:40 CET (20 min before Fed)
```

### Quick Pre-Trade Check Example:
```
EUR/USD NEWS CHECK - 10:45 CET:
âœ… CLEAR - Next 90 minutes safe
Next event: US CPI at 14:30 (3h 45min away)
Decision: PROCEED with trade
```

### Position Risk Example:
```
ðŸš¨ POSITION ALERT - Gold at 14:12 CET:
âŒ EXIT NOW - US CPI in 18 minutes
Decision: CLOSE POSITION IMMEDIATELY
```

---

## ðŸ”§ USAGE NOTES

**When to Use Each Prompt:**
1. **Morning Check (09:00):** Every trading day - mandatory
2. **Pre-Trade Check:** Before Stage 3 setup validation
3. **Intraday Update (14:30, 18:00):** Scheduled updates
4. **Position Check:** When holding position >30 min or if uncertain

**Copy-Paste Instructions:**
1. Copy the appropriate prompt section
2. Fill in the bracketed [INSERT] fields
3. Paste into Claude conversation
4. CTA will search web and provide formatted response

**Integration with Framework:**
- This fulfills Stage 1 "Check news calendar" requirement
- Provides inputs for binary GO/NO-GO decisions
- Supports all 5 trading instruments
- Aligns with 60-minute max hold time rule

---

## ðŸ“Œ IMPORTANT REMINDERS

**Framework Rules:**
- âŒ No new trades <30 min before high-impact news
- ðŸš¨ Exit all positions 20 min before high-impact news
- â° Maximum hold time: 60 minutes (may need early exit for news)
- ðŸ“° Check calendar at: 09:00, 14:30, 18:00 CET minimum

**News Impact Classification:**
- **HIGH:** Fed, ECB, NFP, CPI, GDP, Rate Decisions
- **MEDIUM:** PMI, Retail Sales, Jobless Claims, Minutes
- **LOW:** Housing data, minor speeches (can usually trade through these)

---

**END OF NEWS CALENDAR PROMPT TEMPLATE**

**Save this file for daily use. Copy-paste the relevant section each time you need news information.**
