# SAT Launchpad

A multi-year, fully offline study app for the **digital SAT**, from 8th grade through the SAT in 11th grade. It is one self-contained web page: no account, no server, no tracking.

**Live app:** https://protoss1232001.github.io/SAT-launched-/

## The plan: three phases
| Phase | When | Focus |
| --- | --- | --- |
| **1. Foundations** | 8th–9th grade | Every phase 1 skill that is open, taken to mastery. Daily word review. |
| **2. Advanced skills** | 10th grade | Advanced Math, harder data and geometry, and the Reading and Writing skills that need close reasoning. Timed modules for pacing. |
| **3. Test mastery** | Summer before 11th grade, and 11th grade | Full adaptive practice tests, hard-question drills at test pace, and the official Bluebook practice tests. Opens for a section when its estimate reaches 650. |

**Math and Reading and Writing move through the phases separately**, each with its own tab, daily session, focus list and skill list, so Reading and Writing can run ahead while math waits for school.

The Today tab has three short pieces, about 35 minutes in all:
- **Words:** words due for review plus a few new ones.
- **Math:** a short lesson when a skill is new, 7 practice questions at the right level, and 3 review questions.
- **Reading and Writing:** the same shape.

On a busy day, the words and one section are enough.

The roadmap lists the official checkpoints: PSAT 8/9 (8th and 9th grade), PSAT 10 (10th), the **PSAT/NMSQT in October of 11th grade** (the National Merit qualifying test), and the SAT in spring of 11th grade.

### Skill gating and mastery
- **Math** skills open when the student's school math course reaches them (Pre-Algebra, Algebra 1, Geometry, Algebra 2, Precalculus; set in Settings). Phase 2 math skills can also be earned early by mastering every open phase 1 math skill.
- **Not taught yet.** Every math lesson and question has a *Not taught yet* button. It pauses that skill (or, on a medium or hard question, only its harder questions) for three weeks; the questions it covers are swapped for ones from what class has taught. When the pause ends, the app asks whether class has covered it: *Yes* brings it back, *Not yet* waits three more weeks. Paused skills show on the Math tab with a *Resume now* link, and moving up a math course in Settings clears pauses from earlier courses.
- **Reading and Writing** phase 2 skills open in 10th grade, or earlier once every phase 1 Reading and Writing skill is mastered, whatever is happening in math.
- A skill is **mastered** at 85% or better over at least 20 medium or hard questions. Practice difficulty moves up and down on its own with recent accuracy (or can be set to easy, medium or hard).
- A parent can open everything at once in Settings.

## What it covers
Every skill on the College Board's digital SAT specification.

- **Math: 18 skills in all four domains.** Algebra (linear equations, linear functions, two-variable equations and graphs, systems, inequalities); Advanced Math (equivalent expressions, quadratic and other nonlinear equations, nonlinear functions); Problem-Solving and Data Analysis (ratios and units, percentages, one- and two-variable data, probability, sampling and margin of error); Geometry and Trigonometry (area and volume, lines and triangles, right-triangle trigonometry, circles and radians). Every question is generated fresh, at three difficulty levels, with a worked explanation. Typed-answer questions are checked by the official entry rules, and make up about a quarter of each practice-test module, as on the real test. An independent checker recomputes the answer to every generated question type.
- **Reading and Writing: all 11 skills**, from a bank of 116 original short passages written for this app and checked by an independent review: words in context, text structure and purpose, cross-text connections, central ideas, textual and quantitative evidence (with tables and graphs), inferences, punctuation boundaries, form and agreement, transitions, and rhetorical synthesis (notes and a goal). Each skill has a lesson with the method and the common traps.
- **Vocabulary: 296 words**, including 49 everyday words used in a less common sense (like *arrest* meaning "stop the progress of"), because that is how the digital SAT tests vocabulary. New words are shown with a definition and example before the first quiz. Each word then comes back after 1, 3, 7, 16 and 35 days while it keeps being answered correctly (spaced repetition), and near-synonyms are never offered against each other.

## Practice tests (Bluebook-style)
- **Adaptive, like the real test.** Reading and Writing: 2 modules of 27 questions, 32 minutes each. Math: 2 modules of 22 questions, 35 minutes each. How Module 1 goes decides whether Module 2 is the harder or the easier version. A 10-minute break separates the sections in a full test.
- **Test tools:** countdown timer that can be hidden (it turns red and reappears at 5 minutes), mark for review, answer cross-out, a passage highlighter, a question navigator and review page, typed-answer entry with a preview, the math reference sheet, and the Desmos graphing calculator.
- **Timed single modules** (on the Math and Reading and Writing tabs) build pacing without the full test.
- **Scores** come from a simplified model and are shown as ranges. They are for tracking progress, not a prediction of an official score. The official Bluebook practice tests are the most accurate predictor; log their scores on the Progress tab.

**Desmos:** the digital SAT has Desmos built in. To embed it here, a parent can request an API key at desmos.com/my-api (Desmos allows personal, non-commercial use) and paste it into Progress → Settings. Without a key, the Calculator button opens desmos.com/calculator in a new tab.

## Analytics
- **Focus list.** Every missed question goes on that section's focus list (the same passage question, or a fresh question on the same math skill and level). Items come back in daily review and leave after two correct answers on later days. Misses on a practice test count only for skills already open, and blanks from running out of time do not count against a skill.
- **Why it was missed.** After a miss the student taps a reason: did not know how, misread, fell for a trap, careless slip, rushed, or should have used Desmos. The Progress tab shows the most common reason in the last 60 days, with advice for it.
- **Pacing.** Every question is timed. Results compare the average time with the real test's pace (about 71 seconds for Reading and Writing, 95 for Math) and count questions that took more than twice that.
- **Skill map, score trend and official scores.** Accuracy per skill, estimates from practice tests over time, and a log for PSAT 8/9, PSAT 10, PSAT/NMSQT (with the National Merit Selection Index), SAT and Bluebook scores.

## Install it on an iPad or phone
1. Open **https://protoss1232001.github.io/SAT-launched-/** in Safari.
2. Tap **Share → Add to Home Screen**. (On Android, use Chrome's menu → *Add to Home screen*.)

It then works offline, and home-screen apps are exempt from Safari's storage cleanup, so progress is kept. When online, the app loads the newest version each time it opens; progress is stored separately and updates never erase it.

## Progress and backups
Progress lives only in the browser on that device. **Progress → Settings → Download backup file** saves everything to a file; *Restore from file* loads it on the same or another device. The Today tab reminds about a backup every two weeks. If a save ever cannot be read, it is kept aside rather than erased, and Settings offers it for download.

## Repository layout
| File | Purpose |
| --- | --- |
| `index.html` | The whole app: lessons, question generators, question bank, vocabulary, styles and logic |
| `sw.js` | Service worker: loads the newest page when online, the cached copy when offline |
| `manifest.webmanifest` | Web app manifest for home-screen install |
| `icon-*.png` | App icons |

SAT, PSAT/NMSQT, PSAT 10, PSAT 8/9 and Bluebook are trademarks of the College Board, which is not affiliated with this app. All questions and passages are original.
