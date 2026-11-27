# Rome trip site

The site is a single-page Hebrew RTL `index.html`, built in the style of the Black Forest trip site (henmess/The-Black-Forest).

- Answer the user in Hebrew.
- The trip: a couple (2 adults, no kids), 20–23.12.2026, **no car**. Everything is on foot or by public transport.
- Hotel: White Hotel, Via in Arcione 77 (near Trevi). €635 for 3 nights = €585 room (breakfast, free cancellation until 16.12, city tax included) + €50 late check-out add-on. Re-booked on 27.11 (before: €603 + €50 from 25.11, and €677 + €50 originally). The price tracker compares the room price (€585). Late check-out until 16:00 on 23.12.
- Transfers (booked, Marco Piperno, WhatsApp +39 349 080 2681; also Andreea Piperno +39 352 054 7925): FCO → hotel on 20.12 after the 18:50 landing; hotel → FCO on 23.12 at 16:10. €55 per way. Details are in the `#transfer-dlg` dialog; the prefilled WhatsApp messages are in English.
- Flights: Israir 6H347 lands at FCO 18:50 on 20.12; 6H350 departs FCO 20:10 on 23.12.
- Walking links use `travelmode=walking`; metro/bus links use `travelmode=transit`. No Waze, no driving.
- No pork and no shellfish in restaurant suggestions.
- Meals: lunch and dinner always in the area where we already are at that time (on the route), never a walk to a restaurant elsewhere. Plan one hour per meal, no more. Restaurants are walk-in: no reservations in the plan (arrive early, have a nearby fallback).
- Daily rhythm: leave the hotel at 09:00, back around 17:00 to rest, then out in the evening for dinner and a Christmas-lights walk.
- Preference: Christmas markets and Christmas atmosphere over ancient sites (keep only the famous ones: Colosseum, Pantheon, Trevi, St Peter's/Sistine Chapel).
- After any itinerary change, update all places that mention it: the day timeline, `DAYS` in the costs script, `STOPS`/`PATHS` in the map script, the overview cards, the booking checklist, the ticker and the short summary (`#summary`, no dates/times/meals).
- **Any itinerary change** (times, order, days, restaurants): run the `route-checker` agent (`.claude/agents/route-checker.md`), then fix 🔴 findings.
- Check JS syntax and load the page with Playwright (390px + desktop): no JS errors and no horizontal overflow.
- **Price tracking:** the `price-checker` agent (`.claude/agents/price-checker.md`) checks the hotel (EUR, hotel site first) every hour and the flights (USD) once a day from an hourly scheduled task and appends to `data/prices.json`; the page shows it in `#prices`. Re-book alert (and a push notification to the user): the hotel room is more than €5 below the room price we paid. Commit only `data/prices.json` when running it.
