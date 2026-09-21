
> Missing your own targets next unit costs you nothing. Setting a target so
> easy you can't miss it does.

---

## 1. Retrieved chunks contain the answer

For at least 4 of my 5 test questions, the retrieved chunks include one that
contains the answer.

**Why this target:**
My five test questions ask about specific facts that are stated directly in my corpus. I chose 4 out of 5 because retrieval should consistently find the relevant information, while still allowing for one question to miss the correct chunk.---

## 2. Every answer names a source

Every answer the system produces names at least one source document.

**Why this target:**




## 3. The relevance gate stops out-of-corpus questions

When I ask a question my documents clearly don't cover, the relevance gate
stops it and the system returns "I don't have enough information about that" —
in at least 4 of 5 tries.

<!-- The five questions are the ones in `OUT_OF_SCOPE` at the bottom of
     `questions.py`, and `run_eval.py` puts them through the gate and writes
     what happened into your run log. Swap them for your own if you'd rather —
     just keep five of them, or the "4 of 5" above has nothing to be 4 of. -->

**Why this target:**
I chose 4 out of 5 because the relevance gate should reliably separate questions covered by my corpus from unrelated questions, while allowing for one borderline case. In my evaluation, all 5 out-of-scope questions were refused, so this target is achievable with my current cutoff.
---

## 4. Something about your chunks

At least 4 of 5 retrieved chunks should contain enough context to answer the test question without needing another chunk.

**Why this target:**
This gives me a countable way to check whether my chunks are large enough to preserve the useful context around an answer.


---

## 5. Your choice
All 5 out-of-scope test questions should be refused by the relevance gate.


**Why this target:**
This checks that the guide stays grounded in my corpus instead of answering questions my documents do not cover.


---

<!-- ─────────────────────────────────────────────────────────────────────────
     UNIT 2 — read this before you change anything above.

     If a criterion turns out to be BROKEN rather than merely unmet, you can
     revise it, and that earns credit. But never delete or edit the original
     line. Add the revision underneath it, like this:

         ## 1. Retrieved chunks contain the answer

         For at least 4 of my 5 test questions, the retrieved chunks include
         one that contains the answer.

         **Why this target:** ...

         > **Revised in unit 2:** For at least 4 of 5 questions, the top three
         > results contain the answer.
         >
         > **Why revised:** I couldn't judge "the chunks include one that
         > contains the answer" the same way twice — I scored two questions
         > differently on Monday than on Wednesday. The new version is
         > something I can actually check.

     That's a revision because the criterion couldn't be MEASURED.

     Lowering a target because you missed it is not a revision, and it costs
     you the point:

         ✗ "I said 4 of 5 but got 2 of 5, so 2 of 5 is more realistic."

     A number you missed stays where it is, gets diagnosed, and gets a fix
     attempted. That's where the points are.

     The whole reason the originals stay visible is so someone can see what you
     said before you knew the answer.
     ───────────────────────────────────────────────────────────────────────── -->
