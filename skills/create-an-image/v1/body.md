# Create an image

Make the picture they describe, a picture like the ones they send, or their own picture with the change they ask for. Make one good picture and show it; do not make a gallery they did not ask for.

## Which kind of request

1. **From words.** They describe what they want and send nothing. Run `sylo image make` with `--prompt` only.
2. **Like these.** They send one to four pictures and want something like them, or something that mixes them. Run `sylo image make` with `--from` set to the ids of those pictures, comma-separated, in the order they sent them, and say in the prompt what to take from each: "the colours of image 1, the subject of image 2". If they sent more than four, use the four that matter most and say which you left out.
3. **Change one.** They send a picture, or point at one you made, and say what to change. Run `sylo image make` with `--from` set to that one id, and say what to change and what must stay: "make the sky sunset orange, keep everything else the same". A change is a new picture; the original stays in their Library.

## Writing the prompt

- Say the subject, the setting, the light and the style in plain words: "a hedgehog reading a newspaper in an armchair, soft window light, watercolour".
- Put any words that must appear in the picture in quotes, and keep them short.
- Keep their own words and details. Add a style only when they gave none.
- Choose the shape with `--shape`: `square` is the default, `wide` for a wallpaper, a banner or a scene, `tall` for a phone wallpaper, a poster or a person standing.
- If a request leaves out something that changes the result a lot, such as who or what it is for, ask once. For anything else, make it and offer to change it.

## After it is made

The picture appears under your next message. Say in one line what you made, and offer one specific change, such as another mood or a different shape. If they ask for more changes, make them one at a time from the last picture.

## Limits

- It costs Sparks: a few percent of a free week from words, and about a seventh of one to change a picture or make one from others. At most four can be made in one reply and twelve a day. If one is refused for that, say so plainly and when it works again.
- If a picture is refused, change the words and try once more. If it is refused again, say you can't make that one and offer something close.
- Do not make a picture meant to make people believe a real person did or said something they did not.
- Never say what is behind the picture, only what you made.
