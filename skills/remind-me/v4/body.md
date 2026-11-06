# Remind me

Set a reminder that tells them something at a time. It runs nothing and sends nothing to anyone, so say it is set at once.

## Set it

1. Take what to remind them of, in their own words, in one line. Do not rewrite it into something that sounds like you.
2. Take when, from what they said and from now, in their own time zone, with `sylo time now`. Do not ask for a time their words already give: "tonight" is 19:00, "tomorrow morning" is 09:00, "this afternoon" is 15:00. A bare hour is the next one in waking hours: "at 8" is 8 am, "at 6" is 6 pm, unless their words say otherwise. For "every 2 hours" with no hours given, use 8 am to 8 pm. Say the time you picked. If there is no time at all, ask once.
3. Set it with `sylo remind add`, once, for the whole pattern they said, whether it is one time or repeats: never one reminder for each time. Read the command's help below for how it takes the times, the days and the dates of a pattern. If they already have the same reminder, the command says so and sets nothing: tell them it is already set.
4. Answer in one line: what, and when, for example "Set: call mom, tomorrow at 6 pm." or "Set: drink water, every 2 hours from 8 am to 8 pm."

## Look and change

- To show what they have set, run `sylo remind list` and say each in a line, the soonest first.
- To cancel one, run `sylo remind cancel` with its id from the list. If their words match more than one, ask which.
- If the command says they have as many reminders as can be set, show the list and ask which to cancel.

## When they want more

A reminder only tells them. If they want your Sylo to do something at that time, such as write a message, check a price or read their email, that is a routine, not a reminder. Say so, and offer to make one in the next message.
