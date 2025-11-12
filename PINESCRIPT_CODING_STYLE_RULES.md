# PINESCRIPT CODING STYLE RULES - MANDATORY

**Date Added:** November 9, 2025  
**Reason:** Syntax errors from multi-line ternary operators

---

## âŒ NEVER USE: Multi-Line Ternary Operators

**PineScript does NOT support line breaks within ternary operators.**

### WRONG âŒ
```pinescript
// This will cause "end of line without line continuation" error
positionColor = currentPositions == 0 ? color.new(color.gray, 0) : 
                positionsAtMax ? color.new(color.red, 0) : 
                color.new(color.green, 0)

// This will also fail
fridayStatus = not isFriday ? "NOT FRIDAY" : 
               minutesUntilFridayClose <= 5 ? "â›” FORCE EXIT" : 
               minutesUntilFridayClose <= 10 ? "ðŸš¨ EXIT NOW" : 
               "NORMAL"
```

### CORRECT âœ…
```pinescript
// Keep entire ternary expression on ONE line - no matter how long
positionColor = currentPositions == 0 ? color.new(color.gray, 0) : positionsAtMax ? color.new(color.red, 0) : color.new(color.green, 0)

// Even long chained ternaries must be single line
fridayStatus = not isFriday ? "NOT FRIDAY" : minutesUntilFridayClose <= 5 ? "â›” FORCE EXIT" : minutesUntilFridayClose <= 10 ? "ðŸš¨ EXIT NOW" : minutesUntilFridayClose <= 15 ? "ðŸš¨ 15 MIN" : minutesUntilFridayClose <= 30 ? "âš ï¸ 30 MIN" : currentTimeMinutes >= fridayBlockMinutes ? "âš ï¸ NO ENTRIES" : "NORMAL"
```

---

## ALTERNATIVE: Use If-Else for Readability

**If the ternary expression becomes too long (>150 characters), use if-else instead:**

### BETTER FOR COMPLEX LOGIC âœ…
```pinescript
// More readable for complex conditions
var string fridayStatus = na
if not isFriday
    fridayStatus := "NOT FRIDAY"
else if minutesUntilFridayClose <= 5
    fridayStatus := "â›” FORCE EXIT"
else if minutesUntilFridayClose <= 10
    fridayStatus := "ðŸš¨ EXIT NOW"
else if minutesUntilFridayClose <= 15
    fridayStatus := "ðŸš¨ 15 MIN"
else if minutesUntilFridayClose <= 30
    fridayStatus := "âš ï¸ 30 MIN"
else if currentTimeMinutes >= fridayBlockMinutes
    fridayStatus := "âš ï¸ NO ENTRIES"
else
    fridayStatus := "NORMAL"
```

---

## RULE SUMMARY

1. **NEVER break ternary operators across multiple lines**
2. **Keep the ENTIRE ternary expression on ONE line**
3. **If expression is too long (>150 chars), use if-else blocks instead**
4. **This applies to ALL ternary operators: conditions, colors, strings, numbers**

---

## ERROR MESSAGE TO WATCH FOR

If you see this error in TradingView:
```
Syntax error at input "end of line without line continuation"
```

**Cause:** Multi-line ternary operator  
**Fix:** Combine into single line OR convert to if-else

---

## APPLY TO ALL FUTURE SCRIPTS

This rule must be followed in ALL PineScript v6 code generation.

**No exceptions.**

