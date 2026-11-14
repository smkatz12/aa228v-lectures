# AA228V Lecture 18 — Runtime Monitoring: slide-by-slide content

Extracted from the Keynote deck `18_Runtime_Monitoring.key` (96 slides, 16:9). This is the source material for rebuilding the lecture as a native HTML deck.

## How to read this

- Positions are approximate boxes in % of the slide, `[left,top → right,bottom]`. Use the reference screenshots for the exact layout.
- `[[text|#hex]]` = accent phrase: italic, in that color. `{text|#hex}` = colored (not italic).
- `$...$` is LaTeX. Typeset it with KaTeX (or MathJax) in the same color and roughly the same size as the surrounding text. There are no equation image files.
- Images and videos named in backticks are online, not attached. Use each one by its full address `https://smkatz12.github.io/aa228v-lectures/lectures/18-runtime-monitoring/images/<name>`, for example `<img src="https://smkatz12.github.io/aa228v-lectures/lectures/18-runtime-monitoring/images/coverart-302-green.png">`. Don't ask for uploads.
- **Builds** list what appears on each click, in order ("then" = right after the previous step, "with previous" = at the same time, "(0.1 s later)" = after that pause).
- A long run of images named `gNN-…` that appear one after another at the same spot, a fraction of a second apart, is a frame-by-frame animation: stack them and reveal them in turn with that timing (each frame stays as the next appears).
- **Transition to next: Magic Move** means objects shared with the next slide should glide to their new positions.

## House style

- Same as earlier lectures: black background; white text.
- Spaced all-caps headings in Gill Sans (regular weight, letter-spacing about 0.25em). All other text in Palatino.
- Emphasis is italic + color, never bold.
- The title slide streak is green (`coverart-302-green.png`).
- Graphics are SVGs with transparent backgrounds and white lines/text, made for the black slides; keep them as `<img>` files.
- Most-used text colors: `#ffffff`, `#80b9ff`, `#f3cf80`, `#c3b8ff`, `#000000`, `#fab0ae`, `#c0c0c0`, `#80cfb9`

## Slide 1
- image `coverart-302-green.png` [-0%,46% → 100%,75%]
- text 50pt [6%,9% → 82%,22%]: AA228V/CS238V / VALIDATION OF SAFETY-CRITICAL SYSTEMS
- heading (spaced caps) 50pt [4%,73% → 43%,87%]: LECTURE 18: RUNTIME MONITORING / SYDNEY KATZ (SMKATZ@STANFORD.EDU)

## Slide 2
- text 36pt [6%,48% → 94%,52%]: We do our best to model the world using offline validation, but we will inevitably miss stuff.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 3
- text 36pt [15%,5% → 85%,9%]: We do our best to model the world using offline validation, but we will inevitably miss stuff.
- video `video-38816.mp4` (plays 0.0s–29.2s, once) [13%,20% → 47%,86%]
- YouTube video https://www.youtube.com/watch?v=9xyXAZCxfcE (thumbnail `hqdefault-38822.jpg`) [52%,27% → 91%,79%]
- **Builds:** click 1: video `video-38816.mp4` (plays 0.0s–29.2s, once) — video starts; click 2: YouTube video https://www.youtube.com/watch?v=9xyXAZCxfcE (thumbnail ` — YouTube video starts
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 4
- heading (spaced caps) 36pt [30%,5% → 73%,10%]: GENERAL THOUGHTS ON MODELS
- text 36pt [7%,16% → 19%,21%]: Key Challenges
- text on a #80b9ff filled box 32pt [10%,25% → 14%,32%]: {1|#000000}
- text 36pt [15%,26% → 21%,31%]: Model needs to be expressive enough to capture [[all possible scenarios|#80b9ff]] the system may encounter.
- vector icon `shape-ee75f719.svg` [88%,60% → 96%,96%]
- vector icon `shape-ee75f719.svg` [5%,60% → 12%,95%]
- group [48%,37% → 90%,59%]
  - text 36pt [52%,41% → 85%,48%]: How can I capture all possible scenarios my / {<insert crazy complex system here>|#80b9ff} will end up in?
  - text 28pt [52%,49% → 85%,53%]: … I don’t even know what they all are!
  - shape (outline) [48%,37% → 90%,59%]
- group [8%,36% → 40%,58%]
  - shape (outline) [10%,36% → 40%,58%]
  - text 40pt [8%,39% → 40%,45%]: Yeah, it’s a problem. 😬
- text 28pt [14%,45% → 36%,52%]: But there is some hope! Stay tuned for the {runtime monitoring|#80b9ff} chapter.
- **Builds:** click 1: text on a #80b9ff filled box 32pt — slides in; with previous: text 36pt — slides in; click 2: vector icon `shape-ee75f719.svg` — move in character; click 3: group — wipes in; click 4: vector icon `shape-ee75f719.svg` — move in character; click 5: group — wipes in; click 6: text 28pt — fireworks

## Slide 5
- text 36pt [15%,5% → 85%,9%]: We do our best to model the world using offline validation, but we will inevitably miss stuff.
- rounded box (filled #424242) [13%,38% → 87%,62%]
- text 36pt [33%,12% → 67%,17%]: My answer to all of this: runtime monitoring!
- text 48pt [18%,42% → 82%,48%]: “The ultimate answer to life, the universe, and everything is 42.”
- text 36pt [29%,51% → 44%,55%]: — Douglas Adams
- line #80b9ff [78%,42% → 81%,47%]
- line #80b9ff [32%,51% → 44%,56%]
- text 36pt [71%,48% → 87%,52%]: {runtime monitoring|#80b9ff}
- text 36pt [32%,55% → 43%,60%]: {Sydney Katz|#80b9ff}
- **Builds:** click 1: rounded box (filled #424242) — fades up from dark; with previous: text 48pt — fades up from dark; with previous: text 36pt — fades up from dark; click 2: text 36pt — slides in; with previous: text 36pt — slides in; with previous: line #80b9ff — draws in; with previous: line #80b9ff — draws in

## Slide 6
- text 36pt [21%,46% → 79%,54%]: The goal of runtime monitoring is to [[flag situations that may be hazardous|#80b9ff]] when they occur so that we can trigger [[fallback mechanisms|#80b9ff]].

## Slide 7
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: OPERATIONAL DESIGN DOMAIN MONITORING
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: UNCERTAINTY QUANTIFICATION
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,67% → 11%,73%]: {3|#000000}
- heading (spaced caps) 36pt [13%,68% → 87%,72%]: FAILURE MONITORING
- text 32pt [15%,47% → 18%,54%]: {A|#80b9ff}
- text 32pt [15%,56% → 18%,63%]: {B|#80b9ff}
- text 36pt [20%,48% → 35%,53%]: Output Uncertainty
- text 36pt [20%,57% → 35%,62%]: Model Uncertainty
- text on a #80b9ff filled box 32pt [7%,80% → 11%,87%]: {4|#000000}
- heading (spaced caps) 36pt [13%,81% → 87%,86%]: COURSE WRAP UP 🥲
- **Builds:** then: heading (spaced caps) 50pt — fades up from dark; with previous: line #ffffff — draws in; click 1: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 2: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 3: text 32pt — slides in; with previous: text 36pt — slides in; click 4: text 32pt — slides in; with previous: text 36pt — slides in; click 5: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 6: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 8
- heading (spaced caps) 36pt [21%,6% → 79%,11%]: OPERATIONAL DESIGN DOMAIN MONITORING
- text 36pt [5%,14% → 95%,18%]: The operational design domain (ODD) of a system is the set of conditions under which it is designed to operate safely.
- text 36pt [25%,20% → 75%,24%]: [[(e.g. the set of conditions that the model we used for validation covers)|#80b9ff]]
- text 36pt [20%,26% → 80%,30%]: If we operate outside the ODD, our validation results may no longer be valid!
- text 36pt [48%,86% → 52%,90%]: Therefore, we want to monitor at runtime whether a system is operating within its ODD.
- YouTube video https://www.youtube.com/watch?v=9xyXAZCxfcE (thumbnail `hqdefault-38822.jpg`) [47%,38% → 78%,78%]
- rounded box (outline) [17%,33% → 83%,83%]
- text 36pt [22%,48% → 43%,68%]: {There is a decent chance that “truck transporting traffic lights” was not in the operational design domain.|#80b9ff}
- **Builds:** click 1: text 36pt — slides in; click 2: text 36pt — fades up from dark; click 3: rounded box (outline) — fades up from dark; with previous: YouTube video https://www.youtube.com/watch?v=9xyXAZCxfcE (thumbnail ` — fades up from dark; with previous: text 36pt — fades up from dark; click 4: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 9
- heading (spaced caps) 36pt [21%,6% → 79%,11%]: OPERATIONAL DESIGN DOMAIN MONITORING
- text 36pt [48%,13% → 52%,18%]: There are multiple ways to [[represent|#80b9ff]] the operational design domain.
- text 36pt [40%,24% → 60%,28%]: Hand-Designed Features
- image `sandbox-page-1.svg` (cropped: show only 72–93% across and 11–28% down of the image) [37%,31% → 62%,73%]
- rounded box (outline) [33%,21% → 67%,79%]
- **Builds:** click 1: image `sandbox-page-1.svg` (cropped: show only 72–93% across and 11–28 — fades up from dark; with previous: rounded box (outline) — fades up from dark; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 10
- heading (spaced caps) 36pt [21%,6% → 79%,11%]: OPERATIONAL DESIGN DOMAIN MONITORING
- text 36pt [48%,13% → 52%,18%]: There are multiple ways to [[represent|#80b9ff]] the operational design domain.
- text 36pt [20%,23% → 39%,28%]: Hand-Designed Features
- image `sandbox-page-1.svg` (cropped: show only 72–93% across and 11–28% down of the image) [16%,30% → 42%,72%]
- rounded box (outline) [53%,21% → 87%,78%]
- rounded box (outline) [13%,22% → 47%,79%]
- text 36pt [60%,23% → 79%,28%]: Data-Driven Approaches
- image `boston.jpg` [58%,54% → 71%,66%]
- image `reno.jpg` [61%,57% → 74%,70%]
- image `clouds4.jpg` [65%,60% → 78%,72%]
- image `lateafternoon.jpg` [70%,63% → 81%,75%]
- text 36pt [28%,81% → 32%,85%]: {*requires domain knowledge|#fab0ae}
- image `test-42650.svg` [64%,30% → 75%,50%]
- **Builds:** click 1: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 11
- image `test-42650.svg` [64%,30% → 75%,50%]
- heading (spaced caps) 36pt [21%,6% → 79%,11%]: OPERATIONAL DESIGN DOMAIN MONITORING
- text 36pt [48%,13% → 52%,18%]: There are multiple ways to [[represent|#80b9ff]] the operational design domain.
- text 36pt [20%,23% → 39%,28%]: Hand-Designed Features
- image `sandbox-page-1.svg` (cropped: show only 72–93% across and 11–28% down of the image) [16%,30% → 42%,72%]
- rounded box (outline) [53%,21% → 87%,78%]
- rounded box (outline) [13%,22% → 47%,79%]
- text 36pt [60%,23% → 79%,28%]: Data-Driven Approaches
- image `boston.jpg` [58%,54% → 71%,66%]
- image `reno.jpg` [61%,57% → 74%,70%]
- image `clouds4.jpg` [65%,60% → 78%,72%]
- image `lateafternoon.jpg` [70%,63% → 81%,75%]
- text 36pt [28%,81% → 32%,85%]: {*requires domain knowledge|#fab0ae}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 12
- image `test-42650.svg` [27%,10% → 73%,90%]
- image `test-42656.svg` [27%,10% → 73%,90%]
- image `test-39186.svg` [27%,10% → 73%,90%]
- **Builds:** click 1: image `test-42656.svg` — fades in; click 2: image `test-39186.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 13
- image `test-39186.svg` [44%,10% → 89%,90%]
- text 36pt [7%,44% → 38%,56%]: We want to use this data to determine the [[set of states|#80b9ff]] that are part of the operational design domain.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 14
- rounded box (filled #424242) [4%,49% → 41%,65%]
- image `test-39186.svg` [44%,10% → 89%,90%]
- text 36pt [7%,35% → 38%,47%]: We want to use this data to determine the [[set of states|#80b9ff]] that are part of the operational design domain.
- text 36pt [5%,51% → 40%,63%]: One option is to define the ODD as the set of points whose [[nearest neighbor|#80b9ff]] in the data set is within a certain threshold distance.
- image `test-39358.svg` [44%,10% → 89%,90%]
- text on a #80b9ff filled box 32pt [13%,72% → 32%,80%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 15
- rounded box (filled #424242) [32%,6% → 68%,22%]
- text 36pt [33%,8% → 67%,20%]: One option is to define the ODD as the set of points whose [[nearest neighbor|#80b9ff]] in the data set is within a certain threshold distance.
- image `val-page-288.svg` (cropped: show only 7–55% across and 13–30% down of the image) [23%,27% → 77%,65%]
- rounded box (filled #424242) [27%,67% → 74%,77%]
- heading (spaced caps) 75pt [26%,65% → 32%,79%]: 🤔
- text 36pt [31%,69% → 73%,75%]: What are some potential drawbacks of this approach?
- text 36pt [24%,80% → 76%,88%]: It requires storing the entire dataset in [[memory|#80b9ff]] at runtime and computing nearest neighbors can be [[computationally expensive|#80b9ff]].
- **Builds:** click 1: heading (spaced caps) 75pt — fades up from dark; with previous: rounded box (filled #424242) — fades up from dark; with previous: text 36pt — fades up from dark; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 16
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [6%,38% → 40%,50%]: One option is to define the ODD as the set of points whose [[nearest neighbor|#80b9ff]] in the data set is within a certain threshold distance.
- text 36pt [12%,57% → 34%,69%]: We can improve computational performance by [[clustering|#80b9ff]]!
- image `test-39186.svg` [47%,10% → 92%,90%]
- image `test-39463.svg` [47%,10% → 92%,90%]
- image `test-39469.svg` [47%,10% → 92%,90%]
- text 36pt [7%,21% → 39%,33%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- **Builds:** click 1: image `test-39463.svg` — fades in; click 2: image `test-39469.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 17
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [6%,54% → 40%,66%]: One option is to define the ODD as the set of points whose [[nearest neighbor|#80b9ff]] in the data set is within a certain threshold distance.
- image `test-39186.svg` [47%,10% → 92%,90%]
- text 36pt [7%,38% → 39%,50%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [21%,54% → 25%,58%]: {e.g. take the convex hull of the data|#80b9ff}
- image `test-39512.svg` [47%,10% → 92%,90%]
- text 36pt [68%,69% → 91%,81%]: We might include areas we shouldn’t when the ODD is [[nonconvex|#80b9ff]]!
- arrow #ffffff [64%,60% → 79%,64%]
- **Builds:** click 1: text 36pt — slides in; with previous: image `test-39512.svg` — fades in; click 2: arrow #ffffff — draws in; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 18
- rounded box (filled #424242) [5%,36% → 41%,52%]
- image `test-39186.svg` [47%,10% → 92%,90%]
- text 36pt [7%,38% → 39%,50%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [21%,54% → 25%,58%]: {e.g. take the convex hull of the data|#80b9ff}
- text 36pt [10%,61% → 36%,69%]: Or take the union of the convex hulls of [[clusters|#80b9ff]] of the data.
- image `test-39561.svg` [47%,10% → 92%,90%]
- image `test-39567.svg` [47%,10% → 92%,90%]
- image `test-39573.svg` [47%,10% → 92%,90%]
- image `test-39579.svg` [47%,10% → 92%,90%]
- image `test-39585.svg` [47%,10% → 92%,90%]
- **Builds:** click 1: image `test-39561.svg` — fades in; click 2: image `test-39567.svg` — fades in; click 3: image `test-39573.svg` — fades in; click 4: image `test-39579.svg` — fades in; click 5: image `test-39585.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 19
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [7%,38% → 39%,50%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [21%,54% → 25%,58%]: {e.g. take the convex hull of the data|#80b9ff}
- text 36pt [10%,61% → 36%,69%]: Or take the union of the convex hulls of [[clusters|#80b9ff]] of the data.
- image `screenshot-2025-03-01-at-10-56-28-am.png` [49%,11% → 90%,76%]
- text 36pt [46%,80% → 93%,85%]: And this is how I know I work with the absolute best people!
- **Builds:** click 1: image `screenshot-2025-03-01-at-10-56-28-am.png` — fades up from dark; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 20
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [7%,38% → 39%,50%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [21%,54% → 25%,58%]: {e.g. take the convex hull of the data|#80b9ff}
- text 36pt [10%,61% → 36%,69%]: Or take the union of the convex hulls of [[clusters|#80b9ff]] of the data.
- image `val-page-289.svg` (cropped: show only 11–69% across and 21–42% down of the image) [48%,35% → 90%,66%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 21
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [7%,38% → 39%,50%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [21%,54% → 25%,58%]: {e.g. take the convex hull of the data|#80b9ff}
- text 36pt [10%,61% → 36%,69%]: Or take the union of the convex hulls of [[clusters|#80b9ff]] of the data.
- image `val-page-289.svg` (cropped: show only 11–69% across and 21–42% down of the image) [47%,62% → 89%,93%]
- image `e11d3094-fdcf-4f8d-9e38-25f9a3e95746.png` [56%,12% → 81%,57%]
- text 18pt [74%,9% → 81%,11%]: Credit: ChatGPT
- text 36pt [7%,26% → 39%,34%]: Another option is to define the ODD as the [[superlevel set|#80b9ff]] of a function.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 22
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [7%,55% → 39%,67%]: Another option is to define the ODD using a more compact set representation such as a [[polytope|#80b9ff]].
- text 36pt [7%,39% → 39%,48%]: Another option is to define the ODD as the [[superlevel set|#80b9ff]] of a function.
- image `test-39186.svg` [48%,10% → 93%,90%]
- text 36pt [21%,54% → 25%,58%]: {e.g. take the superlevel set of a distribution|#80b9ff}
- image `test-39705.svg` [48%,10% → 93%,90%]
- image `test-39713.svg` [48%,10% → 93%,90%]
- image `test-39744.svg` [48%,10% → 93%,90%]
- image `test-39751.svg` [48%,10% → 93%,90%]
- text 36pt [67%,67% → 91%,79%]: It is important to select a model class that is expressive enough!
- **Builds:** click 1: text 36pt — slides in; click 2: image `test-39705.svg` — fades in; click 3: image `test-39713.svg` — fades in; click 4: text 36pt — fades up from dark; click 5: image `test-39744.svg` — fades in; click 6: image `test-39751.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 23
- image `test-39186.svg` [48%,10% → 93%,90%]
- image `test-39839.svg` [48%,10% → 93%,90%]
- rounded box (filled #424242) [5%,36% → 41%,52%]
- text 36pt [7%,39% → 39%,48%]: Another option is to define the ODD as the [[superlevel set|#80b9ff]] of a function.
- text 36pt [21%,54% → 25%,58%]: {e.g. take the superlevel set of a distribution|#80b9ff}
- text 36pt [7%,64% → 39%,76%]: {take the superlevel set of a model trained to output the likelihood of a point being in the ODD|#80b9ff}
- text 36pt [21%,59% → 25%,64%]: or
- image `test-39803.svg` [48%,10% → 93%,90%]
- image `test-39809.svg` [48%,10% → 93%,90%]
- rounded box (filled #424242) [64%,53% → 89%,70%]
- heading (spaced caps) 75pt [65%,55% → 71%,68%]: 🤔
- text 36pt [69%,55% → 89%,67%]: What is one potential drawback of this approach?
- text 36pt [75%,71% → 78%,76%]: It requires data from outside the ODD!
- **Builds:** click 1: text 36pt — slides in; click 2: image `test-39839.svg` — fades in; click 3: image `test-39803.svg` — fades in; click 4: image `test-39809.svg` — fades in; click 5: heading (spaced caps) 75pt — fades up from dark; with previous: rounded box (filled #424242) — fades up from dark; with previous: text 36pt — fades up from dark; click 6: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 24
- text 36pt [32%,22% → 68%,27%]: This all works well in low-dimensional ODDs.
- image `test-39358.svg` [14%,31% → 31%,60%]
- image `test-39512.svg` [33%,31% → 49%,60%]
- image `test-39751.svg` [51%,31% → 67%,60%]
- image `test-39809.svg` [69%,31% → 86%,60%]
- text 36pt [32%,64% → 68%,69%]: Things get a little weird in high-dimensions.
- text 36pt [38%,69% → 62%,74%]: {(e.g. ODDs defined by images)|#80b9ff}
- **Builds:** click 1: text 36pt — wipes in; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 25
- text 36pt [33%,6% → 67%,10%]: Things get a little weird in high-dimensions.
- text 36pt [38%,11% → 62%,15%]: {(e.g. ODDs defined by images)|#80b9ff}
- text 36pt [15%,22% → 85%,27%]: The [[volume|#80b9ff]] of the space the data must cover increases [[exponentially|#80b9ff]] with the data dimension.
- outlined circle #ffffff [20%,30% → 25%,38%]
- equation $1$ (36pt, #ffffff) [22%,33% → 23%,35%]
- text 36pt [27%,32% → 69%,36%]: We will need more data to adequately cover the space.
- outlined circle #ffffff [20%,44% → 25%,52%]
- equation $2$ (36pt, #ffffff) [22%,47% → 23%,49%]
- text 36pt [26%,46% → 51%,50%]: Distance metrics lose meaning.
- line #ffffff [10%,17% → 90%,21%]
- text 36pt [27%,53% → 75%,61%]: {e.g. what is the distance between two images? |#80b9ff} / Euclidean distance between vectors of pixel values?
- text 36pt [22%,69% → 78%,73%]: One option is to get [[more data|#80cfb9]] and [[better models|#80cfb9]] (e.g. normalizing flows).
- text 36pt [7%,76% → 95%,80%]: Another option is to [[project the data onto a lower-dimensional manifold|#c3b8ff]] using dimensionality reduction techniques.
- **Builds:** click 1: outlined circle #ffffff — fades up from dark; with previous: equation $1$ — fades up from dark; with previous: text 36pt — fades up from dark; click 2: outlined circle #ffffff — fades up from dark; with previous: equation $2$ — fades up from dark; with previous: text 36pt — fades up from dark; click 3: text 36pt — slides in; click 4: text 36pt — fades up from dark; click 5: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 26
- text 36pt [7%,7% → 93%,11%]: Another option is to [[project the data onto a lower-dimensional manifold|#c3b8ff]] using dimensionality reduction techniques.
- image `test-40030.svg` [29%,22% → 89%,91%]
- image `test-40059.svg` [5%,31% → 26%,69%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 27
- image `test-40030.svg` [29%,22% → 89%,91%]
- image `test-40070.svg` [29%,22% → 89%,91%]
- text 36pt [7%,7% → 93%,11%]: Another option is to [[project the data onto a lower-dimensional manifold|#c3b8ff]] using dimensionality reduction techniques.
- arrow #0072fe [61%,60% → 66%,64%]
- image `test-40059.svg` [54%,46% → 62%,59%]
- image `test-40083.svg` [5%,34% → 26%,73%]
- **Builds:** click 1: image `test-40070.svg` — fades in; click 2: image `test-40083.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 28
- image `test-40030.svg` [29%,22% → 89%,91%]
- image `test-40070.svg` [29%,22% → 89%,91%]
- image `test-40090.svg` [29%,22% → 89%,91%]
- text 36pt [7%,7% → 93%,11%]: Another option is to [[project the data onto a lower-dimensional manifold|#c3b8ff]] using dimensionality reduction techniques.
- arrow #0072fe [61%,60% → 66%,64%]
- image `test-40059.svg` [54%,46% → 62%,59%]
- image `test-40083.svg` [34%,68% → 41%,81%]
- arrow #f5615c [40%,64% → 45%,68%]
- image `test-40140.svg` [5%,34% → 27%,72%]
- **Builds:** click 1: image `test-40140.svg` — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 29
- image `test-40030.svg` [29%,22% → 89%,91%]
- image `test-40070.svg` [29%,22% → 89%,91%]
- image `test-40090.svg` [29%,22% → 89%,91%]
- image `test-40158.svg` [29%,22% → 89%,91%]
- text 36pt [7%,7% → 93%,11%]: Another option is to [[project the data onto a lower-dimensional manifold|#c3b8ff]] using dimensionality reduction techniques.
- arrow #0072fe [61%,60% → 66%,64%]
- image `test-40059.svg` [54%,46% → 62%,59%]
- image `test-40083.svg` [34%,68% → 41%,81%]
- arrow #f5615c [40%,64% → 45%,68%]
- image `test-40140.svg` [77%,28% → 85%,41%]
- arrow #e69f00 [79%,43% → 84%,47%]
- image `test-40195.svg` [69%,28% → 77%,41%]
- arrow #0072fe [73%,43% → 82%,47%]
- text 36pt [7%,49% → 24%,57%]: {This issue is known as |#f3cf80} / feature collapse.
- **Builds:** click 1: image `test-40195.svg` — fades up from dark; with previous: arrow #0072fe — draws in; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 30
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: OPERATIONAL DESIGN DOMAIN MONITORING
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: UNCERTAINTY QUANTIFICATION
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,67% → 11%,73%]: {3|#000000}
- heading (spaced caps) 36pt [13%,68% → 87%,72%]: FAILURE MONITORING
- text 32pt [15%,47% → 18%,54%]: {A|#80b9ff}
- text 32pt [15%,56% → 18%,63%]: {B|#80b9ff}
- text 36pt [20%,48% → 35%,53%]: Output Uncertainty
- text 36pt [20%,57% → 35%,62%]: Model Uncertainty
- text on a #80b9ff filled box 32pt [7%,80% → 11%,87%]: {4|#000000}
- heading (spaced caps) 36pt [13%,81% → 87%,86%]: COURSE WRAP UP 🥲
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 31
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- text 36pt [42%,28% → 58%,32%]: It is helpful to understand our uncertainty in various aspects of the [[current and future behavior|#80b9ff]] of the system.
- rounded box (outline) [24%,3% → 76%,23%]
- text 36pt [17%,34% → 83%,43%]: We can quantify uncertainty by [[creating models|#80b9ff]] that predict some aspect of system behavior and understanding the uncertainty in the predictions.
- vector icon `shape-56a7e441.svg` [31%,73% → 38%,92%]
- group [38%,48% → 67%,71%]
  - shape (outline) [38%,48% → 67%,71%]
- text 28pt [42%,56% → 64%,63%]: {I think I am 2 meters from the wall, but I am only 60% sure of this.|#80b9ff}
- **Builds:** click 1: text 36pt — slides in; click 2: vector icon `shape-56a7e441.svg` — slides in; click 3: group — wipes in; with previous: text 28pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 32
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Builds:** click 1: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 33
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 34
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 35
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 36
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 37
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `screenshot-2025-03-02-at-10-32-44-am.png` [27%,30% → 48%,84%]
- image `pasted-image-40330.png` (cropped: show only 15–83% across and 1–99% down of the image) [53%,30% → 73%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [27%,30% → 48%,84%]
- black cover-up box (Keynote crop hack; just crop the media instead) [53%,31% → 73%,84%]
- text 36pt [48%,90% → 52%,94%]: Which one is Mykel and which one is Matt Damon?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 38
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `agv-vufowx3jocfjzhj-cwzjuwer5txhglm4qfkilup7lmbxxxhsvuz6o18o6nkmmk-442u14vmxrfbppy-aod39fm95mm5indpzoasknodgdf8tznnp5yy5-fcdutt-txur71bncegb7oucywxmdih3rzjntlma2d8-s2048.png` [37%,36% → 63%,85%]
- text 36pt [48%,29% → 52%,33%]: What is this?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 39
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- image `agv-vufowx3jocfjzhj-cwzjuwer5txhglm4qfkilup7lmbxxxhsvuz6o18o6nkmmk-442u14vmxrfbppy-aod39fm95mm5indpzoasknodgdf8tznnp5yy5-fcdutt-txur71bncegb7oucywxmdih3rzjntlma2d8-s2048.png` [24%,36% → 50%,84%]
- text 36pt [48%,29% → 52%,33%]: What is this?
- image `agv-vud0xl-goqki8mlv4ysx9hqcvsja1zggo-qbneqxzk6xp1a5qyr6atephpxaean2ewfprtunvpfk7nd3cwxlflnk510xtijk3ldh9as68vvqezfey1ykkacuguatyekopytruz0icgijgrvclfw4lfifqo1v442f-s2048.png` [53%,36% → 73%,84%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 40
- heading (spaced caps) 36pt [30%,5% → 70%,10%]: UNCERTAINTY QUANTIFICATION
- text 32pt [27%,13% → 31%,19%]: {A|#80b9ff}
- text 32pt [53%,13% → 57%,19%]: {B|#80b9ff}
- text 36pt [33%,14% → 48%,18%]: Output Uncertainty
- text 36pt [58%,14% → 73%,18%]: Model Uncertainty
- rounded box (outline) [24%,3% → 76%,23%]
- heading (spaced caps) 54pt [26%,35% → 44%,81%]: {2🙂2 = 4|#adadad} / {3|#000000}🙂8 = 11 / 2{7|#000000}🙂100 = 127 / 8{😮|#000000}{2|#000000}{ = 6|#adadad} / {23😮|#adadad}{3|#000000} = 20 / 4😮1 {=|#000000} 3
- text 54pt [57%,44% → 78%,51%]: {What is 1🙂6😮2?|#adadad}
- text 54pt [57%,58% → 78%,65%]: {What is 1😂6🙃2?|#80b9ff}
- **Builds:** click 1: text 54pt — wipes in; click 2: text 54pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 41
- heading (spaced caps) 36pt [30%,22% → 70%,26%]: UNCERTAINTY QUANTIFICATION
- text 32pt [10%,36% → 14%,42%]: {A|#80b9ff}
- text 32pt [10%,60% → 14%,66%]: {B|#80b9ff}
- text 36pt [15%,37% → 31%,41%]: Output Uncertainty
- text 36pt [15%,61% → 30%,65%]: Model Uncertainty
- text 36pt [31%,37% → 81%,41%]: {occurs when a single input can lead to multiple different outputs.|#80b9ff}
- text 36pt [17%,44% → 69%,49%]: {e.g. randomness in the real world due to other agents, sensor noise|#c0c0c0}
- text 36pt [30%,61% → 85%,65%]: {occurs due to limitations of the model used to predict system behavior.|#80b9ff}
- text 36pt [17%,69% → 29%,73%]: {e.g. lack of data|#c0c0c0}
- rounded box (outline) [8%,16% → 92%,86%]
- text 36pt [17%,50% → 57%,55%]: {a.k.a aleatoric uncertainty or irreducible uncertainty|#ffa4e7}
- text 36pt [17%,75% → 57%,80%]: {a.k.a epistemic uncertainty or reducible uncertainty|#ffa4e7}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 42
- heading (spaced caps) 36pt [30%,8% → 70%,13%]: UNCERTAINTY QUANTIFICATION
- text 32pt [10%,15% → 14%,22%]: {A|#80b9ff}
- text 32pt [10%,33% → 14%,40%]: {B|#80b9ff}
- text 36pt [15%,16% → 31%,21%]: Output Uncertainty
- text 36pt [15%,34% → 30%,38%]: Model Uncertainty
- text 36pt [31%,16% → 81%,21%]: {occurs when a single input can lead to multiple different outputs.|#80b9ff}
- text 36pt [17%,23% → 69%,28%]: {e.g. randomness in the real world due to other agents, sensor noise|#c0c0c0}
- text 36pt [30%,34% → 85%,38%]: {occurs due to limitations of the model used to predict system behavior.|#80b9ff}
- text 36pt [17%,42% → 29%,47%]: {e.g. lack of data|#c0c0c0}
- rounded box (outline) [8%,4% → 92%,51%]
- image `test-40524.svg` [25%,56% → 75%,95%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 43
- text 36pt [24%,48% → 39%,52%]: Output Uncertainty
- text 36pt [39%,48% → 76%,52%]: is [[present in the data|#80b9ff]] we gather from the system.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 44
- text 36pt [24%,44% → 39%,49%]: Output Uncertainty
- text 36pt [39%,44% → 76%,49%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [48%,49% → 52%,54%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 45
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- text 36pt [5%,18% → 77%,22%]: For regression problems, we get to throwback to my favorite derivation EVER from lecture 2:
- image `val-page-29.svg` (cropped: show only 17–66% across and 25–55% down of the image) [25%,29% → 75%,90%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 46
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- text 36pt [5%,18% → 77%,22%]: For regression problems, we get to throwback to my favorite derivation EVER from lecture 2:
- image `val-page-29.svg` (cropped: show only 17–66% across and 25–55% down of the image) [14%,38% → 45%,76%]
- image `val-page-296.svg` (cropped: show only 8–66% across and 39–72% down of the image) [55%,38% → 88%,76%]
- shape (outline) [47%,53% → 53%,61%]
- text 36pt [27%,30% → 31%,35%]: assume [[constant|#80b9ff]] variance
- text 36pt [62%,30% → 82%,35%]: assume [[nonconstant|#80b9ff]] {(varying?)|#80b9ff} variance
- outlined shape #80b9ff [58%,69% → 77%,75%]
- **Builds:** click 1: outlined shape #80b9ff — LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 47
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- outlined shape #80b9ff [31%,25% → 69%,41%]
- equation $\hat \theta = \operatorname{argmin}_{\mathbf \theta} \sum_{i=1}^m \left[\frac{(y_i - \mu_{\mathbf \theta}(x_i))^2}{\sigma^2_{\mathbf \theta}(x_i)} + \log(\sigma^2_{\mathbf \theta}(x_i)) \right]$ (36pt, #ffffff) [33%,28% → 67%,38%]
- text 36pt [61%,54% → 78%,59%]: {minimize the variance |#80b9ff}
- arrow #80b9ff [60%,43% → 71%,48%]
- text 36pt [34%,56% → 56%,68%]: {make the variance high in areas where the squared error is high|#80b9ff}
- arrow #80b9ff [42%,45% → 54%,49%]
- **Builds:** click 1: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 2: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 48
- image `test-40738.svg` [16%,42% → 84%,94%]
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- outlined shape #80b9ff [31%,19% → 69%,35%]
- equation $\hat \theta = \operatorname{argmin}_{\mathbf \theta} \sum_{i=1}^m \left[\frac{(y_i - \mu_{\mathbf \theta}(x_i))^2}{\sigma^2_{\mathbf \theta}(x_i)} + \log(\sigma^2_{\mathbf \theta}(x_i)) \right]$ (36pt, #ffffff) [33%,22% → 67%,32%]
- image `test-40730.svg` [16%,42% → 84%,94%]
- text 36pt [21%,48% → 51%,52%]: {low variance = low output uncertainty|#80cfb9}
- arrow #80cfb9 [32%,54% → 36%,58%]
- text 36pt [46%,80% → 76%,85%]: {high variance = high output uncertainty|#fab0ae}
- arrow #fab0ae [62%,76% → 68%,80%]
- **Builds:** click 1: image `test-40730.svg` — fades in; click 2: text 36pt — fades up from dark; with previous: text 36pt — fades up from dark; with previous: arrow #80cfb9 — draws in; with previous: arrow #fab0ae — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 49
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- text 36pt [16%,17% → 84%,22%]: For classification models, we can use the [[softmax function|#80b9ff]] to output a discrete distribution:
- image `noun-neural-network-6262188-80b9ff.png` (cropped: show only 15–85% across and 25–75% down of the image) [15%,41% → 47%,83%]
- text 36pt [48%,44% → 54%,48%]: {Class 1|#80b9ff}
- text 36pt [48%,59% → 54%,64%]: {Class 2|#80b9ff}
- text 36pt [48%,75% → 54%,80%]: {Class 3|#80b9ff}
- text 36pt [56%,30% → 62%,34%]: {softmax|#80b9ff}
- group [57%,38% → 82%,86%]
  - outlined shape #80b9ff [57%,38% → 61%,86%]
  - filled shape #80b9ff [61%,41% → 82%,51%]
  - filled shape #80b9ff [61%,57% → 66%,66%]
  - filled shape #80b9ff [61%,73% → 62%,82%]
- equation $0.8$ (36pt, #80b9ff) [83%,45% → 85%,47%]
- equation $0.15$ (36pt, #80b9ff) [66%,61% → 69%,63%]
- equation $0.05$ (36pt, #80b9ff) [63%,76% → 66%,79%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 50
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- outlined shape #80b9ff [65%,53% → 69%,101%]
- filled shape #80b9ff [53%,61% → 62%,70%]
- filled shape #80b9ff [62%,61% → 71%,70%]
- filled shape #80b9ff [71%,61% → 80%,70%]
- text 36pt [33%,23% → 37%,28%]: {Low Uncertainty|#80cfb9}
- text 36pt [60%,23% → 73%,28%]: {High Uncertainty|#fab0ae}
- group [21%,35% → 46%,83%]
  - outlined shape #80b9ff [21%,35% → 25%,83%]
  - filled shape #80b9ff [25%,38% → 46%,48%]
  - filled shape #80b9ff [25%,54% → 29%,63%]
  - filled shape #80b9ff [25%,70% → 26%,79%]
- **Builds:** click 1: text 36pt — slides in; with previous: outlined shape #80b9ff — slides in; with previous: filled shape #80b9ff — slides in; with previous: filled shape #80b9ff — slides in; with previous: filled shape #80b9ff — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 51
- text 36pt [24%,5% → 39%,10%]: Output Uncertainty
- text 36pt [39%,5% → 76%,10%]: is [[present in the data|#80b9ff]] we gather from the system.
- text 36pt [9%,10% → 91%,15%]: Therefore, we can train a model using this data to [[output the parameters of a distribution|#80b9ff]] over its prediction.
- outlined shape #80b9ff [29%,60% → 31%,83%]
- filled shape #80b9ff [24%,63% → 28%,68%]
- filled shape #80b9ff [28%,63% → 32%,68%]
- filled shape #80b9ff [32%,63% → 37%,68%]
- text 36pt [9%,44% → 22%,48%]: {Low Uncertainty|#80cfb9}
- text 36pt [23%,43% → 37%,49%]: {High Uncertainty|#fab0ae}
- group [8%,51% → 20%,74%]
  - outlined shape #80b9ff [8%,51% → 10%,74%]
  - filled shape #80b9ff [10%,53% → 20%,57%]
  - filled shape #80b9ff [10%,60% → 12%,64%]
  - filled shape #80b9ff [10%,67% → 11%,72%]
- image `agv-vuc8fk8x62w7-hr3r4rlrgytslnunszuvir0sgxqzixqsymhjwuz9fuuwbruwv0xq9gddqgrf5t6qv5jmvxob0erbi-ua2shu0icr1lrdpwceag8hcaaflzbzak6j1pdrj5dcvrrefn0vs9y1u7r9z7x2ic5he0-s2048.png` [46%,32% → 91%,101%]
- text 36pt [51%,19% → 86%,27%]: {We often end up having an issue with calibration of the output distribution.|#f3cf80}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 52
- text 36pt [21%,43% → 79%,48%]: {We often end up having an issue with calibration of the output distribution.|#f3cf80}
- text 36pt [3%,48% → 97%,53%]: If we were able to [[perfectly minimize|#80b9ff]] the log-likelihood, the output distribution would [[perfectly match|#80b9ff]] the true distribution.
- text 36pt [28%,55% → 72%,59%]: {In practice, training is approximate and we need to apply some additional techniques to calibrate the model.|#f3cf80}
- **Builds:** click 1: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 53
- text 36pt [9%,7% → 91%,11%]: {In practice, training is approximate and we need to apply some additional techniques to calibrate the model.|#f3cf80}
- rounded box (filled #80b9ff) [26%,15% → 74%,24%]
- text 36pt [48%,17% → 52%,22%]: {See section 12.2.2 for an overview of calibration techniques.|#000000}
- text 36pt [48%,27% → 52%,32%]: An easy technique to try for classification models that use softmax:
- equation $p_i$ (78pt, #ffffff) [29%,50% → 32%,55%]
- equation $\exp($ (78pt, #ffffff) [43%,44% → 49%,50%]
- equation $=$ (78pt, #ffffff) [34%,51% → 36%,53%]
- equation $y_i)$ (78pt, #ffffff) [50%,44% → 54%,51%]
- equation $\sum_{j=1}^k \exp($ (78pt, #ffffff) [40%,54% → 53%,76%]
- equation $y_j)$ (78pt, #ffffff) [54%,61% → 57%,69%]
- line #ffffff [37%,50% → 61%,54%]
- **Builds:** click 1: text 36pt — fades up from dark; with previous: equation $y_i)$ — fades up from dark; with previous: equation $\exp($ — fades up from dark; with previous: equation $p_i$ — fades up from dark; with previous: equation $=$ — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: equation $\sum_{j=1}^k \exp($ — fades up from dark; with previous: equation $y_j)$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 54
- text 36pt [9%,7% → 91%,11%]: {In practice, training is approximate and we need to apply some additional techniques to calibrate the model.|#f3cf80}
- rounded box (filled #80b9ff) [26%,15% → 74%,24%]
- text 36pt [48%,17% → 52%,22%]: {See section 12.2.2 for an overview of calibration techniques.|#000000}
- text 36pt [48%,27% → 52%,32%]: An easy technique to try for classification models that use softmax:
- equation $p_i$ (78pt, #ffffff) [29%,50% → 32%,55%]
- equation $\exp($ (78pt, #ffffff) [43%,44% → 49%,50%]
- equation $=$ (78pt, #ffffff) [34%,51% → 36%,53%]
- equation $y_i)$ (78pt, #ffffff) [52%,44% → 56%,51%]
- equation $\sum_{j=1}^k \exp($ (78pt, #ffffff) [40%,54% → 53%,76%]
- equation $y_j)$ (78pt, #ffffff) [55%,61% → 59%,69%]
- line #ffffff [37%,50% → 61%,54%]
- equation $\lambda$ (78pt, #80b9ff) [50%,45% → 52%,50%]
- equation $\lambda$ (78pt, #80b9ff) [53%,62% → 55%,67%]
- text 36pt [67%,48% → 92%,57%]: We introduce a parameter {$\lambda$|#80b9ff} that adjusts the softmax probabilities.
- text 36pt [37%,83% → 69%,92%]: {This is sometimes written as $\lambda = 1 / T$ where $T$ is a temperature parameter.|#80b9ff}
- arrow #80b9ff [49%,73% → 57%,77%]
- arrow #80b9ff [42%,64% → 60%,69%]
- **Builds:** click 1: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 55
- text 36pt [9%,7% → 91%,11%]: {In practice, training is approximate and we need to apply some additional techniques to calibrate the model.|#f3cf80}
- rounded box (filled #80b9ff) [26%,15% → 74%,24%]
- text 36pt [48%,17% → 52%,22%]: {See section 12.2.2 for an overview of calibration techniques.|#000000}
- text 36pt [48%,27% → 52%,32%]: An easy technique to try for classification models that use softmax:
- equation $p_i$ (36pt, #ffffff) [43%,38% → 44%,40%]
- equation $\exp($ (36pt, #ffffff) [49%,35% → 52%,38%]
- equation $=$ (36pt, #ffffff) [45%,38% → 46%,39%]
- equation $y_i)$ (36pt, #ffffff) [53%,35% → 55%,38%]
- equation $\sum_{j=1}^k \exp($ (36pt, #ffffff) [48%,40% → 54%,50%]
- equation $y_j)$ (36pt, #ffffff) [55%,43% → 56%,46%]
- line #ffffff [46%,37% → 57%,41%]
- equation $\lambda$ (36pt, #80b9ff) [52%,35% → 53%,38%]
- equation $\lambda$ (36pt, #80b9ff) [54%,44% → 55%,46%]
- arrow #80b9ff [9%,82% → 91%,86%]
- equation $\lambda$ (59pt, #80b9ff) [49%,90% → 51%,94%]
- line #80b9ff [35%,82% → 38%,86%]
- equation $1$ (36pt, #80b9ff) [36%,88% → 37%,91%]
- group [31%,56% → 43%,78%]
  - outlined shape #80b9ff [31%,56% → 33%,78%]
  - filled shape #80b9ff [33%,57% → 43%,62%]
  - filled shape #80b9ff [33%,65% → 35%,69%]
  - filled shape #80b9ff [33%,72% → 33%,77%]
- line #80b9ff [14%,82% → 17%,86%]
- equation $0$ (36pt, #80b9ff) [15%,88% → 16%,91%]
- group [10%,56% → 16%,78%]
  - outlined shape #80b9ff [10%,56% → 12%,78%]
  - filled shape #80b9ff [12%,57% → 16%,62%]
  - filled shape #80b9ff [12%,65% → 16%,69%]
  - filled shape #80b9ff [12%,72% → 16%,77%]
- line #80b9ff [85%,82% → 88%,86%]
- equation $\infty$ (36pt, #80b9ff) [86%,89% → 87%,90%]
- group [80%,56% → 95%,78%]
  - outlined shape #80b9ff [80%,56% → 82%,78%]
  - filled shape #80b9ff [82%,57% → 95%,62%]
  - filled shape #80b9ff [82%,65% → 82%,69%]
  - filled shape #80b9ff [82%,72% → 83%,77%]
- group [45%,56% → 77%,72%]
  - text 36pt [46%,58% → 76%,70%]: We can pick the value for {$\lambda$|#80b9ff} that minimizes the negative log likelihood on a calibration set.
  - rounded box (outline) [45%,56% → 77%,72%]
- text on a #80b9ff filled box 32pt [51%,73% → 70%,81%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: line #80b9ff — draws in; with previous: equation $1$ — fades up from dark; click 2: group — slides in; click 3: line #80b9ff — draws in; with previous: equation $0$ — fades up from dark; click 4: group — slides in; click 5: line #80b9ff — draws in; with previous: equation $\infty$ — fades up from dark; click 6: group — slides in; click 7: group — fades up from dark; click 8: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 56
- text 36pt [24%,48% → 76%,52%]: We can also quantify uncertainty using prediction sets.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 57
- text 36pt [29%,46% → 71%,50%]: We can also quantify uncertainty using prediction sets.
- text 36pt [29%,51% → 71%,56%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 58
- image `test-41305.svg` [28%,7% → 74%,89%]
- image `test-41321.svg` [28%,7% → 74%,89%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- line #80b9ff [26%,46% → 45%,50%]
- line #80b9ff [57%,46% → 75%,50%]
- arrow #80b9ff [36%,38% → 66%,42%]
- text 36pt [49%,18% → 53%,22%]: Suppose we want a prediction set with 95% coverage ($c=0.95$).
- **Builds:** click 1: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: image `test-41321.svg` — fades in; click 2: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 59
- shape filled #80b9ff, outlined #80b9ff [51%,49% → 56%,59%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- image `test-41305.svg` [18%,27% → 44%,73%]
- image `test-41321.svg` [18%,27% → 44%,73%]
- line #80b9ff [17%,48% → 27%,52%]
- line #80b9ff [34%,48% → 44%,52%]
- arrow #80b9ff [22%,43% → 39%,48%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [63%,66% → 65%,72%]
- line #ffffff [52%,57% → 55%,61%]
- line #ffffff [59%,57% → 62%,61%]
- line #ffffff [67%,57% → 69%,61%]
- line #ffffff [74%,57% → 77%,61%]
- equation $1$ (36pt, #ffffff) [53%,64% → 54%,66%]
- equation $2$ (36pt, #ffffff) [60%,64% → 61%,66%]
- equation $3$ (36pt, #ffffff) [68%,64% → 68%,66%]
- equation $4$ (36pt, #ffffff) [75%,64% → 76%,66%]
- shape filled #80b9ff, outlined #80b9ff [58%,52% → 63%,59%]
- shape filled #80b9ff, outlined #80b9ff [65%,55% → 71%,59%]
- shape filled #80b9ff, outlined #80b9ff [73%,58% → 78%,59%]
- line #ffffff [50%,57% → 79%,61%]
- equation $0.4$ (28pt, #80b9ff) [53%,46% → 54%,48%]
- equation $0.33$ (28pt, #80b9ff) [60%,49% → 62%,51%]
- equation $0.24$ (28pt, #80b9ff) [67%,52% → 69%,53%]
- equation $0.03$ (28pt, #80b9ff) [74%,56% → 77%,58%]
- text 36pt [49%,18% → 53%,22%]: Suppose we want a prediction set with 95% coverage ($c=0.95$).
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 60
- shape filled #80b9ff, outlined #80b9ff [51%,49% → 56%,59%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- image `test-41305.svg` [18%,27% → 44%,73%]
- image `test-41321.svg` [18%,27% → 44%,73%]
- line #80b9ff [17%,48% → 27%,52%]
- line #80b9ff [34%,48% → 44%,52%]
- arrow #80b9ff [22%,43% → 39%,48%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [63%,66% → 65%,72%]
- line #ffffff [52%,57% → 55%,61%]
- line #ffffff [59%,57% → 62%,61%]
- line #ffffff [67%,57% → 69%,61%]
- line #ffffff [74%,57% → 77%,61%]
- equation $1$ (36pt, #ffffff) [53%,64% → 54%,66%]
- equation $2$ (36pt, #ffffff) [60%,64% → 61%,66%]
- equation $3$ (36pt, #ffffff) [68%,64% → 68%,66%]
- equation $4$ (36pt, #ffffff) [75%,64% → 76%,66%]
- shape filled #80b9ff, outlined #80b9ff [58%,52% → 63%,59%]
- shape filled #80b9ff, outlined #80b9ff [65%,55% → 71%,59%]
- shape filled #80b9ff, outlined #80b9ff [73%,58% → 78%,59%]
- line #ffffff [50%,57% → 79%,61%]
- equation $0.4$ (28pt, #80b9ff) [53%,46% → 54%,48%]
- equation $0.33$ (28pt, #80b9ff) [60%,49% → 62%,51%]
- equation $0.24$ (28pt, #80b9ff) [67%,52% → 69%,53%]
- equation $0.03$ (28pt, #80b9ff) [74%,56% → 77%,58%]
- text 36pt [49%,18% → 53%,22%]: Suppose we want a prediction set with 95% coverage ($c=0.95$).
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 61
- shape filled #80b9ff, outlined #80b9ff [51%,49% → 56%,59%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- image `test-41305.svg` [18%,27% → 44%,73%]
- image `test-41321.svg` [18%,27% → 44%,73%]
- line #80b9ff [17%,48% → 27%,52%]
- line #80b9ff [34%,48% → 44%,52%]
- arrow #80b9ff [22%,43% → 39%,48%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [63%,66% → 65%,72%]
- line #ffffff [52%,57% → 55%,61%]
- line #ffffff [59%,57% → 62%,61%]
- line #ffffff [67%,57% → 69%,61%]
- line #ffffff [74%,57% → 77%,61%]
- equation $1$ (36pt, #ffffff) [53%,64% → 54%,66%]
- equation $2$ (36pt, #ffffff) [60%,64% → 61%,66%]
- equation $3$ (36pt, #ffffff) [68%,64% → 68%,66%]
- equation $4$ (36pt, #ffffff) [75%,64% → 76%,66%]
- shape filled #80b9ff, outlined #80b9ff [58%,52% → 63%,59%]
- shape filled #80b9ff, outlined #80b9ff [65%,55% → 71%,59%]
- shape filled #80b9ff, outlined #80b9ff [73%,58% → 78%,59%]
- line #ffffff [50%,57% → 79%,61%]
- equation $0.4$ (28pt, #80b9ff) [53%,46% → 54%,48%]
- equation $0.33$ (28pt, #80b9ff) [60%,49% → 62%,51%]
- equation $0.24$ (28pt, #80b9ff) [67%,52% → 69%,53%]
- equation $0.03$ (28pt, #80b9ff) [74%,56% → 77%,58%]
- text 36pt [49%,18% → 53%,22%]: Suppose we want a prediction set with 95% coverage ($c=0.95$).
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 62
- shape filled #80b9ff, outlined #80b9ff [51%,49% → 56%,59%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- image `test-41305.svg` [18%,27% → 44%,73%]
- image `test-41321.svg` [18%,27% → 44%,73%]
- line #80b9ff [17%,48% → 27%,52%]
- line #80b9ff [34%,48% → 44%,52%]
- arrow #80b9ff [22%,43% → 39%,48%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [63%,66% → 65%,72%]
- line #ffffff [52%,57% → 55%,61%]
- line #ffffff [59%,57% → 62%,61%]
- line #ffffff [67%,57% → 69%,61%]
- line #ffffff [74%,57% → 77%,61%]
- equation $1$ (36pt, #ffffff) [53%,64% → 54%,66%]
- equation $2$ (36pt, #ffffff) [60%,64% → 61%,66%]
- equation $3$ (36pt, #ffffff) [68%,64% → 68%,66%]
- equation $4$ (36pt, #ffffff) [75%,64% → 76%,66%]
- shape filled #80b9ff, outlined #80b9ff [58%,52% → 63%,59%]
- shape filled #80b9ff, outlined #80b9ff [65%,55% → 71%,59%]
- shape filled #80b9ff, outlined #80b9ff [73%,58% → 78%,59%]
- line #ffffff [50%,57% → 79%,61%]
- equation $0.4$ (28pt, #80b9ff) [53%,46% → 54%,48%]
- equation $0.33$ (28pt, #80b9ff) [60%,49% → 62%,51%]
- equation $0.24$ (28pt, #80b9ff) [67%,52% → 69%,53%]
- equation $0.03$ (28pt, #80b9ff) [74%,56% → 77%,58%]
- line #80b9ff [45%,48% → 56%,52%]
- line #80b9ff [67%,48% → 77%,52%]
- arrow #80b9ff [50%,40% → 72%,45%]
- **Builds:** click 1: line #80b9ff — draws in; with previous: line #80b9ff — draws in; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 63
- image `test-41464.svg` [28%,58% → 49%,96%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- image `test-41305.svg` [28%,13% → 49%,51%]
- image `test-41321.svg` [28%,13% → 49%,51%]
- line #80b9ff [27%,30% → 36%,34%]
- line #80b9ff [41%,30% → 50%,34%]
- arrow #80b9ff [31%,26% → 45%,31%]
- shape filled #80b9ff, outlined #80b9ff [57%,32% → 61%,40%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [67%,46% → 69%,51%]
- line #ffffff [58%,38% → 60%,42%]
- line #ffffff [64%,38% → 66%,42%]
- line #ffffff [70%,38% → 73%,42%]
- line #ffffff [77%,38% → 79%,42%]
- equation $1$ (30pt, #ffffff) [59%,44% → 59%,46%]
- equation $2$ (30pt, #ffffff) [65%,44% → 66%,46%]
- equation $3$ (30pt, #ffffff) [71%,44% → 72%,46%]
- equation $4$ (30pt, #ffffff) [77%,44% → 78%,46%]
- shape filled #80b9ff, outlined #80b9ff [63%,34% → 68%,40%]
- shape filled #80b9ff, outlined #80b9ff [69%,36% → 74%,40%]
- shape filled #80b9ff, outlined #80b9ff [75%,40% → 80%,40%]
- line #ffffff [56%,38% → 80%,42%]
- equation $0.4$ (24pt, #80b9ff) [58%,29% → 60%,31%]
- equation $0.33$ (24pt, #80b9ff) [64%,32% → 66%,33%]
- equation $0.24$ (24pt, #80b9ff) [70%,34% → 73%,35%]
- equation $0.03$ (24pt, #80b9ff) [77%,38% → 79%,39%]
- line #80b9ff [52%,30% → 61%,35%]
- line #80b9ff [70%,30% → 79%,35%]
- arrow #80b9ff [57%,24% → 75%,28%]
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- line #80b9ff [28%,68% → 44%,72%]
- line #80b9ff [32%,68% → 49%,72%]
- arrow #80b9ff [36%,55% → 41%,60%]
- shape filled #80b9ff, outlined #80b9ff [57%,61% → 61%,84%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [67%,90% → 69%,95%]
- line #ffffff [58%,82% → 60%,86%]
- line #ffffff [64%,82% → 66%,86%]
- line #ffffff [70%,82% → 73%,86%]
- line #ffffff [77%,82% → 79%,86%]
- equation $1$ (30pt, #ffffff) [59%,88% → 59%,90%]
- equation $2$ (30pt, #ffffff) [65%,88% → 66%,90%]
- equation $3$ (30pt, #ffffff) [71%,88% → 72%,90%]
- equation $4$ (30pt, #ffffff) [77%,88% → 78%,90%]
- shape filled #80b9ff, outlined #80b9ff [63%,84% → 68%,84%]
- shape filled #80b9ff, outlined #80b9ff [69%,84% → 74%,84%]
- shape filled #80b9ff, outlined #80b9ff [75%,84% → 80%,84%]
- line #ffffff [56%,82% → 80%,86%]
- equation $0.95$ (24pt, #80b9ff) [58%,58% → 60%,60%]
- equation $0.03$ (24pt, #80b9ff) [64%,82% → 66%,83%]
- equation $0.02$ (24pt, #80b9ff) [70%,82% → 73%,83%]
- equation $0.0$ (24pt, #80b9ff) [77%,82% → 78%,84%]
- line #80b9ff [49%,68% → 64%,72%]
- line #80b9ff [54%,68% → 70%,72%]
- arrow #80b9ff [57%,55% → 62%,59%]
- text 36pt [11%,67% → 20%,75%]: {Low|#fab0ae} / Uncertainty
- text 36pt [11%,33% → 20%,41%]: {High|#80cfb9} / Uncertainty
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 64
- image `test-41464.svg` [28%,58% → 49%,96%]
- text 36pt [29%,5% → 71%,9%]: We can also quantify uncertainty using prediction sets.
- image `test-41305.svg` [28%,13% → 49%,51%]
- image `test-41321.svg` [28%,13% → 49%,51%]
- line #80b9ff [27%,30% → 36%,34%]
- line #80b9ff [41%,30% → 50%,34%]
- arrow #80b9ff [31%,26% → 45%,31%]
- shape filled #80b9ff, outlined #80b9ff [57%,32% → 61%,40%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [67%,46% → 69%,51%]
- line #ffffff [58%,38% → 60%,42%]
- line #ffffff [64%,38% → 66%,42%]
- line #ffffff [70%,38% → 73%,42%]
- line #ffffff [77%,38% → 79%,42%]
- equation $1$ (30pt, #ffffff) [59%,44% → 59%,46%]
- equation $2$ (30pt, #ffffff) [65%,44% → 66%,46%]
- equation $3$ (30pt, #ffffff) [71%,44% → 72%,46%]
- equation $4$ (30pt, #ffffff) [77%,44% → 78%,46%]
- shape filled #80b9ff, outlined #80b9ff [63%,34% → 68%,40%]
- shape filled #80b9ff, outlined #80b9ff [69%,36% → 74%,40%]
- shape filled #80b9ff, outlined #80b9ff [75%,40% → 80%,40%]
- line #ffffff [56%,38% → 80%,42%]
- equation $0.4$ (24pt, #80b9ff) [58%,29% → 60%,31%]
- equation $0.33$ (24pt, #80b9ff) [64%,32% → 66%,33%]
- equation $0.24$ (24pt, #80b9ff) [70%,34% → 73%,35%]
- equation $0.03$ (24pt, #80b9ff) [77%,38% → 79%,39%]
- line #80b9ff [52%,30% → 61%,35%]
- line #80b9ff [70%,30% → 79%,35%]
- arrow #80b9ff [57%,24% → 75%,28%]
- text 36pt [16%,10% → 84%,15%]: The [[coverage|#80b9ff]] of a prediction set is the probability that the true output lies within the set.
- line #80b9ff [28%,68% → 44%,72%]
- line #80b9ff [32%,68% → 49%,72%]
- arrow #80b9ff [36%,55% → 41%,60%]
- shape filled #80b9ff, outlined #80b9ff [57%,61% → 61%,84%]
- image `test-41321.svg` (cropped: show only 46–54% across and 87–100% down of the image) [67%,90% → 69%,95%]
- line #ffffff [58%,82% → 60%,86%]
- line #ffffff [64%,82% → 66%,86%]
- line #ffffff [70%,82% → 73%,86%]
- line #ffffff [77%,82% → 79%,86%]
- equation $1$ (30pt, #ffffff) [59%,88% → 59%,90%]
- equation $2$ (30pt, #ffffff) [65%,88% → 66%,90%]
- equation $3$ (30pt, #ffffff) [71%,88% → 72%,90%]
- equation $4$ (30pt, #ffffff) [77%,88% → 78%,90%]
- shape filled #80b9ff, outlined #80b9ff [63%,84% → 68%,84%]
- shape filled #80b9ff, outlined #80b9ff [69%,84% → 74%,84%]
- shape filled #80b9ff, outlined #80b9ff [75%,84% → 80%,84%]
- line #ffffff [56%,82% → 80%,86%]
- equation $0.95$ (24pt, #80b9ff) [58%,58% → 60%,60%]
- equation $0.03$ (24pt, #80b9ff) [64%,82% → 66%,83%]
- equation $0.02$ (24pt, #80b9ff) [70%,82% → 73%,83%]
- equation $0.0$ (24pt, #80b9ff) [77%,82% → 78%,84%]
- line #80b9ff [49%,68% → 64%,72%]
- line #80b9ff [54%,68% → 70%,72%]
- arrow #80b9ff [57%,55% → 62%,59%]
- text 36pt [11%,67% → 20%,75%]: {Low|#fab0ae} / Uncertainty
- text 36pt [11%,33% → 20%,41%]: {High|#80cfb9} / Uncertainty
- rounded box (filled #424242) [30%,40% → 70%,50%]
- heading (spaced caps) 75pt [30%,38% → 36%,52%]: 🤔
- text 36pt [35%,42% → 69%,48%]: What might be an issue with this approach?
- text 36pt [48%,52% → 52%,56%]: It only outputs accurate prediction sets if the output distribution is calibrated!
- text 36pt [48%,59% → 52%,64%]: One option is to calibrate the distribution first using the methods I was talking about before.
- text 36pt [24%,68% → 76%,72%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- image `noun-bee-7592146-ffd65b.png` [17%,64% → 24%,76%]
- **Builds:** click 1: text 36pt — comet; click 2: text 36pt — slides in; click 3: text 36pt — slides in; with previous: image `noun-bee-7592146-ffd65b.png` — pivot-build
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 65
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- text 36pt [17%,26% → 83%,30%]: {If it is after 5:30pm right now, skip to model uncertainty and refer students to this paper:|#fab0ae}
- image `screenshot-2025-03-02-at-3-01-50-pm.png` [27%,34% → 73%,101%]
- **Builds:** click 1: text 36pt — appears; then: text 36pt — action-blink:Action; click 2: image `screenshot-2025-03-02-at-3-01-50-pm.png` — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 66
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- shape filled #80b9ff, outlined #80b9ff [32%,54% → 39%,64%]
- line #ffffff [34%,62% → 38%,67%]
- line #ffffff [44%,62% → 48%,67%]
- line #ffffff [54%,62% → 57%,67%]
- line #ffffff [64%,62% → 67%,67%]
- shape filled #80b9ff, outlined #80b9ff [42%,44% → 49%,64%]
- shape filled #80b9ff, outlined #80b9ff [52%,49% → 59%,64%]
- shape filled #80b9ff, outlined #80b9ff [62%,60% → 69%,64%]
- equation $0.4$ (38pt, #80b9ff) [45%,39% → 47%,42%]
- equation $0.3$ (38pt, #80b9ff) [55%,45% → 57%,48%]
- equation $0.2$ (38pt, #80b9ff) [34%,50% → 37%,52%]
- equation $0.1$ (38pt, #80b9ff) [64%,56% → 67%,58%]
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- line #ffffff [31%,62% → 70%,67%]
- heading (spaced caps) 36pt [34%,69% → 38%,74%]: UP
- heading (spaced caps) 36pt [44%,69% → 47%,74%]: DOWN
- heading (spaced caps) 36pt [54%,69% → 57%,74%]: LEFT
- heading (spaced caps) 36pt [64%,69% → 67%,74%]: RIGHT
- text 36pt [49%,75% → 52%,80%]: Action
- text 36pt [13%,83% → 88%,88%]: Which actions would we include if we wanted 70% coverage using these uncalibrated probabilities?
- heading (spaced caps) 36pt [46%,89% → 55%,94%]: {DOWN, LEFT}
- **Builds:** click 1: outlined circle #ffffff — fades up from dark; with previous: equation $1$ — fades up from dark; with previous: text 36pt — fades up from dark; click 2: text 36pt — slides in; with previous: equation $0.4$ — fades up from dark; with previous: shape filled #80b9ff, outlined #80b9ff — fades up from dark; with previous: equation $0.3$ — fades up from dark; with previous: shape filled #80b9ff, outlined #80b9ff — fades up from dark; with previous: equation $0.2$ — fades up from dark; with previous: shape filled #80b9ff, outlined #80b9ff — fades up from dark; with previous: equation $0.1$ — fades up from dark; with previous: shape filled #80b9ff, outlined #80b9ff — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: line #ffffff — fades up from dark; with previous: heading (spaced caps) 36pt — fades up from dark; with previous: heading (spaced caps) 36pt — fades up from dark; with previous: heading (spaced caps) 36pt — fades up from dark; with previous: heading (spaced caps) 36pt — fades up from dark; with previous: text 36pt — fades up from dark; click 3: text 36pt — wipes in; click 4: heading (spaced caps) 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 67
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- shape filled #80b9ff, outlined #80b9ff [32%,69% → 39%,79%]
- line #ffffff [34%,77% → 38%,81%]
- line #ffffff [44%,77% → 48%,81%]
- line #ffffff [54%,77% → 57%,81%]
- line #ffffff [64%,77% → 67%,81%]
- shape filled #80b9ff, outlined #80b9ff [42%,58% → 49%,79%]
- shape filled #80b9ff, outlined #80b9ff [52%,64% → 59%,79%]
- shape filled #80b9ff, outlined #80b9ff [62%,74% → 69%,79%]
- equation $0.4$ (38pt, #80b9ff) [45%,53% → 47%,56%]
- equation $0.3$ (38pt, #80b9ff) [55%,59% → 57%,62%]
- equation $0.2$ (38pt, #80b9ff) [34%,64% → 37%,66%]
- equation $0.1$ (38pt, #80b9ff) [64%,70% → 67%,72%]
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- line #ffffff [31%,77% → 70%,81%]
- heading (spaced caps) 36pt [35%,83% → 37%,88%]: UP
- heading (spaced caps) 36pt [42%,83% → 49%,88%]: DOWN
- heading (spaced caps) 36pt [54%,83% → 58%,88%]: LEFT
- heading (spaced caps) 36pt [63%,83% → 69%,88%]: RIGHT
- text 36pt [48%,89% → 53%,94%]: Action
- outlined circle #ffffff [9%,36% → 13%,44%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 68
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- shape filled #80b9ff, outlined #80b9ff [32%,69% → 39%,79%]
- line #ffffff [34%,77% → 38%,81%]
- line #ffffff [44%,77% → 48%,81%]
- line #ffffff [54%,77% → 57%,81%]
- line #ffffff [64%,77% → 67%,81%]
- shape filled #80b9ff, outlined #80b9ff [42%,58% → 49%,79%]
- shape filled #80b9ff, outlined #80b9ff [52%,64% → 59%,79%]
- shape filled #80b9ff, outlined #80b9ff [62%,74% → 69%,79%]
- equation $0.4$ (38pt, #80b9ff) [45%,53% → 47%,56%]
- equation $0.3$ (38pt, #80b9ff) [55%,59% → 57%,62%]
- equation $0.2$ (38pt, #80b9ff) [34%,64% → 37%,66%]
- equation $0.1$ (38pt, #80b9ff) [64%,70% → 67%,72%]
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- line #ffffff [31%,77% → 70%,81%]
- heading (spaced caps) 36pt [35%,83% → 37%,88%]: UP
- heading (spaced caps) 36pt [42%,83% → 49%,88%]: DOWN
- heading (spaced caps) 36pt [54%,83% → 58%,88%]: {LEFT|#80b9ff}
- heading (spaced caps) 36pt [63%,83% → 69%,88%]: RIGHT
- text 36pt [48%,89% → 53%,94%]: Action
- outlined circle #ffffff [9%,36% → 13%,44%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 69
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- shape filled #80b9ff, outlined #80b9ff [52%,69% → 59%,79%]
- line #ffffff [34%,77% → 38%,81%]
- line #ffffff [44%,77% → 48%,81%]
- line #ffffff [54%,77% → 57%,81%]
- line #ffffff [64%,77% → 67%,81%]
- shape filled #80b9ff, outlined #80b9ff [32%,59% → 39%,79%]
- shape filled #80b9ff, outlined #80b9ff [42%,63% → 49%,78%]
- shape filled #80b9ff, outlined #80b9ff [62%,74% → 69%,79%]
- equation $0.4$ (38pt, #80b9ff) [35%,54% → 37%,56%]
- equation $0.3$ (38pt, #80b9ff) [45%,59% → 47%,61%]
- equation $0.2$ (38pt, #80b9ff) [54%,64% → 56%,67%]
- equation $0.1$ (38pt, #80b9ff) [64%,70% → 67%,72%]
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- line #ffffff [31%,77% → 70%,81%]
- heading (spaced caps) 36pt [54%,83% → 57%,88%]: UP
- heading (spaced caps) 36pt [33%,83% → 39%,88%]: DOWN
- heading (spaced caps) 36pt [44%,83% → 48%,88%]: {LEFT|#80b9ff}
- heading (spaced caps) 36pt [63%,83% → 69%,88%]: RIGHT
- text 36pt [48%,89% → 53%,94%]: Action
- outlined circle #ffffff [9%,36% → 13%,44%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 70
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- shape filled #80b9ff, outlined #80b9ff [52%,69% → 59%,79%]
- line #ffffff [34%,77% → 38%,81%]
- line #ffffff [44%,77% → 48%,81%]
- line #ffffff [54%,77% → 57%,81%]
- line #ffffff [64%,77% → 67%,81%]
- shape filled #80b9ff, outlined #80b9ff [32%,59% → 39%,79%]
- shape filled #80b9ff, outlined #80b9ff [42%,63% → 49%,78%]
- shape filled #80b9ff, outlined #80b9ff [62%,74% → 69%,79%]
- equation $0.4$ (38pt, #80b9ff) [35%,54% → 37%,56%]
- equation $0.3$ (38pt, #80b9ff) [45%,59% → 47%,61%]
- equation $0.2$ (38pt, #80b9ff) [54%,64% → 56%,67%]
- equation $0.1$ (38pt, #80b9ff) [64%,70% → 67%,72%]
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- line #ffffff [31%,77% → 70%,81%]
- text 36pt [48%,89% → 53%,94%]: Action
- outlined circle #ffffff [9%,36% → 13%,44%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- equation $S = 0.7$ (36pt, #80b9ff) [65%,39% → 71%,41%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- heading (spaced caps) 36pt [54%,83% → 57%,88%]: UP
- heading (spaced caps) 36pt [33%,83% → 39%,88%]: DOWN
- heading (spaced caps) 36pt [44%,83% → 48%,88%]: {LEFT|#80b9ff}
- heading (spaced caps) 36pt [63%,83% → 69%,88%]: RIGHT
- **Builds:** click 1: equation $S = 0.7$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 71
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- outlined circle #ffffff [9%,36% → 13%,44%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- equation $S = 0.7$ (36pt, #80b9ff) [65%,39% → 71%,41%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- outlined circle #ffffff [9%,49% → 14%,57%]
- text 36pt [15%,51% → 64%,55%]: Calculate the $$\lceil (n+1)c \rceil / n$$ quantile of the scores of the calibration set.
- equation $3$ (36pt, #ffffff) [11%,52% → 12%,54%]
- equation $\hat q = 0.95$ (36pt, #80b9ff) [71%,51% → 78%,54%]
- **Builds:** click 1: equation $\hat q = 0.95$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 72
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- outlined circle #ffffff [9%,36% → 13%,44%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- equation $S = 0.7$ (36pt, #80b9ff) [65%,39% → 71%,41%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- outlined circle #ffffff [9%,49% → 14%,57%]
- text 36pt [15%,51% → 64%,55%]: Calculate the $$\lceil (n+1)c \rceil / n$$ quantile of the scores of the calibration set.
- equation $3$ (36pt, #ffffff) [11%,52% → 12%,54%]
- equation $\hat q = 0.95$ (36pt, #80b9ff) [71%,51% → 78%,54%]
- outlined circle #ffffff [9%,62% → 14%,70%]
- text 36pt [15%,61% → 51%,70%]: Create prediction sets by including all labels such that $S < \hat q$.
- equation $4$ (36pt, #ffffff) [11%,65% → 12%,67%]
- shape filled #80b9ff, outlined #80b9ff [74%,73% → 81%,83%]
- line #ffffff [56%,81% → 59%,85%]
- line #ffffff [66%,81% → 69%,85%]
- line #ffffff [75%,81% → 79%,85%]
- line #ffffff [85%,81% → 89%,85%]
- shape filled #80b9ff, outlined #80b9ff [54%,63% → 61%,83%]
- shape filled #80b9ff, outlined #80b9ff [64%,68% → 71%,83%]
- shape filled #80b9ff, outlined #80b9ff [84%,79% → 91%,83%]
- equation $0.4$ (38pt, #80b9ff) [56%,58% → 58%,60%]
- equation $0.3$ (38pt, #80b9ff) [66%,63% → 68%,66%]
- equation $0.2$ (38pt, #80b9ff) [75%,68% → 78%,71%]
- equation $0.1$ (38pt, #80b9ff) [86%,74% → 88%,77%]
- line #ffffff [53%,81% → 91%,85%]
- text 36pt [69%,94% → 75%,98%]: Action
- heading (spaced caps) 36pt [76%,88% → 79%,92%]: UP
- heading (spaced caps) 36pt [54%,88% → 61%,92%]: DOWN
- heading (spaced caps) 36pt [65%,88% → 69%,92%]: LEFT
- heading (spaced caps) 36pt [84%,88% → 90%,92%]: RIGHT
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 73
- text 36pt [25%,8% → 76%,12%]: Or we can use a favorite buzzword these days: [[conformal prediction|#80b9ff]]!
- text 36pt [8%,14% → 92%,19%]: Conformal prediction allows us to generate accurate prediction sets from an [[uncalibrated uncertainty measure|#80b9ff]].
- outlined circle #ffffff [9%,23% → 13%,31%]
- equation $1$ (36pt, #ffffff) [11%,26% → 11%,28%]
- text 36pt [15%,25% → 57%,29%]: Determine a heuristic (uncalibrated notion of uncertainty).
- text 36pt [61%,25% → 73%,29%]: {softmax scores|#80b9ff}
- outlined circle #ffffff [9%,36% → 13%,44%]
- text 36pt [15%,38% → 60%,42%]: Define a score function and compute it on your calibration set.
- equation $S = 0.7$ (36pt, #80b9ff) [65%,39% → 71%,41%]
- equation $2$ (36pt, #ffffff) [11%,39% → 12%,41%]
- outlined circle #ffffff [9%,49% → 14%,57%]
- text 36pt [15%,51% → 64%,55%]: Calculate the $$\lceil (n+1)c \rceil / n$$ quantile of the scores of the calibration set.
- equation $3$ (36pt, #ffffff) [11%,52% → 12%,54%]
- equation $\hat q = 0.95$ (36pt, #80b9ff) [71%,51% → 78%,54%]
- outlined circle #ffffff [9%,62% → 14%,70%]
- text 36pt [15%,61% → 51%,70%]: Create prediction sets by including all labels such that $S < \hat q$.
- equation $4$ (36pt, #ffffff) [11%,65% → 12%,67%]
- shape filled #80b9ff, outlined #80b9ff [74%,73% → 81%,83%]
- line #ffffff [56%,81% → 59%,85%]
- line #ffffff [66%,81% → 69%,85%]
- line #ffffff [75%,81% → 79%,85%]
- line #ffffff [85%,81% → 89%,85%]
- shape filled #80b9ff, outlined #80b9ff [54%,63% → 61%,83%]
- shape filled #80b9ff, outlined #80b9ff [64%,68% → 71%,83%]
- shape filled #80b9ff, outlined #80b9ff [84%,79% → 91%,83%]
- equation $0.4$ (38pt, #80b9ff) [56%,58% → 58%,60%]
- equation $0.3$ (38pt, #80b9ff) [66%,63% → 68%,66%]
- equation $0.2$ (38pt, #80b9ff) [75%,68% → 78%,71%]
- equation $0.1$ (38pt, #80b9ff) [86%,74% → 88%,77%]
- line #ffffff [53%,81% → 91%,85%]
- text 36pt [69%,94% → 75%,98%]: Action
- heading (spaced caps) 36pt [76%,88% → 79%,92%]: UP
- heading (spaced caps) 36pt [54%,88% → 61%,92%]: DOWN
- heading (spaced caps) 36pt [65%,88% → 69%,92%]: LEFT
- heading (spaced caps) 36pt [84%,88% → 90%,92%]: RIGHT
- heading (spaced caps) 36pt [29%,73% → 33%,78%]: {{DOWN, LEFT, UP}|#80b9ff}
- group [3%,83% → 46%,93%]
  - rounded box (filled #424242) [3%,83% → 46%,93%]
  - text 36pt [5%,86% → 45%,90%]: We can do something similar for regression models.
- **Builds:** click 1: heading (spaced caps) 36pt — slides in; click 2: group — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 74
- text 36pt [37%,48% → 63%,52%]: That was output uncertainty.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 75
- text 36pt [39%,45% → 61%,50%]: That was output uncertainty.
- text 36pt [39%,50% → 61%,55%]: Why not quantify model uncertainty in the same way?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 76
- text 36pt [39%,7% → 61%,11%]: That was output uncertainty.
- text 36pt [29%,12% → 71%,16%]: Why not quantify model uncertainty in the same way?
- image `test-41927.svg` [10%,20% → 90%,80%]
- image `test-41933.svg` [10%,20% → 90%,80%]
- text 36pt [48%,85% → 52%,89%]: {There is no way to calibrate output uncertainty in regions with no data!|#c3b8ff}
- **Builds:** click 1: text 36pt — wipes in; click 2: image `test-41933.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 77
- text 36pt [38%,48% → 62%,52%]: Alright, here we go again…
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 78
- text 36pt [39%,45% → 61%,50%]: Alright, here we go again…
- text 36pt [18%,50% → 82%,55%]: Why pick just one model when we could maintain a [[distribution|#80b9ff]] over all possible models?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 79
- text 36pt [39%,42% → 61%,47%]: Alright, here we go again…
- text 36pt [16%,47% → 84%,51%]: Why pick just one model when we could maintain a [[distribution|#80b9ff]] over all possible models?
- text 36pt [16%,52% → 84%,56%]: Let’s take a [[Bayesian|#80b9ff]] approach.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 80
- text 36pt [16%,6% → 84%,10%]: Why pick just one model when we could maintain a [[distribution|#80b9ff]] over all possible models?
- text 36pt [38%,11% → 62%,15%]: Let’s take a [[Bayesian|#80b9ff]] approach.
- image `test-40738.svg` [10%,29% → 90%,90%]
- text 36pt [48%,20% → 52%,24%]: There are many models that fit this data.
- image `test-42016.svg` [10%,29% → 90%,90%]
- **Builds:** click 1: text 36pt — wipes in; with previous: image `test-42016.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 81
- text 36pt [16%,6% → 84%,10%]: Why pick just one model when we could maintain a [[distribution|#80b9ff]] over all possible models?
- text 36pt [38%,11% → 62%,15%]: Let’s take a [[Bayesian|#80b9ff]] approach.
- image `test-42016.svg` [13%,50% → 43%,72%]
- text 36pt [18%,33% → 37%,38%]: distribution over models
- equation $p(\theta \mid D)$ (36pt, #ffffff) [25%,43% → 31%,46%]
- rounded box (outline) [11%,32% → 45%,75%]
- line #ffffff [11%,37% → 44%,41%]
- text 36pt [68%,27% → 71%,32%]: To make a prediction over a new point:
- equation $p(y \mid x, D) = \int p(y \mid x, \theta)p(\theta \mid D) d\theta$ (43pt, #ffffff) [54%,35% → 85%,44%]
- text 36pt [80%,52% → 97%,60%]: {probability of a specific model|#80b9ff}
- arrow #80b9ff [81%,45% → 88%,49%]
- text 36pt [64%,53% → 78%,65%]: {probability of the output given a specific model|#80b9ff}
- arrow #80b9ff [68%,46% → 74%,50%]
- text 36pt [48%,52% → 62%,65%]: {probability of the output given all possible models|#80b9ff}
- arrow #80b9ff [53%,46% → 60%,50%]
- **Builds:** click 1: text 36pt — slides in; click 2: equation $p(y \mid x, D) = \int p(y \mid x, \theta)p(\theta \mid D) d\theta$ — slides in; click 3: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 4: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in; click 5: text 36pt — fades up from dark; with previous: arrow #80b9ff — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 82
- text 36pt [16%,6% → 84%,10%]: Why pick just one model when we could maintain a [[distribution|#80b9ff]] over all possible models?
- text 36pt [38%,11% → 62%,15%]: Let’s take a [[Bayesian|#80b9ff]] approach.
- image `test-42016.svg` [13%,50% → 43%,72%]
- text 36pt [18%,33% → 37%,38%]: distribution over models
- equation $p(\theta \mid D)$ (36pt, #ffffff) [25%,43% → 31%,46%]
- rounded box (outline) [11%,32% → 45%,75%]
- line #ffffff [11%,37% → 44%,41%]
- text 36pt [68%,27% → 71%,32%]: To make a prediction over a new point:
- equation $p(y \mid x, D) = \int p(y \mid x, \theta)p(\theta \mid D) d\theta$ (43pt, #ffffff) [54%,44% → 85%,53%]
- text 36pt [60%,37% → 80%,41%]: Bayesian Model Averaging
- outlined shape #ffffff [52%,34% → 87%,56%]
- text 36pt [68%,58% → 71%,63%]: {…but performing this computation is generally intractable.|#f3cf80}
- text 36pt [68%,65% → 71%,70%]: We could draw samples from $p(\theta \mid D)$ using MCMC.
- text 36pt [48%,72% → 93%,77%]: {…but this is also often intractable.|#f3cf80}
- **Builds:** click 1: text 36pt — slides in; click 2: text 36pt — fades up from dark; click 3: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 83
- equation $p(y \mid x, D) = \int p(y \mid x, \theta)p(\theta \mid D) d\theta$ (43pt, #ffffff) [9%,49% → 40%,58%]
- text 36pt [15%,42% → 35%,46%]: Bayesian Model Averaging
- outlined shape #ffffff [7%,39% → 42%,61%]
- shape (outline) [45%,46% → 50%,54%]
- text 36pt [54%,36% → 93%,53%]: We can approximate Bayesian model averaging by creating an ensemble of models $\mathcal M$ that all have high likelihood according to $p(\theta \mid D)$ and approximate the integral as:
- equation $p(y \mid x, D) \approx \frac{1}{|\mathcal M|}\sum_{\theta \in \mathcal M} p(y \mid x, \theta)$ (36pt, #ffffff) [61%,55% → 86%,64%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 84
- equation $p(y \mid x, D) = \int p(y \mid x, \theta)p(\theta \mid D) d\theta$ (43pt, #ffffff) [9%,17% → 40%,26%]
- text 36pt [15%,10% → 35%,14%]: Bayesian Model Averaging
- outlined shape #ffffff [7%,7% → 42%,29%]
- shape (outline) [45%,14% → 50%,22%]
- text 36pt [54%,4% → 93%,21%]: We can approximate Bayesian model averaging by create and ensemble of models $\mathcal M$ that all have high likelihood according to $p(\theta \mid D)$ and approximate the integral as:
- equation $p(y \mid x, D) \approx \frac{1}{|\mathcal M|}\sum_{\theta \in \mathcal M} p(y \mid x, \theta)$ (36pt, #ffffff) [61%,23% → 86%,31%]
- line #ffffff [2%,34% → 98%,38%]
- text 36pt [12%,40% → 88%,44%]: One way to create the models $\mathcal M$ is train the same model multiple times with [[different initializations|#80b9ff]].
- image `test-42016.svg` [39%,52% → 88%,89%]
- image `test-42249.svg` [13%,52% → 35%,90%]
- **Builds:** then: image `test-42016.svg` — fades in; with previous: image `test-42249.svg` — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 85
- text 36pt [12%,5% → 88%,9%]: One way to create the models $\mathcal M$ is train the same model multiple times with [[different initializations|#80b9ff]].
- image `test-39186.svg` [32%,18% → 68%,82%]
- image `val-page-310.svg` (cropped: show only 11–62% across and 27–72% down of the image) [32%,18% → 68%,82%]
- **Builds:** click 1: image `val-page-310.svg` (cropped: show only 11–62% across and 27–72%  — fades in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 86
- text 36pt [33%,3% → 67%,8%]: {A problem to watch out for with ensembles:|#f3cf80}
- image `test-42016.svg` [39%,36% → 88%,73%]
- image `test-42249.svg` [12%,36% → 35%,75%]
- text 36pt [41%,26% → 59%,31%]: {We hope this happens:|#80cfb9}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 87
- text 36pt [33%,3% → 67%,8%]: {A problem to watch out for with ensembles:|#f3cf80}
- image `test-42016.svg` [42%,18% → 78%,45%]
- image `test-42249.svg` [22%,18% → 39%,46%]
- text 36pt [41%,10% → 59%,15%]: {We hope this happens:|#80cfb9}
- text 36pt [41%,49% → 59%,53%]: {But this could also happen:|#fab0ae}
- image `test-42338.svg` [22%,56% → 39%,85%]
- image `test-42343.svg` [42%,56% → 78%,84%]
- text 36pt [48%,89% → 52%,93%]: It is important to ensure sufficient diversity among the models in the ensemble.
- **Builds:** click 1: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 88
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: OPERATIONAL DESIGN DOMAIN MONITORING
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: UNCERTAINTY QUANTIFICATION
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,67% → 11%,73%]: {3|#000000}
- heading (spaced caps) 36pt [13%,68% → 87%,72%]: FAILURE MONITORING
- text 32pt [15%,47% → 18%,54%]: {A|#80b9ff}
- text 32pt [15%,56% → 18%,63%]: {B|#80b9ff}
- text 36pt [20%,48% → 35%,53%]: Output Uncertainty
- text 36pt [20%,57% → 35%,62%]: Model Uncertainty
- text on a #80b9ff filled box 32pt [7%,80% → 11%,87%]: {4|#000000}
- heading (spaced caps) 36pt [13%,81% → 87%,86%]: COURSE WRAP UP 🥲
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 89
- heading (spaced caps) 36pt [36%,45% → 64%,49%]: FAILURE MONITORING
- text 36pt [4%,51% → 96%,55%]: Once we have determined that we are [[operating in the ODD|#80b9ff]], we still might want to check if we are in a [[dangerous scenario|#fab0ae]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 90
- heading (spaced caps) 36pt [36%,5% → 64%,9%]: FAILURE MONITORING
- text 36pt [4%,10% → 96%,15%]: Once we have determined that we are [[operating in the ODD|#80b9ff]], we still might want to check if we are in a [[dangerous scenario|#fab0ae]].
- image `g01.svg` [8%,24% → 92%,80%]
- image `g02.svg` [8%,24% → 92%,80%]
- image `g03.svg` [8%,24% → 92%,80%]
- image `g04.svg` [8%,24% → 92%,80%]
- image `g05.svg` [8%,24% → 92%,80%]
- image `g06.svg` [8%,24% → 92%,80%]
- image `g07.svg` [8%,24% → 92%,80%]
- image `g08.svg` [8%,24% → 92%,80%]
- image `g09.svg` [8%,24% → 92%,80%]
- image `g10.svg` [8%,24% → 92%,80%]
- image `g11.svg` [8%,24% → 92%,80%]
- image `g12.svg` [8%,24% → 92%,80%]
- image `g13.svg` [8%,24% → 92%,80%]
- image `g14.svg` [8%,24% → 92%,80%]
- image `g15.svg` [8%,24% → 92%,80%]
- image `g16.svg` [8%,24% → 92%,80%]
- image `g17.svg` [8%,24% → 92%,80%]
- image `g18.svg` [8%,24% → 92%,80%]
- image `g19.svg` [8%,24% → 92%,80%]
- image `g20.svg` [8%,24% → 92%,80%]
- image `g21.svg` [8%,24% → 92%,80%]
- image `g22.svg` [8%,24% → 92%,80%]
- image `g23.svg` [8%,24% → 92%,80%]
- image `g24.svg` [8%,24% → 92%,80%]
- image `g25.svg` [8%,24% → 92%,80%]
- image `g26.svg` [8%,24% → 92%,80%]
- image `g27.svg` [8%,24% → 92%,80%]
- image `g28.svg` [8%,24% → 92%,80%]
- image `g29.svg` [8%,24% → 92%,80%]
- image `g30.svg` [8%,24% → 92%,80%]
- image `g31.svg` [8%,24% → 92%,80%]
- image `g32.svg` [8%,24% → 92%,80%]
- image `g33.svg` [8%,24% → 92%,80%]
- image `g34.svg` [8%,24% → 92%,80%]
- image `g35.svg` [8%,24% → 92%,80%]
- image `g36.svg` [8%,24% → 92%,80%]
- image `g37.svg` [8%,24% → 92%,80%]
- image `g38.svg` [8%,24% → 92%,80%]
- image `g39.svg` [8%,24% → 92%,80%]
- image `g40.svg` [8%,24% → 92%,80%]
- image `g41.svg` [8%,24% → 92%,80%]
- **Builds:** click 1: image `g02.svg` — appears; then (0.1 s later): image `g03.svg` — appears; then (0.1 s later): image `g04.svg` — appears; then (0.1 s later): image `g05.svg` — appears; then (0.1 s later): image `g06.svg` — appears; then (0.1 s later): image `g07.svg` — appears; then (0.1 s later): image `g08.svg` — appears; then (0.1 s later): image `g09.svg` — appears; then (0.1 s later): image `g10.svg` — appears; then (0.1 s later): image `g11.svg` — appears; then (0.1 s later): image `g12.svg` — appears; then (0.1 s later): image `g13.svg` — appears; then (0.1 s later): image `g14.svg` — appears; then (0.1 s later): image `g15.svg` — appears; then (0.1 s later): image `g16.svg` — appears; then (0.1 s later): image `g17.svg` — appears; then (0.1 s later): image `g18.svg` — appears; then (0.1 s later): image `g19.svg` — appears; then (0.1 s later): image `g20.svg` — appears; then (0.1 s later): image `g21.svg` — appears; then (0.1 s later): image `g22.svg` — appears; then (0.1 s later): image `g23.svg` — appears; then (0.1 s later): image `g24.svg` — appears; then (0.1 s later): image `g25.svg` — appears; then (0.1 s later): image `g26.svg` — appears; then (0.1 s later): image `g27.svg` — appears; then (0.1 s later): image `g28.svg` — appears; then (0.1 s later): image `g29.svg` — appears; then (0.1 s later): image `g30.svg` — appears; then (0.1 s later): image `g31.svg` — appears; then (0.1 s later): image `g32.svg` — appears; then (0.1 s later): image `g33.svg` — appears; then (0.1 s later): image `g34.svg` — appears; then (0.1 s later): image `g35.svg` — appears; then (0.1 s later): image `g36.svg` — appears; then (0.1 s later): image `g37.svg` — appears; then (0.1 s later): image `g38.svg` — appears; then (0.1 s later): image `g39.svg` — appears; then (0.1 s later): image `g40.svg` — appears; then (0.1 s later): image `g41.svg` — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 91
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,15% → 40%,19%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: OPERATIONAL DESIGN DOMAIN MONITORING
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: UNCERTAINTY QUANTIFICATION
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,67% → 11%,73%]: {3|#000000}
- heading (spaced caps) 36pt [13%,68% → 87%,72%]: FAILURE MONITORING
- text 32pt [15%,47% → 18%,54%]: {A|#80b9ff}
- text 32pt [15%,56% → 18%,63%]: {B|#80b9ff}
- text 36pt [20%,48% → 35%,53%]: Output Uncertainty
- text 36pt [20%,57% → 35%,62%]: Model Uncertainty
- text on a #80b9ff filled box 32pt [7%,80% → 11%,87%]: {4|#000000}
- heading (spaced caps) 36pt [13%,81% → 87%,86%]: COURSE WRAP UP 🥲
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 92
- heading (spaced caps) 36pt [37%,3% → 63%,8%]: COURSE WRAP UP 🥲
- image `pasted-image-42540.png` [55%,13% → 87%,70%]
- text on a #fffbb9 filled box 44pt [79%,54% → 85%,60%]: { * * *|#000000}
- image `pasted-image-42543.png` [61%,75% → 70%,92%]
- image `pasted-image-42546.png` [73%,75% → 82%,92%]
- heading (spaced caps) 24pt [60%,93% → 71%,97%]: AA222/CS361
- heading (spaced caps) 24pt [74%,93% → 82%,97%]: AA228/CS238
- image `cover-validation.png` (book cover) [38%,29% → 52%,55%]
- heading (spaced caps) 28pt [38%,57% → 52%,61%]: AA228V/CS238V
- text 36pt [8%,38% → 31%,46%]: I hope you feel that you have sufficiently found out!
- **Builds:** click 1: image `pasted-image-42540.png` — fades up from dark; with previous: image `cover-validation.png` (book cover) — fades up from dark; with previous: text on a #fffbb9 filled box 44pt — fades up from dark; with previous: heading (spaced caps) 28pt — fades up from dark; with previous: image `pasted-image-42543.png` — fades up from dark; with previous: image `pasted-image-42546.png` — fades up from dark; with previous: heading (spaced caps) 24pt — fades up from dark; with previous: heading (spaced caps) 24pt — fades up from dark; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 93
- group [16%,12% → 32%,19%]
  - text 30pt [21%,14% → 32%,18%]: Failure Analysis
  - image `noun-x-2290001-56b4e9.png` [16%,12% → 21%,19%]
- group [34%,11% → 53%,20%]
  - text 30pt [39%,14% → 53%,18%]: Formal Guarantees
  - image `noun-guarantee-5063107-56b4e9.png` [34%,11% → 39%,20%]
- group [55%,11% → 69%,20%]
  - image `noun-explain-7025341-56b4e9.png` [55%,11% → 59%,20%]
  - text 30pt [60%,14% → 69%,18%]: Explanations
- group [70%,11% → 91%,20%]
  - text 30pt [76%,14% → 91%,18%]: Runtime Assurances
  - image `noun-time-7139295-56b4e9.png` [70%,11% → 76%,20%]
- image `figures.svg` (cropped: show only 0–100% across and 18–100% down of the image) [2%,22% → 92%,94%]
- text on a #80b9ff filled box 32pt [21%,34% → 79%,66%]: {There is no silver bullet in safety validation.|#000000} / We must build a safety case. / This course is a good place to start!
- heading (spaced caps) 36pt [37%,3% → 63%,8%]: COURSE WRAP UP 🥲
- **Builds:** click 1: text on a #80b9ff filled box 32pt — fades up from dark; with previous: image `figures.svg` (cropped: show only 0–100% across and 18–100% down — dims; with previous: group — dims; with previous: group — dims; with previous: group — dims; with previous: group — dims
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 94
- heading (spaced caps) 36pt [37%,41% → 63%,46%]: COURSE WRAP UP 🥲
- text 36pt [24%,48% → 76%,52%]: Thank you all for being part of the second edition of AA228V/CS238V!
- text 36pt [48%,55% → 52%,59%]: {Stay in touch and reach out if you ever need anything!|#80b9ff}
- text 36pt [48%,60% → 52%,64%]: {smkatz@stanford.edu|#80b9ff}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 95
- video `video-40110.mp4` (plays 4.2s–9.9s, once) [9%,9% → 91%,91%]
- video `video-40110.mp4` (plays 9.9s–17.7s, once) [9%,9% → 91%,91%]
- black cover-up box (Keynote crop hack; just crop the media instead) [6%,86% → 94%,95%]
- **Builds:** then: video `video-40110.mp4` (plays 4.2s–9.9s, once) — video starts; click 1: video `video-40110.mp4` (plays 9.9s–17.7s, once) — appears

## Slide 96
- heading (spaced caps) 72pt [12%,47% → 88%,53%]: YAY!
- **Builds:** then: heading (spaced caps) 72pt — fireworks
