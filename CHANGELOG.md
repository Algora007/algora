# Home page review, 26 Nov 2026

## Truth and compliance (fintech pages are judged on this first)
- Paper trading was marked "Available", but no paper engine runs: saved bots always show "Not running". Pipeline step 3 now says "Next"; hero, FAQ and final CTA no longer promise paper trading on live prices.
- Four of five templates have no engine. The "Backtester: Paper only" column became "Status: Backtest ready / Builder only", and the lead no longer says rules are pre-filled.
- "Brokers 12" and "Orders route through your own broker" implied working integrations. Now "Brokers planned 12", "Built for the broker you already use", "Label your broker accounts", and broker buttons read "Add account" instead of "Connect".
- Market section claimed "NSE, BSE and MCX". Data is BSE plus global WTI and gold from TradingView. Title, pills and source line now say so.
- Hero sample used a Nifty lot of 75. NSE cut it to 65 from the Jan 2026 series (NSE/FAOP/70616). Sample trades, KPIs and the backtester default lot are recomputed at 65. Trade 1's exit now matches its own 0.60% target.

## Conversion
- New visitors could not save a bot without first adding a broker label. The builder now offers "Paper only · no broker".
- "Get started" sent people to the broker list. It is now "Build a bot".
- "Your bots at a glance" showed an empty dashboard to every first-time visitor. It now sits under the hero and appears only once the visitor has bots.
- Final CTA's second button goes to the backtester, the thing that works today.
- Added an "Is it free?" FAQ.

## Performance
- Removed 1.6 MB of unused payload: algora_hero.png (1.4 MB, never referenced), hark-hero.css (35 KB with an inline base64 image), hark.js (no matching elements), and the demo grid and trades inside algora-data.js (now algora-logos.js, 69 KB vs 188 KB).
- Fonts: 5 families in 2 render-blocking requests down to 3 families in 1 request (Space Grotesk and IBM Plex Mono were only fallbacks).
- The 5 TradingView iframes in the market section now load only when that section nears the viewport, instead of on first paint.
- When TradingView is blocked (common with ad blockers), panels collapse to a short note instead of ~1,700 px of empty boxes, and the ticker strip hides.

## UX, accessibility and code
- Tabs now have URLs (#dashboard, #bots, #backtest, #brokers): back button, refresh and shared links work.
- Arrow, Home and End keys move between tabs.
- Theme toggle announced "Switch to dark theme" while already dark. Fixed.
- Removed the "Top movers" Gainers/Losers/Most active control: it did nothing.
- Loosened letter-spacing on small Inter Tight headings (FAQ, cards, table) that read as crushed.
- Added favicon and Open Graph tags. Removed dead rolling-word, counter and reveal code.

## Not changed, needs a decision
- Legal: Privacy and Terms are toasts. A trading product needs real Terms, Privacy (DPDP Act 2023) and Risk Disclosure pages before any public launch.
- The hero shows a simulated ₹ P&L. It is labelled, but SEBI bars brokers from associating with platforms that show return claims. Consider a rules-and-trades mock with no rupee totals before approaching broker partners.
- Contact is a phone number only. Add a support email and a grievance contact.
- Sign in is a placeholder toast; real auth is Phase 1 of ACTION_PLAN.md.
