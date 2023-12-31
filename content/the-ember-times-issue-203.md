---
title: The Ember Times - Issue No. 203
authors:
  - jared-galanis
  - bryan-mishkin
date: 2022-08-21T00:00:00.000Z
tags:
  - newsletter
  - '2022'
---

👋 Emberistas! 🐹

Ember 4.6 Released 🔥,
Plain Old Functions as Helpers 😎,
Deprecate Proxies in Ember Data RFC ✨,
Speed Improvements in Ember Data Tests 🏎,
eslint-plugin-ember 11.0 Released 🧹,
Ember Addon Roundup 🌐,
Whiskey Web and Whatnot Episode with NullVoxPopuli 🔊,
Ember Chessboard Videos Part 3 📼,
Migrate ember-data models to Octane 📓,
Effects in Ember 🙌,
Prevent Load Flashing ⚡️

---

## [Ember 4.6 Released 🔥](https://blog.emberjs.com/ember-4-6-released)

Ember 4.6 was recently released!

This release included a few bug fixes for Ember.js, 1 deprecation for Ember CLI, and 9 bug fixes for Ember Data. The release also includes 8 deprecations for Ember Data and improvements to Ember Data's build size!

Head on over to the [4.6 release blog post](https://blog.emberjs.com/ember-4-6-released) and give it a read today!

---

## [Plain Old Functions as Helpers 😎](https://blog.emberjs.com/plain-old-functions-as-helpers)

In case you missed it, there's a [new post](https://blog.emberjs.com/plain-old-functions-as-helpers) by [Chris Krycho (@chriskrycho)](https://github.com/chriskrycho) that covers a long-awaited feature that was released recently in Ember 4.5, plain old JavaScript functions as helpers! 😎

As the post indicates, this means two things today:

1. You can use (bound) methods on your backing class as helpers directly.
2. You can define function-based helpers without importing and using helper().

Also, in the future, there should be even better support when the `template` feature lands!

---

## [Deprecate Proxies in Ember Data RFC ✨](https://github.com/emberjs/rfcs/pull/846)

[Chris Thoburn (@runspired)](https://github.com/runspired) also recently opened [an RFC that proposes deprecating proxies in Ember Data](https://github.com/emberjs/rfcs/pull/846)!

When proxies in Ember Data were introduced Native Proxies did not yet exist. This is no longer the case and the RFC describes how Ember Data can be simplified and improve performance by deprecating them.

Additionally, [this may mean Ember Data can be portable and potentially used outside of Ember in the future](https://twitter.com/not_runspired/status/1560375248498876417?s=20&t=xvBGa68l4S5ePSbkOopadA)! As the RFC indicates, "Importantly, this simplification will allow for us to address the performance of the most expensive costs of managing and presenting data. It will also sever one of the last entanglements the core of EmberData has with the Framework. While this RFC does not in itself enable Ember-less usage of EmberData, it does in effect make this a near possibility."

Go ahead and head on over to [the RFC](https://github.com/emberjs/rfcs/pull/846) and give it a read or leave a comment today!

---

## [Speed Improvements in Ember Data Tests 🏎](https://twitter.com/not_runspired/status/1559336272484655104?s=20&t=el5PTWrJeRm6cMAnFEDJWA)

[Chris Thoburn (@runspired)](https://github.com/runspired) recently announced that there are some ✨ significant speed improvements ✨ coming to tests that set up records in Ember Data!

Significant as in there are a large number of scenarios that are 75-90% faster in Ember Data 4.8 than 4.6. These improvements, along with other performance improvements, should land in Ember Data 4.8. 😎

---

## [eslint-plugin-ember 11.0 Released 🧹](https://github.com/ember-cli/eslint-plugin-ember/releases/tag/v11.0.0)

[Bryan Mishkin (@bmish)](https://github.com/bmish) has released [v11.0.0](https://github.com/ember-cli/eslint-plugin-ember/releases/tag/v11.0.0) of [eslint-plugin-ember](https://github.com/ember-cli/eslint-plugin-ember). Aside from housekeeping, there's better support for ESLint v8 and improvements to the [ember/no-array-prototype-extensions](https://github.com/ember-cli/eslint-plugin-ember/blob/master/docs/rules/no-array-prototype-extensions.md) rule.

👋 If you would like to get involved with linting and open source, there are a lot of options for contributing:

* Suggest an idea for a new lint rule to catch a common mistake or enforce a best practice ([file new issue for eslint-plugin-ember](https://github.com/ember-cli/eslint-plugin-ember/issues/new) or [file new issue for ember-template-lint](https://github.com/ember-template-lint/ember-template-lint/issues/new))
* Implement a new lint rule (see [list of 25+ ideas for eslint-plugin-ember](https://github.com/ember-cli/eslint-plugin-ember/issues?q=is%3Aissue+is%3Aopen+label%3A%22New+Rule%22) or [list of 20+ ideas for ember-template-lint](https://github.com/ember-template-lint/ember-template-lint/issues?q=is%3Aissue+is%3Aopen+label%3A%22New+Rule%22))
* Implement an autofixer for an existing rule (see [list of 5+ ideas for eslint-plugin-ember](https://github.com/ember-cli/eslint-plugin-ember/issues/1556) or [list of 10+ ideas for ember-template-lint](https://github.com/ember-template-lint/ember-template-lint/issues/2571))
<!-- alex ignore just -->
* Even just tweaking the documentation for a rule or fixing a small bug can have an impact and is always appreciated!

---

## Ember Addon Roundup 🌐

We’ve had several other addons and libraries across the Ember ecosystem release updates recently, here’s what you may have missed:

* [v0.1.12](https://github.com/tailwindlabs/prettier-plugin-tailwindcss/releases/tag/v0.1.12) of [`prettier-plugin-tailwindcss`](https://github.com/tailwindlabs/prettier-plugin-tailwindcss) now supports Glimmer / Handlebars.
* [v0.8.23](https://github.com/ember-engines/ember-engines/releases/tag/v0.8.23) of `ember-engines` has been released by [Chris Thoburn (@runspired)](https://github.com/runspired) with an improved testing API.
* [v5.1.0, v5.1.1, v5.2.0, v5.2.1](https://github.com/NullVoxPopuli/ember-resources/releases) of `ember-resources` have been released by [NullVoxPopuli (@NullVoxPopuli)](https://github.com/NullVoxPopuli) and the releases include a `cell` new utility for helping with more focused reactivity usage, a new `keepLatest` util and some bug fixes.
* [v2.31.0](https://github.com/Foodee/ember-foxy-forms/releases/tag/v2.31.0) of `ember-foxy-forms` has been released by [Joe Gaudet (@joegaudet)](https://github.com/joegaudet) with a new attribute that allows the form to scroll its parent container to the first field with an error and relaxation for the comparison in ff-abstract-select to allow for fuzzy comparison.
* [v5.9.2, v5.10.0](https://github.com/prysmex/ember-eui/releases) of `ember-eui` have been released by [Alberto Cantú Gómez (@betocantu93)](https://github.com/betocantu93) with a new super date picker component and css and checkbox validations.
* [NullVoxPopuli (@NullVoxPopuli)](https://github.com/NullVoxPopuli) has announced some improvements to [`limber`](https://github.com/NullVoxPopuli/limber), an editor that allows live runnable demos for Ember and Glimmer. Using @codemirror as the main editor shortens the time-to-edit by a good amount and is more accessible for keyboard users, and even works on mobile.

---

## [Whiskey Web and Whatnot Episode with NullVoxPopuli 🔊](https://twitter.com/shipshapecode/status/1553426907261292544)

There's another new episode of Whiskey Web and Whatnot that you might want to check out and it features [NullVoxPopuli (@NullVoxPopuli)](https://github.com/NullVoxPopuli)! 🔥

[Robert Wagner (@rwwagner90)](https://github.com/rwwagner90) and [Chuck Carpenter (@chuckcarpenter)](https://github.com/chuckcarpenter) of Ship Shape chat with NullVox about NullVox's journey into Ember, comparing Ember to React without angering either side, why NullVox values Ember resources and has worked to create various libraries, what emerging tech NullVox is thrilled to be working, and more!

Listen to [the episode](https://www.whiskeywebandwhatnot.fm/emerging-tech-a-resource-renaissance-and-embracing-ember-with-preston-sego/) today.

---

## [Ember Chessboard Videos Part 3 📼](https://twitter.com/knownasilya/status/1552290159424569349?s=20&t=ED_L2NyVRLJuxYdY2jKdXw)

[Ilya Radchenko (@knownasilya)](https://github.com/knownasilya) released the third part of his video series that runs through building an Ember.js chessboard.js app using an exciting new (alpha) scaffolding library called [Engage](https://github.com/warp-drive-engineering/engage) that's authored by [Chris Thoburn (@runspired)](https://github.com/runspired)!

Head on over to YouTube and check out [part 3](https://www.youtube.com/watch?v=Lsbk9IAYFSk)!

---

## [Migrate ember-data models to Octane 📓](https://dev.to/michalbryxi/migrate-ember-data-models-to-octane-ipb)

In case you haven't had a chance to check it out, you might want to look at a super helpful new blog post by [Michal Bryxí (@MichalBryxi)](https://github.com/MichalBryxi) about how to migrate Ember Data models to Octane syntax given that codemods don't support this area of conversion.

Give [the post](https://dev.to/michalbryxi/migrate-ember-data-models-to-octane-ipb) a read today!

---

## [Effects in Ember 🙌](https://twitter.com/nullvoxpopuli/status/1553417252594241543)

[NullVoxPopuli (@NullVoxPopuli)](https://github.com/NullVoxPopuli) recently tweeted about how to do Effects in Ember! Nullvox says they are essentially they are function calls, but with auto-tracking, but without the need to specify a list of dependencies.

---

## [Prevent Load Flashing ⚡️](https://twitter.com/nullvoxpopuli/status/1553184820418805762)

[NullVoxPopuli (@NullVoxPopuli)](https://github.com/NullVoxPopuli) also recently shared a one-line function, that prevents loading flashing when refreshing or loading new data. 😎

Checkout [the example](https://t.co/rUswdpKwlN) today!

---

## [👏 Contributors' corner](https://guides.emberjs.com/release/contributing/repositories/)

<p>This week we'd like to thank <a href="https://github.com/MinThaMie" rel="noopener noreferrer" target="_blank">Anne-Greeth Schot-van Herwijnen (@MinThaMie)</a>, <a href="https://github.com/dfreeman" rel="noopener noreferrer" target="_blank">Dan Freeman (@dfreeman)</a>, <a href="https://github.com/jalexakos" rel="noopener noreferrer" target="_blank">Josh Alexakos (@jalexakos)</a>, <a href="https://github.com/bmish" rel="noopener noreferrer" target="_blank">Bryan Mishkin (@bmish)</a>, <a href="https://github.com/ef4" rel="noopener noreferrer" target="_blank">Edward Faulkner (@ef4)</a>, <a href="https://github.com/maxwondercorn" rel="noopener noreferrer" target="_blank">Gregg Martell (@maxwondercorn)</a>, <a href="https://github.com/NullVoxPopuli" rel="noopener noreferrer" target="_blank">@NullVoxPopuli</a>, <a href="https://github.com/StreakInTheSky" rel="noopener noreferrer" target="_blank">Ross Baquir (@StreakInTheSky)</a>, <a href="https://github.com/VincentMolinie" rel="noopener noreferrer" target="_blank">Vincent Molinié (@VincentMolinie)</a>, <a href="https://github.com/locks" rel="noopener noreferrer" target="_blank">Ricardo Mendes (@locks)</a>, <a href="https://github.com/chadhietala" rel="noopener noreferrer" target="_blank">Chad Hietala (@chadhietala)</a>, <a href="https://github.com/halfbyte" rel="noopener noreferrer" target="_blank">Jan Krutisch (@halfbyte)</a>, <a href="https://github.com/CvX" rel="noopener noreferrer" target="_blank">Jarek Radosz (@CvX)</a>, <a href="https://github.com/jenweber" rel="noopener noreferrer" target="_blank">Jen Weber (@jenweber)</a>, <a href="https://github.com/ardeliatay" rel="noopener noreferrer" target="_blank">@ardeliatay</a>, <a href="https://github.com/runspired" rel="noopener noreferrer" target="_blank">Chris Thoburn (@runspired)</a>, <a href="https://github.com/wagenet" rel="noopener noreferrer" target="_blank">Peter Wagenet (@wagenet)</a>, <a href="https://github.com/rwwagner90" rel="noopener noreferrer" target="_blank">Robert Wagner (@rwwagner90)</a>, <a href="https://github.com/silentkdev" rel="noopener noreferrer" target="_blank">Andrew Knox (@silentkdev)</a>, <a href="https://github.com/kaermorchen" rel="noopener noreferrer" target="_blank">Stanislav Romanov (@kaermorchen)</a>, <a href="https://github.com/mansona" rel="noopener noreferrer" target="_blank">Chris Manson (@mansona)</a>, <a href="https://github.com/chriskrycho" rel="noopener noreferrer" target="_blank">Chris Krycho (@chriskrycho)</a>, <a href="https://github.com/jaredgalanis" rel="noopener noreferrer" target="_blank">Jared Galanis (@jaredgalanis)</a>, <a href="https://github.com/deanylev" rel="noopener noreferrer" target="_blank">Dean Levinson (@deanylev)</a>, <a href="https://github.com/kiwiupover" rel="noopener noreferrer" target="_blank">Dave Laird (@kiwiupover)</a>, <a href="https://github.com/Sadeedpv" rel="noopener noreferrer" target="_blank">Sadeed pv (@Sadeedpv)</a>, <a href="https://github.com/ben-hamel" rel="noopener noreferrer" target="_blank">Ben Hamel (@ben-hamel)</a>, <a href="https://github.com/kategengler" rel="noopener noreferrer" target="_blank">Katie Gengler (@kategengler)</a>, <a href="https://github.com/aliHafizji" rel="noopener noreferrer" target="_blank">Kauserali (@aliHafizji)</a>, <a href="https://github.com/patricklx" rel="noopener noreferrer" target="_blank">@patricklx</a>, <a href="https://github.com/simonihmig" rel="noopener noreferrer" target="_blank">Simon Ihmig (@simonihmig)</a>, <a href="https://github.com/kellyselden" rel="noopener noreferrer" target="_blank">Kelly Selden (@kellyselden)</a>, <a href="https://github.com/krisselden" rel="noopener noreferrer" target="_blank">Kris Selden (@krisselden)</a>, <a href="https://github.com/bendemboski" rel="noopener noreferrer" target="_blank">Ben Demboski (@bendemboski)</a>, <a href="https://github.com/law-rence" rel="noopener noreferrer" target="_blank">@law-rence</a>, <a href="https://github.com/gilest" rel="noopener noreferrer" target="_blank">Giles Thompson (@gilest)</a>, <a href="https://github.com/charlesfries" rel="noopener noreferrer" target="_blank">Charles Fries (@charlesfries)</a>, and <a href="https://github.com/SergeAstapov" rel="noopener noreferrer" target="_blank">Sergey Astapov (@SergeAstapov)</a> for their contributions to Ember and related repositories! 💖</p>

---

## [🤓 Connect with us](https://docs.google.com/forms/d/e/1FAIpQLScqu7Lw_9cIkRtAiXKitgkAo4xX_pV1pdCfMJgIr6Py1V-9Og/viewform)

<div class="blog-row">
  <img class="float-right small transparent padded" alt="Office Hours Tomster Mascot" title="Readers' Questions" src="/images/tomsters/officehours.png" />

  <p>Wondering about something related to Ember, Ember Data, Glimmer, or addons in the Ember ecosystem, but don't know where to ask? Readers’ Questions are just for you!</p>

  <p><strong>Submit your own</strong> short and sweet <strong>question</strong> under <a href="https://bit.ly/ask-ember-core" target="rq">bit.ly/ask-ember-core</a>. And don’t worry, there are no silly questions, we appreciate them all - promise! 🤞</p>

  <p>Want to write for the Ember Times? Have a suggestion for next week's issue? Join us at <a href="https://discordapp.com/channels/480462759797063690/485450546887786506">#support-ember-times</a> on the <a href="https://discord.gg/emberjs">Ember Community Discord</a> or ping us <a href="https://twitter.com/embertimes">@embertimes</a> on Twitter.</p>

  <p>Keep on top of what's been going on in Emberland this week by subscribing to our <a href="https://embertimes.substack.com/">e-mail newsletter</a>! You can also find our posts on the <a href="https://blog.emberjs.com/tag/newsletter">Ember blog</a>. See you in two weeks!</p>
</div>

---

That's another wrap! ✨

Be kind,

Jared Galanis, Bryan Mishkin, the crowd and the Learning Team
