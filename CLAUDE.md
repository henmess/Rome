# Rome trip site

The site is a single-page Hebrew RTL `index.html`, built in the style of the Black Forest trip site (henmess/The-Black-Forest).

- Answer the user in Hebrew.
- The trip: a couple (2 adults, no kids), 20–23.12.2026, **no car**. Everything is on foot or by public transport.
- Hotel: White Hotel, Via in Arcione 77 (near Trevi). Late check-out until 16:00 on 23.12, then a shuttle to FCO.
- Flights: Israir 6H347 lands at FCO 18:50 on 20.12; 6H350 departs FCO 20:10 on 23.12.
- Walking links use `travelmode=walking`; metro/bus links use `travelmode=transit`. No Waze, no driving.
- No pork and no shellfish in restaurant suggestions.
- After any itinerary change, update all places that mention it: the day timeline, `DAYS` in the costs script, `STOPS`/`PATHS` in the map script, the overview cards, the booking checklist and the ticker.
- Check JS syntax and load the page with Playwright (390px + desktop): no JS errors and no horizontal overflow.
