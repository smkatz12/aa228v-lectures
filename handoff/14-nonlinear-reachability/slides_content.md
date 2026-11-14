# AA228V Lecture 14 — Nonlinear Reachability: slide-by-slide content

Extracted from the Keynote deck `14_Nonlinear_Reachability.key` (79 slides, 16:9). This is the source material for rebuilding the lecture as a native HTML deck.

## How to read this

- Positions are approximate boxes in % of the slide, `[left,top → right,bottom]`. Use the reference screenshots for the exact layout.
- `[[text|#hex]]` = accent phrase: italic, in that color. `{text|#hex}` = colored (not italic).
- `$...$` is LaTeX. Typeset it with KaTeX (or MathJax) in the same color and roughly the same size as the surrounding text. There are no equation image files.
- Images and videos named in backticks are online, not attached. Use each one by its full address `https://smkatz12.github.io/aa228v-lectures/lectures/14-nonlinear-reachability/images/<name>`, for example `<img src="https://smkatz12.github.io/aa228v-lectures/lectures/14-nonlinear-reachability/images/coverart-302-green.png">`. Don't ask for uploads.
- **Builds** list what appears on each click, in order ("then" = right after the previous step, "with previous" = at the same time, "(0.1 s later)" = after that pause).
- A long run of images named `gNN-…` that appear one after another at the same spot, a fraction of a second apart, is a frame-by-frame animation: stack them and reveal them in turn with that timing (each frame stays as the next appears).
- **Transition to next: Magic Move** means objects shared with the next slide should glide to their new positions.

## House style

- Same as earlier lectures: black background; white text.
- Spaced all-caps headings in Gill Sans (regular weight, letter-spacing about 0.25em). All other text in Palatino.
- Emphasis is italic + color, never bold.
- The title slide streak is green (`coverart-302-green.png`).
- Graphics are SVGs with transparent backgrounds and white lines/text, made for the black slides; keep them as `<img>` files.
- Handwritten ink from past lectures (slide 48) has been left out on purpose; the deck's own ink layer handles writing.
- Most-used text colors: `#ffffff`, `#80b9ff`, `#c3b8ff`, `#000000`, `#ffa4e7`, `#fab0ae`, `#f3cf80`, `#80cfb9`

## Slide 1
- image `coverart-302-green.png` [-0%,46% → 100%,75%]
- text 50pt [6%,9% → 82%,22%]: AA228V/CS238V / VALIDATION OF SAFETY-CRITICAL SYSTEMS
- heading (spaced caps) 50pt [4%,73% → 43%,87%]: LECTURE 14: REACHABILITY FOR NONLINEAR SYSTEMS / SYDNEY KATZ (SMKATZ@STANFORD.EDU)

## Slide 2
- text 36pt [19%,48% → 81%,52%]: In the previous lecture, we saw that we could apply [[linear operators|#80b9ff]] to polytopes.
- text 36pt [50%,53% → 79%,57%]: {(i.e. matrix multiplication and addition)|#80b9ff}
- **Builds:** click 1: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 3
- text 36pt [19%,45% → 81%,50%]: In the previous lecture, we saw that we could apply [[linear operators|#80b9ff]] to polytopes.
- text 36pt [19%,50% → 81%,54%]: It turns out that applying [[nonlinear operators|#80b9ff]] to polytopes is [[less straightforward|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 4
- text 36pt [20%,6% → 80%,11%]: It turns out that applying [[nonlinear operators|#80b9ff]] to polytopes is [[less straightforward|#80b9ff]].
- arrow #ffffff [20%,32% → 36%,36%]
- arrow #ffffff [24%,41% → 41%,45%]
- line #c3b8ff [28%,41% → 39%,45%]
- arrow #ffffff [55%,32% → 71%,36%]
- arrow #ffffff [60%,41% → 76%,45%]
- line #ffa4e7 [60%,27% → 72%,31%]
- group [45%,26% → 56%,37%]
  - shape (outline) [45%,26% → 56%,37%]
  - equation $2x + 1$ (31pt, #ffa4e7) [48%,31% → 52%,33%]
- rounded box (outline) [20%,16% → 80%,52%]
- text 36pt [43%,17% → 57%,22%]: Linear Operation
- text 30pt [29%,37% → 39%,41%]: {polytope (line)|#c3b8ff}
- text 30pt [67%,26% → 76%,37%]: {still a polytope (line)|#ffa4e7}
- arrow #ffffff [19%,71% → 35%,75%]
- arrow #ffffff [24%,80% → 40%,84%]
- line #c3b8ff [27%,80% → 39%,84%]
- arrow #ffffff [55%,71% → 71%,75%]
- arrow #ffffff [59%,80% → 76%,84%]
- shape (outline) [63%,70% → 75%,82%]
- group [44%,65% → 55%,76%]
  - shape (outline) [44%,65% → 55%,76%]
  - equation $\sin(x) + 1$ (31pt, #ffa4e7) [46%,69% → 52%,72%]
- rounded box (outline) [20%,54% → 80%,91%]
- text 36pt [41%,56% → 58%,61%]: Nonlinear Operation
- text 30pt [29%,76% → 38%,80%]: {polytope (line)|#c3b8ff}
- text 30pt [68%,61% → 77%,69%]: {not a polytope|#ffa4e7}
- vector icon `shape-3ce73556.svg` [68%,75% → 69%,77%]
- vector icon `shape-3ce73556.svg` [74%,78% → 75%,80%]
- line #f3cf80 [69%,75% → 74%,80%]
- text 30pt [70%,71% → 79%,75%]: {nonconvex!!|#f3cf80}
- **Builds:** click 1: arrow #ffffff — draws in; with previous: arrow #ffffff — draws in; click 2: line #c3b8ff — fades up from dark; click 3: text 30pt — fades up from dark; click 4: group — wipes in; click 5: line #ffa4e7 — slides in; with previous: arrow #ffffff — slides in; with previous: arrow #ffffff — slides in; click 6: text 30pt — fades up from dark; click 7: arrow #ffffff — draws in; with previous: arrow #ffffff — draws in; with previous: text 30pt — fades up from dark; with previous: line #c3b8ff — fades up from dark; click 8: group — wipes in; click 9: shape (outline) — slides in; with previous: arrow #ffffff — slides in; with previous: arrow #ffffff — slides in; click 10: text 30pt — fades up from dark; click 11: vector icon `shape-3ce73556.svg` — fades up from dark; with previous: vector icon `shape-3ce73556.svg` — fades up from dark; with previous: line #f3cf80 — draws in; with previous: text 30pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 5
- text 36pt [20%,6% → 80%,11%]: It turns out that applying [[nonlinear operators|#80b9ff]] to polytopes is [[less straightforward|#80b9ff]].
- group [17%,49% → 67%,79%]
  - arrow #ffffff [17%,52% → 55%,57%]
  - arrow #ffffff [28%,75% → 67%,79%]
  - shape (outline) [37%,49% → 65%,76%]
- text 36pt [40%,37% → 49%,46%]: {not a polytope|#ffa4e7}
- shape (filled #c3b8ff) [36%,46% → 67%,77%]
- text 36pt [54%,43% → 72%,55%]: {But we can overapproximate it with a polytope!|#c3b8ff}
- **Builds:** click 1: shape (filled #c3b8ff) — fades in; with previous: text 36pt — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 6
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Builds:** then: heading (spaced caps) 50pt — fades up from dark; with previous: line #ffffff — draws in; click 1: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 2: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 3: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 4: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 5: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 7
- rounded box (outline) [36%,35% → 64%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- arrow #ffffff [40%,56% → 60%,61%]
- line #80b9ff [42%,56% → 45%,61%]
- line #80b9ff [42%,56% → 45%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [40%,49% → 61%,52%]
- equation $\underline x$ (36pt, #80b9ff) [43%,62% → 44%,64%]
- text 36pt [47%,40% → 53%,44%]: Interval
- **Builds:** click 1: text 36pt — slides in; click 2: rounded box (outline) — fades up from dark; with previous: text 36pt — fades up from dark; with previous: equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ — fades up from dark; with previous: arrow #ffffff — fades up from dark; click 3: equation $\underline x$ — fades up from dark; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 8
- rounded box (outline) [36%,35% → 64%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- arrow #ffffff [40%,56% → 60%,61%]
- line #80b9ff [42%,56% → 45%,61%]
- line #80b9ff [56%,56% → 58%,61%]
- line #80b9ff [44%,56% → 57%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [40%,49% → 61%,52%]
- equation $\underline x$ (36pt, #80b9ff) [43%,62% → 44%,64%]
- equation $\overline x$ (36pt, #80b9ff) [56%,62% → 57%,64%]
- text 36pt [47%,40% → 53%,44%]: Interval
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 9
- rounded box (outline) [36%,35% → 64%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- arrow #ffffff [40%,56% → 60%,61%]
- line #80b9ff [42%,56% → 45%,61%]
- line #80b9ff [56%,56% → 58%,61%]
- line #80b9ff [44%,56% → 57%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [40%,49% → 61%,52%]
- equation $\underline x$ (36pt, #80b9ff) [43%,62% → 44%,64%]
- equation $\overline x$ (36pt, #80b9ff) [56%,62% → 57%,64%]
- text 36pt [47%,40% → 53%,44%]: Interval
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 10
- rounded box (outline) [18%,35% → 47%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- arrow #ffffff [23%,56% → 42%,61%]
- line #80b9ff [25%,56% → 27%,61%]
- line #80b9ff [38%,56% → 41%,61%]
- line #80b9ff [26%,56% → 39%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [22%,49% → 44%,52%]
- equation $\underline x$ (36pt, #80b9ff) [26%,62% → 27%,64%]
- equation $\overline x$ (36pt, #80b9ff) [39%,62% → 40%,64%]
- text 36pt [29%,40% → 36%,44%]: Interval
- rounded box (outline) [54%,29% → 83%,88%]
- text 36pt [64%,34% → 73%,39%]: Interval Box
- equation $[\mathbf x] = [x_1] \times [x_2] \times \cdots \times [x_n]$ (36pt, #80b9ff) [58%,42% → 79%,45%]

## Slide 11
- rounded box (outline) [18%,35% → 47%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- group [23%,56% → 42%,61%]
  - arrow #ffffff [23%,56% → 42%,61%]
  - line #80b9ff [25%,56% → 27%,61%]
  - line #80b9ff [38%,56% → 41%,61%]
  - line #80b9ff [26%,56% → 39%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [22%,49% → 44%,52%]
- equation $\underline x$ (36pt, #80b9ff) [26%,62% → 27%,64%]
- equation $\overline x$ (36pt, #80b9ff) [39%,62% → 40%,64%]
- text 36pt [29%,40% → 36%,44%]: Interval
- rounded box (outline) [54%,29% → 83%,88%]
- text 36pt [64%,34% → 73%,39%]: Interval Box
- group [23%,56% → 42%,61%]
  - arrow #ffffff [23%,56% → 42%,61%]
  - line #80b9ff [25%,56% → 27%,61%]
  - line #80b9ff [38%,56% → 41%,61%]
  - line #80b9ff [26%,56% → 39%,61%]
- group [23%,56% → 42%,61%]
  - arrow #ffffff [23%,56% → 42%,61%]
  - line #80b9ff [25%,56% → 27%,61%]
  - line #80b9ff [38%,56% → 41%,61%]
  - line #80b9ff [26%,56% → 39%,61%]
- equation $[\mathbf x] = [x_1] \times [x_2] \times \cdots \times [x_n]$ (36pt, #80b9ff) [58%,42% → 79%,45%]
- text 36pt [60%,50% → 74%,54%]: Cartesian product
- arrow #ffffff [65%,46% → 68%,50%]
- **Builds:** then: arrow #ffffff — draws in; with previous: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 12
- rounded box (outline) [18%,35% → 47%,72%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [19%,13% → 82%,17%]: We just saw that we [[cannot|#fab0ae]] propagate [[arbitrary polytopes|#fab0ae]] through nonlinear systems.
- text 36pt [19%,19% → 82%,23%]: We [[can|#80cfb9]] propagate [[intervals|#80cfb9]]!
- group [23%,56% → 42%,61%]
  - arrow #ffffff [23%,56% → 42%,61%]
  - line #80b9ff [25%,56% → 27%,61%]
  - line #80b9ff [38%,56% → 41%,61%]
  - line #80b9ff [26%,56% → 39%,61%]
- equation $[x] = [\underline x, \overline x] = \{x \mid \underline x \leq x \leq \overline x\}$ (36pt, #80b9ff) [22%,49% → 44%,52%]
- equation $\underline x$ (36pt, #80b9ff) [26%,62% → 27%,64%]
- equation $\overline x$ (36pt, #80b9ff) [39%,62% → 40%,64%]
- text 36pt [29%,40% → 36%,44%]: Interval
- rounded box (outline) [54%,29% → 83%,88%]
- text 36pt [64%,34% → 73%,39%]: Interval Box
- group [59%,77% → 78%,82%]
  - arrow #ffffff [59%,77% → 78%,82%]
  - line #80b9ff [61%,77% → 63%,82%]
  - line #80b9ff [74%,77% → 77%,82%]
  - line #80b9ff [62%,77% → 75%,81%]
- group [50%,62% → 70%,67%]
  - arrow #ffffff [50%,62% → 70%,67%]
  - line #80b9ff [53%,62% → 55%,67%]
  - line #80b9ff [66%,62% → 68%,67%]
  - line #80b9ff [54%,62% → 67%,67%]
- equation $[\mathbf x] = [x_1] \times [x_2] \times \cdots \times [x_n]$ (36pt, #80b9ff) [58%,42% → 79%,45%]
- equation $[x_1]$ (36pt, #80b9ff) [68%,81% → 70%,84%]
- equation $[x_2]$ (36pt, #80b9ff) [57%,63% → 59%,66%]
- filled shape #80b9ff [62%,48% → 75%,79%]
- filled shape #80b9ff [62%,49% → 75%,80%]
- outlined shape #80b9ff [62%,52% → 75%,76%]
- equation $[\mathbf x] = [x_1] \times [x_2]$ (29pt, #000000) [64%,63% → 73%,66%]
- text 36pt [60%,89% → 77%,94%]: a.k.a. hyperrectangle!
- group [15%,78% → 50%,91%]
  - rounded box (filled #424242) [15%,78% → 50%,91%]
  - text 36pt [16%,80% → 49%,89%]: Instead of doing arithmetic on single points, we will do [[arithmetic on intervals|#80b9ff]]!
- **Builds:** click 1: filled shape #80b9ff — wipes in; with previous: filled shape #80b9ff — wipes in; then: outlined shape #80b9ff — appears; with previous: equation $[\mathbf x] = [x_1] \times [x_2]$ — appears; click 2: text 36pt — slides in; click 3: group — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 13
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- group [26%,35% → 45%,39%]
  - arrow #ffffff [26%,35% → 45%,39%]
  - line #80b9ff [28%,35% → 30%,39%]
  - line #80b9ff [41%,35% → 43%,39%]
  - line #80b9ff [29%,35% → 42%,39%]
- group [55%,35% → 74%,39%]
  - arrow #ffffff [55%,35% → 74%,39%]
  - line #80b9ff [57%,35% → 60%,39%]
  - line #80b9ff [70%,35% → 73%,39%]
  - line #80b9ff [58%,35% → 72%,39%]
- text 36pt [48%,13% → 52%,18%]: Let’s add two intervals to each other!
- equation $[x]$ (36pt, #80b9ff) [34%,33% → 36%,35%]
- equation $[y]$ (36pt, #80b9ff) [64%,33% → 66%,36%]
- equation $\underline x=-1$ (29pt, #80b9ff) [27%,40% → 31%,43%]
- equation $\overline x=1$ (29pt, #80b9ff) [40%,40% → 44%,42%]
- equation $\underline y=2$ (29pt, #80b9ff) [56%,40% → 60%,43%]
- equation $\overline y=4$ (29pt, #80b9ff) [70%,40% → 73%,43%]
- arrow #ffffff [19%,57% → 81%,61%]
- equation $+$ (36pt, #ffffff) [49%,36% → 51%,38%]
- equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [34%,20% → 66%,27%]
- equation $[x] + [y]$ (36pt, #80b9ff) [47%,52% → 53%,55%]
- vector icon `shape-be121871.svg` [31%,36% → 32%,38%]
- vector icon `shape-be121871.svg` [67%,36% → 68%,38%]
- **Builds:** click 1: outlined shape #ffffff — fades up from dark; with previous: equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ — fades up from dark; click 2: arrow #ffffff — draws in; with previous: equation $[x] + [y]$ — fades up from dark; click 3: vector icon `shape-be121871.svg` — fades up from dark; with previous: vector icon `shape-be121871.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 14
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- group [26%,35% → 45%,39%]
  - arrow #ffffff [26%,35% → 45%,39%]
  - line #80b9ff [28%,35% → 30%,39%]
  - line #80b9ff [41%,35% → 43%,39%]
  - line #80b9ff [29%,35% → 42%,39%]
- group [55%,35% → 74%,39%]
  - arrow #ffffff [55%,35% → 74%,39%]
  - line #80b9ff [57%,35% → 60%,39%]
  - line #80b9ff [70%,35% → 73%,39%]
  - line #80b9ff [58%,35% → 72%,39%]
- text 36pt [48%,13% → 52%,18%]: Let’s add two intervals to each other!
- equation $[x]$ (36pt, #80b9ff) [34%,33% → 36%,35%]
- equation $[y]$ (36pt, #80b9ff) [64%,33% → 66%,36%]
- equation $\underline x=-1$ (29pt, #80b9ff) [27%,40% → 31%,43%]
- equation $\overline x=1$ (29pt, #80b9ff) [40%,40% → 44%,42%]
- equation $\underline y=2$ (29pt, #80b9ff) [56%,40% → 60%,43%]
- equation $\overline y=4$ (29pt, #80b9ff) [70%,40% → 73%,43%]
- arrow #ffffff [19%,57% → 81%,61%]
- equation $+$ (36pt, #ffffff) [49%,36% → 51%,38%]
- equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [34%,20% → 66%,27%]
- equation $[x] + [y]$ (36pt, #80b9ff) [47%,52% → 53%,55%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [41%,36% → 42%,38%]
- vector icon `shape-be121871.svg` [70%,36% → 71%,38%]
- **Builds:** click 1: vector icon `shape-be121871.svg` — fades up from dark; with previous: vector icon `shape-be121871.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 15
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- group [26%,35% → 45%,39%]
  - arrow #ffffff [26%,35% → 45%,39%]
  - line #80b9ff [28%,35% → 30%,39%]
  - line #80b9ff [41%,35% → 43%,39%]
  - line #80b9ff [29%,35% → 42%,39%]
- group [55%,35% → 74%,39%]
  - arrow #ffffff [55%,35% → 74%,39%]
  - line #80b9ff [57%,35% → 60%,39%]
  - line #80b9ff [70%,35% → 73%,39%]
  - line #80b9ff [58%,35% → 72%,39%]
- text 36pt [48%,13% → 52%,18%]: Let’s add two intervals to each other!
- equation $[x]$ (36pt, #80b9ff) [34%,33% → 36%,35%]
- equation $[y]$ (36pt, #80b9ff) [64%,33% → 66%,36%]
- equation $\underline x=-1$ (29pt, #80b9ff) [27%,40% → 31%,43%]
- equation $\overline x=1$ (29pt, #80b9ff) [40%,40% → 44%,42%]
- equation $\underline y=2$ (29pt, #80b9ff) [56%,40% → 60%,43%]
- equation $\overline y=4$ (29pt, #80b9ff) [70%,40% → 73%,43%]
- arrow #ffffff [19%,57% → 81%,61%]
- equation $+$ (36pt, #ffffff) [49%,36% → 51%,38%]
- equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [34%,20% → 66%,27%]
- equation $[x] + [y]$ (36pt, #80b9ff) [47%,52% → 53%,55%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [30%,36% → 31%,38%]
- vector icon `shape-be121871.svg` [62%,36% → 63%,38%]
- vector icon `shape-be121871.svg` [69%,58% → 70%,60%]
- vector icon `shape-be121871.svg` [69%,58% → 70%,60%]
- **Builds:** click 1: vector icon `shape-be121871.svg` — fades up from dark; with previous: vector icon `shape-be121871.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 16
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- group [26%,35% → 45%,39%]
  - arrow #ffffff [26%,35% → 45%,39%]
  - line #80b9ff [28%,35% → 30%,39%]
  - line #80b9ff [41%,35% → 43%,39%]
  - line #80b9ff [29%,35% → 42%,39%]
- group [55%,35% → 74%,39%]
  - arrow #ffffff [55%,35% → 74%,39%]
  - line #80b9ff [57%,35% → 60%,39%]
  - line #80b9ff [70%,35% → 73%,39%]
  - line #80b9ff [58%,35% → 72%,39%]
- text 36pt [48%,13% → 52%,18%]: Let’s add two intervals to each other!
- equation $[x]$ (36pt, #80b9ff) [34%,33% → 36%,35%]
- equation $[y]$ (36pt, #80b9ff) [64%,33% → 66%,36%]
- equation $\underline x=-1$ (29pt, #80b9ff) [27%,40% → 31%,43%]
- equation $\overline x=1$ (29pt, #80b9ff) [40%,40% → 44%,42%]
- equation $\underline y=2$ (29pt, #80b9ff) [56%,40% → 60%,43%]
- equation $\overline y=4$ (29pt, #80b9ff) [70%,40% → 73%,43%]
- arrow #ffffff [19%,57% → 81%,61%]
- equation $+$ (36pt, #ffffff) [49%,36% → 51%,38%]
- equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [34%,20% → 66%,27%]
- equation $[x] + [y]$ (36pt, #80b9ff) [47%,52% → 53%,55%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [53%,58% → 54%,60%]
- vector icon `shape-be121871.svg` [35%,58% → 36%,60%]
- vector icon `shape-be121871.svg` [35%,58% → 36%,60%]
- vector icon `shape-be121871.svg` [69%,58% → 70%,60%]
- vector icon `shape-be121871.svg` [69%,58% → 70%,60%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 17
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- group [26%,35% → 45%,39%]
  - arrow #ffffff [26%,35% → 45%,39%]
  - line #80b9ff [28%,35% → 30%,39%]
  - line #80b9ff [41%,35% → 43%,39%]
  - line #80b9ff [29%,35% → 42%,39%]
- group [55%,35% → 74%,39%]
  - arrow #ffffff [55%,35% → 74%,39%]
  - line #80b9ff [57%,35% → 60%,39%]
  - line #80b9ff [70%,35% → 73%,39%]
  - line #80b9ff [58%,35% → 72%,39%]
- text 36pt [48%,13% → 52%,18%]: Let’s add two intervals to each other!
- equation $[x]$ (36pt, #80b9ff) [34%,33% → 36%,35%]
- equation $[y]$ (36pt, #80b9ff) [64%,33% → 66%,36%]
- equation $\underline x=-1$ (29pt, #80b9ff) [27%,40% → 31%,43%]
- equation $\overline x=1$ (29pt, #80b9ff) [40%,40% → 44%,42%]
- equation $\underline y=2$ (29pt, #80b9ff) [56%,40% → 60%,43%]
- equation $\overline y=4$ (29pt, #80b9ff) [70%,40% → 73%,43%]
- arrow #ffffff [19%,57% → 81%,61%]
- equation $+$ (36pt, #ffffff) [49%,36% → 51%,38%]
- equation $[x] + [y] = \{ x + y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [34%,20% → 66%,27%]
- equation $[x] + [y]$ (36pt, #80b9ff) [47%,52% → 53%,55%]
- line #80b9ff [26%,57% → 73%,61%]
- line #80b9ff [24%,57% → 27%,61%]
- line #80b9ff [72%,57% → 74%,61%]
- equation $\underline{x+y} =$ (27pt, #80b9ff) [23%,63% → 28%,65%]
- equation $\overline{x+y} =$ (27pt, #80b9ff) [69%,62% → 74%,64%]
- equation $-1 + 2 = 1$ (26pt, #80b9ff) [28%,63% → 34%,65%]
- equation $1 + 4 = 5$ (26pt, #80b9ff) [74%,62% → 79%,64%]
- equation $[x] + [y] = [\underline x + \underline y, \overline x + \overline y]$ (36pt, #ffffff) [41%,74% → 59%,77%]
- outlined shape #ffffff [38%,72% → 62%,79%]
- text 36pt [48%,84% → 52%,88%]: This operation is known as the [[interval counterpart|#80b9ff]] of addition.
- **Builds:** click 1: equation $1 + 4 = 5$ — slides in; with previous: equation $-1 + 2 = 1$ — slides in; click 2: outlined shape #ffffff — fades up from dark; with previous: equation $[x] + [y] = [\underline x + \underline y, \overline x + \overline y]$ — fades up from dark; click 3: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 18
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can define [[interval counterparts|#80b9ff]] for addition, subtraction, multiplication and division!
- equation $[x] + [y] = [\underline x + \underline y, \overline x + \overline y]$ (36pt, #ffffff) [28%,44% → 46%,47%]
- equation $[x] \circ [y] = \{x \circ y \mid x \in [x], y \in [y]\}$ (36pt, #ffffff) [37%,22% → 63%,25%]
- outlined shape #ffffff [26%,42% → 75%,66%]
- arrow #80b9ff [42%,27% → 48%,31%]
- arrow #80b9ff [39%,27% → 44%,31%]
- text 30pt [41%,33% → 45%,37%]: {Insert your favorite operator here!|#80b9ff}
- equation $[x] - [y] = [\underline x - \overline y, \overline x - \underline y]$ (36pt, #ffffff) [28%,49% → 46%,53%]
- equation $[x] \times [y] = [\min(\underline x \underline y, \underline x \overline y, \overline x \underline y, \overline x \overline y), \max(\underline x \underline y, \underline x \overline y, \overline x \underline y, \overline x \overline y)]$ (36pt, #ffffff) [28%,55% → 66%,59%]
- equation $[x] \ /\ [y] = [\min(\underline x / \underline y, \underline x / \overline y, \overline x / \underline y, \overline x / \overline y), \max(\underline x / \underline y, \underline x / \overline y, \overline x / \underline y, \overline x / \overline y)]$ (36pt, #ffffff) [28%,61% → 71%,64%]
- outlined shape #ffffff [36%,21% → 65%,26%]
- **Builds:** click 1: text 30pt — fades up from dark; with previous: arrow #80b9ff — draws in; with previous: arrow #80b9ff — draws in; click 2: outlined shape #ffffff — fades up from dark; with previous: equation $[x] + [y] = [\underline x + \underline y, \overline x + \overline y]$ — fades up from dark; with previous: equation $[x] - [y] = [\underline x - \overline y, \overline x - \underline y]$ — fades up from dark; with previous: equation $[x] \times [y] = [\min(\underline x \underline y, \underline x \overline y, \overline x \underline y, \overline x \overline y), \max(\underline x \underline y, \underline x \overline y, \overline x \underline y, \overline x \overline y)]$ — fades up from dark; with previous: equation $[x] \ /\ [y] = [\min(\underline x / \underline y, \underline x / \overline y, \overline x / \underline y, \overline x / \overline y), \max(\underline x / \underline y, \underline x / \overline y, \overline x / \underline y, \overline x / \overline y)]$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 19
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- image `test-32619.svg` [27%,33% → 62%,93%]
- line #80b9ff [46%,78% → 55%,82%]
- line #80b9ff [54%,78% → 56%,82%]
- line #80b9ff [45%,78% → 47%,82%]
- equation $[x]$ (36pt, #80b9ff) [50%,76% → 52%,78%]
- line #80b9ff [44%,71% → 49%,75%]
- line #80b9ff [47%,61% → 64%,65%]
- line #80b9ff [37%,66% → 46%,70%]
- line #80b9ff [37%,46% → 55%,50%]
- line #80b9ff [32%,56% → 43%,60%]
- line #80b9ff [36%,66% → 38%,70%]
- line #80b9ff [36%,46% → 38%,50%]
- equation $\exp([x])$ (36pt, #80b9ff) [38%,57% → 44%,60%]
- filled shape #80b9ff [37%,48% → 62%,68%]
- **Builds:** click 1: image `test-32619.svg` — fades up from dark; click 2: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: equation $[x]$ — fades up from dark; click 3: line #80b9ff — draws in; with previous: line #80b9ff — draws in; click 4: line #80b9ff — draws in; with previous: line #80b9ff — draws in; then: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: equation $\exp([x])$ — fades up from dark; click 5: filled shape #80b9ff — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 20
- rounded box (filled #424242) [54%,46% → 89%,70%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- image `test-32619.svg` [13%,33% → 47%,93%]
- line #80b9ff [32%,78% → 40%,82%]
- line #80b9ff [39%,78% → 42%,82%]
- line #80b9ff [30%,78% → 33%,82%]
- equation $[x]$ (36pt, #80b9ff) [35%,76% → 37%,78%]
- line #80b9ff [29%,71% → 34%,75%]
- line #80b9ff [32%,61% → 49%,65%]
- line #80b9ff [23%,66% → 32%,70%]
- line #80b9ff [23%,46% → 40%,50%]
- line #80b9ff [17%,56% → 28%,60%]
- line #80b9ff [22%,66% → 24%,70%]
- line #80b9ff [22%,46% → 24%,50%]
- equation $\exp([x])$ (36pt, #80b9ff) [24%,57% → 29%,60%]
- filled shape #80b9ff [23%,48% → 47%,68%]
- text 36pt [57%,49% → 86%,61%]: In general, the interval counterpart of a [[monotonically increasing function|#80b9ff]] (e.g. exp, log, square root) is
- equation $f([x]) = [f(\underline x), f(\overline x)]$ (44pt, #ffffff) [63%,63% → 81%,67%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 21
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- text 36pt [48%,29% → 52%,34%]: Some functions require us to consider multiple cases:
- image `test-32745.svg` [34%,38% → 62%,85%]
- line #80b9ff [43%,72% → 56%,76%]
- line #80b9ff [54%,72% → 57%,76%]
- line #80b9ff [42%,72% → 44%,76%]
- equation $[x]$ (36pt, #80b9ff) [48%,70% → 50%,73%]
- line #80b9ff [38%,62% → 47%,66%]
- line #80b9ff [54%,67% → 57%,71%]
- **Builds:** click 1: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: equation $[x]$ — fades up from dark; click 2: line #80b9ff — draws in; with previous: line #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 22
- image `test-32745.svg` [16%,38% → 44%,85%]
- filled shape #80b9ff [22%,56% → 43%,74%]
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- text 36pt [48%,29% → 52%,34%]: Some functions require us to consider multiple cases:
- line #80b9ff [25%,72% → 37%,76%]
- line #80b9ff [36%,72% → 38%,76%]
- line #80b9ff [24%,72% → 26%,76%]
- equation $[x]$ (36pt, #80b9ff) [30%,70% → 32%,73%]
- line #80b9ff [20%,62% → 29%,66%]
- line #80b9ff [36%,67% → 39%,71%]
- equation $[x]^2 = \begin{cases} [\min(\underline x^2, \overline x^2), \max(\underline x^2, \overline x^2)] & \text{if } 0 \notin [x] \\ [0, \max(\underline x^2, \overline x^2)] & \text{otherwise} \end{cases}$ (36pt, #ffffff) [47%,53% → 82%,63%]
- filled shape #e69f00 [54%,58% → 82%,63%]
- line #80b9ff [17%,63% → 27%,67%]
- line #80b9ff [21%,72% → 23%,76%]
- line #80b9ff [21%,54% → 23%,58%]
- equation $[x]^2$ (36pt, #80b9ff) [19%,63% → 22%,67%]
- **Builds:** click 1: filled shape #e69f00 — wipes in; click 2: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: equation $[x]^2$ — fades up from dark; click 3: filled shape #80b9ff — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 23
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- image `test-32745.svg` [35%,38% → 61%,80%]
- filled shape #80b9ff [41%,54% → 59%,70%]
- line #80b9ff [43%,68% → 55%,72%]
- line #80b9ff [54%,68% → 56%,72%]
- line #80b9ff [42%,68% → 44%,72%]
- equation $[x]$ (32pt, #80b9ff) [48%,67% → 50%,69%]
- line #80b9ff [39%,59% → 48%,63%]
- line #80b9ff [53%,64% → 56%,68%]
- line #80b9ff [37%,60% → 46%,64%]
- line #80b9ff [40%,68% → 42%,72%]
- line #80b9ff [40%,52% → 42%,56%]
- equation $[x]^2$ (32pt, #80b9ff) [38%,61% → 41%,64%]
- group [6%,35% → 34%,81%]
  - image `test-32619.svg` [6%,35% → 32%,81%]
  - line #80b9ff [20%,69% → 27%,73%]
  - line #80b9ff [26%,69% → 28%,73%]
  - line #80b9ff [19%,69% → 21%,73%]
  - equation $[x]$ (27pt, #80b9ff) [23%,68% → 24%,70%]
  - line #80b9ff [18%,64% → 22%,68%]
  - line #80b9ff [20%,56% → 34%,60%]
  - line #80b9ff [13%,60% → 20%,64%]
  - line #80b9ff [13%,44% → 27%,48%]
  - line #80b9ff [9%,52% → 18%,56%]
  - line #80b9ff [12%,60% → 14%,64%]
  - line #80b9ff [12%,44% → 14%,49%]
  - equation $\exp([x])$ (27pt, #80b9ff) [14%,53% → 18%,55%]
  - filled shape #80b9ff [13%,47% → 32%,62%]
- image `test-32819.svg` [63%,37% → 89%,80%]
- line #80b9ff [80%,68% → 86%,72%]
- line #80b9ff [85%,68% → 87%,72%]
- line #80b9ff [79%,68% → 81%,72%]
- line #80b9ff [79%,54% → 93%,58%]
- line #80b9ff [76%,59% → 84%,63%]
- line #80b9ff [68%,46% → 74%,50%]
- line #80b9ff [70%,52% → 72%,56%]
- line #80b9ff [70%,41% → 72%,45%]
- filled shape #80b9ff [71%,43% → 89%,54%]
- equation $[x]$ (32pt, #80b9ff) [82%,67% → 84%,69%]
- equation $\sin([x])$ (32pt, #80b9ff) [71%,47% → 76%,50%]
- rounded box (outline) [3%,31% → 97%,84%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 24
- heading (spaced caps) 36pt [36%,5% → 64%,10%]: INTERVAL ARITHMETIC
- text 36pt [48%,13% → 52%,18%]: We can also define [[interval counterparts|#80b9ff]] for other elementary functions.
- outlined shape #ffffff [39%,21% → 61%,26%]
- equation $f([x]) = [\{f(x) \mid x \in [x]\}]$ (36pt, #ffffff) [41%,22% → 59%,25%]
- image `test-32745.svg` [35%,38% → 61%,80%]
- filled shape #80b9ff [41%,54% → 59%,70%]
- line #80b9ff [43%,68% → 55%,72%]
- line #80b9ff [54%,68% → 56%,72%]
- line #80b9ff [42%,68% → 44%,72%]
- equation $[x]$ (32pt, #80b9ff) [48%,67% → 50%,69%]
- line #80b9ff [39%,59% → 48%,63%]
- line #80b9ff [53%,64% → 56%,68%]
- line #80b9ff [37%,60% → 46%,64%]
- line #80b9ff [40%,68% → 42%,72%]
- line #80b9ff [40%,52% → 42%,56%]
- equation $[x]^2$ (32pt, #80b9ff) [38%,61% → 41%,64%]
- group [6%,35% → 34%,81%]
  - image `test-32619.svg` [6%,35% → 32%,81%]
  - line #80b9ff [20%,69% → 27%,73%]
  - line #80b9ff [26%,69% → 28%,73%]
  - line #80b9ff [19%,69% → 21%,73%]
  - equation $[x]$ (27pt, #80b9ff) [23%,68% → 24%,70%]
  - line #80b9ff [18%,64% → 22%,68%]
  - line #80b9ff [20%,56% → 34%,60%]
  - line #80b9ff [13%,60% → 20%,64%]
  - line #80b9ff [13%,44% → 27%,48%]
  - line #80b9ff [9%,52% → 18%,56%]
  - line #80b9ff [12%,60% → 14%,64%]
  - line #80b9ff [12%,44% → 14%,49%]
  - equation $\exp([x])$ (27pt, #80b9ff) [14%,53% → 18%,55%]
  - filled shape #80b9ff [13%,47% → 32%,62%]
- image `test-32819.svg` [63%,37% → 89%,80%]
- line #80b9ff [80%,68% → 86%,72%]
- line #80b9ff [85%,68% → 87%,72%]
- line #80b9ff [79%,68% → 81%,72%]
- line #80b9ff [79%,54% → 93%,58%]
- line #80b9ff [76%,59% → 84%,63%]
- line #80b9ff [68%,46% → 74%,50%]
- line #80b9ff [70%,52% → 72%,56%]
- line #80b9ff [70%,41% → 72%,45%]
- filled shape #80b9ff [71%,43% → 89%,54%]
- equation $[x]$ (32pt, #80b9ff) [82%,67% → 84%,69%]
- equation $\sin([x])$ (32pt, #80b9ff) [71%,47% → 76%,50%]
- rounded box (outline) [3%,31% → 97%,84%]
- text 36pt [43%,34% → 57%,38%]: And many others!
- image `pasted-image-32893.png` [33%,40% → 67%,71%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 25
- text 36pt [33%,48% → 67%,52%]: Let’s remind ourselves of the goal…
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 26
- rounded box (outline) [24%,14% → 76%,30%]
- text 36pt [36%,5% → 64%,10%]: Let’s remind ourselves of the goal…
- text 36pt [27%,17% → 73%,21%]: We want to compute the reachable set at a particular depth:
- equation $\mathcal R_d = \{\mathbf s_d \mid \mathbf s_d = \operatorname{Reach}(\mathbf s, \mathbf x_{1:d}), \mathbf s \in \mathcal S, \mathbf x_t \in \mathcal X_t, t \in 1:d\}$ (36pt, #ffffff) [29%,24% → 71%,27%]
- text 36pt [39%,39% → 63%,48%]: [[In the previous lecture, this function was nice and linear.|#80b9ff]]
- arrow #80b9ff [44%,31% → 53%,35%]
- equation $(\mathbf T_s + \mathbf T_a \mathbf \Pi_o \mathbf O_s) \mathbf s + \mathbf T_a \mathbf \Pi_o \mathbf x_o + \mathbf T_a \mathbf x_a + \mathbf x_s$ (36pt, #80b9ff) [36%,49% → 65%,53%]
- text 36pt [12%,39% → 36%,48%]: [[In many real world systems, this function is nonlinear.|#80b9ff]]
- **Builds:** click 1: text 36pt — fades up from dark; with previous: equation $(\mathbf T_s + \mathbf T_a \mathbf \Pi_o \mathbf O_s) \mathbf s + \mathbf T_a \mathbf \Pi_o \mathbf x_o + \mathbf T_a \mathbf x_a + \mathbf x_s$ — fades up from dark; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 27
- rounded box (filled #ffa4e7) [30%,53% → 72%,73%]
- rounded box (outline) [24%,14% → 76%,30%]
- text 36pt [36%,5% → 64%,10%]: Let’s remind ourselves of the goal…
- text 36pt [27%,17% → 73%,21%]: We want to compute the reachable set at a particular depth:
- equation $\mathcal R_d = \{\mathbf s_d \mid \mathbf s_d = \operatorname{Reach}(\mathbf s, \mathbf x_{1:d}), \mathbf s \in \mathcal S, \mathbf x_t \in \mathcal X_t, t \in 1:d\}$ (36pt, #ffffff) [29%,24% → 71%,27%]
- text 36pt [64%,39% → 88%,48%]: [[In the previous lecture, this function was nice and linear.|#80b9ff]]
- arrow #80b9ff [44%,31% → 53%,35%]
- equation $(\mathbf T_s + \mathbf T_a \mathbf \Pi_o \mathbf O_s) \mathbf s + \mathbf T_a \mathbf \Pi_o \mathbf x_o + \mathbf T_a \mathbf x_a + \mathbf x_s$ (36pt, #80b9ff) [62%,49% → 91%,53%]
- text 36pt [39%,39% → 64%,48%]: [[In many real world systems, this function is nonlinear.|#80b9ff]]
- text 36pt [41%,55% → 59%,60%]: {e.g. inverted pendulum|#000000}
- equation $\theta^\prime = \theta + 0.05 \omega^\prime$ (36pt, #000000) [45%,62% → 57%,64%]
- equation $\omega^\prime = -2.25\theta + 15 \sin \theta -0.2\omega -2.25x_\theta -1.2x_\omega$ (36pt, #000000) [33%,67% → 69%,70%]
- text 36pt [12%,76% → 88%,80%]: But this function is [[more complex |#ffa4e7]]than the elementary functions we were using for interval arithmetic.
- **Builds:** click 1: equation $(\mathbf T_s + \mathbf T_a \mathbf \Pi_o \mathbf O_s) \mathbf s + \mathbf T_a \mathbf \Pi_o \mathbf x_o + \mathbf T_a \mathbf x_a + \mathbf x_s$ — slides in; click 2: rounded box (filled #ffa4e7) — fades up from dark; with previous: text 36pt — fades up from dark; with previous: equation $\theta^\prime = \theta + 0.05 \omega^\prime$ — fades up from dark; with previous: equation $\omega^\prime = -2.25\theta + 15 \sin \theta -0.2\omega -2.25x_\theta -1.2x_\omega$ — fades up from dark; click 3: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 28
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 29
- arrow #ffffff [31%,56% → 69%,61%]
- line #c3b8ff [41%,56% → 64%,61%]
- heading (spaced caps) 36pt [35%,4% → 65%,9%]: INCLUSION FUNCTIONS
- text 36pt [48%,12% → 52%,16%]: For more complex functions, the best we can do is define an [[inclusion function|#c3b8ff]].
- text 36pt [48%,19% → 52%,24%]: It outputs an interval that is [[guaranteed to contain|#c3b8ff]] the interval from the interval counterpart:
- equation $f([x]) \subseteq [f]([x])$ (36pt, #ffffff) [44%,28% → 56%,31%]
- text 30pt [33%,39% → 47%,43%]: {Interval Counterpart|#80b9ff}
- text 30pt [53%,39% → 66%,43%]: {Inclusion Function|#c3b8ff}
- arrow #80b9ff [41%,34% → 47%,38%]
- arrow #c3b8ff [52%,34% → 59%,38%]
- line #80b9ff [42%,56% → 45%,61%]
- line #80b9ff [56%,56% → 58%,61%]
- line #80b9ff [44%,56% → 57%,61%]
- line #c3b8ff [63%,56% → 66%,61%]
- line #c3b8ff [40%,56% → 43%,61%]
- equation $f([x])$ (27pt, #80b9ff) [48%,54% → 51%,57%]
- equation $[f]([x])$ (27pt, #c3b8ff) [59%,54% → 63%,57%]
- text 36pt [33%,68% → 67%,73%]: i.e. it represents an [[overapproximate|#c3b8ff]] interval!
- outlined shape #ffffff [32%,68% → 68%,73%]
- **Builds:** click 1: text 36pt — fades up from dark; with previous: equation $f([x]) \subseteq [f]([x])$ — fades up from dark; click 2: text 30pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 3: text 30pt — fades up from dark; with previous: arrow #c3b8ff — draws in; click 4: arrow #ffffff — draws in; click 5: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in; then: equation $f([x])$ — appears; click 6: line #c3b8ff — draws in; with previous: line #c3b8ff — draws in; with previous: line #c3b8ff — draws in; then: equation $[f]([x])$ — appears; click 7: text 36pt — fades up from dark; click 8: outlined shape #ffffff — LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 30
- heading (spaced caps) 36pt [35%,4% → 65%,9%]: INCLUSION FUNCTIONS
- text 36pt [48%,12% → 52%,16%]: For more complex functions, the best we can do is define an [[inclusion function|#c3b8ff]].
- text 36pt [48%,19% → 52%,24%]: It outputs an interval that is [[guaranteed to contain|#c3b8ff]] the interval from the interval counterpart:
- rounded box (outline) [7%,36% → 93%,94%]
- text 36pt [48%,38% → 52%,43%]: In the context of reachability:
- equation $\operatorname{Reach}(\mathbf s, \mathbf x_{1:d})$ (36pt, #ffffff) [15%,54% → 25%,57%]
- equation $= r(\mathbf s, \mathbf x_{1:d})$ (36pt, #ffffff) [26%,54% → 34%,57%]
- equation $= \begin{bmatrix} r_1(\mathbf s, \mathbf x_{1:d}) \\ \vdots \\ r_n(\mathbf s, \mathbf x_{1:d}) \end{bmatrix}$ (36pt, #ffffff) [35%,48% → 45%,62%]
- rounded box (filled #ffa4e7) [11%,67% → 49%,88%]
- text 36pt [21%,69% → 39%,73%]: {e.g. inverted pendulum|#000000}
- text 32pt [12%,74% → 48%,86%]: {$r_1(\mathbf s, \mathbf x_{1:d})$ provides a function for the value of $\theta$ at depth $d$, and $r_2(\mathbf s, \mathbf x_{1:d})$ provides a function for the value of $\omega$ at depth $d$.|#000000}
- shape (outline) [51%,61% → 57%,69%]
- equation $\begin{bmatrix} [r_1]([\mathbf s], [\mathbf x_{1:d}]) \\ \vdots \\ [r_n]([\mathbf s], [\mathbf x_{1:d}]) \end{bmatrix}$ (36pt, #ffffff) [59%,58% → 71%,72%]
- text 36pt [71%,57% → 91%,73%]: represents an overapproximate hyperrectangular reachable set.
- group [51%,78% → 91%,87%]
  - rounded box (filled #424242) [51%,78% → 91%,87%]
  - text 36pt [53%,78% → 89%,87%]: TLDR: we [[pass intervals through the system|#80b9ff]] and get out an overapproximate reachable set.
- text 36pt [33%,26% → 67%,31%]: i.e. it represents an [[overapproximate|#c3b8ff]] interval!
- outlined shape #ffffff [32%,26% → 68%,31%]
- **Builds:** click 1: equation $\operatorname{Reach}(\mathbf s, \mathbf x_{1:d})$ — appears; click 2: equation $= r(\mathbf s, \mathbf x_{1:d})$ — slides in; click 3: equation $= \begin{bmatrix} r_1(\mathbf s, \mathbf x_{1:d}) \\ \vdots \\ r_n(\mathbf s, \mathbf x_{1:d}) \end{bmatrix}$ — slides in; click 4: rounded box (filled #ffa4e7) — fades up from dark; with previous: text 36pt — fades up from dark; with previous: text 32pt — fades up from dark; click 5: shape (outline) — wipes in; with previous: equation $\begin{bmatrix} [r_1]([\mathbf s], [\mathbf x_{1:d}]) \\ \vdots \\ [r_n]([\mathbf s], [\mathbf x_{1:d}]) \end{bmatrix}$ — slides in; with previous: text 36pt — slides in; click 6: group — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 31
- text 36pt [31%,48% → 69%,52%]: So how do I create an inclusion function?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 32
- text 36pt [34%,46% → 66%,50%]: {So how do I create an inclusion function?|#929292}
- text 36pt [34%,50% → 66%,54%]: There are a [[few different|#80b9ff]] ways.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 33
- image `test-33313.svg` [9%,15% → 55%,85%]
- equation $x$ (62pt, #ffffff) [66%,24% → 68%,26%]
- text 40pt [48%,4% → 52%,9%]: Natural Inclusion Function
- shape (outline) [69%,38% → 80%,45%]
- text 36pt [74%,33% → 87%,45%]: {natural inclusion function|#c3b8ff}
- equation $) =$ (62pt, #ffffff) [68%,22% → 73%,27%]
- equation $- \sin($ (62pt, #ffffff) [76%,22% → 82%,27%]
- equation $)$ (62pt, #ffffff) [85%,22% → 86%,27%]
- equation $x$ (62pt, #ffffff) [73%,24% → 75%,26%]
- equation $x$ (62pt, #ffffff) [83%,24% → 84%,26%]
- equation $x$ (62pt, #ffffff) [66%,24% → 68%,26%]
- equation $) =$ (62pt, #ffffff) [68%,22% → 73%,27%]
- equation $- \sin($ (62pt, #ffffff) [76%,22% → 82%,27%]
- equation $)$ (62pt, #ffffff) [85%,22% → 86%,27%]
- equation $x$ (62pt, #ffffff) [73%,24% → 75%,26%]
- equation $x$ (62pt, #ffffff) [83%,24% → 84%,26%]
- equation $x$ (62pt, #ffffff) [66%,24% → 68%,26%]
- equation $($ (62pt, #ffffff) [65%,22% → 66%,27%]
- equation $f$ (62pt, #ffffff) [63%,22% → 65%,27%]
- equation $($ (62pt, #ffffff) [65%,22% → 66%,27%]
- equation $f$ (62pt, #ffffff) [63%,22% → 65%,27%]
- **Builds:** click 1: image `test-33313.svg` — appears; with previous: equation $- \sin($ — appears; with previous: equation $) =$ — appears; with previous: equation $)$ — appears; with previous: equation $x$ — appears; with previous: equation $x$ — appears; with previous: equation $x$ — appears; with previous: equation $- \sin($ — appears; with previous: equation $) =$ — appears; with previous: equation $)$ — appears; with previous: equation $x$ — appears; with previous: equation $x$ — appears; with previous: equation $x$ — appears; with previous: equation $f$ — appears; with previous: equation $($ — appears; with previous: equation $x$ — appears; with previous: equation $f$ — appears; with previous: equation $($ — appears; click 2: shape (outline) — wipes in; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 34
- image `test-33313.svg` [9%,15% → 55%,85%]
- equation $[\ \ ]$ (62pt, #c3b8ff) [85%,57% → 88%,62%]
- image `test-33313.svg` [9%,15% → 55%,85%]
- equation $x$ (62pt, #ffffff) [66%,24% → 68%,26%]
- text 40pt [48%,4% → 52%,9%]: Natural Inclusion Function
- shape (outline) [69%,38% → 80%,45%]
- text 36pt [74%,33% → 87%,45%]: {natural inclusion function|#c3b8ff}
- equation $($ (62pt, #ffffff) [65%,22% → 66%,27%]
- equation $) =$ (62pt, #ffffff) [68%,22% → 73%,27%]
- equation $- \sin($ (62pt, #ffffff) [76%,22% → 82%,27%]
- equation $)$ (62pt, #ffffff) [85%,22% → 86%,27%]
- equation $x$ (62pt, #ffffff) [73%,24% → 75%,26%]
- equation $x$ (62pt, #ffffff) [83%,24% → 84%,26%]
- equation $x$ (62pt, #c3b8ff) [65%,59% → 67%,61%]
- equation $f$ (62pt, #c3b8ff) [60%,57% → 62%,62%]
- equation $) =$ (62pt, #c3b8ff) [68%,57% → 73%,62%]
- equation $- \sin($ (62pt, #c3b8ff) [77%,57% → 84%,62%]
- equation $)$ (62pt, #c3b8ff) [89%,57% → 90%,62%]
- equation $x$ (62pt, #c3b8ff) [74%,59% → 75%,61%]
- equation $x$ (62pt, #c3b8ff) [86%,59% → 87%,61%]
- equation $[\ \ ]$ (62pt, #c3b8ff) [64%,57% → 68%,62%]
- equation $[\ \ ]$ (62pt, #c3b8ff) [73%,57% → 76%,62%]
- group [60%,68% → 93%,77%]
  - rounded box (filled #424242) [60%,68% → 93%,77%]
  - text 36pt [62%,69% → 92%,77%]: i.e. just replace each elementary function with its interval counterpart
- image `test-33456.svg` [9%,15% → 55%,85%]
- line #c3b8ff [22%,38% → 45%,42%]
- line #c3b8ff [23%,42% → 30%,46%]
- filled shape #80b9ff [23%,40% → 53%,44%]
- text 36pt [30%,30% → 45%,35%]: {overapproximation|#c3b8ff}
- text 36pt [30%,48% → 45%,52%]: {overapproximation|#c3b8ff}
- text 36pt [15%,87% → 85%,91%]: The natural inclusion function tends to be overly conservative due to the [[dependency effect|#c3b8ff]].
- text on a #80b9ff filled box 32pt [71%,91% → 85%,98%]: {Example 8.2|#000000}
- equation $f$ (62pt, #ffffff) [63%,22% → 65%,27%]
- equation $($ (62pt, #c3b8ff) [63%,57% → 64%,62%]
- equation $[\ \ ]$ (62pt, #c3b8ff) [59%,57% → 62%,62%]
- **Builds:** click 1: group — fades up from dark; click 2: image `test-33456.svg` — fades up from dark; click 3: line #c3b8ff — draws in; with previous: line #c3b8ff — draws in; click 4: filled shape #80b9ff — wipes in; click 5: text 36pt — fades up from dark; with previous: text 36pt — fades up from dark; click 6: text 36pt — wipes in; click 7: image `test-33313.svg` — appears; click 8: text on a #80b9ff filled box 32pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 35
- text 40pt [48%,4% → 52%,9%]: Natural Inclusion Function
- group [34%,12% → 66%,21%]
  - rounded box (filled #424242) [34%,12% → 66%,21%]
  - text 36pt [36%,12% → 65%,21%]: i.e. just replace each elementary function with its interval counterpart
- image `val-page-207.svg` (cropped: show only 10–64% across and 13–45% down of the image) [26%,25% → 74%,82%]
- image `noun-curly-bracket-1708842.png` (cropped: show only 38–60% across and 30–70% down of the image) [48%,35% → 52%,50%]
- equation $\operatorname{Reach}(\mathbf s, \mathbf x_{1:d})$ (36pt, #000000) [53%,41% → 63%,44%]
- equation $= r(\mathbf s, \mathbf x_{1:d})$ (36pt, #000000) [64%,41% → 72%,44%]
- text 36pt [48%,86% → 52%,90%]: In Julia, we can just pass intervals through all of our rollout code!
- text on a #80b9ff filled box 32pt [77%,46% → 96%,54%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: image `noun-curly-bracket-1708842.png` (cropped: show only 38–60% acro — zoom; then: equation $\operatorname{Reach}(\mathbf s, \mathbf x_{1:d})$ — appears; with previous: equation $= r(\mathbf s, \mathbf x_{1:d})$ — appears; click 2: text 36pt — flame; click 3: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 36
- text 40pt [48%,4% → 52%,9%]: Natural Inclusion Function
- text on a #80b9ff filled box 32pt [40%,12% → 60%,20%]: {Pluto Notebook!|#000000}
- video `video-33597.mp4` (plays 0.0s–4.2s, loops) [33%,40% → 67%,88%]
- text 36pt [39%,25% → 61%,29%]: Can we do better than this?
- text 36pt [31%,30% → 69%,35%]: Yep, just gotta bring back a theorem from calculus.
- **Builds:** then: video `video-33597.mp4` (plays 0.0s–4.2s, loops) — video starts; click 1: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 37
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [40%,16% → 60%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [39%,15% → 61%,20%]
- text 36pt [7%,23% → 93%,27%]: For a function $f(x)$ that is continuous and differentiable on the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(\overline x) - f(\underline x)}{\overline x - \underline x} = f^\prime (x^\prime)$ (36pt, #ffffff) [43%,30% → 57%,38%]
- text 36pt [35%,43% → 46%,51%]: {slope of the secant line|#c3b8ff}
- text 36pt [54%,43% → 65%,51%]: {slope of the tangent line|#c3b8ff}
- arrow #c3b8ff [40%,38% → 44%,42%]
- arrow #c3b8ff [56%,37% → 60%,41%]
- **Builds:** click 1: equation $\frac{f(\overline x) - f(\underline x)}{\overline x - \underline x} = f^\prime (x^\prime)$ — fades up from dark; with previous: text 36pt — fades up from dark; click 2: text 36pt — fades up from dark; with previous: arrow #c3b8ff — draws in; click 3: text 36pt — fades up from dark; with previous: arrow #c3b8ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 38
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [40%,16% → 60%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [39%,15% → 61%,20%]
- text 36pt [7%,23% → 93%,27%]: For a function $f(x)$ that is continuous and differentiable on the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(\overline x) - f(\underline x)}{\overline x - \underline x} = f^\prime (x^\prime)$ (36pt, #ffffff) [13%,31% → 27%,39%]
- text 36pt [5%,44% → 16%,52%]: {slope of the secant line|#c3b8ff}
- text 36pt [24%,44% → 35%,52%]: {slope of the tangent line|#c3b8ff}
- arrow #c3b8ff [10%,38% → 14%,43%]
- arrow #c3b8ff [26%,38% → 30%,42%]
- arrow #929292 [41%,61% → 65%,65%]
- arrow #929292 [50%,78% → 78%,82%]
- shape (outline) [49%,53% → 75%,70%]
- line #ffffff [54%,78% → 56%,82%]
- line #ffffff [72%,78% → 73%,82%]
- equation $\underline x$ (36pt, #ffffff) [55%,83% → 56%,85%]
- equation $\overline x$ (36pt, #ffffff) [72%,83% → 73%,85%]
- line #ffffff [51%,69% → 59%,73%]
- line #ffffff [64%,61% → 81%,65%]
- vector icon `shape-5335365c.svg` [72%,47% → 73%,49%]
- vector icon `shape-5335365c.svg` [54%,62% → 56%,64%]
- line #ffffff [54%,61% → 56%,65%]
- line #ffffff [72%,46% → 73%,50%]
- **Builds:** click 1: line #ffffff — draws in; with previous: line #ffffff — draws in; with previous: equation $\underline x$ — appears; with previous: equation $\overline x$ — appears; click 2: line #ffffff — draws in; with previous: line #ffffff — draws in; then: vector icon `shape-5335365c.svg` — fades up from dark; with previous: vector icon `shape-5335365c.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 39
- line #c3b8ff [54%,53% → 73%,58%]
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [40%,16% → 60%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [39%,15% → 61%,20%]
- text 36pt [7%,23% → 93%,27%]: For a function $f(x)$ that is continuous and differentiable on the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(\overline x) - f(\underline x)}{\overline x - \underline x} = f^\prime (x^\prime)$ (36pt, #ffffff) [13%,31% → 27%,39%]
- text 36pt [5%,44% → 16%,52%]: {slope of the secant line|#c3b8ff}
- text 36pt [24%,44% → 35%,52%]: {slope of the tangent line|#c3b8ff}
- arrow #c3b8ff [10%,38% → 14%,43%]
- arrow #c3b8ff [26%,38% → 30%,42%]
- arrow #929292 [41%,61% → 65%,65%]
- arrow #929292 [50%,78% → 78%,82%]
- shape (outline) [49%,53% → 75%,70%]
- line #ffffff [54%,78% → 56%,82%]
- line #ffffff [72%,78% → 73%,82%]
- equation $\underline x$ (36pt, #ffffff) [55%,83% → 56%,85%]
- equation $\overline x$ (36pt, #ffffff) [72%,83% → 73%,85%]
- line #ffffff [51%,69% → 59%,73%]
- line #ffffff [64%,61% → 81%,65%]
- vector icon `shape-5335365c.svg` [72%,47% → 73%,49%]
- vector icon `shape-5335365c.svg` [54%,62% → 56%,64%]
- line #ffffff [52%,61% → 54%,65%]
- line #ffffff [52%,46% → 54%,50%]
- equation $f(\underline x)$ (36pt, #ffffff) [48%,62% → 52%,65%]
- equation $f(\overline x)$ (36pt, #ffffff) [48%,46% → 51%,49%]
- line #c3b8ff [54%,53% → 73%,58%]
- **Builds:** click 1: line #c3b8ff — draws in; with previous: line #c3b8ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 40
- line #c3b8ff [52%,50% → 71%,54%]
- line #c3b8ff [54%,53% → 73%,58%]
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [40%,16% → 60%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [39%,15% → 61%,20%]
- text 36pt [7%,23% → 93%,27%]: For a function $f(x)$ that is continuous and differentiable on the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(\overline x) - f(\underline x)}{\overline x - \underline x} = f^\prime (x^\prime)$ (36pt, #ffffff) [13%,31% → 27%,39%]
- text 36pt [5%,44% → 16%,52%]: {slope of the secant line|#c3b8ff}
- text 36pt [24%,44% → 35%,52%]: {slope of the tangent line|#c3b8ff}
- arrow #c3b8ff [10%,38% → 14%,43%]
- arrow #c3b8ff [26%,38% → 30%,42%]
- arrow #929292 [41%,61% → 65%,65%]
- arrow #929292 [50%,78% → 78%,82%]
- shape (outline) [49%,53% → 75%,70%]
- line #ffffff [54%,78% → 56%,82%]
- line #ffffff [72%,78% → 73%,82%]
- equation $\underline x$ (36pt, #ffffff) [55%,83% → 56%,85%]
- equation $\overline x$ (36pt, #ffffff) [72%,83% → 73%,85%]
- line #ffffff [51%,69% → 59%,73%]
- line #ffffff [64%,61% → 81%,65%]
- vector icon `shape-5335365c.svg` [72%,47% → 73%,49%]
- vector icon `shape-5335365c.svg` [54%,62% → 56%,64%]
- line #ffffff [52%,61% → 54%,65%]
- line #ffffff [52%,46% → 54%,50%]
- equation $f(\underline x)$ (36pt, #ffffff) [48%,62% → 52%,65%]
- equation $f(\overline x)$ (36pt, #ffffff) [48%,46% → 51%,49%]
- vector icon `shape-56f3a7db.svg` [61%,51% → 63%,53%]
- line #c3b8ff [54%,63% → 70%,68%]
- equation $x^\prime$ (36pt, #c3b8ff) [61%,82% → 63%,85%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 41
- line #c3b8ff [12%,33% → 31%,37%]
- line #c3b8ff [14%,36% → 33%,41%]
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [12%,16% → 32%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [11%,15% → 33%,20%]
- arrow #929292 [1%,44% → 25%,48%]
- arrow #929292 [10%,61% → 38%,65%]
- shape (outline) [9%,36% → 35%,53%]
- line #ffffff [14%,61% → 16%,65%]
- line #ffffff [31%,61% → 33%,65%]
- equation $\underline x$ (36pt, #ffffff) [14%,66% → 15%,68%]
- equation $\overline x$ (36pt, #ffffff) [32%,66% → 33%,68%]
- line #ffffff [11%,52% → 19%,56%]
- line #ffffff [24%,44% → 41%,48%]
- vector icon `shape-5335365c.svg` [32%,30% → 33%,32%]
- vector icon `shape-5335365c.svg` [14%,45% → 16%,47%]
- line #ffffff [12%,44% → 14%,48%]
- line #ffffff [12%,29% → 14%,33%]
- equation $f(\underline x)$ (36pt, #ffffff) [8%,45% → 11%,48%]
- equation $f(\overline x)$ (36pt, #ffffff) [8%,29% → 11%,32%]
- vector icon `shape-56f3a7db.svg` [21%,34% → 22%,36%]
- line #c3b8ff [14%,46% → 30%,51%]
- equation $x^\prime$ (36pt, #c3b8ff) [21%,65% → 22%,68%]
- image `pasted-movie-33819.png` [45%,16% → 92%,87%]
- text 14pt [84%,88% → 92%,90%]: Credit: @miniapeur on X
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 42
- line #ffa4e7 [38%,57% → 49%,61%]
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [39%,16% → 59%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [38%,15% → 60%,21%]
- arrow #929292 [28%,52% → 51%,56%]
- arrow #929292 [37%,68% → 65%,73%]
- shape (outline) [36%,44% → 62%,61%]
- line #ffffff [41%,68% → 43%,73%]
- line #ffffff [58%,68% → 60%,73%]
- equation $\underline x$ (36pt, #ffffff) [41%,74% → 42%,76%]
- equation $\overline x$ (36pt, #ffffff) [59%,74% → 60%,76%]
- line #ffffff [38%,59% → 46%,64%]
- line #ffa4e7 [42%,53% → 58%,57%]
- vector icon `shape-5335365c.svg` [59%,38% → 60%,40%]
- vector icon `shape-5335365c.svg` [41%,53% → 42%,55%]
- line #ffffff [39%,52% → 40%,56%]
- line #ffffff [39%,37% → 40%,41%]
- equation $f(\underline x)$ (36pt, #ffffff) [35%,52% → 38%,55%]
- equation $f(\overline x)$ (36pt, #ffffff) [35%,37% → 38%,40%]
- line #ffa4e7 [49%,68% → 51%,73%]
- equation $c$ (36pt, #ffa4e7) [50%,74% → 50%,75%]
- equation $x$ (36pt, #ffa4e7) [43%,74% → 44%,75%]
- line #ffa4e7 [42%,68% → 44%,73%]
- vector icon `shape-0b3e04f5.svg` [43%,49% → 44%,51%]
- vector icon `shape-0b3e04f5.svg` [49%,40% → 51%,42%]
- line #ffa4e7 [43%,44% → 51%,48%]
- line #ffa4e7 [43%,44% → 51%,48%]
- line #ffffff [51%,52% → 68%,56%]
- **Builds:** click 1: line #ffa4e7 — draws in; with previous: equation $c$ — appears; click 2: line #ffa4e7 — draws in; with previous: equation $x$ — appears; click 3: line #ffa4e7 — draws in; with previous: line #ffa4e7 — draws in; then: vector icon `shape-0b3e04f5.svg` — fades up from dark; with previous: vector icon `shape-0b3e04f5.svg` — fades up from dark; with previous: line #ffa4e7 — draws in; with previous: line #ffa4e7 — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 43
- line #ffa4e7 [38%,57% → 49%,61%]
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [39%,16% → 59%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [38%,15% → 60%,21%]
- arrow #929292 [28%,52% → 51%,56%]
- arrow #929292 [37%,68% → 65%,73%]
- shape (outline) [36%,44% → 62%,61%]
- line #ffffff [41%,68% → 43%,73%]
- line #ffffff [58%,68% → 60%,73%]
- equation $\underline x$ (36pt, #ffffff) [41%,74% → 42%,76%]
- equation $\overline x$ (36pt, #ffffff) [59%,74% → 60%,76%]
- line #ffffff [38%,59% → 46%,64%]
- line #ffa4e7 [42%,53% → 58%,57%]
- vector icon `shape-5335365c.svg` [59%,38% → 60%,40%]
- vector icon `shape-5335365c.svg` [41%,53% → 42%,55%]
- line #ffffff [39%,52% → 40%,56%]
- line #ffffff [39%,37% → 40%,41%]
- equation $f(\underline x)$ (36pt, #ffffff) [35%,52% → 38%,55%]
- equation $f(\overline x)$ (36pt, #ffffff) [35%,37% → 38%,40%]
- line #ffa4e7 [49%,68% → 51%,73%]
- equation $c$ (36pt, #ffa4e7) [50%,74% → 50%,75%]
- equation $x$ (36pt, #ffa4e7) [43%,74% → 44%,75%]
- line #ffa4e7 [42%,68% → 44%,73%]
- vector icon `shape-0b3e04f5.svg` [43%,49% → 44%,51%]
- vector icon `shape-0b3e04f5.svg` [49%,40% → 51%,42%]
- line #ffa4e7 [43%,44% → 51%,48%]
- line #ffa4e7 [42%,43% → 50%,47%]
- vector icon `shape-0b3e04f5.svg` [45%,44% → 46%,46%]
- line #ffa4e7 [39%,56% → 53%,60%]
- equation $x^\prime$ (36pt, #ffa4e7) [45%,73% → 47%,75%]
- line #ffffff [51%,52% → 68%,56%]
- **Builds:** then: line #ffa4e7 — draws in; click 1: equation $x^\prime$ — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 44
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [39%,16% → 59%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [38%,15% → 60%,21%]
- arrow #929292 [3%,52% → 27%,56%]
- arrow #929292 [13%,68% → 41%,73%]
- shape (outline) [12%,43% → 38%,61%]
- line #ffffff [17%,68% → 19%,73%]
- line #ffffff [34%,68% → 36%,73%]
- equation $\underline x$ (36pt, #ffffff) [17%,73% → 18%,76%]
- equation $\overline x$ (36pt, #ffffff) [35%,74% → 35%,75%]
- line #ffffff [13%,59% → 22%,63%]
- vector icon `shape-5335365c.svg` [34%,38% → 36%,40%]
- vector icon `shape-5335365c.svg` [17%,53% → 18%,55%]
- line #ffffff [14%,52% → 16%,56%]
- line #ffffff [14%,37% → 16%,41%]
- equation $f(\underline x)$ (36pt, #ffffff) [11%,52% → 14%,55%]
- equation $f(\overline x)$ (36pt, #ffffff) [11%,37% → 14%,40%]
- line #ffa4e7 [25%,68% → 27%,73%]
- equation $c$ (36pt, #ffa4e7) [25%,74% → 26%,75%]
- equation $x$ (36pt, #ffa4e7) [19%,74% → 20%,75%]
- line #ffa4e7 [18%,68% → 20%,73%]
- vector icon `shape-0b3e04f5.svg` [18%,49% → 20%,51%]
- vector icon `shape-0b3e04f5.svg` [25%,40% → 26%,42%]
- line #ffa4e7 [19%,44% → 27%,48%]
- line #ffa4e7 [18%,43% → 26%,47%]
- vector icon `shape-0b3e04f5.svg` [21%,44% → 22%,46%]
- equation $x^\prime$ (36pt, #ffa4e7) [21%,73% → 22%,75%]
- equation $x^\prime \in [x, c]$ (36pt, #ffffff) [54%,33% → 61%,35%]
- shape (outline) [64%,30% → 69%,38%]
- equation $x^\prime \in [\underline x, \overline x]$ (36pt, #ffffff) [72%,33% → 79%,36%]
- line #ffffff [27%,53% → 43%,57%]
- line #ffa4e7 [15%,56% → 29%,60%]
- line #ffa4e7 [14%,58% → 25%,62%]
- line #ffa4e7 [18%,54% → 33%,58%]
- text 36pt [49%,41% → 85%,49%]: Given the centerpoint $c$ of the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(x) - f(c)}{x-c} = f^\prime(x^\prime)$ (36pt, #ffffff) [61%,53% → 75%,60%]
- text 36pt [61%,63% → 73%,68%]: for any $x \in [x]$
- **Builds:** click 1: shape (outline) — wipes in; with previous: equation $x^\prime \in [\underline x, \overline x]$ — slides in; click 2: text 36pt — fades up from dark; with previous: equation $\frac{f(x) - f(c)}{x-c} = f^\prime(x^\prime)$ — fades up from dark; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 45
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [39%,16% → 59%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [38%,15% → 60%,21%]
- arrow #929292 [3%,52% → 27%,56%]
- arrow #929292 [13%,68% → 41%,73%]
- shape (outline) [12%,43% → 38%,61%]
- line #ffffff [17%,68% → 19%,73%]
- line #ffffff [34%,68% → 36%,73%]
- equation $\underline x$ (36pt, #ffffff) [17%,73% → 18%,76%]
- equation $\overline x$ (36pt, #ffffff) [35%,74% → 35%,75%]
- line #ffffff [13%,59% → 22%,63%]
- vector icon `shape-5335365c.svg` [34%,38% → 36%,40%]
- vector icon `shape-5335365c.svg` [17%,53% → 18%,55%]
- line #ffffff [14%,52% → 16%,56%]
- line #ffffff [14%,37% → 16%,41%]
- equation $f(\underline x)$ (36pt, #ffffff) [11%,52% → 14%,55%]
- equation $f(\overline x)$ (36pt, #ffffff) [11%,37% → 14%,40%]
- line #ffa4e7 [25%,68% → 27%,73%]
- equation $c$ (36pt, #ffa4e7) [25%,74% → 26%,75%]
- equation $x$ (36pt, #ffa4e7) [33%,73% → 34%,75%]
- line #ffa4e7 [32%,68% → 34%,72%]
- vector icon `shape-0b3e04f5.svg` [33%,38% → 34%,40%]
- vector icon `shape-0b3e04f5.svg` [25%,40% → 26%,42%]
- line #ffa4e7 [26%,38% → 33%,42%]
- line #ffa4e7 [26%,38% → 33%,42%]
- vector icon `shape-0b3e04f5.svg` [29%,39% → 30%,41%]
- equation $x^\prime$ (36pt, #ffa4e7) [29%,72% → 30%,74%]
- equation $x^\prime \in [x, c]$ (36pt, #ffffff) [54%,33% → 61%,35%]
- shape (outline) [64%,30% → 69%,38%]
- equation $x^\prime \in [\underline x, \overline x]$ (36pt, #ffffff) [72%,33% → 79%,36%]
- line #ffffff [27%,53% → 43%,57%]
- line #ffa4e7 [21%,53% → 38%,57%]
- line #ffa4e7 [25%,52% → 42%,57%]
- line #ffa4e7 [18%,54% → 33%,58%]
- text 36pt [49%,41% → 85%,49%]: Given the centerpoint $c$ of the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(x) - f(c)}{x-c} = f^\prime(x^\prime)$ (36pt, #ffffff) [61%,53% → 75%,60%]
- text 36pt [61%,63% → 73%,68%]: for any $x \in [x]$
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 46
- text 36pt [31%,5% → 69%,9%]: Yep, just gotta bring back a theorem from calculus.
- text 36pt [39%,16% → 59%,20%]: {The Mean Value Theorem|#c3b8ff}
- outlined shape #c3b8ff [38%,15% → 60%,21%]
- text 36pt [6%,31% → 42%,40%]: Given the centerpoint $c$ of the interval $[x]$, there exists a point $x^\prime \in [x]$ such that
- equation $\frac{f(x) - f(c)}{x-c} = f^\prime(x^\prime)$ (36pt, #ffffff) [18%,43% → 32%,50%]
- text 36pt [18%,53% → 30%,58%]: for any $x \in [x]$
- rounded box (outline) [4%,28% → 44%,61%]
- shape (outline) [48%,41% → 53%,49%]
- equation $\frac{f(x) - f(c)}{x-c} = f^\prime(x^\prime)$ (36pt, #ffffff) [64%,32% → 78%,39%]
- equation $f(x) = f(c) + f^\prime(x^\prime)(x - c)$ (36pt, #ffffff) [62%,43% → 80%,46%]
- equation $[f]([x]) = f(c) + [f^\prime]([x])([x] - c)$ (36pt, #ffffff) [59%,51% → 84%,54%]
- text 36pt [67%,58% → 82%,67%]: {natural inclusion function for $f^\prime(x)$|#c3b8ff}
- arrow #c3b8ff [74%,55% → 75%,59%]
- **Builds:** click 1: equation $f(x) = f(c) + f^\prime(x^\prime)(x - c)$ — slides in; click 2: equation $[f]([x]) = f(c) + [f^\prime]([x])([x] - c)$ — slides in; click 3: arrow #c3b8ff — draws in; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 47
- text 36pt [36%,5% → 64%,10%]: {Mean Value Inclusion Function |#c3b8ff}
- outlined shape #ffffff [36%,33% → 64%,39%]
- equation $[f]([x]) = f(c) + [f^\prime]([x])([x] - c)$ (36pt, #ffffff) [38%,15% → 62%,18%]
- shape (outline) [47%,22% → 53%,30%]
- text 30pt [54%,21% → 67%,28%]: generalize the more than one dimension
- equation $[f]([\mathbf x]) = f(\mathbf c) + [\nabla f]([\mathbf x])^\top ([\mathbf x] - \mathbf c)$ (36pt, #ffffff) [36%,34% → 64%,38%]
- outlined shape #c3b8ff [38%,5% → 62%,10%]
- **Builds:** click 1: shape (outline) — wipes in; with previous: text 30pt — wipes in; with previous: equation $[f]([\mathbf x]) = f(\mathbf c) + [\nabla f]([\mathbf x])^\top ([\mathbf x] - \mathbf c)$ — slides in; click 2: outlined shape #ffffff — LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 48
- text 36pt [19%,6% → 81%,14%]: Let’s evaluate the natural inclusion function and mean value inclusion function for / $f(x) = x - \sin(x)$ over the interval $[x] = [-1, 1]$.
- text 36pt [14%,19% → 34%,24%]: natural inclusion function
- text 36pt [64%,19% → 86%,24%]: mean value inclusion function
- line #ffffff [29%,53% → 71%,58%]
- group [31%,15% → 44%,17%]
  - line #80b9ff [32%,16% → 34%,16%]
  - line #80b9ff [31%,15% → 44%,17%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 49
- text 36pt [19%,6% → 81%,14%]: Let’s evaluate the natural inclusion function and mean value inclusion function for / $f(x) = x - \sin(x)$ over the interval $[x] = [-1, 1]$.
- text 36pt [14%,19% → 34%,24%]: natural inclusion function
- image `test-33456.svg` [5%,34% → 36%,81%]
- text 36pt [64%,19% → 86%,24%]: mean value inclusion function
- line #ffffff [29%,53% → 71%,58%]
- image `test-34165.svg` [56%,34% → 87%,81%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 50
- text 36pt [34%,48% → 66%,52%]: It is possible to do even better!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 51
- rounded box (outline) [21%,12% → 79%,28%]
- text 36pt [38%,6% → 62%,10%]: It is possible to do even better!
- equation $f(x) = f(c) + f^\prime(x^\prime)(x - c)$ (36pt, #ffffff) [23%,22% → 42%,24%]
- shape (outline) [45%,19% → 50%,27%]
- equation $[f]([x]) = f(c) + [f^\prime]([x])([x] - c)$ (36pt, #ffffff) [53%,22% → 77%,24%]
- group [16%,33% → 52%,46%]
  - rounded box (filled #424242) [16%,33% → 52%,45%]
  - heading (spaced caps) 100pt [17%,33% → 22%,46%]: 🤔
  - text 36pt [22%,35% → 52%,43%]: Does this function look like another topic you learned about in calculus?
- arrow #ffffff [32%,28% → 37%,33%]
- text 36pt [33%,48% → 37%,52%]: {It is a first-order Taylor series!|#80b9ff}
- text 36pt [38%,12% → 62%,17%]: Mean Value Inclusion Function
- **Builds:** click 1: group — fades up from dark; with previous: arrow #ffffff — draws in; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 52
- rounded box (outline) [21%,12% → 79%,28%]
- text 36pt [38%,6% → 62%,10%]: It is possible to do even better!
- equation $f(x) = f(c) + f^\prime(x^\prime)(x - c)$ (36pt, #ffffff) [23%,22% → 42%,24%]
- shape (outline) [45%,19% → 50%,27%]
- equation $[f]([x]) = f(c) + [f^\prime]([x])([x] - c)$ (36pt, #ffffff) [53%,22% → 77%,24%]
- text 36pt [38%,12% → 62%,17%]: Mean Value Inclusion Function
- shape (outline) [45%,40% → 55%,48%]
- text 36pt [53%,40% → 67%,44%]: more general case
- rounded box (outline) [21%,60% → 79%,76%]
- text 36pt [40%,61% → 60%,65%]: Taylor Inclusion Functions
- equation $[f]([x]) = f(c) + f'(c)([x] - c) + \frac{f''(c)}{2!}([x] - c)^2 + \cdots + \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #ffffff) [22%,66% → 78%,74%]
- text 36pt [18%,81% → 82%,85%]: A [[zero-order|#c3b8ff]] Taylor inclusion function is the same as the [[natural inclusion function|#c3b8ff]].
- text 36pt [19%,87% → 81%,91%]: A [[first-order|#c3b8ff]] Taylor inclusion function is the same as the [[mean value inclusion function|#c3b8ff]].
- **Builds:** click 1: shape (outline) — wipes in; with previous: text 36pt — fades up from dark; click 2: rounded box (outline) — fades up from dark; with previous: text 36pt — fades up from dark; with previous: equation $[f]([x]) = f(c) + f'(c)([x] - c) + \frac{f''(c)}{2!}([x] - c)^2 + \cdots + \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ — fades up from dark; click 3: text 36pt — slides in; click 4: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 53
- rounded box (outline) [21%,9% → 79%,25%]
- text 36pt [40%,10% → 60%,15%]: Taylor Inclusion Functions
- equation $[f]([x]) = f(c) + f'(c)([x] - c) + \frac{f''(c)}{2!}([x] - c)^2 + \cdots + \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #ffffff) [22%,15% → 78%,23%]
- image `pasted-movie-35235.png` [30%,33% → 70%,89%]
- text 36pt [73%,59% → 91%,63%]: I tried my best here…
- text 18pt [63%,91% → 70%,93%]: Credit: ChatGPT
- **Builds:** click 1: image `pasted-movie-35235.png` — fades up from dark; with previous: text 36pt — fades up from dark; with previous: text 18pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 54
- rounded box (outline) [21%,9% → 79%,25%]
- text 36pt [40%,10% → 60%,15%]: Taylor Inclusion Functions
- equation $[f]([x]) = f(c) + f'(c)([x] - c) + \frac{f''(c)}{2!}([x] - c)^2 + \cdots + \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #ffffff) [22%,15% → 78%,23%]
- image `test-34303.svg` [18%,31% → 76%,92%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 55
- rounded box (outline) [21%,9% → 79%,25%]
- text 36pt [40%,10% → 60%,15%]: Taylor Inclusion Functions
- equation $[f]([x]) = f(c) + f'(c)([x] - c) + \frac{f''(c)}{2!}([x] - c)^2 + \cdots + \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #ffffff) [22%,15% → 78%,23%]
- image `val-page-210.svg` (cropped: show only 6–61% across and 38–80% down of the image) [12%,29% → 52%,91%]
- outlined shape #ff48cf [20%,49% → 49%,52%]
- text 36pt [56%,49% → 79%,53%]: {Mean Value Inclusion Function|#ff48cf}
- arrow #ff48cf [49%,49% → 56%,53%]
- text 36pt [59%,61% → 87%,73%]: Julia seamlessly allows us to pass an interval through the GRADIENT of our rollout function.
- heading (spaced caps) 150pt [69%,75% → 77%,94%]: 🤯
- text on a #80b9ff filled box 32pt [71%,33% → 90%,41%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: outlined shape #ff48cf — LineDraw; with previous: arrow #ff48cf — draws in; with previous: text 36pt — fades up from dark; click 2: text 36pt — flame; click 3: heading (spaced caps) 150pt — bc-drop; click 4: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 56
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 57
- heading (spaced caps) 36pt [35%,31% → 65%,35%]: INCLUSION FUNCTIONS
- heading (spaced caps) 36pt [40%,51% → 60%,55%]: TAYLOR MODELS
- text 36pt [48%,38% → 52%,42%]: only ever output [[hyperrectangular|#80b9ff]] sets (no matter how high the order)
- text 36pt [23%,57% → 77%,62%]: are able to represent more [[expressive|#80b9ff]] sets
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 58
- image `image-8-35327.png` [13%,20% → 47%,80%]
- image `image-7-35330.png` [53%,20% → 87%,80%]
- text 18pt [40%,81% → 47%,84%]: Credit: ChatGPT
- text 18pt [80%,81% → 87%,84%]: Credit: ChatGPT
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 59
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- text 36pt [20%,28% → 36%,37%]: {Taylor polynomial of degree $n-1$|#80b9ff}
- arrow #80b9ff [28%,21% → 43%,25%]
- arrow #80b9ff [48%,21% → 64%,25%]
- text 36pt [59%,28% → 70%,37%]: {interval remainder|#80b9ff}
- equation $p(x) = f(c) + f'(c)(x - c) + \frac{f''(c)}{2!}(x - c)^2 + \cdots + \frac{f^{(n-1)}(c)}{(n-1)!}(x - c)^{(n-1)}$ (29pt, #80b9ff) [7%,40% → 48%,46%]
- equation $[\alpha] = \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #80b9ff) [55%,39% → 74%,47%]
- equation $\mathcal T = \{p(\mathbf x) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [38%,16% → 62%,19%]
- text 36pt [63%,50% → 67%,54%]: {Lagrange Remainder|#80b9ff}
- **Builds:** click 1: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 2: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 3: equation $p(x) = f(c) + f'(c)(x - c) + \frac{f''(c)}{2!}(x - c)^2 + \cdots + \frac{f^{(n-1)}(c)}{(n-1)!}(x - c)^{(n-1)}$ — slides in; click 4: equation $[\alpha] = \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ — slides in; click 5: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 60
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- text 36pt [20%,28% → 36%,37%]: {Taylor polynomial of degree $n-1$|#80b9ff}
- arrow #80b9ff [28%,21% → 43%,25%]
- arrow #80b9ff [48%,21% → 64%,25%]
- text 36pt [59%,28% → 70%,37%]: {interval remainder|#80b9ff}
- equation $p(x) = f(c) + f'(c)(x - c) + \frac{f''(c)}{2!}(x - c)^2 + \cdots + \frac{f^{(n-1)}(c)}{(n-1)!}(x - c)^{(n-1)}$ (29pt, #80b9ff) [7%,40% → 48%,46%]
- equation $[\alpha] = \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #80b9ff) [55%,39% → 74%,47%]
- text 36pt [63%,50% → 67%,54%]: {Lagrange Remainder|#80b9ff}
- text 36pt [26%,35% → 30%,40%]: approximates the function
- equation $\mathcal T = \{p(\mathbf x) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [38%,16% → 62%,19%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 61
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- text 36pt [20%,28% → 36%,37%]: {Taylor polynomial of degree $n-1$|#80b9ff}
- arrow #80b9ff [28%,21% → 43%,25%]
- arrow #80b9ff [48%,21% → 64%,25%]
- text 36pt [59%,28% → 70%,37%]: {interval remainder|#80b9ff}
- equation $p(x) = f(c) + f'(c)(x - c) + \frac{f''(c)}{2!}(x - c)^2 + \cdots + \frac{f^{(n-1)}(c)}{(n-1)!}(x - c)^{(n-1)}$ (29pt, #80b9ff) [7%,40% → 48%,46%]
- equation $[\alpha] = \frac{[f^{(n)}]([x])}{n!}([x] - c)^n$ (36pt, #80b9ff) [55%,39% → 74%,47%]
- text 36pt [63%,50% → 67%,54%]: {Lagrange Remainder|#80b9ff}
- text 36pt [26%,35% → 30%,40%]: approximates the function
- text 36pt [50%,35% → 80%,40%]: bounds the error in the approximation
- equation $\mathcal T = \{p(\mathbf x) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [38%,16% → 62%,19%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 62
- image `test-35478.svg` [16%,53% → 83%,88%]
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- rounded box (filled #f3cf80) [30%,23% → 71%,36%]
- text 36pt [31%,24% → 70%,34%]: {Note: if we replace $p(\mathbf x)$ with $[p]([\mathbf x])$, we recover the Taylor inclusion function!|#000000}
- text 36pt [23%,40% → 77%,48%]: Taylor models provide [[increased flexibility|#80b9ff]] by allowing us to pass other types of sets (such as zonotopes) through the Taylor polynomial.
- text 36pt [23%,89% → 35%,96%]: {Natural |#f3cf80} / Inclusion Function
- text 30pt [39%,89% → 52%,96%]: {Mean Value Inclusion Function|#f3cf80}
- equation $\mathcal T = \{p(\mathbf x) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [38%,16% → 62%,19%]
- **Builds:** click 1: text 36pt — slides in; click 2: image `test-35478.svg` — fades up from dark; click 3: text 36pt — fades up from dark; click 4: text 30pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 63
- image `test-35478.svg` [16%,53% → 83%,88%]
- image `test-35464.svg` [16%,53% → 83%,88%]
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- rounded box (filled #f3cf80) [30%,23% → 71%,36%]
- text 36pt [31%,24% → 70%,34%]: {Note: if we replace $p(\mathbf x)$ with $[p]([\mathbf x])$, we recover the Taylor inclusion function!|#000000}
- text 36pt [23%,40% → 77%,48%]: Taylor models provide [[increased flexibility|#80b9ff]] by allowing us to pass other types of sets (such as zonotopes) through the Taylor polynomial.
- text 36pt [23%,89% → 35%,96%]: {Natural |#f3cf80} / Inclusion Function
- text 30pt [39%,89% → 52%,96%]: {Mean Value Inclusion Function|#f3cf80}
- equation $\mathcal T = \{p(\mathbf x) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [38%,16% → 62%,19%]
- text 30pt [85%,42% → 97%,56%]: {After second order, the sets may become nonconvex!|#f3cf80}
- arrow #f3cf80 [80%,60% → 92%,64%]
- text 30pt [54%,89% → 67%,96%]: {Conservative Linearization|#ffa4e7}
- **Builds:** click 1: text 30pt — fades up from dark; with previous: arrow #f3cf80 — draws in; click 2: text 30pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 64
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- text 36pt [38%,14% → 62%,19%]: {Conservative Linearization (second order Taylor model)|#ffa4e7}
- equation $f (\mathbf x) = \begin{bmatrix} f_1(\mathbf x) \\ \vdots \\ f_n(\mathbf x) \end{bmatrix}$ (36pt, #ffffff) [16%,32% → 27%,46%]
- shape (outline) [32%,37% → 37%,44%]
- text 30pt [30%,27% → 40%,36%]: Taylor polynomial
- equation $\begin{bmatrix} f_1(\mathbf c) + \nabla f_1(\mathbf c)^\top(\mathbf x - \mathbf c) \\ \vdots \\ f_n(\mathbf c) + \nabla f_n(\mathbf c)^\top(\mathbf x - \mathbf c) \end{bmatrix}$ (36pt, #ffffff) [43%,32% → 61%,46%]
- equation $= f(\mathbf c) + \begin{bmatrix} \nabla f_1(\mathbf c)^\top \\ \vdots \\ \nabla f_n(\mathbf c)^\top \end{bmatrix} (\mathbf x - \mathbf c)$ (36pt, #ffffff) [62%,32% → 82%,46%]
- text 36pt [69%,56% → 77%,61%]: {Jacobian $\mathbf J$|#80b9ff}
- arrow #80b9ff [71%,50% → 75%,54%]
- equation $\mathcal T = \{f(\mathbf c) + \mathbf J(\mathbf x - \mathbf c) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [33%,71% → 66%,74%]
- outlined shape #ffffff [32%,70% → 68%,75%]
- **Builds:** click 1: equation $f (\mathbf x) = \begin{bmatrix} f_1(\mathbf x) \\ \vdots \\ f_n(\mathbf x) \end{bmatrix}$ — appears; click 2: text 30pt — wipes in; with previous: shape (outline) — wipes in; with previous: equation $\begin{bmatrix} f_1(\mathbf c) + \nabla f_1(\mathbf c)^\top(\mathbf x - \mathbf c) \\ \vdots \\ f_n(\mathbf c) + \nabla f_n(\mathbf c)^\top(\mathbf x - \mathbf c) \end{bmatrix}$ — slides in; click 3: equation $= f(\mathbf c) + \begin{bmatrix} \nabla f_1(\mathbf c)^\top \\ \vdots \\ \nabla f_n(\mathbf c)^\top \end{bmatrix} (\mathbf x - \mathbf c)$ — slides in; click 4: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 5: outlined shape #ffffff — fades up from dark; with previous: equation $\mathcal T = \{f(\mathbf c) + \mathbf J(\mathbf x - \mathbf c) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 65
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- text 36pt [38%,14% → 62%,19%]: {Conservative Linearization (second order Taylor model)|#ffa4e7}
- equation $\mathcal T = \{f(\mathbf c) + \mathbf J(\mathbf x - \mathbf c) + \mathbf \alpha \mid \mathbf x \in \mathcal X, \mathbf \alpha \in [\mathbf \alpha]\}$ (36pt, #ffffff) [34%,26% → 66%,29%]
- outlined shape #ffffff [38%,60% → 62%,66%]
- arrow #80b9ff [42%,31% → 46%,36%]
- text 36pt [38%,48% → 62%,52%]: This is a [[linear function|#80b9ff]].
- text 36pt [48%,53% → 52%,58%]: We know how to pass [[polytopes|#80b9ff]] through linear functions!
- equation $\mathcal T = f(\mathbf c) + \mathbf J(\mathcal X \oplus -\mathbf c) \oplus [\mathbf \alpha]$ (36pt, #ffffff) [39%,61% → 61%,64%]
- outlined shape #ffffff [33%,25% → 68%,30%]
- text 36pt [39%,38% → 47%,43%]: {Jacobian $\mathbf J$|#80b9ff}
- **Builds:** click 1: text 36pt — wipes in; click 2: text 36pt — slides in; click 3: outlined shape #ffffff — fades up from dark; with previous: equation $\mathcal T = f(\mathbf c) + \mathbf J(\mathcal X \oplus -\mathbf c) \oplus [\mathbf \alpha]$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 66
- heading (spaced caps) 36pt [40%,6% → 60%,10%]: TAYLOR MODELS
- outlined shape #ffffff [38%,27% → 62%,33%]
- text 36pt [41%,15% → 59%,19%]: This is a [[linear function|#80b9ff]].
- text 36pt [28%,20% → 72%,25%]: We know how to pass [[polytopes|#80b9ff]] through linear functions!
- equation $\mathcal T = f(\mathbf c) + \mathbf J(\mathcal X \oplus -\mathbf c) \oplus [\mathbf \alpha]$ (36pt, #ffffff) [39%,28% → 61%,31%]
- image `val-page-214.svg` (cropped: show only 6–67% across and 36–73% down of the image) [48%,39% → 87%,88%]
- text 36pt [9%,58% → 42%,63%]: And Julia, of course, handles this beautifully.
- text on a #80b9ff filled box 32pt [16%,67% → 35%,75%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 67
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 68
- heading (spaced caps) 36pt [34%,6% → 66%,11%]: CONCRETE REACHABILITY
- image `test-34785.svg` [17%,20% → 83%,85%]
- rounded box (outline) [14%,14% → 87%,54%]
- text 36pt [48%,15% → 52%,20%]: What we have discussed so far this lecture:
- text 36pt [49%,86% → 53%,90%]: “Concretize” the reachable set at every step.
- **Builds:** click 1: rounded box (outline) — LineDraw; with previous: text 36pt — fades up from dark; click 2: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 69
- heading (spaced caps) 36pt [6%,45% → 38%,49%]: CONCRETE REACHABILITY
- heading (spaced caps) 36pt [6%,5% → 39%,10%]: SYMBOLIC REACHABILITY
- group [10%,13% → 85%,20%]
  - text 36pt [15%,13% → 85%,18%]: Can be computationally expensive because they consider the entire rollout function at once
  - vector icon `shape-8d0d2714.svg` [10%,14% → 13%,20%]
- group [10%,24% → 77%,31%]
  - text 36pt [15%,24% → 77%,29%]: Nonlinearities in the agent, environment, and sensor models compound over time
  - vector icon `shape-8d0d2714.svg` [10%,25% → 13%,31%]
- group [10%,35% → 51%,41%]
  - text 36pt [15%,35% → 51%,40%]: Does not have an issue with the wrapping effect
  - vector icon `shape-218897dc.svg` [10%,35% → 13%,41%]
- group [10%,54% → 45%,60%]
  - text 36pt [14%,55% → 45%,59%]: Typically more computationally efficient
  - vector icon `shape-218897dc.svg` [10%,54% → 13%,60%]
- group [10%,65% → 42%,71%]
  - text 36pt [15%,65% → 42%,70%]: No issue of compounding nonlinearities
  - vector icon `shape-218897dc.svg` [10%,65% → 13%,71%]
- group [10%,75% → 73%,81%]
  - text 36pt [14%,76% → 73%,80%]: Error from concretizing the reachable set at each time step (wrapping effect)
  - vector icon `shape-8d0d2714.svg` [10%,75% → 13%,81%]
- group [8%,84% → 86%,96%]
  - rounded box (filled #80b9ff) [8%,84% → 86%,96%]
  - text 36pt [10%,86% → 85%,94%]: {Whether symbolic reachability or concrete reachability will perform better is |#000000}[[problem dependent|#000000]]{.|#000000} / See discussion in section 9.4.
- text on a #80b9ff filled box 32pt [64%,48% → 83%,56%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: group — slides in; click 2: group — slides in; click 3: group — slides in; click 4: group — slides in; click 5: group — slides in; click 6: group — slides in; click 7: group — fades up from dark; click 8: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 70
- text 36pt [39%,48% → 61%,52%]: Can we do even better?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 71
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 72
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- image `test-34968.svg` [13%,31% → 41%,79%]
- image `test-34968.svg` [48%,31% → 76%,79%]
- filled shape #c0c0c0 [30%,34% → 33%,61%]
- equation $\mathcal R_1$ (36pt, #ffffff) [30%,24% → 33%,27%]
- equation $\mathcal R_2$ (36pt, #ffffff) [65%,24% → 68%,27%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 73
- filled shape #c0c0c0 [30%,34% → 33%,61%]
- image `test-34968.svg` [13%,31% → 41%,79%]
- shape filled #c3b8ff, outlined #c3b8ff [30%,34% → 31%,47%]
- shape filled #80b9ff, outlined #80b9ff [30%,48% → 31%,61%]
- shape filled #0072fe, outlined #0072fe [31%,34% → 33%,47%]
- shape filled #ffa4e7, outlined #ffa4e7 [31%,48% → 33%,61%]
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- image `test-34968.svg` [48%,31% → 76%,79%]
- equation $\mathcal R_1$ (36pt, #ffffff) [30%,24% → 33%,27%]
- equation $\mathcal R_2$ (36pt, #ffffff) [65%,24% → 68%,27%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 74
- image `test-34968.svg` [48%,31% → 76%,79%]
- shape filled #80b9ff, outlined #80b9ff [65%,41% → 67%,49%]
- image `test-34968.svg` [13%,31% → 41%,79%]
- shape filled #c3b8ff, outlined #c3b8ff [65%,44% → 67%,52%]
- shape filled #0072fe, outlined #0072fe [67%,46% → 68%,53%]
- shape filled #ffa4e7, outlined #ffa4e7 [67%,43% → 68%,51%]
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- equation $\mathcal R_1$ (36pt, #ffffff) [30%,24% → 33%,27%]
- equation $\mathcal R_2$ (36pt, #ffffff) [65%,24% → 68%,27%]
- filled shape #c0c0c0 [30%,34% → 33%,61%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 75
- image `test-34968.svg` [48%,31% → 76%,79%]
- shape filled #c0c0c0, outlined #c0c0c0 [65%,41% → 67%,49%]
- image `test-34968.svg` [13%,31% → 41%,79%]
- shape filled #c0c0c0, outlined #c0c0c0 [65%,44% → 67%,52%]
- shape filled #c0c0c0, outlined #c0c0c0 [67%,46% → 68%,53%]
- shape filled #c0c0c0, outlined #c0c0c0 [67%,43% → 68%,51%]
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- equation $\mathcal R_1$ (36pt, #ffffff) [30%,24% → 33%,27%]
- equation $\mathcal R_2$ (36pt, #ffffff) [65%,24% → 68%,27%]
- filled shape #c0c0c0 [30%,34% → 33%,61%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 76
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- image `test-34968.svg` [52%,20% → 73%,54%]
- shape filled #c0c0c0, outlined #c0c0c0 [65%,28% → 66%,33%]
- image `test-34968.svg` [27%,20% → 48%,54%]
- shape filled #c0c0c0, outlined #c0c0c0 [65%,30% → 66%,35%]
- shape filled #c0c0c0, outlined #c0c0c0 [66%,31% → 67%,36%]
- shape filled #c0c0c0, outlined #c0c0c0 [66%,29% → 67%,34%]
- equation $\mathcal R_1$ (26pt, #ffffff) [40%,15% → 42%,18%]
- equation $\mathcal R_2$ (26pt, #ffffff) [65%,15% → 67%,18%]
- filled shape #c0c0c0 [40%,23% → 42%,42%]
- text 36pt [45%,61% → 55%,65%]: Why do this?
- text 36pt [22%,70% → 78%,74%]: Propagating smaller sets tends to result in less overapproximation error.
- text 36pt [27%,77% → 73%,82%]: We can represent nonconvex sets as a union of convex sets!
- rounded box (outline) [43%,60% → 57%,67%]
- **Builds:** click 1: text 36pt — fades up from dark; click 2: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 77
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: PARTITIONING
- text 36pt [48%,12% → 52%,17%]: Partitioning can significantly reduce overapproximation error!
- image `g01.svg` [19%,37% → 81%,82%]
- image `g02.svg` [19%,37% → 81%,82%]
- image `g03.svg` [19%,37% → 81%,82%]
- image `g04.svg` [19%,37% → 81%,82%]
- image `g05.svg` [19%,37% → 81%,82%]
- image `g06.svg` [19%,37% → 81%,82%]
- image `g07.svg` [19%,37% → 81%,82%]
- image `g08.svg` [19%,37% → 81%,82%]
- image `g09.svg` [19%,37% → 81%,82%]
- image `g10.svg` [19%,37% → 81%,82%]
- equation $\mathcal R_1$ (36pt, #ffffff) [31%,30% → 33%,33%]
- equation $\mathcal R_2$ (36pt, #ffffff) [69%,30% → 71%,33%]
- text 36pt [48%,21% → 52%,25%]: First-Order Taylor Inclusion Function
- **Builds:** click 1: image `g02.svg` — appears; then (0.2 s later): image `g03.svg` — appears; then (0.2 s later): image `g04.svg` — appears; then (0.2 s later): image `g05.svg` — appears; then (0.2 s later): image `g06.svg` — appears; then (0.2 s later): image `g07.svg` — appears; then (0.2 s later): image `g08.svg` — appears; then (0.2 s later): image `g09.svg` — appears; then (0.2 s later): image `g10.svg` — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 78
- heading (spaced caps) 36pt [41%,5% → 59%,9%]: {PARTITIONING|#000000}
- text 36pt [48%,12% → 52%,17%]: {Partitioning can significantly reduce overapproximation error!|#000000}
- text 36pt [29%,19% → 71%,23%]: {And it generally makes some really cool looking GIFs! |#000000}
- heading (spaced caps) 36pt [71%,18% → 73%,23%]: 😎
- video `all-split-pol-reorder.gif` (plays 0.0s–3.7s, loops) [10%,40% → 54%,83%]
- video `threshold-reduction.gif` (plays 0.0s–2.9s, loops) [60%,29% → 84%,93%]
- **Builds:** then: video `all-split-pol-reorder.gif` (plays 0.0s–3.7s, loops) — video starts; with previous: video `threshold-reduction.gif` (plays 0.0s–2.9s, loops) — video starts
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 79
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: INTERVAL ARITHMETIC
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: INCLUSION FUNCTIONS
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: TAYLOR MODELS
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: CONCRETE REACHABILITY
- text on a #80b9ff filled box 32pt [7%,78% → 11%,85%]: {5|#000000}
- heading (spaced caps) 36pt [13%,79% → 86%,83%]: PARTITIONING
- **Transition to next:** Magic Move (shared objects glide; others fade)
