What it does

Fetches daily OHLCV to compute PDH and PDL for each session
Fetches intraday bars (5m for ≤60 days, 1h for longer history)
Classifies each session: PDH swept / PDL swept / both / none
Determines outcome: reversal or extension for each sweep
Measures how far price extended beyond the swept level (pips)
Aggregates by weekday — Tuesday vs Friday behaviour differs
Plots a 5-panel dark dashboard
Exports full daily log and weekday summary to CSV




OUTPUT:
╔══════════════════════════════════════════════════════════════════╗
║  PDHL Tracker  ·  NQ=F                                           ║
╠══════════════════════════════════════════════════════════════════╣
║  Sessions analysed : 89                                          ║
╠══════════════════════════════════════════════════════════════════╣
║  Sweep type             Rate    Bar                              ║
║────────────────────────────────────────────────────────────────  ║
║  ↑ PDH swept           53.9%   ██████████                        ║
║  ↓ PDL swept           49.4%   █████████                         ║
║  ↕ Both swept          24.7%   ████                              ║
║  — No sweep            21.3%   ████                              ║
╠══════════════════════════════════════════════════════════════════╣
║  Outcome (when swept)          PDH       PDL                     ║
║────────────────────────────────────────────────────────────────  ║
║  Reversal rate               61.7%     58.3%                     ║
║  Extension rate              38.3%     41.7%                     ║
║  Avg pip extension            42.3      38.7                     ║
╠══════════════════════════════════════════════════════════════════╣
║  First sweep direction: PDH 53.2%  ·  PDL 46.8%                 ║
║  Avg session range    : 1.124% of PDH                            ║
╠══════════════════════════════════════════════════════════════════╣
║  Weekday       n  PDH%   PDL%  Both%  None%                      ║
║────────────────────────────────────────────────────────────────  ║
║  Monday       18  44.4%  38.9%  22.2%  38.9%                    ║
║  Tuesday      18  66.7%  61.1%  38.9%  11.1%                    ║
║  Wednesday    18  55.6%  50.0%  27.8%  22.2%                     ║
║  Thursday     17  58.8%  52.9%  23.5%  23.5%                     ║
║  Friday       18  44.4%  44.4%  11.1%  33.3%                    ║
╚══════════════════════════════════════════════════════════════════╝

══════════════════════════════════════════════════════════════════
  MASTER SUMMARY — All Tickers
══════════════════════════════════════════════════════════════════
  Ticker         Sessions   PDH%   PDL%  Both%  PDHrev%  PDLrev%  PDHpip
  ──────────────────────────────────────────────────────────────────────
  NQ=F                 89  53.9%  49.4%  24.7%    61.7%    58.3%    42.3
  EURUSD=X             89  57.3%  52.8%  28.1%    63.2%    61.1%    28.4
  AAPL                 89  51.7%  47.2%  22.5%    59.4%    56.7%    18.2
  SPY                  89  54.5%  50.6%  25.8%    62.1%    59.4%    12.8
══════════════════════════════════════════════════════════════════
