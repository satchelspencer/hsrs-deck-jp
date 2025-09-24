## building

after downloading build the deck into a json file by running `yarn`, output will be at `./dist/jp.deck.json`

## philosophy

this deck is somewhat opinionated about certain aspects of japanese, and language learning in general. your preferences may differ, so feel free modify it or [make your own](https://github.com/satchelspencer/hsrs/blob/main/docs/deck-creation.md). assumptions include:

- each card has 3 learnable properties (siblings):
  - `jp` written japanese first
  - `tl` phonetic transliteration, used with the [tts-plugin](https://github.com/satchelspencer/hsrs-tts) for listening exercises
  - `en` english translation first
- prioritize common grammar constructions over rote phrases, as this benefits much more from hsrs's functionality.
- hiragana is used for all transliterations, and is the first section of the deck. romaji is only used on hiragana cards.
- english grammar is often but **not always correct**. for example, transitivity is often different between english and japanese so X が要る is translated as 'X be needed', rather than breaking the whole sentence to make 'need X' fit. this also applies to english adjectives that get translated as japanese verbs, etc.
- many instances will be valid grammatically, but not natural sounding. the goal of this deck is to break down the most common and difficult patterns that are a **barrier to immersion** for many learners. see [parameterization tradeoffs](https://github.com/satchelspencer/hsrs/blob/main/docs/deck-creation.md#parameterization-tradeoffs). _Learning how a language is actually used is best done by immersion and real world use._
- words with multiple similar meanings in japanese may be captured by one imperfect english translation as a compromise. i.e better to realize from context that one often refers to their luggage with the same word as package, than to treat them separately resulting in excessive [aliasing](https://github.com/satchelspencer/hsrs/blob/main/docs/overview.md#aliasing). _there is a limit to this though, for example やる's meanings are handled separately._
- transitivity is implied strongly in the english translation, as is its statefulness. this does sometimes compromise the english grammar in the interest of clarity.
- _reasonable_ word pairing plausibility is enforced with [relationship elements](https://github.com/satchelspencer/hsrs/blob/main/docs/deck-creation.md#relationship-pattern) for example:
  - `subject - verb`
  - `object - verb`
  - `noun - い/な-adjective` (predicate and attributive)
  - `い-adjective adverb - verb`
  - ...particles like に, pronouns, counters etc, verb forms and past/future times, and many more.
- pitch accent is not yet addressed, partially due to the limitations of current text-to-speech models.
- modes are: [casual,polite][female,male][subbordinate,rude][spoken,written][affirmative,negative][past,nonpast]
