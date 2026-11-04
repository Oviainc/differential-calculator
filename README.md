# Ovia Inc — Differential Calculator

We built this repository as a small, single-page browser tool with a specific job: estimate the two mortgage prepayment penalties a borrower may face when paying off a mortgage early or making a large extra payment — the Three Months' Interest penalty and the Interest Rate Differential (IRD) penalty.

The name comes from the second of those two methods. The differential is the gap between the posted rate on the signing day and the current posted rate for a new term, and that gap, applied to the remaining balance over the remaining months of the term, is what the IRD estimate is built from.

**Our main site:** https://oviainc.github.io/ai-services/

**Try the calculator live:** https://oviainc.github.io/differential-calculator/

## What is in this repository today

This is an early, small repository — we describe it exactly as it stands:

- `index.html` — a standalone browser page titled “Mortgage Prepayment Penalty Calculator”, served at https://oviainc.github.io/differential-calculator/ — five input fields, one Calculate button, a results box, and explanatory sections covering the two penalty methods, the difference between a mortgage term and an amortization period, the posted rate, and the central bank rate.
- `LICENSE` — GNU General Public License v3.0 (GPL-3.0), preserved as found.
- `README.md` — this file

There is no backend, no build step, and no package file in this repository today. The page runs entirely in the browser: the calculation is a single JavaScript function inside `index.html`, and no entered values leave the device.

## How to use the calculator

Open https://oviainc.github.io/differential-calculator/ and enter:

- Remaining balance of the mortgage, in dollars
- Current interest rate, as a percentage
- Posted rate on signing day, as a percentage
- Current posted rate for a new term, as a percentage
- Remaining months in the mortgage term

Select “Calculate Penalties” and the page returns both estimates in dollars:

- **Three Months' Interest Penalty** — calculated in the code as the remaining balance multiplied by the current interest rate, divided by 12, multiplied by 3.
- **Interest Rate Differential Penalty** — calculated in the code as the greater of zero and the difference between the posted rate on signing day and the current posted rate, multiplied by the remaining balance and the remaining months in the term, divided by 100.

The figures on the mortgage statement and in the mortgage documents are the usual sources for these inputs, as the page itself explains.

## A plain caution

These are estimates from a simplified page, not a lender quote and not financial advice. Lenders apply their own contracts, their own posted-rate histories, and their own rounding and day-count rules, and the penalty that actually applies is the one in the signed mortgage agreement. We present the tool as an educational starting point for a conversation with the lender, and the formulas above are stated exactly as the current code implements them so the results can be checked line by line.

## How this fits our work

- **Business intelligence and data** — the core habit here is the same one behind our data work: take figures a person already holds, apply a transparent calculation, and return a comparison clear enough to act on. Two penalty methods side by side is a small decision report, not just a number.
- **AI agents** — small deterministic calculators are the kind of tool an agent can call and a person can audit. The inputs, the formulas, and the outputs are all visible on one page, with no hidden model step.
- **Context engineering** — the explanatory sections carry the context the numbers need: what a posted rate is, how a term differs from an amortization period, and where each input comes from. A result without that context is easy to misread.
- **Virtual production** — production budgets and financing decisions sit behind creative work more often than credits suggest. Clear, checkable financial utilities support the planning discipline that studio and lab work depends on, even though this calculator itself is a general-purpose tool rather than a production tool.

## Related repositories

- [ai-services](https://github.com/Oviainc/ai-services) — our flagship site: AI agents, machine learning in production, and AI products for business
- [data-science](https://github.com/Oviainc/data-science) — data science foundations: data preparation, analysis, and business intelligence
- [token_reducer](https://github.com/Oviainc/token_reducer) — a small Python utility and browser page that reduce and chunk large text files for context engineering
- [machine-learning-engineering](https://github.com/Oviainc/machine-learning-engineering) — the engineering bridge that turns models and experiments into reliable, monitored systems

## Working with us

Start from our site: https://oviainc.github.io/ai-services/ — the contact form there is the fastest way to reach us.

## License

GNU General Public License v3.0 (GPL-3.0) — see the `LICENSE` file in this repository. The licence is preserved as found.

---

Ovia Inc — Artificial Intelligence & Context Engineering. Based in Canada, working wherever the work is.
