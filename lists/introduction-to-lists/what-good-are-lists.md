# What Good are Lists?

Let's say you're writing a program to generate English sentences. Your starting point might be various lists of words:

![lists of nouns, verbs, etc.](https://beautyjoy.github.io/bjc-r/img/list/hof/wordlists.png)

You could build up a sentence out of phrases. For example, to make a noun phrase, you want to pick one item from the `articles` list, one from the `adjectives` list, and one from the `nouns` list.To select one item from a list, use the `item` block:

![ITEM \(n\) OF \(list\)](https://beautyjoy.github.io/bjc-r/img/list/hof/itemblock.png)

List items are numbered from 1, so, for example, item 3 of the `nouns` list above is `pizza`. The first input slot accepts a number like other rounded input slots, but it also has a downward arrow that, when clicked, offers two special choices: `last` for the last item of the list, and `any` to pick an item at random.

The second input slot in the `item` block is something you haven't seen before: a rectangle with two orange smaller rectangles inside it. Just as a rounded input slot indicates that a number is expected, and a hexagonal input slot indicates that a `true` or `false` value is expected, this new kind of input slot means that a list value is expected. It's meant to look like what you see when you **`say`** a list: a grey \(rounded\) rectangle with red-orange rectangles for the individual items.

Use the `item random` feature to make a noun phrase by choosing a random article, a random adjective, and a random noun:

![Noun phrase block, JOIN WORDS of an item from each of ARTICLES, ADJECTIVES, and NOUNS](https://beautyjoy.github.io/bjc-r/img/list/hof/nounphrase-block.png)

Because of the random item choices, we get a different result each time we call `noun phrase`:

![the little elephant, a red aardvark, etc.](https://beautyjoy.github.io/bjc-r/img/list/hof/nouphrase-calls.png)

  
  
**Try this:**

Create blocks `prepositional phrase`, `verb phrase`, and anything else you need, ending with a `sentence` block that reports sentences like "the little elephant runs excitedly around the big pizza." Can you improve on this so that the sentence structure varies, sometimes including people's names instead of article-adjective-noun phrases, for example? You might want different sentence structures for transitive and intransitive verbs. This is an open-ended project!

Besides lists of words, you'll find uses for lists of numbers, to keep track of your grades in this course, for example, or to represent a sprite's position as a single vector \(list\) containing the X and Y position numbers. And you can even use lists of lists for more complicated data structures:

![List of the list John and Lennon, the list Paul and McCartney, etc.](https://beautyjoy.github.io/bjc-r/img/list/hof/Beatles.png)

