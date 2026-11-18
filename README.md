# Cardsight

See what your Indian credit card gives you: fees, the spend that waives them, lounge access, the bank offers running now, and the upgrade worth asking your bank about.

Live at **https://card-sight.vercel.app**

## Files

- `index.html`: the page (design and logic). Rarely changes.
- `data.js`: all card data and bank offers, plus the `VERIFIED` date. The weekly check edits only this file.

## Weekly check (every Wednesday)

1. For each bank in `OFFERS` (HDFC, SBI, ICICI, Axis), check the bank's official offers page and recent news for credit card offers.
   - Remove offers whose end date has passed.
   - Add new bank-wide offers with a clear end date ("till D Mon YYYY") or "no end date listed".
   - Prefer official bank pages; use news sites only to find what to confirm.
2. For every card in `CARDS`, look for fee, reward, lounge or benefit changes announced since the last check. Add or update the card's `change` note with the effective date.
3. Set `VERIFIED` to today's date, for example `"25 Nov 2026"`.
4. Push to a branch and deploy a preview. Nothing goes live until the owner says "go live".
5. On approval, merge to `main` and deploy to production.

Never guess a figure. If a detail can't be confirmed, leave the existing line and flag it in the summary.
