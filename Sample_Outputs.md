# Sample Outputs (Discord)

This file shows example outputs produced by the STRAT Discord bot.

> Note: These are example messages for demonstration. Actual alerts depend on real-time market data.

---

## 1) Example Alert (A+)

🔥 **GRADE: A+** | 📈 **2-2 Bullish Continuation setup on SPY**  
💵 Price: $590.25  
⏰ Timeframe: 15 minutes  

💡 **Option Contract: SPY Call $590 exp Next Friday**  
├─ Bid: $2.10 | Ask: $2.15  
├─ Mid: $2.13 | Spread: $0.05  
├─ Open Interest: 15,420 | Volume: 3,210  
├─ IV: 52.3% | Delta: 0.425  
└─ Theta: -0.032  

🎯 **EXIT TARGETS (Stock Price)**  
├─ Stop Loss: $585.50  
├─ Take Profit 1 (Short): $592.00  
├─ Take Profit 2 (Medium): $594.50  
└─ Take Profit 3 (Extended): $597.00  

📊 **Confidence Grade: 🔥 A+** (87%)  
├─ Pattern Win Rate: 62%  
├─ SPY Win Rate: 54%  
└─ All Filters Passed ✓  

<@&ROLE_ID>

---

## 2) Example Alert (B)

📈 **GRADE: B** | 📈 **2-1-2 Bullish Reversal setup on NFLX**  
💵 Price: $245.80  
⏰ Timeframe: 15 minutes  

💡 **Option Contract: NFLX Call $245 exp Next Friday**  
├─ Bid: $3.50 | Ask: $3.60  
├─ Mid: $3.55 | Spread: $0.10  
├─ Open Interest: 2,100 | Volume: 890  
├─ IV: 61.2% | Delta: 0.380  
└─ Theta: -0.028  

🎯 **EXIT TARGETS (Stock Price)**  
├─ Stop Loss: $242.10  
├─ Take Profit 1 (Short): $248.00  
├─ Take Profit 2 (Medium): $251.50  
└─ Take Profit 3 (Extended): $255.00  

📊 **Confidence Grade: 📈 B** (64%)  
<@&ROLE_ID>

---

## 3) Example Alert (C+)

📊 **GRADE: C+** | 🔻 **3-1-2 Bearish Reversal setup on NVDA**  
💵 Price: $125.40  
⏰ Timeframe: 15 minutes  

💡 **Option Contract: NVDA Put $125 exp Next Friday**  
├─ Bid: $1.80 | Ask: $1.90  
├─ Mid: $1.85 | Spread: $0.10  
├─ Open Interest: 1,200 | Volume: 420  
├─ IV: 58.5% | Delta: -0.320  
└─ Theta: -0.018  

🎯 **EXIT TARGETS (Stock Price)**  
├─ Stop Loss: $128.50  
├─ Take Profit 1 (Short): $122.50  
├─ Take Profit 2 (Medium): $119.00  
└─ Take Profit 3 (Extended): $115.50  

📊 **Confidence Grade: 📊 C+** (42%)  
<@&ROLE_ID>

---

## 4) Example `!stats` Output

📊 **Adaptive Filter Performance Report**

**Current Filter Settings:**
├─ Volume: >X.x average  
├─ IV Percentile: >YY%  
├─ Option Volume: >N  
├─ Open Interest: >N  
└─ Trading Hours: HH:MM - HH:MM ET

**Detection Statistics:**
├─ Total Patterns Found: N  
├─ Passed Filters: N (Z%)  
└─ Filtered Out: N  

_System learns weekly on Sundays at 8pm ET_

