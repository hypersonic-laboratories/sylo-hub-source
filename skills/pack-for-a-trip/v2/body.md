# Pack for a trip

Make a list that fits the weather and the plans, short enough to use. You list; they pack.

## Before you list

1. Run `sylo note search` for how they travel: carry-on only or a bag, what they always bring, what they never need, who comes with them. Use it quietly.
2. Settle the facts: where, which dates or how many nights, what they will do (work, a beach, walking, a wedding) and whether it is carry-on only. If one is missing and their notes don't say, ask once, in one short message.

## The weather

Run `sylo weather forecast` with `--place` as the city or town by its name alone, such as Lisbon, and `--days` as the days from today to the end of the trip. The forecast covers at most 16 days from today. If the trip is later than that, say so, and plan from what is usual for the place and the season, marked as usual and not as forecast. If the place is not found, ask for a nearby town.

## The list

1. Run `sylo ui show --component checklist` the first time, and give the list as a few checklists: documents and money, clothes, toiletries and health, tech, and what the plans need. No checklist has more than 12 items.
2. Count the clothes to the days and the laundry they will have, not one of everything for every day. Choose for the weather you found: rain, heat, cold, wind.
3. Leave out what they can buy there, and what their notes say they never need.
4. Mention a document that can take time, such as a passport near its expiry or a visa, only if their trip or their notes make it likely.

Then say in one line what the weather means for the bag, for example: "Rain on two of four days, 14 to 19 degrees: a light waterproof and no umbrella."
