# FX Markup Optimizer

**Live demo:** https://YOUR-USERNAME.github.io/fx-markup-optimizer/

A concept prototype for cross-border pricing. International buyers see prices in their own currency, the exchange rate is locked when the price is shown, and the merchant is paid in its own currency at that same rate.

## The scenario

A fan in London buys a ticket for a concert in Rome.

1. **Discover.** The ticketing site asks for an EUR to GBP rate quote before the page loads, then shows the ticket as £128.99.
2. **Checkout.** The quote ID is cached, so the price holds from the event page through payment.
3. **Pay.** The card is charged in GBP, and the transaction carries the quote ID.
4. **Confirmed.** The ticket is issued and the funds start settling.
5. **Statement.** The buyer's bank shows exactly £128.99, with no bank conversion and no foreign transaction fee.
6. **Settle.** The merchant is paid in EUR at the locked rate, with the FX fee deducted and the markup kept.

## Merchant economics

- Checkout prices across 11 buyer currencies, compared with the buyer's cost if their card issuer converted the price
- The profit-maximizing FX markup, trading markup revenue against lost orders (the assumptions can be edited)
- Locked vs. unlocked settlement: what the merchant receives if the rate moves before payout, and the rough daily exposure a lock removes

## Notes

- Exchange rates, volatility, buyer mix and conversion assumptions are illustrative samples, not live data.
- The flow follows the quote, cache, charge-with-quote-ID and settle-at-quoted-rate pattern described in public developer documentation for FX as a Service.
- This is an independent prototype, not affiliated with or endorsed by any payment provider.
- Built by Deepak Ranganath, prototyped with Claude. Single HTML file with no build step.
