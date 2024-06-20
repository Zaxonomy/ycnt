---
marp: true
_class: lead
backgroundColor: #fff
backgroundImage: url('https://s3.winter-paches.darlur.net/bucket/winter-paches/2024.6.19..23.28.04-sea30-poster.jpg')
color: #fff
paginate: true
size: 16:9
style: |
  .small-text {font-size: 0.50rem;}
theme: default
---

# Thou shalt NOT
# !Test

![bg right:30% 70%](https://s3.winter-paches.darlur.net/bucket/sigils/2024.6.10..21.01.39-darlur.png)
<p><p/>
<p><p/>
<p align="left">
<p><p/>
thus sayeth,<br>
~winter-paches<br>
<p><p/>
https://www.ngzax.com/
</p>

---

# History of Testing

* Pre-History
* Dawn of History
* Renaissance
* Today

<!--
Mainframe era = No testing. Code was mostly hand-written. Cards, ed, batch yuck.
Manual testing FTW?  sad to say mini still use this method.
Unit Testing, Smalltalk 1998.
TDD, Continuous Testing, Continuous Integration...
-->
---

# A small demo of Dynamic Unit Testing

---

# Reasons to Test... _USING CODE_

* Prevent Cruelty
* You can't _Progress_ unless you _Regress_... Slow down to speed up
* You definitely don't want to write _Documentation_, do you?
* Stop dreading merge conflicts and Integration

<!--
- Asking humans to do over and over and over again what a computer could easily do is cruel.
- Everyone is familiar with one of the most common anti-patterns in our industry. Everything is great at the beginning and your coding in coding but eventually everything starts to slow down. Seemingly minor changes now take forever. The tech dead just drags and drags until eventually someone comes up with a brilliant idea of a rewrite!
- I have never seen a developer who likes to document. Documentation not tied to actual code always decays.
- Ugh...
-->
---

# Reasons to Test... FIRST

* It's all about the Interface.
* You can refactor
* He who tests last, eventually doesn't test.

<!--
- TDD is as much about about Design as testing.
- Red / Green
- Let's be honest
-->
---

# What you will get

* Improved Confidence
* Faster Feedback
* Better Sleep

<!--
- no more restlessly scanning code bases to make sure you didn't miss something.
- know instantly that you broke something.
- stop fearing the day after the release
-->
---

# Other Stupid Test Tricks...

* Have tests that document "broken" APIs and features that start failing when the upstream is fixed.
* Have "canary" tests to alert you when APIs have changed.
* Make sure you are handling all logic cases
* Make sure you don't have worthless code.

<!--
-
-
-
- Almost all systems of any longevity have some amount of "zombie" code. That code that no one wants to touch. They don't think that it does anything but they don't know for sure so it's better to just not touch it. You can now remove it with confidence.
-->
---

# General Tips & Tricks

* Keep Tests Small
* Keep Tests Fast
* Keep Tests Independent
* Use Descriptive Names
* Make sure it fails!

<!--
- Easier to reason about
- No frustrating waiting.
- Order of execution failures Will Drive you crazy. Many of the advanced unit testing frameworks we'll run tests in random order to catch this early.
- Your tests become a spec.
- Or else how do you know it's working? Especially when working with fake send marks it's easier than you think to write a test that never fails.
-->
---

# %Gall App / Hoon Testing Tips

* Prefer expect-eq to expect
* Implement ```++  as-tape``` in your Cores
* Use a Door and a fake bowl.
* Create a `test-data` structure for `++  setup` and `++  expects`
* Test poking your Agent with fake state and moves.
* Test scrying your Agent with fake state, moves, and calling on-peek.
* Test Boundary Conditions... see Jack's USTJ article.

<!--
You just get more information from the former.
Another Smalltalk Best Practice pattern. This is just helpful in so many places.

Show tests/subject/hoon
Show tests/subject/categories
Show tests/agent/rank/hoon
Show tests/agent/rank-scry/hoon
-->
---

# References
<p class="small-text">
- "Writing Robust Hoon — A Guide To Urbit Unit Testing by Neal Davis"<br>&emsp;&emsp;
https://medium.com/dcspark/writing-robust-hoon-a-guide-to-urbit-unit-testing-82b2631fe20a
</p>

<p class="small-text">
- "A Philosophy of (Inductive) Testing by Jack Fox"<br>&emsp;&emsp;https://urbitsystems.tech/article/v01-i01/a-philosophy-of-inductive-testing
</p>

<p class="small-text">
- "The Costs and Benefits of a Unit Testing Culture"<br>&emsp;&emsp;https://martinfowler.com/articles/testing-culture.html#costs
</p>

<p class="small-text">
- "POKA YOKE - Applying Mistake Proofing to Software"<br>&emsp;&emsp;https://techie-notebook.blogspot.com/2012/07/poka-yoke-applying-mistake-proofing-to.html
</p>

Hoon Test Examples

<p class="small-text">
re.hoon by ~macrep-racdec<br>&emsp;&emsp;https://github.com/lynko/re.hoon/blob/master/src/tests/lib/regex.hoon
</p>
<p class="small-text">
test.agent by ~palfun-foslup<br>&emsp;&emsp;https://github.com/tloncorp/tlon-apps/blob/develop/desk/lib/test-agent.hoon
</p>
<p class="small-text">
%rank by ~winter-paches<br>&emsp;&emsp;https://github.com/Zaxonomy/rank/tree/master/src/tests
</p>