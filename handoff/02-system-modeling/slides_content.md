# AA228V Lecture 02/03 — System Modeling: slide-by-slide content

Extracted from the Keynote deck `02_03_System_Modeling.key` (106 slides, 16:9). This is the source material for rebuilding the lecture as a native HTML deck.

## How to read this

- Positions are approximate boxes in % of the slide, `[left,top → right,bottom]`.
- `[[text|#hex]]` = accent phrase: italic, in that color. `{text|#hex}` = colored (not italic).
- `$...$` is LaTeX. Typeset it with KaTeX (or MathJax) in the same color and roughly the same size as the surrounding text. There are no equation image files.
- Images and videos named in backticks are online, not attached. Use each one by its full address `https://smkatz12.github.io/aa228v-lectures/lectures/02-system-modeling/images/<name>`, for example `<img src="https://smkatz12.github.io/aa228v-lectures/lectures/02-system-modeling/images/val-page-37.svg">`. Don't ask for uploads.
- **Builds** list what appears on each click, in order ("then" = right after the previous step, "with previous" = at the same time).
- **Transition to next: Magic Move** means objects shared with the next slide should glide to their new positions.

## House style

- Same as Lecture 01: black background; white text.
- Spaced all-caps headings in Gill Sans (regular weight, letter-spacing about 0.25em). All other text in Palatino.
- Emphasis is italic + color, never bold.
- Book covers: use `cover-optimization.png`, `cover-decision-making.png`, `cover-validation.png` with a thin light-gray outline.
- The title slide streak is green (`coverart-302-green.png`).
- Graphics are SVGs with transparent backgrounds and white lines/text, made for the black slides; keep them as `<img>` files.
- Handwritten ink from past lectures (slides 1, 32, 45) has been left out on purpose; the deck's own ink layer handles writing.
- Most-used text colors: `#ffffff`, `#80b9ff`, `#abdaf4`, `#000000`, `#ffa4e7`, `#c3b8ff`, `#0072fe`, `#fab0ae`

## Slide 1
- image `coverart-302-green.png` [-0%,46% → 100%,75%]
- heading (spaced caps) 50pt [6%,9% → 82%,22%]: AA228V/CS238V / VALIDATION OF SAFETY-CRITICAL SYSTEMS
- heading (spaced caps) 30pt [4%,73% → 43%,87%]: LECTURE 02/03: SYSTEM MODELING / SYDNEY KATZ (SMKATZ@STANFORD.EDU)

## Slide 2
- image `pasted-image-2226.png` [55%,13% → 87%,70%]
- text on a #fffbb9 filled box 44pt [79%,54% → 85%,60%]: { * * *|#000000}
- text 36pt [6%,32% → 27%,49%]: *In a [[controlled, safe environment|#c3b8ff]] such as a simulation [[instead of the real world|#c3b8ff]]
- image `cover-optimization.png` [61%,75% → 70%,92%]
- image `cover-decision-making.png` [73%,75% → 82%,92%]
- text 24pt [60%,93% → 71%,97%]: AA222/CS361
- text 24pt [74%,93% → 82%,97%]: AA228/CS238
- image `cover-validation.png` (book cover) [38%,29% → 52%,55%]
- text 28pt [38%,57% → 52%,61%]: AA228V/CS238V
- **Builds:** click 1: text 36pt — slides in

## Slide 3
- text 36pt [6%,32% → 27%,49%]: *In a [[controlled, safe environment|#c3b8ff]] such as a simulation [[instead of the real world|#c3b8ff]]
- text 36pt [6%,52% → 26%,57%]: … unlike these people.
- video `video-2279.mp4` (plays 4.2s–9.9s, loops) [67%,34% → 114%,80%]
- black cover-up box (Keynote crop hack; just crop the media instead) [98%,31% → 119%,83%]
- black cover-up box (Keynote crop hack; just crop the media instead) [63%,31% → 83%,82%]
- image `pasted-image-2285.png` (cropped: show only 6–98% across and 4–100% down of the image) [63%,54% → 78%,80%]
- black cover-up box (Keynote crop hack; just crop the media instead) [30%,21% → 60%,24%]
- black cover-up box (Keynote crop hack; just crop the media instead) [30%,48% → 60%,51%]
- video `video-2281.mp4` (plays 15.2s–26.8s, loops) [61%,26% → 81%,46%]
- black cover-up box (Keynote crop hack; just crop the media instead) [62%,24% → 93%,27%]
- black cover-up box (Keynote crop hack; just crop the media instead) [60%,45% → 82%,46%]
- video `elon-musk-test.gif` (plays 0.0s–3.6s, loops) [32%,25% → 58%,47%]
- video `video-2283.mp4` (plays 6.0s–10.4s, loops) [29%,52% → 58%,81%]
- **Builds:** then: video `video-2279.mp4` (plays 4.2s–9.9s, loops) — video starts; with previous: video `video-2281.mp4` (plays 15.2s–26.8s, loops) — video starts; with previous: video `elon-musk-test.gif` (plays 0.0s–3.6s, loops) — video starts; with previous: video `video-2283.mp4` (plays 6.0s–10.4s, loops) — video starts

## Slide 4
- text 36pt [50%,50% → 50%,50%]: We [[don’t|#fab0ae]] want to [[find out|#c3b8ff]] in the [[real world|#80b9ff]]!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 5
- text 36pt [31%,43% → 69%,48%]: We [[don’t|#fab0ae]] want to [[find out|#c3b8ff]] in the [[real world|#80b9ff]]!
- text 36pt [33%,49% → 67%,54%]: We [[do|#80cfb9]] want to [[find out|#c3b8ff]] in [[simulation|#80b9ff]]!
- group [27%,65% → 73%,78%]
  - text 36pt [29%,67% → 71%,76%]: Today, we will discuss ways to [[model|#80b9ff]] systems so that we can [[simulate them|#80b9ff]] for offline validation.
  - line #ffffff [27%,65% → 73%,78%]
- **Builds:** click 1: group — fades up from dark

## Slide 6
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text on a #8dd0f5 filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #8dd0f5 filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- heading (spaced caps) 36pt [18%,30% → 61%,35%]: GENERAL THOUGHTS ON MODELS
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: STEPS FOR BUILDING MODELS
- text on a #8dd0f5 filled box 20pt [21%,53% → 24%,57%]: {A|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 30pt [26%,53% → 99%,57%]: {SELECT A MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,60% → 24%,64%]: {B|#000000}
- heading (spaced caps) 30pt [26%,60% → 99%,64%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,67% → 24%,71%]: {C|#000000}
- heading (spaced caps) 30pt [26%,67% → 99%,71%]: {VALIDATE THE MODEL|#abdaf4}
- **Builds:** click 1: text on a #8dd0f5 filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 2: text on a #8dd0f5 filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 3: text on a #8dd0f5 filled box 20pt — slides in; with previous: heading (spaced caps) 30pt — slides in; click 4: text on a #8dd0f5 filled box 20pt — slides in; with previous: heading (spaced caps) 30pt — slides in; click 5: text on a #8dd0f5 filled box 20pt — slides in; with previous: heading (spaced caps) 30pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 7
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [30%,20% → 70%,25%]: There are many different types of models/simulators.
- text 36pt [29%,27% → 71%,32%]: They don’t even have to be on the computer!
- image `pasted-image-7597.png` [38%,40% → 62%,74%]
- text 36pt [27%,82% → 73%,87%]: We will focus on [[computational models|#80b9ff]] in this class.
- **Builds:** click 1: text 36pt — appears; click 2: image `pasted-image-7597.png` — appears; click 3: text 36pt — appears

## Slide 8
- line #80b9ff [22%,32% → 80%,89%]
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [30%,20% → 70%,25%]: Models vary in complexity.
- vector icon `shape-20641945.svg` [13%,20% → 32%,39%]
- equation $h^\prime = h + \dot h \Delta t$ (65pt, #80b9ff) [42%,54% → 59%,59%]
- equation $\dot h^\prime = \dot h + \ddot h \Delta t$ (65pt, #80b9ff) [42%,62% → 59%,68%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 9
- line #80b9ff [22%,32% → 80%,89%]
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [30%,20% → 70%,25%]: Models vary in complexity.
- vector icon `shape-20641945.svg` [13%,20% → 32%,39%]
- image `pasted-image-7678.png` [31%,40% → 72%,82%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 10
- line #80b9ff [22%,32% → 80%,89%]
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [30%,20% → 70%,25%]: Models vary in complexity.
- vector icon `shape-20641945.svg` [13%,20% → 32%,39%]
- image `pasted-image-7678.png` [63%,42% → 77%,56%]
- group [27%,46% → 36%,54%]
  - equation $h^\prime = h + \dot h \Delta t$ (34pt, #80b9ff) [27%,46% → 36%,49%]
  - equation $\dot h^\prime = \dot h + \ddot h \Delta t$ (34pt, #80b9ff) [27%,51% → 36%,54%]
- arrow #80b9ff [26%,59% → 77%,59%]
- text 30pt [26%,60% → 34%,67%]: {low complexity |#80b9ff}
- text 30pt [68%,60% → 76%,67%]: {high complexity |#80b9ff}
- text 36pt [33%,73% → 67%,81%]: We want to pick the model that is [[just complex enough|#80b9ff]] to capture what matters.
- **Builds:** click 1: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 11
- rounded box (outline) [73%,46% → 93%,62%]
- line #80b9ff [10%,32% → 69%,89%]
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [30%,20% → 70%,25%]: Models vary in complexity.
- vector icon `shape-20641945.svg` [1%,20% → 20%,39%]
- image `pasted-image-7678.png` [51%,42% → 65%,56%]
- group [15%,46% → 24%,54%]
  - equation $h^\prime = h + \dot h \Delta t$ (34pt, #80b9ff) [15%,46% → 24%,49%]
  - equation $\dot h^\prime = \dot h + \ddot h \Delta t$ (34pt, #80b9ff) [15%,51% → 24%,54%]
- arrow #80b9ff [14%,59% → 65%,59%]
- text 30pt [15%,60% → 22%,67%]: {low complexity |#80b9ff}
- text 30pt [56%,60% → 64%,67%]: {high complexity |#80b9ff}
- text 36pt [21%,73% → 55%,81%]: We want to pick the model that is [[just complex enough|#80b9ff]] to capture what matters.
- text 36pt [75%,48% → 92%,60%]: “Everything should be as simple as possible, but not simpler.”
- text 36pt [80%,65% → 94%,70%]: — Albert Einstein
- text 36pt [85%,70% → 91%,74%]: {(maybe)|#80b9ff}
- line #80b9ff [10%,32% → 69%,89%]
- vector icon `shape-20641945.svg` [1%,20% → 20%,39%]
- **Builds:** click 1: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 12
- line #ffffff [10%,32% → 43%,89%]
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [43%,15% → 57%,20%]: Models can be…
- vector icon `shape-89a9a182.svg` [1%,20% → 20%,39%]
- group [18%,54% → 35%,68%]
  - equation $h^\prime = h + \dot h \Delta t$ (65pt, #80b9ff) [18%,54% → 35%,59%]
  - equation $\dot h^\prime = \dot h + \ddot h \Delta t$ (65pt, #80b9ff) [18%,62% → 35%,68%]
- line #ffffff [58%,32% → 90%,89%]
- line #ffffff [48%,20% → 68%,39%]
- text 36pt [23%,26% → 32%,30%]: White Box
- text 36pt [72%,26% → 80%,30%]: Black Box
- text 36pt [49%,59% → 51%,64%]: or
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 13
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [43%,15% → 57%,20%]: Models can be…
- line #ffffff [11%,39% → 30%,73%]
- vector icon `shape-dd2badf0.svg` [5%,32% → 17%,43%]
- group [15%,52% → 26%,60%]
  - equation $h^\prime = h + \dot h \Delta t$ (39pt, #80b9ff) [15%,52% → 26%,55%]
  - equation $\dot h^\prime = \dot h + \ddot h \Delta t$ (39pt, #80b9ff) [15%,57% → 26%,60%]
- line #ffffff [74%,40% → 93%,74%]
- line #ffffff [68%,33% → 80%,44%]
- text 20pt [18%,35% → 26%,38%]: White Box
- text 20pt [83%,37% → 88%,39%]: Black Box
- text 36pt [34%,54% → 36%,58%]: or
- line #a9a9a9 [42%,40% → 61%,74%]
- vector icon `shape-59d255e5.svg` [36%,32% → 48%,44%]
- text 20pt [48%,36% → 57%,39%]: Gray Box
- text 36pt [66%,54% → 69%,59%]: or
- image `pasted-image-7678.png` [44%,49% → 58%,63%]
- black cover-up box (Keynote crop hack; just crop the media instead) [43%,42% → 59%,71%]

## Slide 14
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [7%,16% → 19%,21%]: Key Challenges
- text on a #80b9ff filled box 32pt [10%,25% → 14%,32%]: {1|#000000}
- text 36pt [15%,26% → 21%,31%]: Model needs to be expressive enough to capture [[all possible scenarios|#80b9ff]] the system may encounter.
- vector icon `shape-e6a98bf6.svg` [88%,60% → 96%,96%]
- vector icon `shape-e6a98bf6.svg` [5%,60% → 12%,95%]
- group [48%,37% → 90%,59%]
  - text 28pt [52%,41% → 85%,48%]: How can I capture all possible scenarios my / {<insert crazy complex system here>|#80b9ff} will end up in?
  - text 28pt [52%,49% → 85%,53%]: … I don’t even know what they all are!
  - shape (outline) [48%,37% → 90%,59%]
- group [8%,36% → 40%,58%]
  - shape (outline) [10%,36% → 40%,58%]
  - text 40pt [8%,39% → 40%,45%]: Yeah, it’s a problem. 😬
- text 28pt [14%,45% → 36%,52%]: But there is some hope! Stay tuned for the {runtime monitoring|#80b9ff} chapter.
- **Builds:** click 1: text on a #80b9ff filled box 32pt — slides in; with previous: text 36pt — slides in; click 2: vector icon `shape-e6a98bf6.svg` — apple:move in character; click 3: group — wipes in; click 4: vector icon `shape-e6a98bf6.svg` — apple:move in character; click 5: group — wipes in; click 6: text 28pt — fireworks

## Slide 15
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [7%,16% → 19%,21%]: Key Challenges
- text on a #80b9ff filled box 32pt [10%,25% → 14%,32%]: {1|#000000}
- text 36pt [15%,26% → 21%,31%]: Model needs to be expressive enough to capture [[all possible scenarios|#80b9ff]] the system may encounter.
- text on a #80b9ff filled box 32pt [10%,36% → 14%,43%]: {2|#000000}
- text 36pt [15%,37% → 89%,42%]: Requires data and/or expert knowledge.
- text on a #80b9ff filled box 32pt [10%,47% → 14%,54%]: {3|#000000}
- text 36pt [15%,48% → 46%,53%]: Need to select an objective and optimization technique to find model parameters.
- group [39%,62% → 58%,75%]
  - rounded box (outline) [39%,62% → 58%,75%]
  - text 36pt [39%,64% → 58%,72%]: “All models are wrong, but some are useful.”
- text 36pt [44%,77% → 70%,81%]: — British statistician George Box
- text 36pt [55%,82% → 62%,86%]: {(for real)|#80b9ff}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — slides in; with previous: text 36pt — slides in; click 2: text on a #80b9ff filled box 32pt — slides in; with previous: text 36pt — slides in; click 3: group — fades up from dark; with previous: text 36pt — slides in; click 4: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 16
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text on a #8dd0f5 filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #8dd0f5 filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- heading (spaced caps) 36pt [18%,30% → 61%,35%]: GENERAL THOUGHTS ON MODELS
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: STEPS FOR BUILDING MODELS
- text on a #8dd0f5 filled box 20pt [21%,53% → 24%,57%]: {A|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 30pt [26%,53% → 99%,57%]: {SELECT A MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,60% → 24%,64%]: {B|#000000}
- heading (spaced caps) 30pt [26%,60% → 99%,64%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,67% → 24%,71%]: {C|#000000}
- heading (spaced caps) 30pt [26%,67% → 99%,71%]: {VALIDATE THE MODEL|#abdaf4}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 17
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [29%,12% → 71%,17%]: We are going to focus on creating [[probabilistic|#80b9ff]] models.
- text 36pt [-48%,44% → -0%,56%]: [[The probability of a particular outcome is a number between 0 and 1 that quantifies the likelihood of that outcome occurring, relative to all possible outcomes.|#80b9ff]]
- image `pasted-movie-13104.png` [14%,31% → 47%,100%] (links to https://www.nature.com/articles/d41586-024-04096-5)
- text 100pt [86%,68% → 92%,81%]: 🤔
- text 48pt [56%,47% → 87%,73%]: {“All of statistics and much of science depends on probability — an astonishing achievement, considering no one’s really sure what it is.”|#80b9ff}
- **Builds:** click 1: image `pasted-movie-13104.png` — appears; click 2: text 48pt — slides in; click 3: text 100pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 18
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [29%,12% → 71%,17%]: We are going to focus on creating [[probabilistic|#80b9ff]] models.
- text 36pt [26%,42% → 74%,58%]: [[The probability of a particular outcome is a number between zero and one that quantifies the likelihood of that outcome occurring, relative to all possible outcomes.|#80b9ff]]
- image `pasted-movie-13104.png` [14%,103% → 47%,172%] (links to https://www.nature.com/articles/d41586-024-04096-5)
- text 100pt [86%,140% → 92%,153%]: 🤔
- text 48pt [56%,119% → 87%,145%]: {“All of statistics and much of science depends on probability — an astonishing achievement, considering no one’s really sure what it is.”|#80b9ff}
- **Builds:** then: text 100pt — appears

## Slide 19
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [24%,46% → 76%,54%]: A common type of model class is a [[probability distribution|#80b9ff]], which is a function that assigns probabilities to different outcomes.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 20
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [24%,11% → 76%,20%]: A common type of model class is a [[probability distribution|#80b9ff]], which is a function that assigns probabilities to different outcomes.
- image `test-8341.svg` [15%,33% → 34%,61%]
- text 36pt [19%,24% → 36%,29%]: Discrete Distributions
- text 36pt [58%,24% → 75%,29%]: Continuous Distributions
- text 36pt [25%,63% → 29%,68%]: Probability Mass Function $P(x)$
- text 36pt [57%,63% → 77%,68%]: Probability Density Function $p(x)$
- equation $\sum_x P(x) = 1$ (36pt, #ffffff) [22%,78% → 31%,85%]
- equation $0 \leq P(x) \leq 1$ (36pt, #ffffff) [22%,71% → 31%,74%]
- equation $\int_{-\infty}^{\infty} p(x) d x = 1$ (36pt, #ffffff) [61%,78% → 72%,86%]
- equation $p(x) \geq 0$ (36pt, #ffffff) [64%,71% → 70%,74%]
- image `test-8461.svg` [60%,30% → 74%,60%]
- **Builds:** click 1: text 36pt — appears; click 2: text 36pt — appears; click 3: equation $0 \leq P(x) \leq 1$ — appears; click 4: equation $p(x) \geq 0$ — appears; click 5: equation $\sum_x P(x) = 1$ — appears; click 6: equation $\int_{-\infty}^{\infty} p(x) d x = 1$ — appears

## Slide 21
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [50%,50% → 50%,50%]: We often represent probability distributions using a set of [[parameters|#80b9ff]] $\theta$.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 22
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [23%,20% → 77%,24%]: We often represent probability distributions using a set of [[parameters|#80b9ff]] $\theta$.
- image `test-8495.svg` [52%,29% → 78%,80%]
- equation $\theta = [\mu, \sigma]$ (47pt, #80b9ff) [76%,78% → 85%,82%]
- arrow #80b9ff [70%,72% → 75%,79%]
- arrow #80b9ff [66%,73% → 75%,79%]
- image `test-8658.svg` [15%,37% → 43%,80%]

## Slide 23
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [32%,33% → 68%,38%]: [[Main consideration|#80b9ff]] when selecting a model class:
- text 36pt [37%,39% → 63%,44%]: It needs to be “[[expressive enough|#80b9ff]].”
- text 36pt [15%,52% → 85%,57%]: i.e. there is some setting of the model parameters for which the model will fit the data well
- text on a #80b9ff filled box 32pt [40%,67% → 60%,76%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text 36pt — appears; click 2: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 24
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #80b9ff filled box 32pt [40%,11% → 60%,19%]: {Pluto Notebook!|#000000}
- text 36pt [62%,13% → 69%,18%]: Summary
- video `video-8673.mp4` (plays 0.0s–7.6s, loops) [16%,24% → 38%,53%]
- text 36pt [43%,33% → 75%,45%]: If a simple distribution does not fit the data well for any setting of its parameters, we need a [[more complex|#80b9ff]] model class.
- video `video-8731.mp4` (plays 0.0s–20.1s, loops) [16%,56% → 38%,90%]
- text 36pt [43%,67% → 75%,79%]: One way to create more complex distributions is to used a [[weighted mixture|#80b9ff]] of simpler distributions.
- text 36pt [-91%,26% → -2%,30%]: Another way to create a more complex model class is by applying a [[functional transformation|#80b9ff]] to a simple distribution.
- **Builds:** click 1: video `video-8731.mp4` (plays 0.0s–20.1s, loops) — appears; with previous: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 25
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #80b9ff filled box 32pt [40%,11% → 60%,19%]: {Pluto Notebook!|#000000}
- text 36pt [62%,13% → 69%,18%]: Summary
- video `video-8673.mp4` (plays 0.0s–7.6s, loops) [105%,24% → 127%,53%]
- text 36pt [132%,33% → 164%,45%]: If a simple distribution does not fit the data well for any setting of its parameters, we need a [[more complex|#80b9ff]] model class.
- video `video-8731.mp4` (plays 0.0s–20.1s, loops) [105%,56% → 127%,90%]
- text 36pt [132%,67% → 164%,79%]: One way to create more complex distributions is to used a [[weighted mixture|#80b9ff]] of simpler distributions.
- text 36pt [48%,26% → 52%,30%]: Another way to create a more complex model class is by applying a [[functional transformation|#80b9ff]] to a simple distribution.
- image `test-8807.svg` [30%,49% → 70%,82%]
- equation $Z \sim p_z(\cdot)$ (36pt, #80b9ff) [34%,41% → 41%,44%]
- equation $X \sim p_x(\cdot)$ (36pt, #c3b8ff) [58%,41% → 65%,44%]
- arrow #ffffff [44%,43% → 56%,43%]
- equation $x = f(z)$ (36pt, #ffffff) [47%,38% → 53%,41%]
- line #ffffff [4%,33% → 96%,33%]
- **Builds:** click 1: equation $Z \sim p_z(\cdot)$ — appears; with previous: equation $x = f(z)$ — appears; with previous: arrow #ffffff — appears; with previous: equation $X \sim p_x(\cdot)$ — appears; with previous: image `test-8807.svg` — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 26
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #80b9ff filled box 32pt [40%,11% → 60%,19%]: {Pluto Notebook!|#000000}
- text 36pt [62%,13% → 69%,18%]: Summary
- text 36pt [48%,26% → 52%,30%]: Another way to create a more complex model class is by applying a [[functional transformation|#80b9ff]] to a simple distribution.
- equation $p_x(X) = p_z(g(x))|g^\prime(x)|$ (36pt, #ffffff) [64%,42% → 82%,45%]
- line #ffffff [63%,39% → 83%,48%]
- image `test-8807.svg` [10%,49% → 49%,82%]
- equation $Z \sim p_z(\cdot)$ (36pt, #80b9ff) [14%,41% → 21%,44%]
- equation $X \sim p_x(\cdot)$ (36pt, #c3b8ff) [38%,41% → 45%,44%]
- arrow #ffffff [24%,43% → 35%,43%]
- equation $x = f(z)$ (36pt, #ffffff) [27%,38% → 33%,41%]
- text on a #f3cf80 filled box 26pt [60%,54% → 86%,63%]: {Note:|#000000}{ This formula requires $f$ to be differentiable and invertible!|#000000}
- text 36pt [56%,68% → 90%,84%]: We can still apply a functional transformation that is not differentiable and invertible! We just won’t be able to calculate the resulting PDF.
- line #ffffff [4%,33% → 96%,33%]
- **Builds:** click 1: text on a #f3cf80 filled box 26pt — appears; click 2: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 27
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #80b9ff filled box 32pt [40%,11% → 60%,19%]: {Pluto Notebook!|#000000}
- text 36pt [62%,13% → 69%,18%]: Summary
- text 36pt [48%,26% → 52%,30%]: Another way to create a more complex model class is by applying a [[functional transformation|#80b9ff]] to a simple distribution.
- text 36pt [5%,41% → 39%,56%]: We can still apply a functional transformation that is not differentiable and invertible! We just won’t be able to calculate the resulting PDF.
- image `test-8963.svg` [45%,35% → 86%,63%]
- text 36pt [40%,71% → 65%,79%]: {samples from a pseudorandom number generator|#80b9ff}
- arrow #80b9ff [52%,65% → 52%,70%]
- text 36pt [67%,72% → 92%,77%]: {transformed samples|#c3b8ff}
- arrow #c3b8ff [79%,64% → 79%,70%]
- text on a #ffa4e7 filled box 26pt [9%,67% → 35%,76%]: {We call models represented in this way |#000000}[[generative models|#000000]]{.|#000000}
- line #ffffff [4%,33% → 96%,33%]
- text 24pt [16%,79% → 34%,91%]: {To throw in some buzz words:|#ffa4e7} / {Generative adversarial networks (GANs), variational autoencoders (VAEs), diffusion models, etc.|#ffa4e7}
- image `noun-bee-5600972-ffd65b.png` [8%,78% → 16%,92%]
- **Builds:** click 1: image `test-8963.svg` — slides in; click 2: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 3: text 36pt — fades up from dark; with previous: arrow #c3b8ff — draws in; click 4: text on a #ffa4e7 filled box 26pt — appears; click 5: text 24pt — slides in; with previous: image `noun-bee-5600972-ffd65b.png` — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 28
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #80b9ff filled box 32pt [40%,11% → 60%,19%]: {Pluto Notebook!|#000000}
- text 36pt [62%,13% → 69%,18%]: Summary
- text 36pt [48%,26% → 52%,30%]: Another way to create a more complex model class is by applying a [[functional transformation|#80b9ff]] to a simple distribution.
- text 36pt [5%,41% → 39%,56%]: We can still apply a functional transformation that is not differentiable and invertible! We just won’t be able to calculate the resulting PDF.
- image `test-8963.svg` [45%,106% → 86%,133%]
- text 36pt [40%,141% → 65%,149%]: {samples from a pseudorandom number generator|#80b9ff}
- arrow #80b9ff [52%,135% → 52%,141%]
- text 36pt [67%,142% → 92%,147%]: {transformed samples|#c3b8ff}
- arrow #c3b8ff [79%,135% → 79%,140%]
- text on a #ffa4e7 filled box 26pt [9%,67% → 35%,76%]: {We call models represented in this way |#000000}[[generative models|#000000]]{.|#000000}
- line #ffffff [4%,33% → 96%,33%]
- text 24pt [16%,79% → 34%,91%]: {To throw in some buzz words:|#ffa4e7} / {Generative adversarial networks (GANs), variational autoencoders (VAEs), diffusion models, etc.|#ffa4e7}
- image `noun-bee-5600972-ffd65b.png` [8%,78% → 16%,92%]
- image `test-9116.svg` [43%,53% → 53%,72%]
- text on a #ffa4e7 filled box 22pt [58%,60% → 73%,69%]: {$f(x) =$neural network|#000000}
- arrow #ffffff [74%,64% → 77%,64%]
- arrow #ffffff [54%,64% → 58%,64%]
- image `pasted-image-9149.png` [78%,50% → 93%,77%]
- text 18pt [79%,78% → 92%,81%]: Credit: https://ajolicoeur.ca/cats/
- **Builds:** click 1: image `test-9116.svg` — appears; click 2: arrow #ffffff — draws in; then: text on a #ffa4e7 filled box 22pt — appears; click 3: arrow #ffffff — draws in; then: image `pasted-image-9149.png` — appears; with previous: text 18pt — appears

## Slide 29
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [50%,50% → 50%,50%]: If we have [[multiple variables|#80b9ff]] involved, we are interested in [[joint|#80b9ff]] or [[conditional|#80b9ff]] distributions.

## Slide 30
- rounded box (outline) [22%,27% → 78%,37%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [26%,14% → 74%,18%]: [[joint distribution|#80b9ff]]{:|#80b9ff} probability distribution over multiple variables.
- text 36pt [41%,19% → 59%,23%]: [[(multivariate distribution)|#80b9ff]]
- text 36pt [23%,30% → 77%,34%]: {represents the likelihood of|#000000} [[multiple outcomes|#0072fe]] {occurring|#000000} [[simultaneously|#0072fe]]
- text 36pt [19%,46% → 32%,51%]: Discrete: $P(x, y)$
- group [19%,60% → 32%,84%]
  - equation $x$ (36pt, #80b9ff) [20%,62% → 21%,63%]
  - equation $y$ (36pt, #80b9ff) [23%,61% → 24%,63%]
  - equation $P(x, y)$ (36pt, #80b9ff) [27%,61% → 31%,64%]
  - line #ffffff [19%,65% → 32%,65%]
  - equation $1$ (36pt, #80b9ff) [20%,75% → 21%,78%]
  - equation $0$ (36pt, #80b9ff) [20%,67% → 21%,69%]
  - equation $0$ (36pt, #80b9ff) [20%,71% → 21%,73%]
  - equation $1$ (36pt, #80b9ff) [20%,79% → 21%,82%]
  - equation $0$ (36pt, #80b9ff) [23%,67% → 24%,69%]
  - equation $0$ (36pt, #80b9ff) [23%,75% → 24%,78%]
  - equation $1$ (36pt, #80b9ff) [24%,71% → 24%,73%]
  - equation $1$ (36pt, #80b9ff) [24%,80% → 24%,82%]
  - equation $0.1$ (36pt, #80b9ff) [29%,67% → 31%,69%]
  - equation $0.2$ (36pt, #80b9ff) [29%,71% → 31%,74%]
  - equation $0.5$ (36pt, #80b9ff) [29%,75% → 31%,78%]
  - equation $0.2$ (36pt, #80b9ff) [29%,80% → 31%,82%]
  - line #ffffff [19%,84% → 32%,84%]
  - line #ffffff [19%,60% → 32%,60%]
- text 36pt [55%,46% → 70%,51%]: Continuous: $p(x, y)$
- text 30pt [24%,53% → 28%,57%]: {e.g. table representation|#80b9ff}
- text 30pt [54%,53% → 70%,57%]: {e.g. multivariate Gaussian|#80b9ff}
- image `test-9407.svg` [43%,69% → 54%,89%]
- image `test-9413.svg` [57%,69% → 68%,89%]
- image `test-9418.svg` [71%,69% → 82%,89%]
- vector icon `shape-e1119cb8.svg` [48%,79% → 49%,80%]
- equation $\mu$ (33pt, #ffffff) [49%,80% → 50%,82%]
- vector icon `shape-e1119cb8.svg` [62%,79% → 63%,80%]
- equation $\mu$ (33pt, #ffffff) [63%,80% → 63%,82%]
- vector icon `shape-e1119cb8.svg` [76%,79% → 76%,80%]
- equation $\mu$ (33pt, #ffffff) [77%,80% → 77%,82%]
- equation $\Sigma = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ (26pt, #ffffff) [44%,60% → 50%,66%]
- equation $\Sigma = \begin{bmatrix} 1 & 0.5 \\ 0.5 & 1 \end{bmatrix}$ (26pt, #ffffff) [58%,60% → 66%,66%]
- equation $\Sigma = \begin{bmatrix} 1 & -0.8 \\ -0.8 & 1 \end{bmatrix}$ (26pt, #ffffff) [71%,60% → 81%,66%]
- text on a #80b9ff filled box 32pt [73%,47% → 92%,55%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text 36pt — appears; click 2: text 30pt — slides in; with previous: group — slides in; click 3: text 36pt — appears; click 4: text 30pt — slides in; with previous: image `test-9407.svg` — slides in; with previous: image `test-9413.svg` — slides in; with previous: image `test-9418.svg` — slides in; click 5: equation $\mu$ — appears; with previous: equation $\mu$ — appears; with previous: equation $\mu$ — appears; with previous: vector icon `shape-e1119cb8.svg` — appears; with previous: vector icon `shape-e1119cb8.svg` — appears; with previous: vector icon `shape-e1119cb8.svg` — appears; click 6: equation $\Sigma = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ — appears; with previous: equation $\Sigma = \begin{bmatrix} 1 & 0.5 \\ 0.5 & 1 \end{bmatrix}$ — appears; with previous: equation $\Sigma = \begin{bmatrix} 1 & -0.8 \\ -0.8 & 1 \end{bmatrix}$ — appears; click 7: text on a #80b9ff filled box 32pt — appears

## Slide 31
- rounded box (outline) [22%,27% → 78%,37%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [26%,14% → 74%,18%]: [[joint distribution|#80b9ff]]{:|#80b9ff} probability distribution over multiple variables.
- text 36pt [41%,19% → 59%,23%]: [[(multivariate distribution)|#80b9ff]]
- text 36pt [23%,30% → 77%,34%]: {represents the likelihood of|#000000} [[multiple outcomes|#0072fe]] {occurring|#000000} [[simultaneously|#0072fe]]
- text on a #f3cf80 filled box 26pt [31%,43% → 69%,54%]: {Note: |#000000}{If two variables are |#000000}[[independent|#000000]]{, then $P(x, y) = P(x)P(y)$. Otherwise, this is not the case.|#000000}
- **Builds:** click 1: text on a #f3cf80 filled box 26pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 32
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text on a #f3cf80 filled box 26pt [4%,16% → 43%,27%]: {Note: |#000000}{If two variables are |#000000}[[independent|#000000]]{, then $P(x, y) = P(x)P(y)$. Otherwise, this is not the case.|#000000}
- text 36pt [52%,17% → 92%,26%]: [[Fun aside:|#80b9ff]] what is the probability that four textbook authors have 0, 0, 4, and 5 wisdom teeth?
- vector icon `shape-e12516a3.svg` [47%,18% → 50%,25%]
- text on a #80b9ff filled box 32pt [39%,79% → 58%,87%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — appears

## Slide 33
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [26%,14% → 74%,18%]: [[conditional|#80b9ff]] [[distribution|#80b9ff]]{:|#80b9ff} distribution over a variable given one or more other variables
- equation $P(y \mid x) = \frac{P(y, x)}{P(x)}$ (51pt, #ffffff) [41%,23% → 59%,34%]
- text 36pt [31%,46% → 45%,51%]: Discrete: $P(y \mid x)$
- group [31%,60% → 44%,84%]
  - equation $x$ (36pt, #80b9ff) [32%,62% → 33%,64%]
  - equation $y$ (36pt, #80b9ff) [35%,62% → 36%,64%]
  - equation $P(y \mid x)$ (36pt, #80b9ff) [39%,62% → 44%,65%]
  - line #ffffff [31%,66% → 44%,66%]
  - equation $1$ (36pt, #80b9ff) [32%,76% → 33%,78%]
  - equation $0$ (36pt, #80b9ff) [32%,68% → 33%,70%]
  - equation $0$ (36pt, #80b9ff) [32%,72% → 33%,74%]
  - equation $1$ (36pt, #80b9ff) [32%,80% → 33%,82%]
  - equation $0$ (36pt, #80b9ff) [35%,68% → 36%,70%]
  - equation $0$ (36pt, #80b9ff) [35%,76% → 36%,78%]
  - equation $1$ (36pt, #80b9ff) [36%,72% → 36%,74%]
  - equation $1$ (36pt, #80b9ff) [36%,80% → 36%,82%]
  - equation $0.1$ (36pt, #80b9ff) [41%,68% → 43%,70%]
  - equation $?$ (36pt, #f3cf80) [42%,72% → 42%,74%]
  - equation $0.5$ (36pt, #80b9ff) [41%,76% → 43%,79%]
  - equation $?$ (36pt, #f3cf80) [42%,80% → 42%,83%]
  - line #ffffff [31%,84% → 44%,84%]
  - line #ffffff [31%,60% → 44%,60%]
- text 30pt [30%,53% → 46%,57%]: {e.g. table representation|#80b9ff}
- text 36pt [61%,46% → 76%,50%]: Continuous: $p(y \mid x)$
- text 30pt [61%,53% → 77%,57%]: {e.g. conditional Gaussian|#80b9ff}
- image `test-9620.svg` [60%,66% → 76%,94%]
- equation $p(y \mid x) = \mathcal N(y \mid x, \sigma^2)$ (38pt, #80b9ff) [60%,59% → 77%,63%]
- **Builds:** click 1: text 36pt — appears; click 2: text 30pt — slides in; with previous: group — slides in; click 3: text 36pt — appears; click 4: text 30pt — slides in; with previous: equation $p(y \mid x) = \mathcal N(y \mid x, \sigma^2)$ — slides in; with previous: image `test-9620.svg` — slides in

## Slide 34
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT A MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 27%,7%]
- line #ffffff [27%,0% → 27%,7%]
- text 36pt [40%,141% → 65%,149%]: {samples from a pseudorandom number generator|#80b9ff}
- arrow #80b9ff [52%,135% → 52%,141%]
- text 36pt [67%,142% → 92%,147%]: {transformed samples|#c3b8ff}
- arrow #c3b8ff [79%,135% → 79%,140%]
- text 36pt [26%,14% → 74%,18%]: [[conditional|#80b9ff]] [[distribution|#80b9ff]]{:|#80b9ff} distribution over a variable given one or more other variables
- text on a #f3cf80 filled box 26pt [34%,23% → 66%,33%]: {Note: |#000000}{the distributions we want to model for the system are conditional distributions!|#000000}
- group [25%,43% → 75%,86%]
  - group [60%,62% → 67%,78%]
    - equation $s$ (35pt, #80b9ff) [66%,69% → 67%,71%]
    - arrow #80b9ff [60%,62% → 65%,78%]
  - text 24pt [33%,44% → 37%,48%]: {Agent|#80b9ff}
  - rounded box (outline) [25%,43% → 44%,62%]
  - rounded box (outline) [40%,67% → 60%,86%]
  - rounded box (outline) [56%,43% → 75%,62%]
  - equation $\pi (a \mid o)$ (42pt, #80b9ff) [31%,51% → 38%,55%]
  - group [33%,62% → 40%,78%]
    - equation $o$ (35pt, #80b9ff) [33%,69% → 34%,71%]
    - line #80b9ff [35%,62% → 40%,78%]
  - group [45%,50% → 55%,53%]
    - arrow #80b9ff [45%,53% → 55%,53%]
    - equation $a$ (35pt, #80b9ff) [50%,50% → 50%,51%]
  - line #80b9ff [31%,47% → 38%,47%]
  - text 24pt [62%,44% → 69%,48%]: {Environment|#80b9ff}
  - equation $T(s^\prime \mid s , a)$ (42pt, #80b9ff) [61%,51% → 69%,55%]
  - line #80b9ff [62%,47% → 69%,47%]
  - text 24pt [48%,68% → 52%,71%]: {Sensor|#80b9ff}
  - equation $O(o \mid s)$ (42pt, #80b9ff) [47%,75% → 53%,78%]
  - line #80b9ff [46%,71% → 54%,71%]

## Slide 35
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text on a #8dd0f5 filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #8dd0f5 filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- heading (spaced caps) 36pt [18%,30% → 61%,35%]: GENERAL THOUGHTS ON MODELS
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: STEPS FOR BUILDING MODELS
- text on a #8dd0f5 filled box 20pt [21%,53% → 24%,57%]: {A|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 30pt [26%,53% → 99%,57%]: {SELECT A MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,60% → 24%,64%]: {B|#000000}
- heading (spaced caps) 30pt [26%,60% → 99%,64%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,67% → 24%,71%]: {C|#000000}
- heading (spaced caps) 30pt [26%,67% → 99%,71%]: {VALIDATE THE MODEL|#abdaf4}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 36
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- video `video-8731.mp4` (plays 0.0s–20.1s, loops) [32%,27% → 72%,89%]
- text 36pt [50%,17% → 54%,22%]: We want to [[automatically|#80b9ff]] do this:
- line #80b9ff [32%,28% → 58%,43%]
- text 36pt [59%,33% → 69%,38%]: {Parameters $\theta$|#80b9ff}
- text 36pt [60%,63% → 68%,68%]: {Dataset $D$|#80b9ff}
- **Builds:** click 1: text 36pt — appears; with previous: video `video-8731.mp4` (plays 0.0s–20.1s, loops) — appears; click 2: line #80b9ff — fades up from dark; with previous: text 36pt — fades up from dark; click 3: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 37
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- video `video-8731.mp4` (plays 0.0s–20.1s, loops) [7%,27% → 48%,89%]
- text 36pt [15%,17% → 40%,22%]: We want to [[automatically|#80b9ff]] do this:
- line #80b9ff [7%,28% → 33%,43%]
- text 36pt [34%,33% → 44%,38%]: {Parameters $\theta$|#80b9ff}
- text 36pt [35%,63% → 43%,68%]: {Dataset $D$|#80b9ff}
- text 36pt [59%,46% → 85%,54%]: How do we know which parameters are the best?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 38
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- video `video-8731.mp4` (plays 0.0s–20.1s, loops) [7%,27% → 48%,89%]
- text 36pt [15%,17% → 40%,22%]: We want to [[automatically|#80b9ff]] do this:
- line #80b9ff [7%,28% → 33%,43%]
- text 36pt [34%,33% → 44%,38%]: {Parameters $\theta$|#80b9ff}
- text 36pt [35%,63% → 43%,68%]: {Dataset $D$|#80b9ff}
- text 36pt [59%,41% → 85%,50%]: How do we know which parameters are the best?
- text 36pt [60%,52% → 83%,60%]: [[We look for the ones that make the data most likely.|#80b9ff]]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 39
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [37%,15% → 63%,23%]: How do we know which parameters are the best?
- text 36pt [39%,26% → 61%,34%]: [[We look for the ones that make the data most likely.|#80b9ff]]
- equation $\hat \theta = \operatorname{argmax}_\theta P(D \mid \theta)$ (36pt, #ffffff) [42%,39% → 58%,43%]
- line #80b9ff [41%,37% → 59%,46%]
- equation $D$ (36pt, #ffffff) [54%,40% → 55%,42%]
- text 36pt [50%,49% → 70%,57%]: {probability of the data set given the parameters|#80b9ff}
- arrow #80b9ff [57%,43% → 59%,48%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 40
- rounded box (outline) [6%,63% → 41%,94%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [37%,15% → 63%,23%]: How do we know which parameters are the best?
- text 36pt [39%,26% → 61%,34%]: [[We look for the ones that make the data most likely.|#80b9ff]]
- equation $\hat \theta = \operatorname{argmax}_\theta P(D \mid \theta)$ (36pt, #ffffff) [42%,39% → 58%,43%]
- text 36pt [50%,49% → 70%,57%]: {probability of the data set given the parameters|#80b9ff}
- arrow #80b9ff [57%,43% → 59%,48%]
- equation $D$ (36pt, #ffffff) [15%,52% → 17%,54%]
- equation $= \{o_1, o_2, \ldots, o_m\}$ (36pt, #ffffff) [17%,52% → 30%,55%]
- equation $P(D \mid \theta) = P(o_1 \mid \theta)P(o_2 \mid \theta) \cdots P(o_m \mid \theta)$ (36pt, #000000) [9%,77% → 39%,80%]
- equation $= o_{1:m}$ (36pt, #ffffff) [17%,57% → 22%,59%]
- equation $= \prod_{i=1}^m P(o_i \mid \theta)$ (36pt, #000000) [16%,82% → 26%,91%]
- shape (outline) [47%,76% → 53%,83%]
- text 24pt [43%,68% → 57%,74%]: {take logarithm for better numerical stability|#80b9ff}
- equation $\log P(D \mid \theta) = \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [65%,61% → 87%,70%]
- shape (outline) [75%,73% → 79%,82%]
- text 24pt [80%,72% → 94%,80%]: {maximizing the log will have the same solution for $\theta$ as the original|#80b9ff}
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [66%,85% → 87%,94%]
- text 32pt [8%,65% → 37%,73%]: {Assume the datapoints in $D$ are independent and identically distributed.|#000000}
- line #80b9ff [41%,37% → 59%,46%]
- **Builds:** click 1: equation $= o_{1:m}$ — slides in; click 2: rounded box (outline) — fades up from dark; with previous: text 32pt — fades up from dark; click 3: equation $P(D \mid \theta) = P(o_1 \mid \theta)P(o_2 \mid \theta) \cdots P(o_m \mid \theta)$ — appears; click 4: equation $= \prod_{i=1}^m P(o_i \mid \theta)$ — slides in; click 5: text 24pt — wipes in; with previous: shape (outline) — wipes in; then: equation $\log P(D \mid \theta) = \sum_{i=1}^m \log P(o_i \mid \theta)$ — appears; click 6: shape (outline) — wipes in; with previous: text 24pt — wipes in; then: equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 41
- rounded box (outline) [6%,63% → 41%,94%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [37%,15% → 63%,23%]: How do we know which parameters are the best?
- text 36pt [39%,26% → 61%,34%]: [[We look for the ones that make the data most likely.|#80b9ff]]
- equation $\hat \theta = \operatorname{argmax}_\theta P(D \mid \theta)$ (36pt, #ffffff) [42%,39% → 58%,43%]
- text 36pt [50%,49% → 70%,57%]: {probability of the data set given the parameters|#80b9ff}
- arrow #80b9ff [57%,43% → 59%,48%]
- equation $D$ (36pt, #ffffff) [15%,52% → 17%,54%]
- equation $= \{o_1, o_2, \ldots, o_m\}$ (36pt, #ffffff) [17%,52% → 30%,55%]
- equation $= o_{1:m}$ (36pt, #ffffff) [17%,57% → 22%,59%]
- shape (outline) [47%,76% → 53%,83%]
- text 24pt [43%,68% → 57%,74%]: {take logarithm for better numerical stability|#80b9ff}
- equation $\log P(D \mid \theta) = \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [65%,61% → 87%,70%]
- shape (outline) [75%,73% → 79%,82%]
- text 24pt [80%,72% → 94%,80%]: {maximizing the log will have the same solution for $\theta$ as the original|#80b9ff}
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [66%,85% → 87%,94%]
- line #80b9ff [64%,84% → 88%,96%]
- equation $P(D \mid \theta) = P(o_1 \mid \theta)P(o_2 \mid \theta) \cdots P(o_m \mid \theta)$ (36pt, #000000) [9%,77% → 39%,80%]
- equation $= \prod_{i=1}^m P(o_i \mid \theta)$ (36pt, #000000) [16%,82% → 26%,91%]
- text 32pt [8%,65% → 37%,73%]: {Assume the datapoints in $D$ are independent and identically distributed.|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 42
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- equation $\hat \theta = \operatorname{argmax}_\theta P(D \mid \theta)$ (36pt, #ffffff) [42%,44% → 58%,47%]
- line #80b9ff [40%,60% → 64%,71%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [42%,61% → 63%,70%]
- text on a #ffa4e7 filled box 36pt [28%,26% → 72%,35%]: {Maximum Likelihood Parameter Estimation|#000000}
- equation $\hat \theta = \operatorname{argmax}_\theta \prod_{i=1}^m P(o_i \mid \theta)$ (36pt, #ffffff) [42%,49% → 60%,58%]
- text 36pt [20%,83% → 55%,88%]: A silly way to solve this optimization problem:
- text on a #80b9ff filled box 32pt [57%,81% → 76%,89%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — appears; with previous: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 43
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [41%,15% → 79%,19%]: A better way to solve this optimization problem:
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [47%,19% → 73%,24%]: [[give it to an optimization algorithm!|#80b9ff]]
- text 36pt [44%,51% → 56%,60%]: Optimization Algorithm
- line #ffffff [42%,45% → 58%,66%]
- text 36pt [25%,49% → 32%,53%]: Objective
- text 36pt [23%,58% → 32%,62%]: Parameters
- arrow #ffffff [58%,56% → 65%,56%]
- arrow #ffffff [34%,51% → 42%,51%]
- text 36pt [65%,53% → 81%,58%]: Optimal Parameters
- arrow #ffffff [34%,61% → 42%,61%]
- text 24pt [21%,80% → 41%,88%]: {To throw in some more buzz words:|#ffa4e7} / {gradient descent, ADAM, genetic algorithms, momentum, etc.|#ffa4e7}
- image `noun-bee-5600972-ffd65b.png` [13%,77% → 20%,91%]
- text on a #ffa4e7 filled box 36pt [43%,79% → 87%,89%]: {We will talk a bit more about these in Chapter 4.|#000000} / {Take AA222/CS361 for the full story!|#000000}
- **Builds:** click 1: image `noun-bee-5600972-ffd65b.png` — appears; with previous: text 24pt — appears; click 2: text on a #ffa4e7 filled box 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 44
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [41%,15% → 79%,19%]: A better way to solve this optimization problem:
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [47%,19% → 73%,24%]: [[give it to an optimization algorithm!|#80b9ff]]
- text 36pt [44%,38% → 56%,46%]: Optimization Algorithm
- line #ffffff [42%,31% → 58%,52%]
- text 36pt [25%,35% → 32%,39%]: Objective
- text 36pt [23%,44% → 32%,48%]: Parameters
- arrow #ffffff [58%,42% → 65%,42%]
- arrow #ffffff [34%,37% → 42%,37%]
- text 36pt [65%,39% → 81%,44%]: Optimal Parameters
- arrow #ffffff [34%,47% → 42%,47%]
- image `val-page-29.svg` (cropped: show only 11–70% across and 70–85% down of the image) [22%,60% → 78%,88%]
- text on a #80b9ff filled box 32pt [67%,58% → 86%,66%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — appears

## Slide 45
- rounded box (outline) [46%,18% → 81%,27%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [39%,11% → 85%,15%]: This optimization problem leads to many common loss functions!
- image `noun-seat-belt-7368374-80b9ff.png` [47%,18% → 52%,27%]
- text 32pt [53%,19% → 80%,26%]: {Buckle up because I am about to show you my favorite derivation EVER.|#80b9ff}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 46
- rounded box (outline) [46%,18% → 81%,27%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [39%,11% → 85%,15%]: This optimization problem leads to many common loss functions!
- image `noun-seat-belt-7368374-80b9ff.png` [47%,18% → 52%,27%]
- text 32pt [53%,19% → 80%,26%]: {Buckle up because I am about to show you my favorite derivation EVER.|#80b9ff}
- image `val-page-29.svg` (cropped: show only 17–66% across and 25–55% down of the image) [31%,38% → 67%,83%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 47
- rounded box (outline) [46%,18% → 81%,27%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [39%,11% → 85%,15%]: This optimization problem leads to many common loss functions!
- image `noun-seat-belt-7368374-80b9ff.png` [47%,18% → 52%,27%]
- text 32pt [53%,19% → 80%,26%]: {Buckle up because I am about to show you my favorite derivation EVER.|#80b9ff}
- image `val-page-29.svg` (cropped: show only 17–66% across and 25–55% down of the image) [11%,38% → 47%,83%]
- text on a #ffa4e7 filled box 36pt [55%,56% → 84%,65%]: {Sometimes we can keep going and get an analytical solution!|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 48
- rounded box (outline) [46%,18% → 81%,27%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [39%,11% → 85%,15%]: This optimization problem leads to many common loss functions!
- image `noun-seat-belt-7368374-80b9ff.png` [47%,18% → 52%,27%]
- text 32pt [53%,19% → 80%,26%]: {Buckle up because I am about to show you my favorite derivation EVER.|#80b9ff}
- image `val-page-29.svg` (cropped: show only 17–66% across and 25–55% down of the image) [11%,38% → 47%,83%]
- text on a #ffa4e7 filled box 36pt [55%,49% → 84%,58%]: {Sometimes we can keep going and get an analytical solution!|#000000}
- rounded box (outline) [56%,61% → 83%,72%]
- text 36pt [58%,62% → 81%,71%]: {Example 2.9 in textbook - try it if you want |#000000}{extra|#0072fe} {practice|#0072fe}{!|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 49
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [5%,14% → 29%,24%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [7%,14% → 28%,23%]
- text 36pt [17%,46% → 83%,54%]: We can also derive analytical solutions for the parameters of a [[Gaussian distribution|#80b9ff]] and a [[Bernoulli distribution|#80b9ff]] (and many others!).
- arrow #ffffff [73%,38% → 73%,45%]
- rounded box (outline) [60%,25% → 87%,36%]
- text 36pt [62%,26% → 85%,35%]: {Example 2.8 in textbook - try it if you want |#000000}{extra|#0072fe} {practice|#0072fe}{!|#000000}
- arrow #ffffff [44%,55% → 44%,62%]
- rounded box (outline) [31%,63% → 57%,74%]
- text 36pt [33%,65% → 56%,73%]: {Example 2.7 in textbook - try it if you want |#000000}{extra|#0072fe} {practice|#0072fe}{!|#000000}
- **Builds:** click 1: arrow #ffffff — draws in; with previous: text 36pt — fades up from dark; with previous: rounded box (outline) — fades up from dark; click 2: arrow #ffffff — draws in; with previous: text 36pt — fades up from dark; with previous: rounded box (outline) — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 50
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [38%,52% → 62%,63%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [40%,53% → 61%,62%]
- text 36pt [31%,45% → 69%,49%]: That’s [[maximum likelihood|#80b9ff]] parameter learning!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 51
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- line #80b9ff [107%,52% → 130%,63%]
- equation $\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$ (36pt, #ffffff) [108%,53% → 129%,62%]
- text 36pt [101%,45% → 136%,49%]: That’s [[maximum likelihood|#80b9ff]] parameter learning!
- text 36pt [50%,50% → 50%,50%]: There is another option…
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 52
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [40%,46% → 60%,50%]: There is another option…
- text 36pt [40%,50% → 60%,55%]: [[Bayesian parameter learning!|#80b9ff]]

## Slide 53
- YouTube video https://www.youtube.com/watch?v=8xsGtcSidFc (thumbnail `hqdefault-13142.jpg`) [-0%,-18% → 120%,142%]
- **Builds:** click 1: YouTube video https://www.youtube.com/watch?v=8xsGtcSidFc (thumbnail ` — YouTube video starts

## Slide 54
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [50%,50% → 50%,50%]: Bayesian parameter learning is perfect for [[indecisive|#80b9ff]] people like me and Chidi!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 55
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [14%,48% → 86%,53%]: Why pick just one set of parameters? [[Let’s maintain a distribution over all possible parameters!|#80b9ff]]
- line #ffffff [35%,85% → 69%,85%]
- shape (outline) [34%,51% → 67%,107%]
- equation $\theta$ (56pt, #ffffff) [49%,88% → 51%,92%]
- equation $P(\theta \mid D)$ (46pt, #ffffff) [54%,60% → 62%,64%]
- text 32pt [3%,73% → 32%,80%]: {We do not know how to compute $P(\theta \mid D)$|#000000}
- text 36pt [21%,41% → 79%,46%]: Bayesian parameter learning is perfect for [[indecisive|#80b9ff]] people like me and Chidi!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 56
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- equation $P(\theta \mid D)$ (46pt, #ffffff) [46%,18% → 54%,21%]
- text 36pt [32%,25% → 68%,30%]: We do not know how to directly compute this.
- text 36pt [33%,32% → 67%,37%]: {But we do know how to compute $P(D \mid \theta)$! |#80b9ff}
- group [29%,43% → 71%,92%]
  - rounded box (outline) [33%,57% → 67%,88%]
  - equation $D$ (36pt, #80b9ff) [42%,47% → 43%,49%]
  - equation $= \{o_1, o_2, \ldots, o_m\}$ (36pt, #80b9ff) [44%,46% → 56%,49%]
  - equation $P(D \mid \theta) = P(o_1 \mid \theta)P(o_2 \mid \theta) \cdots P(o_m \mid \theta)$ (36pt, #000000) [36%,72% → 66%,75%]
  - equation $= o_{1:m}$ (36pt, #80b9ff) [44%,51% → 48%,54%]
  - equation $= \prod_{i=1}^m P(o_i \mid \theta)$ (36pt, #000000) [43%,77% → 54%,86%]
  - text 32pt [36%,60% → 64%,68%]: {Assume the datapoints in $D$ are independent and identically distributed.|#000000}
  - line #80b9ff [29%,43% → 71%,92%]
- **Builds:** click 1: text 36pt — appears; click 2: text 36pt — appears; with previous: group — appears

## Slide 57
- line #ffffff [72%,31% → 81%,31%]
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- **Builds:** click 1: text 36pt — appears; with previous: equation $P(y \mid x)$ — appears; with previous: equation $P(y \mid x)$ — appears; with previous: equation $P(x, y)$ — appears; with previous: equation $P(x, y)$ — appears; with previous: equation $=$ — appears; with previous: equation $=$ — appears; with previous: equation $P(x)$ — appears; with previous: equation $P(x)$ — appears; with previous: line #ffffff — appears; with previous: line #ffffff — appears; click 2: text 36pt — slides in; with previous: equation $P(x, y)$ — slides in; with previous: equation $P(x, y)$ — slides in; with previous: equation $P(x \mid y)$ — slides in; with previous: equation $P(x \mid y)$ — slides in; with previous: equation $=$ — slides in; with previous: equation $=$ — slides in; with previous: equation $P(y)$ — slides in; with previous: equation $P(y)$ — slides in; with previous: line #ffffff — slides in; with previous: line #ffffff — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 58
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]

## Slide 59
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 60
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]
- equation $P(y \mid x)$ (47pt, #ffffff) [44%,55% → 51%,59%]
- equation $P(x)$ (47pt, #ffffff) [52%,55% → 56%,59%]
- equation $=$ (47pt, #ffffff) [57%,57% → 59%,58%]
- equation $P(x \mid y)$ (47pt, #ffffff) [60%,55% → 67%,59%]
- equation $P(y)$ (47pt, #ffffff) [68%,55% → 72%,59%]

## Slide 61
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]
- equation $P(y \mid x)$ (47pt, #ffffff) [44%,55% → 51%,59%]
- equation $P(x)$ (47pt, #ffffff) [52%,55% → 56%,59%]
- equation $=$ (47pt, #ffffff) [57%,57% → 59%,58%]
- equation $P(x \mid y)$ (47pt, #ffffff) [60%,55% → 67%,59%]
- equation $P(y)$ (47pt, #ffffff) [68%,55% → 72%,59%]
- equation $P(y \mid x)$ (47pt, #ffffff) [44%,55% → 51%,59%]
- equation $P(x)$ (47pt, #ffffff) [52%,55% → 56%,59%]
- equation $=$ (47pt, #ffffff) [57%,57% → 59%,58%]
- equation $P(x \mid y)$ (47pt, #ffffff) [60%,55% → 67%,59%]
- equation $P(y)$ (47pt, #ffffff) [68%,55% → 72%,59%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 62
- rounded box (outline) [43%,12% → 57%,21%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [46%,14% → 54%,19%]: Bayes’ Rule
- text 36pt [6%,29% → 34%,34%]: Definition of conditional probability:
- equation $P(y \mid x)$ (47pt, #ffffff) [35%,30% → 43%,34%]
- equation $=$ (47pt, #ffffff) [43%,31% → 45%,32%]
- line #ffffff [46%,32% → 54%,32%]
- equation $P(x, y)$ (47pt, #ffffff) [47%,26% → 53%,30%]
- equation $P(x)$ (47pt, #ffffff) [48%,35% → 52%,38%]
- text 36pt [56%,30% → 60%,34%]: and
- equation $P(x \mid y)$ (47pt, #ffffff) [62%,29% → 69%,33%]
- equation $=$ (47pt, #ffffff) [70%,31% → 71%,32%]
- line #ffffff [72%,31% → 81%,31%]
- equation $P(x, y)$ (47pt, #ffffff) [73%,26% → 79%,29%]
- equation $P(y)$ (47pt, #ffffff) [74%,34% → 78%,38%]
- equation $P(y \mid x)$ (47pt, #ffffff) [33%,43% → 41%,47%]
- equation $P(x)$ (47pt, #ffffff) [41%,43% → 46%,47%]
- equation $=$ (47pt, #ffffff) [46%,45% → 48%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [49%,43% → 55%,47%]
- equation $P(x \mid y)$ (47pt, #ffffff) [61%,43% → 69%,47%]
- equation $P(y)$ (47pt, #ffffff) [69%,43% → 74%,47%]
- equation $=$ (47pt, #ffffff) [75%,45% → 76%,46%]
- equation $P(x, y)$ (47pt, #ffffff) [77%,43% → 84%,47%]
- equation $P(y \mid x)$ (47pt, #ffffff) [44%,55% → 51%,59%]
- equation $P(x)$ (47pt, #ffffff) [52%,55% → 56%,59%]
- equation $=$ (47pt, #ffffff) [57%,57% → 59%,58%]
- equation $P(x \mid y)$ (47pt, #ffffff) [60%,55% → 67%,59%]
- equation $P(y)$ (47pt, #ffffff) [68%,55% → 72%,59%]
- equation $P(y \mid x)$ (47pt, #ffffff) [44%,70% → 52%,74%]
- equation $=$ (47pt, #ffffff) [53%,72% → 54%,73%]
- equation $P(x \mid y)$ (47pt, #ffffff) [56%,66% → 63%,70%]
- equation $P(y)$ (47pt, #ffffff) [64%,66% → 68%,70%]
- line #ffffff [55%,72% → 69%,72%]
- equation $P(x)$ (47pt, #ffffff) [60%,75% → 64%,78%]
- equation $=$ (47pt, #ffffff) [71%,72% → 72%,73%]
- group [73%,66% → 88%,84%]
  - equation $P(x \mid y)$ (47pt, #ffffff) [75%,66% → 82%,70%]
  - equation $P(y)$ (47pt, #ffffff) [83%,66% → 87%,70%]
  - line #ffffff [74%,72% → 88%,72%]
  - equation $\sum_y P(x \mid y) P(y)$ (47pt, #ffffff) [73%,75% → 88%,85%]
- **Builds:** click 1: equation $=$ — slides in; with previous: group — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 63
- rounded box (outline) [33%,32% → 71%,62%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [45%,33% → 57%,39%]: Bayes’ Rule
- equation $P(y \mid x)$ (47pt, #ffffff) [37%,45% → 45%,49%]
- equation $=$ (47pt, #ffffff) [47%,47% → 48%,48%]
- group [49%,41% → 64%,59%]
  - equation $P(x \mid y)$ (47pt, #ffffff) [51%,41% → 58%,45%]
  - equation $P(y)$ (47pt, #ffffff) [59%,41% → 63%,45%]
  - line #ffffff [50%,47% → 64%,47%]
  - equation $\sum_y P(x \mid y) P(y)$ (47pt, #ffffff) [49%,50% → 64%,60%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 64
- rounded box (outline) [7%,35% → 45%,65%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [19%,37% → 31%,42%]: Bayes’ Rule
- equation $P(y \mid x)$ (47pt, #ffffff) [11%,48% → 19%,52%]
- equation $=$ (47pt, #ffffff) [21%,50% → 22%,51%]
- group [23%,44% → 38%,63%]
  - equation $P(x \mid y)$ (47pt, #ffffff) [25%,44% → 32%,48%]
  - equation $P(y)$ (47pt, #ffffff) [33%,44% → 37%,48%]
  - line #ffffff [24%,51% → 38%,51%]
  - equation $\sum_y P(x \mid y) P(y)$ (47pt, #ffffff) [23%,53% → 38%,63%]
- equation $P(\theta \mid D) = \frac{P(D \mid \theta) P(\theta)}{\sum_\theta P(D \mid \theta) P(\theta)}$ (55pt, #ffffff) [57%,44% → 90%,57%]
- shape (outline) [49%,47% → 54%,53%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 65
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- equation $P(\theta \mid D) = \frac{P(D \mid \theta) P(\theta)}{\sum_\theta P(D \mid \theta) P(\theta)}$ (55pt, #ffffff) [35%,57% → 68%,70%]
- text on a #ffa4e7 filled box 36pt [30%,16% → 74%,25%]: {Bayesian Parameter Estimation|#000000}
- equation $\prod_{i=1}^m P(o_i \mid \theta)$ (57pt, #80b9ff) [54%,30% → 68%,45%]
- arrow #80b9ff [57%,43% → 62%,56%]
- arrow #80b9ff [59%,43% → 62%,64%]
- text 36pt [71%,46% → 84%,54%]: {prior distribution over $\theta$|#80b9ff}
- arrow #80b9ff [65%,53% → 74%,57%]
- arrow #80b9ff [68%,53% → 74%,66%]
- text 36pt [19%,49% → 37%,58%]: {posterior distribution over $\theta$|#80b9ff}
- arrow #80b9ff [28%,58% → 34%,61%]
- text 36pt [59%,27% → 72%,32%]: {likelihood model|#80b9ff}
- **Builds:** click 1: equation $\prod_{i=1}^m P(o_i \mid \theta)$ — fades up from dark; with previous: arrow #80b9ff — draws in; with previous: arrow #80b9ff — draws in; with previous: text 36pt — fades up from dark; click 2: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; with previous: arrow #80b9ff — draws in; click 3: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 66
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- equation $P(\theta \mid D) = \frac{P(D \mid \theta) P(\theta)}{\sum_\theta P(D \mid \theta) P(\theta)}$ (55pt, #ffffff) [33%,32% → 65%,45%]
- text on a #ffa4e7 filled box 36pt [30%,16% → 74%,25%]: {Bayesian Parameter Estimation|#000000}
- text 32pt [36%,60% → 64%,68%]: {Assume the datapoints in $D$ are independent and identically distributed.|#000000}
- text 48pt [20%,35% → 30%,41%]: Discrete:
- text 48pt [17%,54% → 30%,60%]: Continuous:
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (55pt, #ffffff) [32%,51% → 66%,65%]
- rounded box (outline) [35%,69% → 69%,91%]
- text 32pt [37%,71% → 67%,89%]: {In general, the denominator is difficult to compute analytically. However, we can compute the numerator, which allows us to sample from the posterior using |#000000}[[probabilistic programming|#000000]]{.|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 67
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text on a #ffa4e7 filled box 36pt [30%,16% → 74%,25%]: {Bayesian Parameter Estimation|#000000}
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (46pt, #ffffff) [7%,41% → 35%,52%]
- rounded box (outline) [4%,58% → 38%,80%]
- text 32pt [6%,60% → 36%,78%]: {In general, the denominator is difficult to compute analytically. However, we can compute the numerator, which allows us to sample from the posterior using |#000000}[[probabilistic programming|#000000]]{.|#000000}
- image `val-page-37.svg` (cropped: show only 11–64% across and 18–45% down of the image) [44%,35% → 92%,85%]
- vector icon `shape-f902cfcf.svg` [20%,40% → 28%,45%]
- vector icon `shape-94217f63.svg` [47%,39% → 55%,42%]
- vector icon `shape-1f571656.svg` [28%,40% → 33%,45%]
- vector icon `shape-fe5d674a.svg` [47%,42% → 52%,45%]
- text on a #80b9ff filled box 32pt [22%,84% → 41%,92%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: vector icon `shape-94217f63.svg` — wipes in; with previous: vector icon `shape-f902cfcf.svg` — wipes in; click 2: vector icon `shape-1f571656.svg` — wipes in; with previous: vector icon `shape-fe5d674a.svg` — wipes in; click 3: text on a #80b9ff filled box 32pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 68
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [43%,48% → 57%,52%]: Sometimes, it is possible to compute the posterior [[analytically|#80b9ff]].

## Slide 69
- YouTube video https://www.youtube.com/watch?v=WRweeidN7aM (thumbnail `hqdefault-10963.jpg`) [16%,12% → 84%,102%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [43%,13% → 57%,18%]: Let’s flip frisbees!
- **Builds:** then: YouTube video https://www.youtube.com/watch?v=WRweeidN7aM (thumbnail ` — YouTube video starts

## Slide 70
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [43%,13% → 57%,18%]: Let’s flip frisbees!
- equation $\theta$ (55pt, #ffffff) [10%,25% → 11%,28%]
- text 36pt [11%,24% → 55%,29%]: : probability of both frisbees landing in the same direction
- equation $1 - \theta$ (55pt, #ffffff) [5%,30% → 11%,34%]
- text 36pt [11%,30% → 58%,35%]: : probability of both frisbees landing in the different directions
- text 36pt [48%,40% → 52%,45%]: Flip 10 times…
- equation $D = \{s, d, s, s, d, d, d, s,d, s\}$ (47pt, #ffffff) [37%,47% → 63%,51%]
- equation $n$ (56pt, #ffffff) [31%,54% → 32%,57%]
- text 36pt [33%,53% → 51%,58%]: : number of times same
- equation $m$ (56pt, #ffffff) [54%,54% → 56%,57%]
- text 36pt [56%,53% → 73%,58%]: : total number of flips
- equation $p(D \mid \theta) = \theta^n (1- \theta)^{m-n}$ (49pt, #ffffff) [38%,60% → 62%,65%]
- text 36pt [48%,68% → 52%,73%]: Turns out that if we select our prior distribution to be $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$ …
- text 36pt [22%,76% → 78%,81%]: Our posterior distribution will be $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- **Builds:** click 1: equation $1 - \theta$ — appears; with previous: text 36pt — appears; click 2: text 36pt — appears; with previous: equation $D = \{s, d, s, s, d, d, d, s,d, s\}$ — appears; click 3: text 36pt — appears; with previous: text 36pt — appears; with previous: equation $n$ — appears; with previous: equation $m$ — appears; click 4: equation $p(D \mid \theta) = \theta^n (1- \theta)^{m-n}$ — appears; click 5: text 36pt — appears; click 6: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 71
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [43%,13% → 57%,18%]: Let’s flip frisbees!
- equation $\theta$ (55pt, #ffffff) [6%,25% → 7%,28%]
- text 36pt [7%,24% → 51%,29%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [5%,30% → 7%,33%]
- text 36pt [7%,29% → 25%,34%]: : number of times same
- equation $m$ (56pt, #ffffff) [5%,35% → 7%,38%]
- text 36pt [7%,34% → 24%,39%]: : total number of flips
- text 36pt [5%,40% → 21%,45%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [4%,46% → 34%,50%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #80b9ff [4%,45% → 34%,52%]
- rounded box (outline) [54%,23% → 93%,92%]
- text 32pt [57%,25% → 90%,29%]: {Some Notes|#000000}
- text 36pt [55%,31% → 92%,39%]: {I skipped over the actual calculation of the posterior using this equation:|#000000}
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (40pt, #000000) [61%,42% → 86%,52%]
- text 36pt [55%,54% → 92%,63%]: {You can either trust me or check out chapter 4 of |#000000}[[Algorithms for Decision Making|#000000]]{.|#000000}
- text 36pt [55%,66% → 93%,78%]: {The Beta distribution is a |#000000}[[conjugate prior|#000000]]{ for the Bernoulli distribution, meaning that the posterior distribution is the same class as the prior.|#000000}
- text on a #80b9ff filled box 32pt [16%,68% → 36%,76%]: {Pluto Notebook!|#000000}
- text 36pt [55%,81% → 93%,85%]: {See demo for some intuition!|#000000}
- **Builds:** click 1: rounded box (outline) — fades up from dark; with previous: text 32pt — fades up from dark; click 2: text 36pt — appears; with previous: equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ — appears; click 3: text 36pt — appears; click 4: text 36pt — appears; click 5: text 36pt — appears; click 6: text on a #80b9ff filled box 32pt — appears

## Slide 72
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [31%,13% → 69%,18%]: many common distributions have [[conjugate priors|#80b9ff]]
- text 36pt [36%,23% → 43%,27%]: Bernoulli
- text 36pt [34%,32% → 43%,36%]: multinomial
- arrow #ffffff [46%,26% → 56%,26%]
- arrow #ffffff [46%,35% → 56%,35%]
- text 36pt [59%,23% → 63%,28%]: Beta
- text 36pt [59%,31% → 66%,36%]: Dirichlet
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 73
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [7%,31% → 45%,35%]: many common distributions have [[conjugate priors|#80b9ff]]
- text 36pt [12%,40% → 19%,44%]: binomial
- text 36pt [9%,49% → 19%,54%]: multinomial
- text 36pt [12%,59% → 19%,63%]: Gaussian
- arrow #ffffff [22%,61% → 32%,61%]
- arrow #ffffff [22%,43% → 32%,43%]
- arrow #ffffff [22%,52% → 32%,52%]
- text 36pt [35%,40% → 39%,45%]: Beta
- text 36pt [35%,49% → 42%,53%]: Dirichlet
- text 36pt [35%,58% → 42%,63%]: Gaussian
- image `pasted-image-11469.png` [49%,22% → 94%,81%]
- text on a #000000 filled box 32pt [50%,46% → 61%,58%]: likelihood model
- text on a #000000 filled box 32pt [80%,45% → 91%,57%]: conjugate prior
- **Builds:** click 1: text on a #000000 filled box 32pt — appears; with previous: text on a #000000 filled box 32pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 74
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [50%,50% → 50%,50%]: What if we do have to make a choice though? 😬
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 75
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 48pt [33%,15% → 71%,21%]: What if we do have to make a choice though? 😬
- text 36pt [33%,25% → 71%,29%]: We can use the expectation of the distribution.
- text 36pt [41%,38% → 73%,46%]: {Although that might not be the best plan if the distribution is multimodal…|#80b9ff}
- image `test-11546.svg` [25%,33% → 39%,57%]
- equation $\hat \theta = \operatorname{argmax}_\theta P(\theta \mid D)$ (36pt, #ffffff) [44%,68% → 60%,72%]
- text 36pt [31%,60% → 69%,65%]: We can instead use the [[maximum a posteriori|#80b9ff]] of the distribution:
- text 36pt [36%,75% → 68%,80%]: *sometimes also referred to as the [[mode|#80b9ff]]
- **Builds:** click 1: text 36pt — appears; click 2: text 36pt — appears; with previous: image `test-11546.svg` — appears; click 3: text 36pt — appears; click 4: equation $\hat \theta = \operatorname{argmax}_\theta P(\theta \mid D)$ — appears; click 5: text 36pt — appears

## Slide 76
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [46%,13% → 54%,18%]: Summary
- text on a #ffa4e7 filled box 36pt [28%,23% → 72%,52%]: {Maximum Likelihood Parameter Estimation|#000000} / {$\hat \theta = \operatorname{argmax}_\theta \sum_{i=1}^m \log P(o_i \mid \theta)$|#000000}
- text on a #ffa4e7 filled box 36pt [28%,58% → 72%,87%]: {Bayesian Parameter Estimation|#000000} / {$P(\theta \mid D) = \frac{P(D \mid \theta) P(\theta)}{\sum_\theta P(D \mid \theta) P(\theta)}$|#000000}

## Slide 77
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [50%,50% → 50%,50%]: One last thing on parameter learning: we should be careful about [[generalization|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 78
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [20%,14% → 80%,19%]: One last thing on parameter learning: we should be careful about [[generalization|#80b9ff]].
- text 36pt [48%,23% → 52%,27%]: We should evaluate our model on a [[separate validation set|#80b9ff]] to ensure that we do not have [[overfitting|#80b9ff]].
- image `test-13005.svg` [36%,37% → 64%,87%]
- vector icon `shape-b1c91ebc.svg` [66%,39% → 68%,41%]
- text 36pt [68%,38% → 78%,43%]: Training Set
- vector icon `shape-eee4115a.svg` [67%,44% → 68%,46%]
- text 36pt [68%,43% → 78%,47%]: {Validation Set|#80b9ff}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 79
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- line #ffffff [-0%,7% → 52%,7%]
- line #ffffff [52%,0% → 52%,7%]
- text 36pt [20%,14% → 80%,19%]: One last thing on parameter learning: we should be careful about [[generalization|#80b9ff]].
- text 36pt [48%,23% → 52%,27%]: We should evaluate our model on a [[separate validation set|#80b9ff]] to ensure that we do not have [[overfitting|#80b9ff]].
- image `test-13005.svg` [9%,37% → 38%,87%]
- vector icon `shape-b1c91ebc.svg` [40%,39% → 41%,41%]
- text 36pt [42%,38% → 51%,43%]: Training Set
- vector icon `shape-eee4115a.svg` [40%,44% → 41%,46%]
- text 36pt [42%,43% → 53%,47%]: {Validation Set|#80b9ff}
- text 36pt [59%,34% → 72%,39%]: Holdout Method
- vector icon `shape-4398b24c.svg` [59%,41% → 64%,44%]
- vector icon `shape-4398b24c.svg` [64%,41% → 70%,44%]
- vector icon `shape-4398b24c.svg` [70%,41% → 75%,44%]
- vector icon `shape-4398b24c.svg` [75%,41% → 80%,44%]
- vector icon `shape-83ba0972.svg` [80%,41% → 85%,44%]
- text 36pt [59%,49% → 83%,54%]: K-fold Cross Validation Method
- vector icon `shape-4398b24c.svg` [59%,56% → 64%,59%]
- vector icon `shape-4398b24c.svg` [64%,56% → 70%,59%]
- vector icon `shape-4398b24c.svg` [70%,56% → 75%,59%]
- vector icon `shape-4398b24c.svg` [75%,56% → 80%,59%]
- vector icon `shape-83ba0972.svg` [80%,56% → 85%,59%]
- vector icon `shape-4398b24c.svg` [59%,61% → 64%,64%]
- vector icon `shape-4398b24c.svg` [64%,61% → 70%,64%]
- vector icon `shape-4398b24c.svg` [69%,61% → 75%,64%]
- vector icon `shape-83ba0972.svg` [75%,61% → 80%,64%]
- vector icon `shape-4398b24c.svg` [80%,61% → 85%,64%]
- vector icon `shape-4398b24c.svg` [59%,66% → 64%,69%]
- vector icon `shape-4398b24c.svg` [64%,66% → 70%,69%]
- vector icon `shape-83ba0972.svg` [69%,66% → 75%,69%]
- vector icon `shape-4398b24c.svg` [75%,66% → 80%,69%]
- vector icon `shape-4398b24c.svg` [80%,66% → 85%,69%]
- vector icon `shape-4398b24c.svg` [59%,71% → 64%,75%]
- vector icon `shape-83ba0972.svg` [64%,71% → 70%,75%]
- vector icon `shape-4398b24c.svg` [69%,71% → 75%,75%]
- vector icon `shape-4398b24c.svg` [75%,71% → 80%,75%]
- vector icon `shape-4398b24c.svg` [80%,71% → 85%,75%]
- vector icon `shape-83ba0972.svg` [59%,77% → 64%,80%]
- vector icon `shape-4398b24c.svg` [64%,77% → 70%,80%]
- vector icon `shape-4398b24c.svg` [69%,77% → 75%,80%]
- vector icon `shape-4398b24c.svg` [75%,77% → 80%,80%]
- vector icon `shape-4398b24c.svg` [80%,77% → 85%,80%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 80
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text on a #8dd0f5 filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #8dd0f5 filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- heading (spaced caps) 36pt [18%,30% → 61%,35%]: GENERAL THOUGHTS ON MODELS
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: STEPS FOR BUILDING MODELS
- text on a #8dd0f5 filled box 20pt [21%,53% → 24%,57%]: {A|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 30pt [26%,53% → 99%,57%]: {SELECT A MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,60% → 24%,64%]: {B|#000000}
- heading (spaced caps) 30pt [26%,60% → 99%,64%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,67% → 24%,71%]: {C|#000000}
- heading (spaced caps) 30pt [26%,67% → 99%,71%]: {VALIDATE THE MODEL|#abdaf4}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 81
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [9%,39% → 91%,61%]: There is a story that has been going around about a physicist, a chemist, and an economist who were stranded on a desert island with only a can of food. The physicist and the chemist each devised an ingenious mechanism for getting the can open; the economist merely said, "Assume we have a can opener"!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 82
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,37% → 90%,63%]: Our assumptions don’t mean much if they aren’t grounded in reality.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 83
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,42% → 90%,48%]: Our assumptions don’t mean much if they aren’t grounded in reality.
- text 48pt [10%,50% → 90%,56%]: {All our of downstream validation results depend on how good our model is!|#80b9ff}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 84
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,38% → 90%,44%]: Our assumptions don’t mean much if they aren’t grounded in reality.
- text 48pt [10%,47% → 90%,53%]: {All our of downstream validation results depend on how good our model is!|#80b9ff}
- text 48pt [10%,56% → 90%,62%]: So we need to validate the model.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 85
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,47% → 90%,53%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 86
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11776.svg` [20%,34% → 46%,77%]
- image `test-11798.svg` [51%,34% → 77%,77%]
- text 36pt [46%,22% → 54%,27%]: PDF Plot
- text 36pt [32%,28% → 39%,32%]: {good fit|#80cfb9}
- text 36pt [64%,28% → 70%,32%]: {bad fit|#fab0ae}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 87
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11776.svg` [33%,35% → 49%,62%]
- image `test-11798.svg` [33%,65% → 49%,91%]
- text 36pt [23%,45% → 29%,49%]: {good fit|#80cfb9}
- text 36pt [23%,73% → 28%,78%]: {bad fit|#fab0ae}
- text 36pt [39%,24% → 47%,28%]: PDF Plot
- text 36pt [57%,24% → 65%,28%]: CDF Plot

## Slide 88
- image `test-11776.svg` [33%,35% → 49%,62%]
- image `test-11798.svg` [33%,65% → 49%,91%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- text 36pt [39%,24% → 47%,28%]: PDF Plot
- text 36pt [23%,45% → 29%,49%]: {good fit|#80cfb9}
- text 36pt [23%,73% → 28%,78%]: {bad fit|#fab0ae}
- text 36pt [57%,24% → 65%,28%]: CDF Plot
- image `fit-flipbook.svg` [33%,34% → 67%,91%] — an animated SVG: 40 frames that play by themselves over about 4 s and stop on the last frame (the CDF sweeps across). Start it when this slide appears by setting the img `src` again (for example add `?t=` + Date.now()); it restarts every time the image loads.
- **Builds:** the flipbook plays automatically as soon as the slide appears (no click).
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 89
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [18%,41% → 45%,86%]
- text 36pt [54%,29% → 77%,34%]: Quantile-Quantile (Q-Q) Plot
- text 36pt [31%,29% → 38%,34%]: PDF Plot
- image `test-12174.svg` [49%,41% → 75%,86%]
- equation $\alpha = 0.1$ (36pt, #f3cf80) [79%,43% → 85%,45%]
- equation $q_\text{model} = -2.28$ (36pt, #c3b8ff) [79%,54% → 92%,57%]
- equation $q_\text{data} = -1.29$ (36pt, #ffffff) [79%,48% → 91%,52%]
- arrow #ffffff [24%,79% → 31%,79%]
- arrow #c3b8ff [24%,78% → 28%,79%]
- **Builds:** click 1: equation $q_\text{data} = -1.29$ — appears; with previous: arrow #ffffff — appears; click 2: arrow #c3b8ff — appears; with previous: equation $q_\text{model} = -2.28$ — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 90
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [18%,41% → 45%,86%]
- text 36pt [54%,29% → 77%,34%]: Quantile-Quantile (Q-Q) Plot
- text 36pt [31%,29% → 38%,34%]: PDF Plot
- image `test-12174.svg` [49%,41% → 75%,86%]
- equation $\alpha = 0.1$ (36pt, #f3cf80) [79%,43% → 85%,45%]
- equation $q_\text{model} = -2.28$ (36pt, #c3b8ff) [79%,54% → 92%,57%]
- equation $q_\text{data} = -1.29$ (36pt, #ffffff) [79%,48% → 91%,52%]
- arrow #ffffff [54%,65% → 54%,78%]
- arrow #c3b8ff [54%,78% → 58%,78%]
- line #ffffff [54%,66% → 58%,66%]
- line #ffffff [58%,66% → 58%,78%]
- vector icon `shape-b23752eb.svg` [57%,65% → 59%,67%]
- **Builds:** click 1: line #ffffff — draws in; with previous: line #ffffff — draws in; then: vector icon `shape-b23752eb.svg` — appears

## Slide 91
- image `test-12174.svg` [49%,41% → 75%,86%]
- image `test-12237.svg` [49%,41% → 75%,86%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [18%,41% → 45%,86%]
- text 36pt [54%,29% → 77%,34%]: Quantile-Quantile (Q-Q) Plot
- text 36pt [31%,29% → 38%,34%]: PDF Plot
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 92
- image `test-12174.svg` [36%,41% → 62%,86%]
- image `test-12237.svg` [36%,41% → 62%,86%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [2%,41% → 29%,86%]
- text 36pt [41%,29% → 64%,34%]: Quantile-Quantile (Q-Q) Plot
- text 36pt [15%,29% → 22%,34%]: PDF Plot
- text 36pt [78%,29% → 91%,34%]: Calibration Plot
- image `test-12278.svg` [69%,41% → 96%,87%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 93
- image `test-12237.svg` [53%,64% → 68%,89%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [10%,14% → 90%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [19%,63% → 34%,88%]
- text 30pt [53%,29% → 72%,33%]: Quantile-Quantile (Q-Q) Plot
- text 30pt [25%,29% → 31%,33%]: PDF Plot
- text 30pt [74%,29% → 84%,33%]: Calibration Plot
- image `test-12278.svg` [70%,63% → 85%,88%]
- image `test-12299.svg` [36%,62% → 51%,88%]
- image `test-11776.svg` [19%,35% → 34%,61%]
- image `test-12315.svg` [53%,36% → 68%,61%]
- image `test-12337.svg` [36%,35% → 51%,61%]
- image `test-12343.svg` [70%,35% → 85%,61%]
- text 30pt [43%,29% → 49%,33%]: CDF Plot
- text 36pt [10%,43% → 16%,48%]: {good fit|#80cfb9}
- text 36pt [10%,71% → 15%,76%]: {bad fit|#fab0ae}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 94
- image `test-12237.svg` [53%,64% → 68%,89%]
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [99%,14% → 178%,20%]: We want to compare features of the [[model|#80b9ff]] to features of the [[data|#80b9ff]].
- image `test-11798.svg` [19%,63% → 34%,88%]
- text 30pt [53%,29% → 72%,33%]: Quantile-Quantile (Q-Q) Plot
- text 30pt [25%,29% → 31%,33%]: PDF Plot
- text 30pt [74%,29% → 84%,33%]: Calibration Plot
- image `test-12278.svg` [70%,63% → 85%,88%]
- image `test-12299.svg` [36%,62% → 51%,88%]
- image `test-11776.svg` [19%,35% → 34%,61%]
- image `test-12315.svg` [53%,36% → 68%,61%]
- image `test-12337.svg` [36%,35% → 51%,61%]
- image `test-12343.svg` [70%,35% → 85%,61%]
- text 30pt [43%,29% → 49%,33%]: CDF Plot
- text 36pt [10%,43% → 16%,48%]: {good fit|#80cfb9}
- text 36pt [10%,71% → 15%,76%]: {bad fit|#fab0ae}
- text 48pt [20%,15% → 80%,19%]: These are [[visual diagnostics|#80b9ff]]. We can summarize them using [[summary metrics|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 95
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- image `test-11798.svg` [19%,63% → 34%,88%]
- text 30pt [25%,29% → 31%,33%]: PDF Plot
- image `test-11776.svg` [19%,35% → 34%,61%]
- text 36pt [10%,43% → 16%,48%]: {good fit|#80cfb9}
- text 36pt [10%,71% → 15%,76%]: {bad fit|#fab0ae}
- text 48pt [20%,15% → 80%,19%]: These are [[visual diagnostics|#80b9ff]]. We can summarize them using [[summary metrics|#80b9ff]].
- text 36pt [51%,28% → 89%,36%]: We can summarize the PDF plot using the [[Kullback-Leibler divergence (K-L divergence)|#80b9ff]].
- equation $D_{\text{KL}}(p \parallel q) = \int p(x) \log \left( \frac{p(x)}{q(x)} \right) \, dx$ (36pt, #ffffff) [57%,41% → 84%,49%]
- equation $D_{\text{KL}} = 8.6 \times 10^{-5}$ (36pt, #80cfb9) [31%,37% → 45%,41%]
- equation $D_{\text{KL}} = 0.49$ (36pt, #fab0ae) [31%,65% → 40%,68%]
- group [50%,56% → 90%,92%]
  - rounded box (outline) [50%,56% → 90%,92%]
  - text 36pt [52%,70% → 88%,78%]: {The K-L divergence is part of a broad class of divergences called the F-divergences.|#000000} / {The K-L divergence is not symmetric and it is not defined if the support of $p$ is not a subset of the support of $q$.|#000000}
- **Builds:** click 1: equation $D_{\text{KL}} = 8.6 \times 10^{-5}$ — appears; with previous: equation $D_{\text{KL}} = 0.49$ — appears; click 2: group — appears

## Slide 96
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [10%,43% → 16%,48%]: {good fit|#80cfb9}
- text 36pt [10%,71% → 15%,76%]: {bad fit|#fab0ae}
- text 48pt [20%,15% → 80%,19%]: These are [[visual diagnostics|#80b9ff]]. We can summarize them using [[summary metrics|#80b9ff]].
- text 36pt [51%,28% → 89%,36%]: We can summarize the CDF plot using the [[Kolmogorov-Smirnov statistic (K-S statistic)|#80b9ff]].
- image `test-12299.svg` [18%,62% → 33%,88%]
- image `test-12337.svg` [18%,34% → 33%,60%]
- text 30pt [25%,28% → 31%,32%]: CDF Plot
- equation $D_{\text{KS}} = \max_x | P(X \leq x) - Q(X \leq x) |$ (39pt, #ffffff) [56%,43% → 85%,48%]
- line #fab0ae [26%,73% → 26%,80%]
- arrow #ffffff [26%,49% → 61%,75%]
- **Builds:** click 1: line #fab0ae — draws in; with previous: arrow #ffffff — draws in

## Slide 97
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [10%,43% → 16%,48%]: {good fit|#80cfb9}
- text 36pt [10%,71% → 15%,76%]: {bad fit|#fab0ae}
- text 48pt [20%,15% → 80%,19%]: These are [[visual diagnostics|#80b9ff]]. We can summarize them using [[summary metrics|#80b9ff]].
- text 36pt [51%,28% → 89%,36%]: We can summarize the calibration plot using the [[Maximum Calibration Error (MCE)|#80b9ff]] and [[Expected Calibration Error (ECE)|#80b9ff]].
- text 30pt [21%,30% → 31%,34%]: Calibration Plot
- image `test-12278.svg` [17%,64% → 32%,90%]
- image `test-12343.svg` [17%,37% → 32%,62%]
- line #fab0ae [27%,74% → 27%,80%]
- arrow #ffffff [73%,39% → 73%,48%]
- arrow #ffffff [29%,35% → 61%,76%]
- text 36pt [71%,48% → 75%,53%]: Average Gap
- **Builds:** click 1: line #fab0ae — draws in; then: arrow #ffffff — draws in; click 2: arrow #ffffff — draws in; then: text 36pt — appears

## Slide 98
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 48pt [20%,15% → 80%,19%]: What if we want to compare [[multiple|#80b9ff]] features?
- text 36pt [48%,22% → 52%,27%]: We need to be careful!
- text 36pt [48%,85% → 52%,89%]: We don’t want to miss the [[interactions|#80b9ff]] between features.
- image `test-12673.svg` [22%,22% → 90%,83%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 99
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [28%,12% → 72%,16%]: We don’t want to miss the [[interactions|#80b9ff]] between features.
- text 36pt [16%,18% → 84%,23%]: One option: create a [[single feature that captures the relationship|#80b9ff]] between multiple features.
- image `test-12673.svg` [22%,22% → 90%,83%]
- line #ffa4e7 [22%,39% → 43%,76%]
- line #ffa4e7 [59%,39% → 79%,76%]
- line #ffa4e7 [25%,57% → 29%,64%]
- vector icon `shape-3e052375.svg` [25%,57% → 26%,58%]
- **Builds:** click 1: line #ffa4e7 — draws in; with previous: line #ffa4e7 — draws in; click 2: vector icon `shape-3e052375.svg` — apple:bc-zoom-big character; click 3: line #ffa4e7 — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 100
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [28%,12% → 72%,16%]: We don’t want to miss the [[interactions|#80b9ff]] between features.
- text 36pt [16%,18% → 84%,23%]: One option: create a [[single feature that captures the relationship|#80b9ff]] between multiple features.
- image `test-12673.svg` [10%,35% → 59%,80%]
- line #ffa4e7 [10%,48% → 25%,74%]
- line #ffa4e7 [36%,48% → 51%,74%]
- line #ffa4e7 [12%,61% → 15%,66%]
- vector icon `shape-8f80588f.svg` [12%,61% → 12%,62%]
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [59%,34% → 94%,79%]
- text 36pt [10%,29% → 24%,34%]: Multiple Features
- text 36pt [70%,28% → 83%,33%]: Combined Feature
- text 36pt [37%,29% → 50%,34%]: Multiple Features
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 101
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [28%,12% → 72%,16%]: We don’t want to miss the [[interactions|#80b9ff]] between features.
- text 36pt [101%,18% → 169%,23%]: One option: create a [[single feature that captures the relationship|#80b9ff]] between multiple features.
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [144%,34% → 179%,79%]
- text 36pt [154%,28% → 169%,33%]: Combined Feature
- image `test-12673.svg` [18%,31% → 86%,93%]
- text 36pt [48%,19% → 52%,23%]: Another option: extend summary metrics to multiple dimensions.
- image `test-12806.svg` [18%,29% → 87%,93%]
- **Builds:** click 1: image `test-12806.svg` — appears

## Slide 102
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- text 36pt [12%,30% → 41%,34%]: What about conditional distributions?
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [144%,34% → 179%,79%]
- text 36pt [154%,28% → 169%,33%]: Combined Feature
- image `test-12830.svg` [53%,10% → 87%,27%]
- image `test-12836.svg` [53%,27% → 87%,90%]
- rounded box (outline) [5%,42% → 48%,58%]
- text 36pt [6%,37% → 47%,63%]: {Partition conditioning variable into bins and compute visual diagnostics and metrics for each bin.|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 103
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [144%,34% → 179%,79%]
- text 36pt [154%,28% → 169%,33%]: Combined Feature
- text 36pt [50%,50% → 50%,50%]: We can also validate models using [[expert knowledge|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 104
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [144%,34% → 179%,79%]
- text 36pt [154%,28% → 169%,33%]: Combined Feature
- text 36pt [30%,11% → 70%,16%]: We can also validate models using [[expert knowledge|#80b9ff]].
- image `test-12906.svg` [13%,24% → 75%,79%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 105
- heading (spaced caps) 30pt [1%,2% → 74%,6%]: {VALIDATE THE MODEL|#abdaf4}
- line #ffffff [-27%,8% → 25%,8%]
- line #ffffff [25%,1% → 25%,8%]
- image `test-12738.svg` (cropped: show only 0–100% across and 17–100% down of the image) [144%,34% → 179%,79%]
- text 36pt [154%,28% → 169%,33%]: Combined Feature
- text 36pt [30%,11% → 70%,16%]: We can also validate models using [[expert knowledge|#80b9ff]].
- image `test-12906.svg` [5%,34% → 44%,70%]
- image `test-12920.svg` [50%,34% → 89%,70%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 106
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text on a #8dd0f5 filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #8dd0f5 filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- heading (spaced caps) 36pt [18%,30% → 61%,35%]: GENERAL THOUGHTS ON MODELS
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: STEPS FOR BUILDING MODELS
- text on a #8dd0f5 filled box 20pt [21%,53% → 24%,57%]: {A|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 30pt [26%,53% → 99%,57%]: {SELECT A MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,60% → 24%,64%]: {B|#000000}
- heading (spaced caps) 30pt [26%,60% → 99%,64%]: {SELECT THE PARAMETERS FOR THE MODEL CLASS|#abdaf4}
- text on a #8dd0f5 filled box 20pt [21%,67% → 24%,71%]: {C|#000000}
- heading (spaced caps) 30pt [26%,67% → 99%,71%]: {VALIDATE THE MODEL|#abdaf4}
- **Transition to next:** Magic Move (shared objects glide; others fade)
