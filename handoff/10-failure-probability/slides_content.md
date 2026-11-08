# AA228V Lecture 10: Failure Probability Estimation: slide-by-slide content

Combined from three Keynote decks (Lectures 10, 11 and 12, "Failure Probability Estimation" parts 1–3) into one deck of 160 slides, 16:9. Each slide notes which Keynote deck and slide it came from. This is the source material for rebuilding the lecture as a native HTML deck.

## How to read this

- Positions are approximate boxes in % of the slide, `[left,top → right,bottom]`.
- `[[text|#hex]]` = accent phrase: italic, in that color. `{text|#hex}` = colored (not italic).
- `$...$` is LaTeX. Typeset it with KaTeX (or MathJax) in the same color and roughly the same size as the surrounding text. There are no equation image files.
- Images and videos named in backticks are online, not attached. Use each one by its full address `https://smkatz12.github.io/aa228v-lectures/lectures/10-failure-probability/images/<name>`, for example `<img src="https://smkatz12.github.io/aa228v-lectures/lectures/10-failure-probability/images/coverart-302-green.png">`. Don't ask for uploads.
- **Builds** list what appears on each click, in order ("then" = right after the previous step, "with previous" = at the same time, "(0.1 s later)" = after that pause).
- A long run of images named `gNN-…` that appear one after another at the same spot, a fraction of a second apart, is a frame-by-frame animation: stack them and reveal them in turn with that timing (each frame stays as the next appears).
- **Transition to next: Magic Move** means objects shared with the next slide should glide to their new positions.

## Combining the three parts

- This is one deck now: a single title slide (use "Failure Probability Estimation", without "Part 1").
- The "PLAN FOR TODAY" agenda slides came from three separate lectures, each listing only its own sections. Replace every one of them with a single combined agenda covering all three parts, highlighting the section that comes next, in this order: Direct estimation · Importance sampling · Cross entropy method (adaptive importance sampling) · Multiple importance sampling · Population Monte Carlo · Sequential Monte Carlo · Ratio of normalizing constants · Self-normalized importance sampling · Bridge sampling · Multilevel splitting. Group them visually as Part 1 (first two), Part 2 (next four) and Part 3 (last four).
- Lecture 11's importance-sampling recap and Lecture 12's opening were left out because the previous part just covered them; where text says "last lecture" or "as we saw last lecture", say "earlier" instead.

## House style

- Same as Lecture 01: black background; white text.
- Spaced all-caps headings in Gill Sans (regular weight, letter-spacing about 0.25em). All other text in Palatino.
- Emphasis is italic + color, never bold.
- The title slide streak is green (`coverart-302-green.png`).
- Graphics are SVGs with transparent backgrounds and white lines/text, made for the black slides; keep them as `<img>` files.
- Handwritten ink from past lectures (slides 28, 35, 110, 113, 118, 124, 127, 134, 151) has been left out on purpose; the deck's own ink layer handles writing.
- Most-used text colors: `#ffffff`, `#80b9ff`, `#000000`, `#fab0ae`, `#ffa4e7`, `#0072fe`, `#929292`, `#80cfb9`

## Slide 1
_(Keynote: Lecture 10, slide 1)_
- image `coverart-302-green.png` [-0%,46% → 100%,75%]
- heading (spaced caps) 50pt [6%,9% → 82%,22%]: AA228V/CS238V / VALIDATION OF SAFETY-CRITICAL SYSTEMS
- heading (spaced caps) 30pt [4%,73% → 43%,87%]: LECTURE 10: FAILURE PROBABILITY ESTIMATION (PART 1) / SYDNEY KATZ (SMKATZ@STANFORD.EDU)

## Slide 2
_(Keynote: Lecture 10, slide 2)_
- heading (spaced caps) 50pt [12%,47% → 88%,53%]: WHAT IS THE PROBABILITY OF FAILURE?

## Slide 3
_(Keynote: Lecture 10, slide 3)_
- equation $p_\text{fail}$ (92pt, #fab0ae) [27%,45% → 35%,52%]
- equation $= \mathbb E_{\tau \sim p(\cdot)}[1\{\tau \notin \psi\}]$ (92pt, #fab0ae) [37%,45% → 73%,55%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 4
_(Keynote: Lecture 10, slide 4)_
- equation $p_\text{fail}$ (92pt, #fab0ae) [27%,37% → 34%,44%]
- equation $= \int 1\{\tau \notin \psi\}p(\tau) d\tau$ (92pt, #fab0ae) [36%,50% → 74%,70%]
- equation $= \mathbb E_{\tau \sim p(\cdot)}[1\{\tau \notin \psi\}]$ (92pt, #fab0ae) [36%,37% → 73%,46%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 5
_(Keynote: Lecture 10, slide 5)_
- group [50%,41% → 92%,60%]
  - equation $p(\tau)$ (58pt, #fab0ae) [82%,51% → 87%,56%]
  - equation $p(\tau \mid \tau \notin \psi )$ (58pt, #fab0ae) [50%,44% → 64%,49%]
  - equation $p(\tau)$ (58pt, #fab0ae) [83%,41% → 88%,45%]
  - equation $=$ (58pt, #fab0ae) [65%,46% → 67%,47%]
  - line #fab0ae [69%,47% → 92%,47%]
  - equation $1\{\tau \notin \psi\}$ (58pt, #fab0ae) [72%,41% → 82%,45%]
  - equation $\int 1\{\tau \notin \psi\}$ (58pt, #fab0ae) [69%,48% → 82%,60%]
  - equation $d\tau$ (58pt, #fab0ae) [88%,51% → 91%,55%]
- line #f5615c [67%,46% → 93%,62%]
- text 36pt [26%,27% → 29%,32%]: Failure Probability
- text 36pt [73%,27% → 87%,32%]: Failure Distribution
- arrow #f5615c [42%,47% → 66%,54%]
- equation $p_\text{fail}$ (60pt, #fab0ae) [10%,45% → 15%,49%]
- equation $= \int 1\{\tau \notin \psi\}p(\tau) d\tau$ (60pt, #fab0ae) [16%,41% → 40%,53%]
- line #f5615c [18%,39% → 41%,54%]
- text 48pt [12%,76% → 88%,82%]: The [[probability of failure|#80b9ff]] is the [[normalizing constant|#80b9ff]] of the failure distribution!
- **Builds:** click 1: line #f5615c — com.apple.iWork.Keynote.LineDraw; with previous: line #f5615c — com.apple.iWork.Keynote.LineDraw; then: arrow #f5615c — draws in; click 2: text 48pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 6
_(Keynote: Lecture 10, slide 6)_
- image `test-13882.svg` [22%,-31% → 78%,80%]
- equation $p_\text{fail}$ (60pt, #fab0ae) [16%,83% → 21%,87%]
- equation $= \int 1\{\tau \notin \psi\}p(\tau) d\tau$ (60pt, #fab0ae) [22%,79% → 47%,92%]
- arrow #f5615c [34%,53% → 42%,78%]
- group [12%,18% → 88%,28%]
  - rounded box (outline) [12%,18% → 88%,28%]
  - text 36pt [17%,19% → 83%,27%]: Last lecture, we noted that this normalizing constant is [[generally intractable to compute|#80b9ff]] exactly. / In this lecture, we will discuss ways to [[estimate|#80b9ff]] it.
- text 48pt [12%,8% → 88%,14%]: The [[probability of failure|#80b9ff]] is the [[normalizing constant|#80b9ff]] of the failure distribution!
- **Builds:** click 1: group — fades up from dark

## Slide 7
_(Keynote: Lecture 10, slide 7)_
- text on a #80b9ff filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #80b9ff filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 36pt [18%,30% → 94%,35%]: DIRECT ESTIMATION
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: IMPORTANCE SAMPLING
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text 36pt [58%,43% → 93%,48%]: {This is what I would start with for Project 2!|#80b9ff}
- arrow #80b9ff [49%,46% → 58%,46%]
- **Builds:** click 1: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 2: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 3: arrow #80b9ff — draws in; with previous: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 8
_(Keynote: Lecture 10, slide 8)_
- line #ffffff [32%,32% → 36%,40%]
- equation $1$ (36pt, #ffffff) [34%,35% → 34%,37%]
- text 36pt [38%,34% → 62%,38%]: Perform a rollout of the system
- image `test-18979.svg` [13%,28% → 29%,49%]
- image `test-18986.svg` [13%,55% → 29%,76%]
- line #ffffff [32%,59% → 36%,67%]
- equation $2$ (36pt, #ffffff) [34%,62% → 34%,64%]
- text 36pt [38%,60% → 87%,65%]: Label outcome as $1$ if the trajectory is a failure and $0$ otherwise
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 9
_(Keynote: Lecture 10, slide 9)_
- rounded box (outline) [9%,13% → 91%,68%]
- line #ffffff [32%,22% → 36%,29%]
- equation $1$ (36pt, #ffffff) [34%,24% → 34%,27%]
- text 36pt [38%,23% → 62%,28%]: Perform a rollout of the system
- image `test-18979.svg` [13%,18% → 29%,39%]
- image `test-18986.svg` [13%,45% → 29%,66%]
- line #ffffff [32%,49% → 36%,56%]
- equation $2$ (36pt, #ffffff) [34%,51% → 34%,53%]
- text 36pt [38%,50% → 87%,55%]: Label outcome as $1$ if the trajectory is a failure and $0$ otherwise
- text 36pt [11%,72% → 89%,77%]: This process is [[equivalent|#80b9ff]] to producing samples from a [[Bernoulli distribution|#80b9ff]] defined by parameter $p_\text{fail}$.
- group [19%,81% → 81%,90%]
  - rounded box (outline) [19%,81% → 81%,90%]
  - text 36pt [20%,83% → 80%,88%]: We can use the [[parameter estimation techniques|#80b9ff]] from chapter 2 to estimate it!
- text 36pt [28%,91% → 72%,96%]: (maximum likelihood estimation or Bayesian estimation)
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- **Builds:** click 1: group — slides in; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 10
_(Keynote: Lecture 10, slide 10)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [38%,37% → 62%,42%]: maximum likelihood estimator
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m 1\{\tau_i \not\in \psi\} = \frac{n}{m}$ (48pt, #ffffff) [36%,48% → 64%,60%]
- text 36pt [72%,40% → 95%,45%]: {number of failure trajectories|#fab0ae}
- text 36pt [72%,62% → 94%,67%]: {total number of trajectories|#80b9ff}
- arrow #fab0ae [64%,43% → 71%,50%]
- arrow #80b9ff [65%,58% → 72%,64%]
- **Builds:** click 1: text 36pt — appears; with previous: arrow #fab0ae — draws in; click 2: text 36pt — appears; with previous: arrow #80b9ff — draws in

## Slide 11
_(Keynote: Lecture 10, slide 11)_
- text 36pt [48%,48% → 52%,52%]: {Quick Aside:|#80b9ff} How do we assess how good an estimator is?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 12
_(Keynote: Lecture 10, slide 12)_
- text 36pt [28%,36% → 72%,40%]: {Quick Aside: |#80b9ff}How do we assess how good an estimator is?
- heading (spaced caps) 36pt [37%,43% → 63%,48%]: BIAS
- heading (spaced caps) 36pt [37%,50% → 63%,55%]: CONSISTENCY
- heading (spaced caps) 36pt [37%,58% → 63%,62%]: VARIANCE
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 13
_(Keynote: Lecture 10, slide 13)_
- rounded box (outline) [67%,20% → 95%,52%]
- rounded box (outline) [36%,20% → 64%,52%]
- rounded box (outline) [5%,20% → 33%,52%]
- text 36pt [28%,7% → 72%,12%]: {Quick Aside: |#80b9ff}How do we assess how good an estimator is?
- heading (spaced caps) 36pt [6%,21% → 32%,25%]: BIAS
- heading (spaced caps) 36pt [37%,21% → 63%,25%]: CONSISTENCY
- heading (spaced caps) 36pt [68%,21% → 94%,25%]: VARIANCE
- group [8%,27% → 30%,46%]
  - text 36pt [8%,27% → 30%,39%]: An estimator is [[unbiased|#80b9ff]] if it predicts the true value in expectation:
  - equation $\mathbb E[\hat p_\text{fail}] = p_\text{fail}$ (40pt, #ffffff) [13%,43% → 25%,46%]
- group [38%,27% → 62%,47%]
  - text 36pt [38%,27% → 62%,39%]: An estimator is [[consistent|#80b9ff]] if it converges to the true value in the limit of infinite samples:
  - equation $\lim_{m \rightarrow \infty} \hat p_\text{fail} = p_\text{fail}$ (40pt, #ffffff) [43%,42% → 57%,47%]
- text 36pt [68%,30% → 93%,42%]: The [[variance|#80b9ff]] of an estimator quantifies the spread of the estimates around the true value.
- image `test-19319.svg` [25%,59% → 75%,93%]
- **Builds:** click 1: group — appears; click 2: group — appears; click 3: text 36pt — appears; click 4: image `test-19319.svg` — fades up from dark

## Slide 14
_(Keynote: Lecture 10, slide 14)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [38%,37% → 62%,42%]: maximum likelihood estimator
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m 1\{\tau_i \not\in \psi\} = \frac{n}{m}$ (48pt, #ffffff) [36%,48% → 64%,60%]
- text 36pt [72%,40% → 95%,45%]: {number of failure trajectories|#fab0ae}
- text 36pt [72%,62% → 94%,67%]: {total number of trajectories|#80b9ff}
- arrow #fab0ae [64%,43% → 71%,50%]
- arrow #80b9ff [65%,58% → 72%,64%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 15
_(Keynote: Lecture 10, slide 15)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [38%,17% → 62%,21%]: maximum likelihood estimator
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m 1\{\tau_i \not\in \psi\} = \frac{n}{m}$ (48pt, #ffffff) [36%,28% → 64%,39%]
- line #ffffff [6%,50% → 95%,50%]
- text 36pt [20%,69% → 28%,74%]: {Unbiased|#80cfb9}
- equation $\text{Var}[\hat p_\text{fail}] = \frac{p_\text{fail}(1 - p_\text{fail})}{m}$ (48pt, #ffffff) [37%,67% → 63%,77%]
- text 36pt [34%,84% → 66%,89%]: {What happens to the variance as $m \rightarrow \infty$?|#80b9ff}
- shape (outline) [68%,73% → 76%,87%]
- text 36pt [76%,69% → 84%,74%]: {Consistent|#80cfb9}
- **Builds:** click 1: text 36pt — appears; click 2: equation $\text{Var}[\hat p_\text{fail}] = \frac{p_\text{fail}(1 - p_\text{fail})}{m}$ — appears; click 3: text 36pt — slides in; click 4: shape (outline) — wipes in; then: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 16
_(Keynote: Lecture 10, slide 16)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 22pt [17%,18% → 33%,21%]: maximum likelihood estimator
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m 1\{\tau_i \not\in \psi\} = \frac{n}{m}$ (32pt, #ffffff) [16%,24% → 35%,32%]
- text 36pt [39%,17% → 47%,22%]: {Unbiased|#80cfb9}
- equation $\text{Var}[\hat p_\text{fail}] = \frac{p_\text{fail}(1 - p_\text{fail})}{m}$ (48pt, #ffffff) [54%,20% → 81%,30%]
- text 36pt [38%,25% → 47%,30%]: {Consistent|#80cfb9}
- line #ffffff [13%,16% → 37%,34%]
- image `test-19409.svg` [26%,43% → 74%,92%]
- line #ffffff [-63%,46% → -59%,54%]
- equation $1$ (36pt, #ffffff) [-62%,49% → -61%,51%]
- text 36pt [-57%,48% → -1%,52%]: As the number of samples [[increases|#80b9ff]], the variance in the estimate [[decreases|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 17
_(Keynote: Lecture 10, slide 17)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 22pt [17%,18% → 33%,21%]: maximum likelihood estimator
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m 1\{\tau_i \not\in \psi\} = \frac{n}{m}$ (32pt, #ffffff) [16%,24% → 35%,32%]
- text 36pt [39%,17% → 47%,22%]: {Unbiased|#80cfb9}
- equation $\text{Var}[\hat p_\text{fail}] = \frac{p_\text{fail}(1 - p_\text{fail})}{m}$ (48pt, #ffffff) [54%,20% → 81%,30%]
- text 36pt [38%,25% → 47%,30%]: {Consistent|#80cfb9}
- line #ffffff [13%,16% → 37%,34%]
- image `test-19409.svg` [100%,43% → 147%,92%]
- line #ffffff [18%,46% → 22%,54%]
- equation $1$ (36pt, #ffffff) [20%,49% → 20%,51%]
- text 36pt [24%,48% → 48%,52%]: As the number of samples [[increases|#80b9ff]], the variance in the estimate [[decreases|#80b9ff]].
- line #ffffff [18%,59% → 22%,67%]
- equation $2$ (36pt, #ffffff) [20%,62% → 21%,64%]
- text 36pt [24%,61% → 82%,65%]: As the probability of failure [[decreases|#80b9ff]], the variance in the estimate [[increases|#80b9ff]].
- text 36pt [30%,66% → 70%,71%]: {Again, |#c0c0c0}[[bad news|#80b9ff]]{ for systems with |#c0c0c0}[[rare|#80b9ff]]{ failure events.|#c0c0c0}
- group [33%,76% → 67%,90%]
  - rounded box (outline) [33%,76% → 67%,90%]
  - text 36pt [35%,77% → 65%,89%]: {We will discuss importance sampling techniques this lecture and next lecture that aim to address this issue!|#000000}
- **Builds:** click 1: text 36pt — slides in; with previous: line #ffffff — slides in; with previous: equation $2$ — slides in; click 2: text 36pt — slides in; click 3: group — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 18
_(Keynote: Lecture 10, slide 18)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [48%,15% → 52%,19%]: But first: one more issue with maximum likelihood estimation.
- vector icon `shape-98123330.svg` [35%,29% → 41%,33%]
- vector icon `shape-98123330.svg` [59%,34% → 65%,38%]
- shape (outline) [41%,22% → 50%,37%]
- shape (outline) [50%,32% → 59%,47%]
- group [10%,50% → 90%,74%]
  - rounded box (outline) [10%,50% → 90%,74%]
  - text 36pt [13%,52% → 87%,72%]: Imagine that we want to [[estimate the probability of failure|#80b9ff]] for an aircraft collision avoidance system from an aviation safety database that contains [[flight records from the month of December|#80b9ff]]. / What would the [[maximum likelihood estimate|#80b9ff]] of the probability of failure be if there were no recorded midair collisions in December?
- text 36pt [48%,78% → 52%,82%]: Zero!
- text 36pt [48%,86% → 52%,91%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- **Builds:** click 1: shape (outline) — appears; with previous: vector icon `shape-98123330.svg` — appears; with previous: vector icon `shape-98123330.svg` — appears; with previous: shape (outline) — appears; with previous: group — appears; click 2: text 36pt — fades up from dark; click 3: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 19
_(Keynote: Lecture 10, slide 19)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- image `pxl-20250114-140253068.jpg` [29%,30% → 71%,87%]
- text 36pt [39%,23% → 61%,27%]: Remember these fun times?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 20
_(Keynote: Lecture 10, slide 20)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- image `pxl-20250114-140253068.jpg` [4%,30% → 46%,87%]
- text 36pt [14%,23% → 36%,28%]: Remember these fun times?
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (42pt, #ffffff) [58%,26% → 84%,37%]
- line #ffffff [57%,24% → 85%,38%]
- equation $\theta$ (55pt, #ffffff) [52%,43% → 54%,47%]
- text 36pt [54%,43% → 98%,47%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [52%,49% → 54%,51%]
- text 36pt [54%,48% → 72%,52%]: : number of times same
- equation $m$ (56pt, #ffffff) [52%,54% → 54%,56%]
- text 36pt [54%,53% → 71%,58%]: : total number of flips
- text 36pt [62%,64% → 79%,69%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [56%,73% → 86%,77%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #ffffff [55%,72% → 86%,79%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 21
_(Keynote: Lecture 10, slide 21)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- image `pxl-20250114-140253068.jpg` [4%,102% → 46%,159%]
- text 36pt [14%,23% → 36%,28%]: Remember these fun times?
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (42pt, #ffffff) [58%,26% → 84%,37%]
- line #ffffff [57%,24% → 85%,38%]
- equation $\theta$ (55pt, #ffffff) [52%,43% → 54%,47%]
- text 36pt [54%,43% → 98%,47%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [52%,49% → 54%,51%]
- text 36pt [54%,48% → 72%,52%]: : number of times same
- equation $m$ (56pt, #ffffff) [52%,54% → 54%,56%]
- text 36pt [54%,53% → 71%,58%]: : total number of flips
- text 36pt [62%,64% → 79%,69%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [56%,73% → 86%,77%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #ffffff [55%,72% → 86%,79%]
- image `test-19683.svg` [3%,33% → 42%,87%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 22
_(Keynote: Lecture 10, slide 22)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- text 36pt [14%,23% → 36%,28%]: Remember these fun times?
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (42pt, #ffffff) [58%,26% → 84%,37%]
- line #ffffff [57%,24% → 85%,38%]
- equation $\theta$ (55pt, #ffffff) [52%,43% → 54%,47%]
- text 36pt [100%,43% → 144%,47%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [52%,49% → 54%,51%]
- text 36pt [54%,48% → 72%,52%]: : number of times same
- equation $m$ (56pt, #ffffff) [52%,54% → 54%,56%]
- text 36pt [54%,53% → 71%,58%]: : total number of flips
- text 36pt [62%,64% → 79%,69%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [56%,73% → 86%,77%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #ffffff [55%,72% → 86%,79%]
- image `test-19683.svg` [3%,33% → 42%,87%]
- text 36pt [54%,42% → 59%,47%]: : $p_\text{fail}$
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 23
_(Keynote: Lecture 10, slide 23)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- text 36pt [14%,23% → 36%,28%]: Remember these fun times?
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (42pt, #ffffff) [58%,26% → 84%,37%]
- line #ffffff [57%,24% → 85%,38%]
- equation $\theta$ (55pt, #ffffff) [52%,43% → 54%,47%]
- text 36pt [100%,43% → 144%,47%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [52%,49% → 54%,51%]
- text 36pt [100%,48% → 119%,52%]: : number of times same
- equation $m$ (56pt, #ffffff) [52%,54% → 54%,56%]
- text 36pt [54%,53% → 71%,58%]: : total number of flips
- text 36pt [62%,64% → 79%,69%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [56%,73% → 86%,77%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #ffffff [55%,72% → 86%,79%]
- image `test-19683.svg` [3%,33% → 42%,87%]
- text 36pt [54%,42% → 59%,47%]: : $p_\text{fail}$
- text 36pt [54%,48% → 78%,52%]: : number of failure trajectories
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 24
_(Keynote: Lecture 10, slide 24)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- text 36pt [14%,23% → 36%,28%]: Remember these fun times?
- equation $p(\theta \mid D) = \frac{p(D \mid \theta) p(\theta)}{\int_\theta p(D \mid \theta) p(\theta) d\theta}$ (42pt, #ffffff) [58%,26% → 84%,37%]
- line #ffffff [57%,24% → 85%,38%]
- equation $\theta$ (55pt, #ffffff) [52%,43% → 54%,47%]
- text 36pt [100%,43% → 144%,47%]: : probability of both frisbees landing in the same direction
- equation $n$ (56pt, #ffffff) [52%,49% → 54%,51%]
- text 36pt [100%,48% → 119%,52%]: : number of times same
- equation $m$ (56pt, #ffffff) [52%,54% → 54%,56%]
- text 36pt [101%,53% → 117%,58%]: : total number of flips
- text 36pt [62%,64% → 79%,69%]: $p(\theta) = \text{Beta}(\theta \mid \alpha, \beta)$
- text 36pt [56%,73% → 86%,77%]: $p(\theta \mid D) = \text{Beta}(\theta \mid \alpha + n, \beta + m - n)$
- line #ffffff [55%,72% → 86%,79%]
- image `test-19683.svg` [3%,33% → 42%,87%]
- text 36pt [54%,42% → 59%,47%]: : $p_\text{fail}$
- text 36pt [54%,48% → 78%,52%]: : number of failure trajectories
- text 36pt [54%,53% → 77%,57%]: : total number of trajectories
- text on a #80b9ff filled box 32pt [61%,84% → 80%,92%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 25
_(Keynote: Lecture 10, slide 25)_
- heading (spaced caps) 36pt [37%,6% → 113%,11%]: DIRECT ESTIMATION
- text 36pt [13%,13% → 87%,18%]: We could use [[Bayesian estimation|#80b9ff]] in this case to produce a [[distribution over the probability of failure|#80b9ff]].
- image `test-19719.svg` [19%,40% → 81%,83%]
- text 36pt [48%,23% → 52%,27%]: A cool thing about Bayesian estimation is that is allows us to [[quantify the confidence|#80b9ff]] we have in our estimate.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 26
_(Keynote: Lecture 10, slide 26)_
- text on a #80b9ff filled box 32pt [12%,29% → 16%,36%]: {1|#000000}
- text on a #80b9ff filled box 32pt [12%,43% → 16%,49%]: {2|#000000}
- line #ffffff [12%,22% → 45%,22%]
- heading (spaced caps) 36pt [18%,30% → 94%,35%]: DIRECT ESTIMATION
- heading (spaced caps) 36pt [18%,44% → 92%,48%]: IMPORTANCE SAMPLING
- heading (spaced caps) 50pt [-9%,14% → 67%,20%]: PLAN FOR TODAY
- text 36pt [58%,43% → 93%,48%]: {This is what I would start with for Project 2!|#80b9ff}
- arrow #80b9ff [49%,46% → 58%,46%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 27
_(Keynote: Lecture 10, slide 27)_
- heading (spaced caps) 36pt [60%,8% → 133%,12%]: IMPORTANCE SAMPLING
- heading (spaced caps) 36pt [11%,8% → 51%,12%]: DIRECT ESTIMATION
- line #ffffff [48%,5% → 48%,95%]
- group [5%,21% → 37%,29%]
  - line #ffffff [5%,21% → 9%,29%]
  - equation $1$ (36pt, #ffffff) [7%,24% → 7%,26%]
  - text 36pt [11%,21% → 37%,29%]: Draw samples from the [[nominal trajectory distribution|#80b9ff]].
- group [5%,38% → 42%,50%]
  - line #ffffff [5%,40% → 9%,48%]
  - equation $2$ (36pt, #ffffff) [7%,43% → 8%,45%]
  - text 36pt [11%,38% → 42%,50%]: Estimate the probability of failure by [[dividing|#80b9ff]] the number of [[failure|#80b9ff]] samples by the [[total|#80b9ff]] number of samples.
- text 36pt [6%,59% → 42%,70%]: What might be a problem with this method? / {Hint: what theme seems to be coming up over and over again in this course?|#929292}
- group [2%,74% → 46%,83%]
  - rounded box (outline) [2%,74% → 46%,83%]
  - text 36pt [3%,76% → 44%,80%]: It will be [[inefficient|#80b9ff]] for systems with [[rare failure events|#80b9ff]]!
- group [52%,19% → 83%,31%]
  - line #ffffff [52%,21% → 56%,29%]
  - equation $1$ (36pt, #ffffff) [53%,24% → 54%,26%]
  - text 36pt [57%,21% → 83%,29%]: Draw samples from a [[proposal distribution|#80b9ff]] that is more likely to produce failure trajectories.
- group [51%,40% → 88%,48%]
  - line #ffffff [51%,40% → 56%,48%]
  - equation $2$ (36pt, #ffffff) [53%,43% → 54%,45%]
  - text 36pt [57%,40% → 88%,48%]: Estimate the probability of failure by [[ reweighing |#80b9ff]]the samples.
- **Builds:** click 1: group — appears; click 2: group — appears; click 3: text 36pt — slides in; click 4: group — slides in; click 5: group — appears; click 6: group — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 28
_(Keynote: Lecture 10, slide 28)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- group [15%,14% → 46%,27%]
  - line #ffffff [15%,17% → 19%,24%]
  - equation $1$ (36pt, #ffffff) [17%,19% → 17%,22%]
  - text 36pt [21%,16% → 46%,25%]: Draw samples from a [[proposal distribution|#80b9ff]] that is more likely to produce failure trajectories.
- group [14%,34% → 51%,42%]
  - line #ffffff [14%,34% → 19%,41%]
  - equation $2$ (36pt, #ffffff) [16%,37% → 17%,39%]
  - text 36pt [20%,34% → 51%,42%]: Estimate the probability of failure by [[ reweighing |#80b9ff]]the samples.
- rounded box (outline) [13%,13% → 88%,29%]
- rounded box (outline) [13%,31% → 88%,85%]
- group [20%,24% → 20%,24%]
  - line #80b9ff [20%,23% → 27%,24%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 29
_(Keynote: Lecture 10, slide 29)_
- rounded box (outline) [13%,31% → 88%,85%]
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- group [15%,14% → 46%,27%]
  - line #ffffff [15%,17% → 19%,24%]
  - equation $1$ (36pt, #ffffff) [17%,19% → 17%,22%]
  - text 36pt [21%,16% → 46%,25%]: Draw samples from a [[proposal distribution|#80b9ff]] that is more likely to produce failure trajectories.
- group [14%,34% → 51%,42%]
  - line #ffffff [14%,34% → 19%,41%]
  - equation $2$ (36pt, #ffffff) [16%,37% → 17%,39%]
  - text 36pt [20%,34% → 51%,42%]: Estimate the probability of failure by [[ reweighing |#80b9ff]]the samples.
- rounded box (outline) [13%,13% → 88%,29%]
- equation $\tau \sim q(\cdot)$ (36pt, #ffffff) [62%,19% → 69%,22%]
- group [22%,46% → 45%,81%]
  - rounded box (outline) [22%,46% → 45%,81%]
  - image `val-page-145.svg` (cropped: show only 28–54% across and 41–62% down of the image) [23%,47% → 44%,80%]
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m \frac{p(\tau_i)}{q(\tau_i)} 1\{\tau_i \not\in \psi\}$ (36pt, #ffffff) [55%,46% → 76%,54%]
- equation $w_i = \frac{p(\tau_i)}{q(\tau_i)}$ (38pt, #ffa4e7) [69%,72% → 77%,80%]
- arrow #ffa4e7 [67%,63% → 70%,74%]
- text 36pt [58%,56% → 75%,66%]: $= \frac{1}{m} \sum_{i=1}^m${$w_i$|#ffa4e7}$1\{\tau_i \notin \psi\}$
- text 36pt [48%,89% → 52%,93%]: This estimator is both [[unbiased|#80cfb9]] and [[consistent|#80cfb9]].
- **Builds:** click 1: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 30
_(Keynote: Lecture 10, slide 30)_
- heading (spaced caps) 36pt [61%,18% → 134%,22%]: IMPORTANCE SAMPLING
- heading (spaced caps) 36pt [12%,18% → 52%,22%]: DIRECT ESTIMATION
- line #ffffff [49%,14% → 49%,82%]
- group [6%,31% → 38%,39%]
  - line #ffffff [6%,31% → 10%,39%]
  - equation $1$ (36pt, #ffffff) [8%,34% → 8%,36%]
  - text 36pt [12%,31% → 38%,39%]: Draw samples from $p(\cdot)$
- group [6%,42% → 43%,54%]
  - line #ffffff [6%,45% → 10%,52%]
  - equation $2$ (36pt, #ffffff) [8%,47% → 8%,49%]
  - text 36pt [12%,42% → 43%,54%]: Estimate the probability of failure:
- equation $\hat p_\text{fail} = \frac{1}{m}\sum_{i=1}^m 1\{\tau_i \notin \psi\}$ (45pt, #ffffff) [15%,54% → 37%,66%]
- group [56%,31% → 87%,39%]
  - line #ffffff [56%,31% → 60%,39%]
  - equation $1$ (36pt, #ffffff) [57%,34% → 58%,36%]
  - text 36pt [61%,31% → 87%,39%]: Draw samples from $q(\cdot)$
- group [55%,42% → 92%,54%]
  - line #ffffff [55%,44% → 60%,52%]
  - equation $2$ (36pt, #ffffff) [57%,47% → 58%,49%]
  - text 36pt [61%,42% → 92%,54%]: Estimate the probability of failure:
- text 45pt [63%,54% → 84%,66%]: $= \frac{1}{m} \sum_{i=1}^m${$w_i$|#ffa4e7}$1\{\tau_i \notin \psi\}$
- equation $w_i = \frac{p(\tau_i)}{q(\tau_i)}$ (38pt, #ffa4e7) [76%,72% → 84%,80%]
- arrow #ffa4e7 [74%,63% → 77%,73%]
- text 36pt [47%,89% → 51%,94%]: Samples that are [[more likely|#80b9ff]] under the nominal trajectory distribution will have a [[higher importance weight|#ffa4e7]].
- text 36pt [86%,72% → 96%,80%]: {importance weight|#ffa4e7}
- equation $\hat p_\text{fail}$ (45pt, #ffffff) [59%,56% → 63%,61%]
- **Builds:** click 1: text 36pt — slides in; click 2: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 31
_(Keynote: Lecture 10, slide 31)_
- heading (spaced caps) 36pt [10%,12% → 83%,17%]: IMPORTANCE SAMPLING
- group [5%,25% → 37%,34%]
  - line #ffffff [5%,26% → 9%,33%]
  - equation $1$ (36pt, #ffffff) [7%,28% → 7%,31%]
  - text 36pt [11%,25% → 37%,34%]: Draw samples from $q(\cdot)$
- group [5%,37% → 42%,49%]
  - line #ffffff [5%,39% → 9%,47%]
  - equation $2$ (36pt, #ffffff) [6%,42% → 7%,44%]
  - text 36pt [11%,37% → 42%,49%]: Estimate the probability of failure:
- text 45pt [13%,48% → 34%,61%]: $= \frac{1}{m} \sum_{i=1}^m${$w_i$|#ffa4e7}$1\{\tau \notin \psi\}$
- equation $w_i = \frac{p(\tau_i)}{q(\tau_i)}$ (38pt, #ffa4e7) [26%,66% → 34%,75%]
- arrow #ffa4e7 [24%,58% → 26%,68%]
- text 36pt [35%,66% → 46%,75%]: {importance weight|#ffa4e7}
- image `val-page-147.svg` (cropped: show only 11–64% across and 21–42% down of the image) [50%,26% → 92%,60%]
- line #ff48cf [53%,45% → 76%,48%]
- arrow #ff48cf [31%,30% → 52%,46%]
- **Builds:** click 1: line #ff48cf — fades up from dark; with previous: arrow #ff48cf — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 32
_(Keynote: Lecture 10, slide 32)_
- heading (spaced caps) 36pt [10%,12% → 83%,17%]: IMPORTANCE SAMPLING
- group [5%,25% → 37%,34%]
  - line #ffffff [5%,26% → 9%,33%]
  - equation $1$ (36pt, #ffffff) [7%,28% → 7%,31%]
  - text 36pt [11%,25% → 37%,34%]: Draw samples from $q(\cdot)$
- group [5%,37% → 42%,49%]
  - line #ffffff [5%,39% → 9%,47%]
  - equation $2$ (36pt, #ffffff) [6%,42% → 7%,44%]
  - text 36pt [11%,37% → 42%,49%]: Estimate the probability of failure:
- text 45pt [13%,48% → 34%,61%]: $= \frac{1}{m} \sum_{i=1}^m${$w_i$|#ffa4e7}$1\{\tau \notin \psi\}$
- equation $w_i = \frac{p(\tau_i)}{q(\tau_i)}$ (38pt, #ffa4e7) [26%,66% → 34%,75%]
- arrow #ffa4e7 [24%,58% → 26%,68%]
- text 36pt [35%,66% → 46%,75%]: {importance weight|#ffa4e7}
- image `val-page-147.svg` (cropped: show only 11–64% across and 21–42% down of the image) [50%,26% → 92%,60%]
- line #ff48cf [53%,47% → 72%,55%]
- arrow #ff48cf [36%,51% → 52%,65%]
- equation $\hat p_\text{fail}$ (45pt, #ffffff) [9%,51% → 13%,55%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 33
_(Keynote: Lecture 10, slide 33)_
- heading (spaced caps) 36pt [10%,12% → 83%,17%]: IMPORTANCE SAMPLING
- group [5%,25% → 37%,34%]
  - line #ffffff [5%,26% → 9%,33%]
  - equation $1$ (36pt, #ffffff) [7%,28% → 7%,31%]
  - text 36pt [11%,25% → 37%,34%]: Draw samples from $q(\cdot)$
- group [5%,37% → 42%,49%]
  - line #ffffff [5%,39% → 9%,47%]
  - equation $2$ (36pt, #ffffff) [6%,42% → 7%,44%]
  - text 36pt [11%,37% → 42%,49%]: Estimate the probability of failure:
- text 45pt [13%,48% → 34%,61%]: $= \frac{1}{m} \sum_{i=1}^m${$w_i$|#ffa4e7}$1\{\tau \notin \psi\}$
- equation $w_i = \frac{p(\tau_i)}{q(\tau_i)}$ (38pt, #ffa4e7) [26%,66% → 34%,75%]
- arrow #ffa4e7 [24%,58% → 26%,68%]
- text 36pt [35%,66% → 46%,75%]: {importance weight|#ffa4e7}
- text on a #80b9ff filled box 32pt [40%,83% → 60%,91%]: {Pluto Notebook!|#000000}
- image `val-page-147.svg` (cropped: show only 11–64% across and 21–42% down of the image) [50%,26% → 92%,60%]
- line #ff48cf [53%,55% → 91%,58%]
- arrow #ff48cf [34%,54% → 52%,56%]
- equation $\hat p_\text{fail}$ (45pt, #ffffff) [9%,51% → 13%,55%]
- **Builds:** click 1: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 34
_(Keynote: Lecture 10, slide 34)_
- rounded box (outline) [61%,45% → 91%,61%]
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [40%,13% → 60%,21%]: {Pluto Notebook!|#000000}
- text 36pt [62%,47% → 90%,59%]: We want the proposal distribution to [[sample likely failures|#80b9ff]] more often than unlikely failures or successes.
- text 36pt [60%,65% → 92%,69%]: Is there an optimal proposal distribution?
- video `video-20602.mp4` (plays 0.0s–17.0s, loops) [19%,26% → 52%,93%]
- **Builds:** then: video `video-20602.mp4` (plays 0.0s–17.0s, loops) — video starts; click 1: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 35
_(Keynote: Lecture 10, slide 35)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- text 36pt [8%,31% → 40%,36%]: Is there an optimal proposal distribution?
- text 36pt [6%,42% → 41%,54%]: We will define the optimal proposal distribution as the one that [[minimizes the variance|#80b9ff]] of the estimator:
- equation $\text{Var}[\hat p_\text{fail}] = \frac{1}{m} \mathbb E_{\tau \sim q(\cdot)}\left[\frac{(p(\tau) 1\{\tau \notin \psi\} - q(\tau)p_\text{fail})^2}{q(\tau)}\right]$ (29pt, #ffffff) [8%,58% → 39%,67%]
- line #ffffff [8%,37% → 40%,37%]
- group [8%,70% → 8%,70%]
  - line #80b9ff [8%,69% → 39%,70%]
  - line #80b9ff [16%,68% → 39%,71%]
  - line #80b9ff [32%,62% → 35%,63%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 36
_(Keynote: Lecture 10, slide 36)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- text 36pt [8%,31% → 40%,36%]: Is there an optimal proposal distribution?
- text 36pt [6%,42% → 41%,54%]: We will define the optimal proposal distribution as the one that [[minimizes the variance|#80b9ff]] of the estimator:
- equation $\text{Var}[\hat p_\text{fail}] = \frac{1}{m} \mathbb E_{\tau \sim q(\cdot)}\left[\frac{(p(\tau) 1\{\tau \notin \psi\} - q(\tau)p_\text{fail})^2}{q(\tau)}\right]$ (29pt, #ffffff) [8%,58% → 39%,67%]
- line #ffffff [8%,37% → 40%,37%]
- shape (outline) [48%,46% → 55%,54%]
- equation $q^\ast(\tau) = \frac{p(\tau) 1\{\tau \notin \psi\}}{p_\text{fail}}$ (53pt, #ffffff) [60%,44% → 84%,56%]
- line #ffffff [58%,42% → 86%,58%]
- text 36pt [70%,60% → 74%,65%]: Does this distribution look familiar?
- text 36pt [62%,66% → 81%,71%]: It’s the [[failure distribution|#fab0ae]]!
- rounded box (outline) [53%,76% → 91%,88%]
- text 100pt [55%,76% → 61%,89%]: 🤔
- text 36pt [62%,77% → 89%,86%]: …but it is written in terms of the thing we want to estimate ($p_\text{fail}$).
- **Builds:** click 1: text 36pt — slides in; click 2: text 36pt — slides in; click 3: text 100pt — fades up from dark; with previous: text 36pt — fades up from dark; with previous: rounded box (outline) — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 37
_(Keynote: Lecture 10, slide 37)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- equation $q^\ast(\tau) = \frac{p(\tau) 1\{\tau \notin \psi\}}{p_\text{fail}}$ (53pt, #ffffff) [14%,28% → 38%,40%]
- line #ffffff [12%,27% → 40%,42%]
- text 36pt [12%,45% → 40%,49%]: Does this distribution look familiar?
- text 36pt [16%,51% → 35%,55%]: It’s the [[failure distribution|#fab0ae]]!
- rounded box (outline) [7%,60% → 45%,73%]
- text 100pt [10%,60% → 15%,73%]: 🤔
- text 36pt [16%,62% → 43%,71%]: …but it is written in terms of the thing we want to estimate ($p_\text{fail}$).
- image `pasted-movie-20620.png` [50%,23% → 94%,77%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 38
_(Keynote: Lecture 10, slide 38)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- equation $q^\ast(\tau) = \frac{p(\tau) 1\{\tau \notin \psi\}}{p_\text{fail}}$ (53pt, #ffffff) [14%,28% → 38%,40%]
- line #ffffff [12%,27% → 40%,42%]
- text 36pt [12%,45% → 40%,49%]: Does this distribution look familiar?
- text 36pt [16%,51% → 35%,55%]: It’s the [[failure distribution|#fab0ae]]!
- rounded box (outline) [7%,60% → 45%,73%]
- text 100pt [10%,60% → 15%,73%]: 🤔
- text 36pt [16%,62% → 43%,71%]: …but it is written in terms of the thing we want to estimate ($p_\text{fail}$).
- text 36pt [54%,28% → 90%,37%]: Best we can do is select a proposal that is [[as close as possible|#80b9ff]] to the [[failure distribution|#fab0ae]].
- group [55%,41% → 89%,55%]
  - rounded box (outline) [55%,41% → 89%,55%]
  - text 36pt [56%,41% → 88%,55%]: {Note: we must be able to |#000000}[[sample from|#0072fe]]{ and |#000000}[[compute the (normalized) density|#0072fe]]{ of the proposal distribution we choose.|#000000}
- **Builds:** click 1: group — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 39
_(Keynote: Lecture 10, slide 39)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- text 36pt [10%,21% → 46%,30%]: Best we can do is select a proposal that is [[as close as possible|#80b9ff]] to the [[failure distribution|#fab0ae]].
- group [11%,34% → 45%,48%]
  - rounded box (outline) [11%,34% → 45%,48%]
  - text 36pt [12%,34% → 44%,48%]: {Note: we must be able to |#000000}[[sample from|#0072fe]]{ and |#000000}[[compute the (normalized) density|#0072fe]]{ of the proposal distribution we choose.|#000000}
- text 36pt [13%,66% → 43%,74%]: ..but we [[don’t know|#80b9ff]] how to [[compute the normalized density|#80b9ff]] for it.
- group [11%,52% → 45%,78%]
  - text 36pt [13%,54% → 43%,62%]: From previous lecture, we [[know|#80b9ff]] how to [[sample from|#80b9ff]] the [[failure distribution|#fab0ae]]!
  - rounded box (outline) [11%,52% → 45%,78%]
- group [54%,40% → 92%,62%]
  - rounded box (outline) [54%,40% → 92%,62%]
  - vector icon `shape-61531053.svg` [57%,46% → 60%,57%]
  - text 36pt [62%,43% → 91%,59%]: We can [[fit a distribution|#80b9ff]] that we know how to compute the normalized density of using [[samples from the failure distribution|#80b9ff]].
- text on a #80b9ff filled box 32pt [64%,66% → 83%,74%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: group — fades up from dark; click 2: text 36pt — slides in; click 3: group — slides in; click 4: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 40
_(Keynote: Lecture 10, slide 40)_
- heading (spaced caps) 36pt [35%,5% → 109%,10%]: IMPORTANCE SAMPLING
- group [31%,14% → 69%,36%]
  - rounded box (outline) [31%,14% → 69%,36%]
  - vector icon `shape-61531053.svg` [34%,20% → 37%,31%]
  - text 36pt [39%,17% → 67%,33%]: We can [[fit a distribution|#80b9ff]] that we know how to compute the normalized density of using [[samples from the failure distribution|#80b9ff]].
- text 36pt [10%,42% → 19%,46%]: Challenges
- group [11%,50% → 67%,58%]
  - line #ffffff [11%,50% → 15%,58%]
  - equation $1$ (36pt, #ffffff) [12%,53% → 13%,55%]
  - text 36pt [17%,50% → 67%,58%]: Producing samples from the failure distribution is a [[nontrivial task|#80b9ff]] (as we saw last lecture).
- group [11%,64% → 73%,72%]
  - line #ffffff [11%,64% → 15%,72%]
  - equation $2$ (36pt, #ffffff) [12%,67% → 13%,69%]
  - text 36pt [17%,64% → 73%,72%]: It may be [[difficult|#80b9ff]] to produce a good fit to samples from the failure distribution for [[high-dimensional|#80b9ff]] systems with [[multiple failure modes|#80b9ff]].
- **Builds:** click 1: group — appears; click 2: group — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 41
_(Keynote: Lecture 11, slide 14)_
- rounded box (outline) [15%,43% → 85%,52%]
- text 36pt [18%,45% → 82%,49%]: Various [[importance sampling algorithms|#80b9ff]] have different ways of selecting this proposal.
- text 36pt [29%,54% → 71%,59%]: One option: [[hand design|#80b9ff]] based on domain knowledge.
- text 36pt [29%,61% → 71%,66%]: Perhaps your fuzzing distribution? Hint, hint: project 2.
- **Builds:** click 1: text 36pt — com.apple.iWork.Keynote.KNBuildSkidByCharacter
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 42
_(Keynote: Lecture 11, slide 15)_
- rounded box (outline) [15%,43% → 85%,52%]
- text 36pt [18%,45% → 82%,49%]: Various [[importance sampling algorithms|#80b9ff]] have different ways of selecting this proposal.
- text 36pt [18%,55% → 82%,59%]: Another option: [[fit|#80b9ff]] a proposal distribution to [[samples |#80b9ff]]from the [[failure distribution|#fab0ae]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 43
_(Keynote: Lecture 11, slide 16)_
- rounded box (outline) [15%,7% → 85%,16%]
- text 36pt [18%,9% → 82%,14%]: Various [[importance sampling algorithms|#80b9ff]] have different ways of selecting this proposal.
- text 36pt [19%,19% → 81%,24%]: Another option: [[fit|#80b9ff]] a proposal distribution to [[samples |#80b9ff]]from the [[failure distribution|#fab0ae]].
- image `test-22262.svg` [17%,27% → 84%,92%]
- equation $p(\tau)$ (36pt, #929292) [70%,66% → 73%,69%]
- equation $q^\ast(\tau) = p(\tau \mid \tau \notin \psi)$ (36pt, #fab0ae) [62%,35% → 77%,38%]
- equation $q(\tau)$ (36pt, #c3b8ff) [56%,41% → 59%,44%]
- text 32pt [64%,90% → 95%,94%]: {samples from failure distribution using MCMC|#fab0ae}
- arrow #fab0ae [60%,85% → 77%,90%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 44
_(Keynote: Lecture 11, slide 17)_
- rounded box (outline) [15%,7% → 85%,16%]
- text 36pt [18%,9% → 82%,14%]: Various [[importance sampling algorithms|#80b9ff]] have different ways of selecting this proposal.
- text 36pt [19%,19% → 81%,24%]: Another option: [[fit|#80b9ff]] a proposal distribution to [[samples |#80b9ff]]from the [[failure distribution|#fab0ae]].
- text 36pt [10%,42% → 19%,46%]: Challenges
- group [11%,50% → 67%,58%]
  - line #ffffff [11%,50% → 15%,58%]
  - equation $1$ (36pt, #ffffff) [12%,53% → 13%,55%]
  - text 36pt [17%,50% → 67%,58%]: Producing samples from the failure distribution is a [[nontrivial task|#80b9ff]] (as we saw last lecture).
- group [11%,64% → 73%,72%]
  - line #ffffff [11%,64% → 15%,72%]
  - equation $2$ (36pt, #ffffff) [12%,67% → 13%,69%]
  - text 36pt [17%,64% → 73%,72%]: It may be [[difficult|#80b9ff]] to produce a good fit to samples from the failure distribution for [[high-dimensional|#80b9ff]] systems with [[multiple failure modes|#80b9ff]].
- **Builds:** click 1: group — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 45
_(Keynote: Lecture 11, slide 18)_
- rounded box (outline) [15%,7% → 85%,16%]
- text 36pt [18%,9% → 82%,14%]: Various [[importance sampling algorithms|#80b9ff]] have different ways of selecting this proposal.
- text 36pt [19%,19% → 81%,24%]: Another option: [[fit|#80b9ff]] a proposal distribution to [[samples |#80b9ff]]from the [[failure distribution|#fab0ae]].
- text 36pt [10%,42% → 19%,46%]: Challenges
- group [11%,50% → 67%,58%]
  - line #ffffff [11%,50% → 15%,58%]
  - equation $1$ (36pt, #ffffff) [12%,53% → 13%,55%]
  - text 36pt [17%,50% → 67%,58%]: Producing samples from the failure distribution is a [[nontrivial task|#80b9ff]] (as we saw in the failure distribution lecture).
- rounded box (outline) [16%,61% → 69%,75%]
- vector icon `shape-05d0c7b7.svg` [18%,63% → 22%,73%]
- text 36pt [23%,63% → 69%,73%]: What if we could [[still|#80b9ff]] [[fit a good proposal|#80b9ff]] using samples from [[a different distribution|#80b9ff]] that is easier to sample from?
- group [11%,78% → 73%,86%]
  - line #ffffff [11%,78% → 15%,86%]
  - equation $2$ (36pt, #ffffff) [12%,81% → 13%,83%]
  - text 36pt [17%,78% → 73%,86%]: It may be [[difficult|#80b9ff]] to produce a good fit to samples from the failure distribution for [[high-dimensional|#80b9ff]] systems with [[multiple failure modes|#80b9ff]].
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 46
_(Keynote: Lecture 11, slide 19)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: CROSS ENTROPY METHOD (ADAPTIVE IMPORTANCE SAMPLING)
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: MULTIPLE IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: POPULATION MONTE CARLO
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: SEQUENTIAL MONTE CARLO
- **Builds:** click 1: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 2: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 3: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in; click 4: text on a #80b9ff filled box 32pt — slides in; with previous: heading (spaced caps) 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 47
_(Keynote: Lecture 11, slide 20)_
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- rounded box (outline) [24%,11% → 76%,25%]
- vector icon `shape-05d0c7b7.svg` [26%,13% → 29%,24%]
- text 36pt [30%,13% → 76%,24%]: What if we could [[still|#80b9ff]] [[fit a good proposal|#80b9ff]] using samples from [[a different distribution|#80b9ff]] that is easier to sample from?
- group [8%,34% → 74%,42%]
  - line #ffffff [8%,34% → 12%,42%]
  - equation $1$ (36pt, #ffffff) [10%,37% → 10%,39%]
  - text 36pt [14%,36% → 74%,40%]: Draw samples from an [[initial proposal distribution|#80b9ff]] that is easy sample from.
- group [8%,44% → 84%,56%]
  - line #ffffff [8%,46% → 12%,54%]
  - equation $2$ (36pt, #ffffff) [10%,49% → 11%,51%]
  - text 36pt [14%,44% → 84%,56%]: Use the samples to [[fit a new proposal distribution|#80b9ff]] from a model class that we also know how to sample from by selecting the parameters that [[minimize the cross entropy|#80b9ff]] between the [[proposal distribution|#80b9ff]] and the [[failure distribution|#80b9ff]].
- **Builds:** click 1: group — slides in; click 2: group — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 48
_(Keynote: Lecture 11, slide 21)_
- group [8%,34% → 74%,42%]
  - line #ffffff [8%,34% → 12%,42%]
  - equation $1$ (36pt, #ffffff) [10%,37% → 10%,39%]
  - text 36pt [14%,36% → 74%,40%]: Draw samples from an [[initial proposal distribution|#80b9ff]] that is easy sample from.
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- rounded box (outline) [24%,11% → 76%,25%]
- vector icon `shape-05d0c7b7.svg` [26%,13% → 29%,24%]
- text 36pt [30%,13% → 76%,24%]: What if we could [[still|#80b9ff]] [[fit a good proposal|#80b9ff]] using samples from [[a different distribution|#80b9ff]] that is easier to sample from?
- group [8%,58% → 84%,70%]
  - line #ffffff [8%,60% → 12%,68%]
  - equation $2$ (36pt, #ffffff) [10%,63% → 11%,65%]
  - text 36pt [14%,58% → 84%,70%]: Use the samples to [[fit a new proposal distribution|#80b9ff]] from a model class that we also know how to sample from by selecting the parameters that [[minimize the cross entropy|#80b9ff]] between the [[proposal distribution|#80b9ff]] and the [[failure distribution|#80b9ff]].
- equation $\tau \sim q(\cdot)$ (67pt, #ffa4e7) [18%,44% → 30%,49%]
- text 36pt [16%,73% → 87%,81%]: {For many common model classes (e.g. Gaussian), minimizing the cross entropy is equivalent to computing the weighted maximum likelihood estimate for the parameters with weights|#ffa4e7}
- equation $w = \frac{p(\tau)1\{\tau \notin \psi\}}{q(\tau)}$ (44pt, #ffa4e7) [16%,84% → 33%,93%]
- text 36pt [41%,44% → 74%,49%]: {What proposal distribution should we try?|#c3b8ff}
- arrow #c3b8ff [31%,47% → 40%,47%]
- text 36pt [39%,49% → 76%,54%]: {How about the nominal trajectory distribution?|#a9a9a9}
- text on a #80b9ff filled box 32pt [77%,45% → 96%,53%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: equation $\tau \sim q(\cdot)$ — appears; click 2: text 36pt — appears; with previous: equation $w = \frac{p(\tau)1\{\tau \notin \psi\}}{q(\tau)}$ — appears; click 3: text 36pt — appears; with previous: arrow #c3b8ff — draws in; click 4: text 36pt — slides in; click 5: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 49
_(Keynote: Lecture 11, slide 22)_
- text on a #80b9ff filled box 32pt [40%,14% → 60%,22%]: {Pluto Notebook!|#000000}
- video `video-22409.mp4` (plays 0.0s–10.1s, loops) [30%,39% → 70%,91%]
- text 36pt [25%,25% → 75%,34%]: If we sample from the nominal distribution and failures are rare, / we may not get any failures and all the [[weights will be zero|#80b9ff]]!
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** then: video `video-22409.mp4` (plays 0.0s–10.1s, loops) — video starts
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 50
_(Keynote: Lecture 11, slide 23)_
- video `video-22409.mp4` (plays 0.0s–10.1s, loops) [8%,41% → 46%,90%]
- rounded box (outline) [51%,50% → 91%,68%]
- vector icon `shape-61531053.svg` [54%,53% → 57%,64%]
- text 36pt [59%,53% → 89%,65%]: Start with the nominal distribution and iteratively [[adapt it|#ffa4e7]] to move closer to the failure distribution.
- text 36pt [52%,76% → 92%,80%]: {The adaptive part of adaptive importance sampling!|#ffa4e7}
- arrow #ffa4e7 [71%,61% → 73%,75%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- text on a #80b9ff filled box 32pt [40%,14% → 60%,22%]: {Pluto Notebook!|#000000}
- text 36pt [25%,25% → 75%,34%]: If we sample from the nominal distribution and failures are rare, / we may not get any failures and all the [[weights will be zero|#80b9ff]]!
- **Builds:** then: video `video-22409.mp4` (plays 0.0s–10.1s, loops) — video starts; click 1: text 36pt — appears; with previous: arrow #ffa4e7 — draws in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 51
_(Keynote: Lecture 11, slide 24)_
- text 36pt [8%,22% → 12%,27%]: Before we start:
- text 36pt [14%,30% → 44%,38%]: Pick an [[initial proposal|#80b9ff]] to adapt / (e.g. nominal trajectory distribution)
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- image `test-20993.svg` [52%,25% → 89%,84%]
- text 36pt [14%,41% → 44%,50%]: Pick a notion of [[closeness to failure $f(\tau)$|#80b9ff]] / (e.g. robustness)
- line #ffffff [9%,42% → 13%,50%]
- equation $2$ (36pt, #ffffff) [11%,45% → 11%,47%]
- arrow #ffffff [59%,76% → 68%,76%]
- line #ffffff [68%,75% → 69%,77%]
- text 36pt [15%,56% → 41%,64%]: We will require that {$f(\tau) \leq 0$|#fab0ae} for failure trajectories such that
- equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ (36pt, #ffffff) [17%,65% → 38%,68%]
- rounded box (outline) [12%,54% → 43%,71%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [31%,57% → 37%,60%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: line #ffffff — appears; with previous: equation $1$ — appears; with previous: text 36pt — appears; with previous: image `test-20993.svg` — appears; click 2: equation $2$ — appears; with previous: line #ffffff — appears; with previous: text 36pt — appears; click 3: line #ffffff — fades up from dark; then: arrow #ffffff — draws in; click 4: text 36pt — fades up from dark; with previous: equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ — fades up from dark; with previous: rounded box (outline) — fades up from dark; with previous: equation $f(\tau) \leq 0$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 52
_(Keynote: Lecture 11, slide 25)_
- rounded box (outline) [7%,74% → 49%,93%]
- text 36pt [8%,22% → 12%,27%]: Before we start:
- text 36pt [14%,30% → 44%,38%]: Pick an [[initial proposal|#80b9ff]] to adapt / (e.g. nominal trajectory distribution)
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- image `test-20993.svg` [52%,25% → 89%,84%]
- text 36pt [14%,41% → 44%,50%]: Pick a notion of [[closeness to failure $f(\tau)$|#80b9ff]] / (e.g. robustness)
- line #ffffff [9%,42% → 13%,50%]
- equation $2$ (36pt, #ffffff) [11%,45% → 11%,47%]
- arrow #ffffff [59%,76% → 68%,76%]
- line #ffffff [68%,75% → 69%,77%]
- text 36pt [15%,56% → 41%,64%]: We will require that {$f(\tau) \leq 0$|#fab0ae} for failure trajectories such that
- equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ (36pt, #ffffff) [17%,65% → 38%,68%]
- rounded box (outline) [12%,54% → 43%,71%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- text 36pt [8%,76% → 47%,84%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: text 36pt — fades up from dark; with previous: rounded box (outline) — fades up from dark

## Slide 53
_(Keynote: Lecture 11, slide 26)_
- rounded box (outline) [7%,74% → 49%,93%]
- image `test-21174.svg` [52%,25% → 89%,84%]
- text 36pt [8%,22% → 12%,27%]: Before we start:
- text 36pt [14%,30% → 44%,38%]: Pick an [[initial proposal|#80b9ff]] to adapt / (e.g. nominal trajectory distribution)
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,41% → 44%,50%]: Pick a notion of [[closeness to failure $f(\tau)$|#80b9ff]] / (e.g. robustness)
- line #ffffff [9%,42% → 13%,50%]
- equation $2$ (36pt, #ffffff) [11%,45% → 11%,47%]
- text 36pt [15%,56% → 41%,64%]: We will require that {$f(\tau) \leq 0$|#fab0ae} for failure trajectories such that
- equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ (36pt, #ffffff) [17%,65% → 38%,68%]
- rounded box (outline) [12%,54% → 43%,71%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- text 36pt [8%,76% → 47%,84%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 36pt [14%,86% → 42%,90%]: …but the weights might all be {zero|#f3cf80}!
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 54
_(Keynote: Lecture 11, slide 27)_
- image `test-21174.svg` [52%,25% → 89%,84%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 11%,46%]
- image `test-21232.svg` [52%,25% → 89%,84%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: equation $1$ — appears; with previous: line #ffffff — appears; with previous: text 36pt — appears; click 2: text 36pt — appears; with previous: equation $2$ — appears; with previous: line #ffffff — appears; with previous: image `test-21232.svg` — appears

## Slide 55
_(Keynote: Lecture 11, slide 28)_
- image `test-21297.svg` [52%,25% → 89%,84%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 56
_(Keynote: Lecture 11, slide 29)_
- image `test-21308.svg` [52%,25% → 89%,84%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 57
_(Keynote: Lecture 11, slide 30)_
- rounded box (outline) [25%,78% → 34%,85%]
- image `test-21316.svg` [52%,25% → 89%,84%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: text 36pt — fades up from dark; with previous: rounded box (outline) — fades up from dark

## Slide 58
_(Keynote: Lecture 11, slide 31)_
- image `test-21340.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 59
_(Keynote: Lecture 11, slide 32)_
- image `test-21356.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 11%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 60
_(Keynote: Lecture 11, slide 33)_
- image `test-21363.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 61
_(Keynote: Lecture 11, slide 34)_
- image `test-21370.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 62
_(Keynote: Lecture 11, slide 35)_
- image `test-21378.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 11%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 63
_(Keynote: Lecture 11, slide 36)_
- image `test-21386.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [52%,41% → 59%,44%]
- text 36pt [64%,34% → 89%,42%]: {Perform importance sampling with the final proposal.|#c0c0c0}
- arrow #a9a9a9 [59%,43% → 72%,49%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: text 36pt — appears; with previous: arrow #a9a9a9 — draws in

## Slide 64
_(Keynote: Lecture 11, slide 37)_
- image `test-22482.svg` [52%,25% → 89%,84%]
- rounded box (outline) [25%,78% → 34%,85%]
- text 36pt [8%,22% → 21%,27%]: At each iteration
- text 36pt [14%,32% → 47%,36%]: Draw samples from the current proposal.
- line #ffffff [9%,30% → 13%,38%]
- equation $1$ (36pt, #ffffff) [11%,33% → 11%,35%]
- text 36pt [14%,43% → 47%,48%]: Compute $f(\tau)$ for each sample and pick the top {$m_\text{elite}$|#80b9ff} samples.
- line #ffffff [9%,42% → 13%,49%]
- equation $2$ (36pt, #ffffff) [11%,44% → 12%,46%]
- rounded box (outline) [63%,16% → 93%,29%]
- text 24pt [64%,17% → 92%,23%]: Ideally, we minimize the [[cross entropy|#80b9ff]] between the new proposal distribution and {$p(\tau \mid f(\tau) \leq 0)$|#fab0ae}.
- text 24pt [68%,24% → 88%,28%]: …but the weights might all be {zero|#f3cf80}!
- text 36pt [14%,65% → 47%,73%]: Compute the next proposal by minimizing the cross entropy with {$p(\tau \mid f(\tau) \leq \gamma)$|#80b9ff}.
- line #ffffff [9%,65% → 13%,73%]
- equation $4$ (36pt, #ffffff) [11%,68% → 11%,70%]
- text 36pt [14%,53% → 48%,61%]: Select the threshold {$\gamma$|#80b9ff} to be the highest $f(\tau)$ of the elite samples.
- line #ffffff [9%,53% → 13%,61%]
- equation $3$ (36pt, #ffffff) [11%,56% → 12%,58%]
- text 36pt [26%,79% → 33%,84%]: REPEAT!
- text 36pt [64%,34% → 89%,42%]: {Perform importance sampling with the final proposal.|#c0c0c0}
- arrow #a9a9a9 [59%,43% → 72%,49%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD

## Slide 65
_(Keynote: Lecture 11, slide 38)_
- image `g01-21552.svg` [25%,22% → 66%,96%]
- image `g02-21558.svg` [25%,22% → 66%,96%]
- image `g03-21561.svg` [25%,22% → 66%,96%]
- image `g04-21556.svg` [25%,22% → 66%,96%]
- image `g05-21562.svg` [25%,22% → 66%,96%]
- image `g06-21557.svg` [25%,22% → 66%,96%]
- image `g07-21560.svg` [25%,22% → 66%,96%]
- image `g08-21554.svg` [25%,22% → 66%,96%]
- image `g09-21553.svg` [25%,22% → 66%,96%]
- image `g10-21563.svg` [25%,22% → 66%,96%]
- image `g11-21559.svg` [25%,22% → 66%,96%]
- image `g12-21555.svg` [25%,22% → 66%,96%]
- heading (spaced caps) 36pt [34%,5% → 66%,9%]: CROSS ENTROPY METHOD
- **Builds:** click 1: image `g02-21558.svg` — appears; click 2: image `g03-21561.svg` — appears; then (0.25 s later): image `g04-21556.svg` — appears; then (0.25 s later): image `g05-21562.svg` — appears; then (0.25 s later): image `g06-21557.svg` — appears; then (0.25 s later): image `g07-21560.svg` — appears; then (0.25 s later): image `g08-21554.svg` — appears; then (0.25 s later): image `g09-21553.svg` — appears; then (0.25 s later): image `g10-21563.svg` — appears; then (0.25 s later): image `g11-21559.svg` — appears; then (0.25 s later): image `g12-21555.svg` — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 66
_(Keynote: Lecture 11, slide 39)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: CROSS ENTROPY METHOD (ADAPTIVE IMPORTANCE SAMPLING)
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: MULTIPLE IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: POPULATION MONTE CARLO
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: SEQUENTIAL MONTE CARLO
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 67
_(Keynote: Lecture 11, slide 40)_
- rounded box (outline) [22%,73% → 77%,88%]
- heading (spaced caps) 36pt [28%,75% → 71%,80%]: MULTIPLE IMPORTANCE SAMPLING
- text 36pt [25%,81% → 75%,85%]: Why pick just one proposal distribution when you can have many?
- text 36pt [48%,6% → 52%,11%]: In regular importance sampling, we have to pick a proposal distribution!
- image `pasted-image-22575.png` [37%,15% → 63%,67%]
- text 36pt [26%,90% → 55%,94%]: *perfect for indecisive people like me!
- **Builds:** click 1: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 68
_(Keynote: Lecture 11, slide 41)_
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- text 36pt [12%,18% → 46%,23%]: Draw samples from the current proposals.
- line #ffffff [7%,17% → 11%,24%]
- equation $1$ (36pt, #ffffff) [9%,19% → 9%,22%]
- equation $\tau_i \sim q_i(\tau)$ (52pt, #ffffff) [13%,27% → 22%,31%]
- text 36pt [12%,38% → 46%,43%]: Use the samples to estimate $p_\text{fail}$.
- line #ffffff [7%,37% → 11%,44%]
- equation $2$ (36pt, #ffffff) [9%,39% → 10%,42%]
- text 36pt [13%,45% → 33%,55%]: $\hat p_\text{fail}= \frac{1}{m} \sum_{i=1}^m$$w_i$$1\{\tau_i \notin \psi\}$
- image `test-22725.svg` [50%,14% → 86%,83%]
- vector icon `shape-4a963724.svg` [56%,74% → 58%,77%]
- vector icon `shape-4a963724.svg` [61%,74% → 62%,77%]
- vector icon `shape-4a963724.svg` [59%,74% → 61%,77%]
- vector icon `shape-4a963724.svg` [63%,74% → 65%,77%]
- vector icon `shape-4a963724.svg` [66%,74% → 68%,77%]
- vector icon `shape-a77812c0.svg` [78%,74% → 80%,77%]
- vector icon `shape-a77812c0.svg` [73%,74% → 75%,77%]
- vector icon `shape-a77812c0.svg` [71%,74% → 73%,77%]
- vector icon `shape-a77812c0.svg` [65%,74% → 67%,77%]
- vector icon `shape-a77812c0.svg` [61%,74% → 63%,77%]
- vector icon `shape-a77812c0.svg` [55%,74% → 57%,77%]
- vector icon `shape-4a963724.svg` [58%,74% → 60%,77%]
- equation $w_i = \frac{p(\tau_i)}{q_i(\tau_i)}$ (36pt, #ffffff) [21%,58% → 29%,66%]
- text 36pt [15%,60% → 20%,64%]: where
- text 36pt [6%,71% → 42%,75%]: {Standard Multiple Importance Sampling (s-MIS)|#c3b8ff}
- line #c3b8ff [21%,57% → 30%,67%]
- text 36pt [21%,79% → 25%,83%]: There is another option…
- **Builds:** click 1: equation $1$ — appears; with previous: line #ffffff — appears; with previous: text 36pt — appears; with previous: equation $\tau_i \sim q_i(\tau)$ — appears; click 2: image `test-22725.svg` — slides in; click 3: vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; click 4: vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; click 5: text 36pt — appears; with previous: equation $2$ — appears; with previous: line #ffffff — appears; with previous: text 36pt — appears; with previous: text 36pt — appears; with previous: equation $w_i = \frac{p(\tau_i)}{q_i(\tau_i)}$ — appears; click 6: text 36pt — fades up from dark; with previous: line #c3b8ff — com.apple.iWork.Keynote.LineDraw; click 7: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 69
_(Keynote: Lecture 11, slide 42)_
- image `test-22725.svg` [9%,20% → 45%,90%]
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- text 36pt [62%,12% → 83%,17%]: There is another option…
- image `test-22732.svg` [9%,20% → 45%,90%]
- image `test-22728.svg` [9%,20% → 45%,90%]
- image `test-22725.svg` [9%,20% → 45%,90%]
- vector icon `shape-4a963724.svg` [15%,81% → 17%,84%]
- vector icon `shape-4a963724.svg` [20%,81% → 21%,84%]
- vector icon `shape-4a963724.svg` [19%,81% → 20%,84%]
- vector icon `shape-4a963724.svg` [22%,81% → 24%,84%]
- vector icon `shape-4a963724.svg` [25%,81% → 27%,84%]
- vector icon `shape-a77812c0.svg` [37%,81% → 39%,84%]
- vector icon `shape-a77812c0.svg` [32%,81% → 34%,84%]
- vector icon `shape-a77812c0.svg` [30%,81% → 32%,84%]
- vector icon `shape-a77812c0.svg` [24%,81% → 26%,84%]
- vector icon `shape-a77812c0.svg` [20%,81% → 22%,84%]
- vector icon `shape-a77812c0.svg` [14%,81% → 16%,84%]
- vector icon `shape-4a963724.svg` [17%,81% → 19%,84%]
- text 36pt [9%,19% → 45%,23%]: {Standard Multiple Importance Sampling (s-MIS)|#c3b8ff}
- image `test-22725.svg` [53%,20% → 89%,90%]
- image `test-22728.svg` [53%,20% → 89%,90%]
- image `test-22732.svg` [53%,20% → 89%,90%]
- image `test-22728.svg` [53%,20% → 89%,90%]
- image `test-22725.svg` [53%,20% → 89%,90%]
- vector icon `shape-4a963724.svg` [59%,81% → 61%,84%]
- vector icon `shape-4a963724.svg` [64%,81% → 65%,84%]
- vector icon `shape-4a963724.svg` [62%,81% → 64%,84%]
- vector icon `shape-4a963724.svg` [66%,81% → 68%,84%]
- vector icon `shape-4a963724.svg` [69%,81% → 71%,84%]
- vector icon `shape-a77812c0.svg` [81%,81% → 83%,84%]
- vector icon `shape-a77812c0.svg` [76%,81% → 78%,84%]
- vector icon `shape-a77812c0.svg` [74%,81% → 76%,84%]
- vector icon `shape-a77812c0.svg` [68%,81% → 70%,84%]
- vector icon `shape-a77812c0.svg` [64%,81% → 66%,84%]
- vector icon `shape-a77812c0.svg` [58%,81% → 60%,84%]
- vector icon `shape-4a963724.svg` [61%,81% → 63%,84%]
- text 36pt [54%,19% → 90%,23%]: {Deterministic Mixture Multiple Importance Sampling (DM-MIS)|#80cfb9}
- equation $w_i = \frac{p(\tau_i)}{q_i(\tau_i)}$ (36pt, #ffffff) [30%,29% → 38%,37%]
- line #c3b8ff [30%,28% → 39%,37%]
- **Builds:** click 1: image `test-22732.svg` — appears; click 2: vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; then (0.2 s later): vector icon `shape-4a963724.svg` — appears; click 3: image `test-22728.svg` — appears; click 4: vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; then (0.2 s later): vector icon `shape-a77812c0.svg` — appears; click 5: image `test-22725.svg` — appears; click 6: image `test-22725.svg` — appears; click 7: image `test-22728.svg` — appears; click 8: vector icon `shape-a77812c0.svg` — appears; click 9: image `test-22732.svg` — appears; click 10: vector icon `shape-4a963724.svg` — appears; click 11: image `test-22728.svg` — appears; click 12: vector icon `shape-a77812c0.svg` — appears; click 13: image `test-22725.svg` — appears; with previous: vector icon `shape-a77812c0.svg` — appears; with previous: vector icon `shape-4a963724.svg` — appears; with previous: vector icon `shape-4a963724.svg` — appears; with previous: vector icon `shape-4a963724.svg` — appears; with previous: vector icon `shape-4a963724.svg` — appears; with previous: vector icon `shape-a77812c0.svg` — appears; with previous: vector icon `shape-4a963724.svg` — appears; with previous: vector icon `shape-a77812c0.svg` — appears; with previous: vector icon `shape-a77812c0.svg` — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 70
_(Keynote: Lecture 11, slide 43)_
- image `test-22725.svg` [9%,20% → 45%,90%]
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- text 36pt [62%,12% → 83%,17%]: There is another option…
- image `test-22732.svg` [9%,20% → 45%,90%]
- image `test-22728.svg` [9%,20% → 45%,90%]
- image `test-22725.svg` [9%,20% → 45%,90%]
- vector icon `shape-4a963724.svg` [15%,81% → 17%,84%]
- vector icon `shape-4a963724.svg` [20%,81% → 21%,84%]
- vector icon `shape-4a963724.svg` [19%,81% → 20%,84%]
- vector icon `shape-4a963724.svg` [22%,81% → 24%,84%]
- vector icon `shape-4a963724.svg` [25%,81% → 27%,84%]
- vector icon `shape-a77812c0.svg` [37%,81% → 39%,84%]
- vector icon `shape-a77812c0.svg` [32%,81% → 34%,84%]
- vector icon `shape-a77812c0.svg` [30%,81% → 32%,84%]
- vector icon `shape-a77812c0.svg` [24%,81% → 26%,84%]
- vector icon `shape-a77812c0.svg` [20%,81% → 22%,84%]
- vector icon `shape-a77812c0.svg` [14%,81% → 16%,84%]
- vector icon `shape-4a963724.svg` [17%,81% → 19%,84%]
- text 36pt [9%,19% → 45%,23%]: {Standard Multiple Importance Sampling (s-MIS)|#c3b8ff}
- image `test-22725.svg` [53%,20% → 89%,90%]
- image `test-22728.svg` [53%,20% → 89%,90%]
- image `test-22732.svg` [53%,20% → 89%,90%]
- image `test-22728.svg` [53%,20% → 89%,90%]
- image `test-22725.svg` [53%,20% → 89%,90%]
- image `test-22888.svg` [53%,20% → 89%,90%]
- vector icon `shape-b6282b21.svg` [59%,81% → 61%,84%]
- vector icon `shape-b6282b21.svg` [64%,81% → 65%,84%]
- vector icon `shape-b6282b21.svg` [62%,81% → 64%,84%]
- vector icon `shape-b6282b21.svg` [66%,81% → 68%,84%]
- vector icon `shape-b6282b21.svg` [69%,81% → 71%,84%]
- vector icon `shape-b6282b21.svg` [81%,81% → 83%,84%]
- vector icon `shape-b6282b21.svg` [76%,81% → 78%,84%]
- vector icon `shape-b6282b21.svg` [74%,81% → 76%,84%]
- vector icon `shape-b6282b21.svg` [68%,81% → 70%,84%]
- vector icon `shape-b6282b21.svg` [64%,81% → 66%,84%]
- vector icon `shape-b6282b21.svg` [58%,81% → 60%,84%]
- vector icon `shape-b6282b21.svg` [61%,81% → 63%,84%]
- text 36pt [54%,19% → 90%,23%]: {Deterministic Mixture Multiple Importance Sampling (DM-MIS)|#80cfb9}
- equation $w_i = \frac{p(\tau_i)}{q_i(\tau_i)}$ (36pt, #ffffff) [30%,29% → 38%,37%]
- line #c3b8ff [30%,28% → 39%,37%]
- equation $w_i = \frac{p(\tau_i)}{\frac{1}{m}\sum_{j=1}^m q_j(\tau_i)}$ (36pt, #ffffff) [75%,29% → 89%,39%]
- line #80cfb9 [74%,27% → 90%,40%]
- **Builds:** click 1: equation $w_i = \frac{p(\tau_i)}{\frac{1}{m}\sum_{j=1}^m q_j(\tau_i)}$ — slides in; with previous (0.5 s later): line #80cfb9 — com.apple.iWork.Keynote.LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 71
_(Keynote: Lecture 11, slide 44)_
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- text 36pt [12%,18% → 46%,23%]: Draw samples from the current proposals.
- line #ffffff [7%,17% → 11%,24%]
- equation $1$ (36pt, #ffffff) [9%,19% → 9%,22%]
- equation $\tau_i \sim q_i(\tau)$ (52pt, #ffffff) [13%,27% → 22%,31%]
- text 36pt [12%,38% → 46%,43%]: Use the samples to estimate $p_\text{fail}$.
- line #ffffff [7%,37% → 11%,44%]
- equation $2$ (36pt, #ffffff) [9%,39% → 10%,42%]
- text 36pt [13%,45% → 33%,55%]: $\hat p_\text{fail}= \frac{1}{m} \sum_{i=1}^m$$w_i$$1\{\tau_i \notin \psi\}$
- image `test-22725.svg` [50%,14% → 86%,83%]
- vector icon `shape-4a963724.svg` [56%,74% → 58%,77%]
- vector icon `shape-4a963724.svg` [61%,74% → 62%,77%]
- vector icon `shape-4a963724.svg` [59%,74% → 61%,77%]
- vector icon `shape-4a963724.svg` [63%,74% → 65%,77%]
- vector icon `shape-4a963724.svg` [66%,74% → 68%,77%]
- vector icon `shape-a77812c0.svg` [78%,74% → 80%,77%]
- vector icon `shape-a77812c0.svg` [73%,74% → 75%,77%]
- vector icon `shape-a77812c0.svg` [71%,74% → 73%,77%]
- vector icon `shape-a77812c0.svg` [65%,74% → 67%,77%]
- vector icon `shape-a77812c0.svg` [61%,74% → 63%,77%]
- vector icon `shape-a77812c0.svg` [55%,74% → 57%,77%]
- vector icon `shape-4a963724.svg` [58%,74% → 60%,77%]
- equation $w_i = \frac{p(\tau_i)}{q_i(\tau_i)}$ (36pt, #ffffff) [15%,60% → 23%,68%]
- text 36pt [9%,62% → 14%,66%]: where
- text 36pt [25%,60% → 48%,68%]: {Standard Multiple Importance Sampling (s-MIS)|#c3b8ff}
- line #c3b8ff [14%,59% → 24%,69%]
- text 36pt [18%,71% → 20%,75%]: or
- equation $w_i = \frac{p(\tau_i)}{\frac{1}{m}\sum_{j=1}^m q_j(\tau_i)}$ (36pt, #ffffff) [12%,79% → 26%,89%]
- line #80cfb9 [11%,77% → 27%,91%]
- text 36pt [29%,80% → 54%,88%]: {Deterministic Mixture Multiple Importance Sampling (DM-MIS)|#80cfb9}
- text 36pt [11%,92% → 49%,96%]: {*DM-MIS has been shown to have lower variance.|#80cfb9}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 72
_(Keynote: Lecture 11, slide 45)_
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- image `test-22963.svg` [15%,18% → 85%,86%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 73
_(Keynote: Lecture 11, slide 46)_
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- image `test-22963.svg` [37%,16% → 61%,39%]
- line #ffffff [37%,15% → 63%,40%]
- image `test-22979.svg` [26%,45% → 74%,92%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 74
_(Keynote: Lecture 11, slide 47)_
- heading (spaced caps) 36pt [29%,6% → 71%,10%]: MULTIPLE IMPORTANCE SAMPLING
- image `test-22963.svg` [16%,27% → 40%,50%]
- line #ffffff [15%,25% → 41%,75%]
- image `test-22979.svg` [16%,51% → 40%,74%]
- image `test-22991.svg` [50%,17% → 86%,83%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 75
_(Keynote: Lecture 11, slide 48)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: CROSS ENTROPY METHOD (ADAPTIVE IMPORTANCE SAMPLING)
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: MULTIPLE IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: POPULATION MONTE CARLO
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: SEQUENTIAL MONTE CARLO
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 76
_(Keynote: Lecture 11, slide 49)_
- heading (spaced caps) 36pt [32%,44% → 68%,49%]: POPULATION MONTE CARLO
- text 36pt [48%,50% → 52%,55%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 77
_(Keynote: Lecture 11, slide 50)_
- image `test-23130.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 78
_(Keynote: Lecture 11, slide 51)_
- image `test-23115.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 79
_(Keynote: Lecture 11, slide 52)_
- image `test-23139.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 80
_(Keynote: Lecture 11, slide 53)_
- image `test-23147.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 81
_(Keynote: Lecture 11, slide 54)_
- image `test-23156.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 82
_(Keynote: Lecture 11, slide 55)_
- image `test-23164.svg` [26%,21% → 68%,96%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- image `test-22979.svg` (cropped: show only 53–100% across and 0–100% down of the image) [57%,49% → 80%,96%]
- **Builds:** click 1: image `test-22979.svg` (cropped: show only 53–100% across and 0–100% d — appears

## Slide 83
_(Keynote: Lecture 11, slide 56)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!

## Slide 84
_(Keynote: Lecture 11, slide 57)_
- image `test-23130.svg` [29%,19% → 66%,86%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [35%,88% → 71%,97%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [29%,89% → 33%,96%]
- equation $1$ (36pt, #ffffff) [31%,91% → 31%,94%]
- group [68%,43% → 95%,65%]
  - rounded box (outline) [68%,43% → 95%,65%]
  - text 36pt [69%,44% → 94%,64%]: {Note: it is important for the initial population of proposals to |#000000}[[cover the space|#0072fe]]{ of possibilities as best as possible.|#000000}
- **Builds:** click 1: group — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 85
_(Keynote: Lecture 11, slide 58)_
- image `test-23130.svg` [54%,21% → 88%,81%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [9%,20% → 46%,29%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [4%,21% → 8%,28%]
- equation $1$ (36pt, #ffffff) [6%,24% → 6%,26%]
- line #ffffff [49%,20% → 49%,94%]
- text 36pt [61%,84% → 94%,88%]: Draw a sample from each proposal.
- line #ffffff [55%,82% → 60%,90%]
- equation $2$ (36pt, #ffffff) [57%,85% → 58%,87%]
- image `test-23115.svg` [54%,21% → 88%,81%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 86
_(Keynote: Lecture 11, slide 59)_
- image `test-23130.svg` [54%,21% → 88%,81%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [9%,20% → 46%,29%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [4%,21% → 8%,28%]
- equation $1$ (36pt, #ffffff) [6%,24% → 6%,26%]
- line #ffffff [49%,20% → 49%,94%]
- text 36pt [9%,35% → 42%,39%]: Draw a sample from each proposal.
- line #ffffff [4%,33% → 8%,41%]
- equation $2$ (36pt, #ffffff) [6%,36% → 6%,38%]
- image `test-23115.svg` [54%,21% → 88%,81%]
- text 36pt [58%,84% → 97%,89%]: Compute the [[importance weight|#80b9ff]] for each sample.
- line #ffffff [53%,83% → 57%,90%]
- equation $3$ (36pt, #ffffff) [55%,85% → 55%,87%]
- image `test-23147.svg` [54%,21% → 88%,81%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 87
_(Keynote: Lecture 11, slide 60)_
- image `test-23130.svg` [54%,21% → 88%,81%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [9%,20% → 46%,29%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [4%,21% → 8%,28%]
- equation $1$ (36pt, #ffffff) [6%,24% → 6%,26%]
- line #ffffff [49%,20% → 49%,94%]
- text 36pt [9%,35% → 42%,39%]: Draw a sample from each proposal.
- line #ffffff [4%,33% → 8%,41%]
- equation $2$ (36pt, #ffffff) [6%,36% → 6%,38%]
- image `test-23115.svg` [54%,21% → 88%,81%]
- text 36pt [9%,47% → 49%,52%]: Compute the [[importance weight|#80b9ff]] for each sample.
- line #ffffff [4%,45% → 8%,53%]
- equation $3$ (36pt, #ffffff) [6%,48% → 6%,50%]
- image `test-23147.svg` [54%,21% → 88%,81%]
- text 36pt [59%,84% → 98%,89%]: [[Resample|#80b9ff]] based on the importance weights.
- line #ffffff [54%,83% → 58%,90%]
- equation $4$ (36pt, #ffffff) [55%,86% → 56%,88%]
- image `test-23156.svg` [54%,21% → 88%,81%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 88
_(Keynote: Lecture 11, slide 61)_
- image `test-23130.svg` [54%,21% → 88%,81%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [9%,20% → 46%,29%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [4%,21% → 8%,28%]
- equation $1$ (36pt, #ffffff) [6%,24% → 6%,26%]
- line #ffffff [49%,20% → 49%,94%]
- text 36pt [9%,35% → 42%,39%]: Draw a sample from each proposal.
- line #ffffff [4%,33% → 8%,41%]
- equation $2$ (36pt, #ffffff) [6%,36% → 6%,38%]
- image `test-23115.svg` [54%,21% → 88%,81%]
- text 36pt [9%,47% → 49%,52%]: Compute the [[importance weight|#80b9ff]] for each sample.
- line #ffffff [4%,45% → 8%,53%]
- equation $3$ (36pt, #ffffff) [6%,48% → 6%,50%]
- image `test-23147.svg` [54%,21% → 88%,81%]
- text 36pt [9%,59% → 49%,64%]: [[Resample|#80b9ff]] based on the importance weights.
- line #ffffff [4%,58% → 8%,65%]
- equation $4$ (36pt, #ffffff) [6%,60% → 7%,63%]
- image `test-23156.svg` [54%,21% → 88%,81%]
- text 36pt [62%,83% → 94%,91%]: Create [[new|#80b9ff]] proposal distributions centered at the samples.
- line #ffffff [56%,83% → 61%,91%]
- equation $5$ (36pt, #ffffff) [58%,86% → 59%,88%]
- image `test-23164.svg` [54%,21% → 88%,81%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 89
_(Keynote: Lecture 11, slide 62)_
- image `test-23130.svg` [54%,21% → 88%,81%]
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: POPULATION MONTE CARLO
- text 36pt [29%,12% → 71%,16%]: Let’s adapt a whole [[population|#80b9ff]] of proposal distributions!
- text 36pt [9%,20% → 46%,29%]: Select an [[initial population|#80b9ff]] of proposals spread out over the space of possible trajectories.
- line #ffffff [4%,21% → 8%,28%]
- equation $1$ (36pt, #ffffff) [6%,24% → 6%,26%]
- line #ffffff [49%,20% → 49%,94%]
- text 36pt [9%,35% → 42%,39%]: Draw a sample from each proposal.
- line #ffffff [4%,33% → 8%,41%]
- equation $2$ (36pt, #ffffff) [6%,36% → 6%,38%]
- image `test-23115.svg` [54%,21% → 88%,81%]
- text 36pt [9%,47% → 49%,52%]: Compute the [[importance weight|#80b9ff]] for each sample.
- line #ffffff [4%,45% → 8%,53%]
- equation $3$ (36pt, #ffffff) [6%,48% → 6%,50%]
- image `test-23147.svg` [54%,21% → 88%,81%]
- text 36pt [9%,59% → 49%,64%]: [[Resample|#80b9ff]] based on the importance weights.
- line #ffffff [4%,58% → 8%,65%]
- equation $4$ (36pt, #ffffff) [6%,60% → 7%,63%]
- image `test-23156.svg` [54%,21% → 88%,81%]
- text 36pt [9%,70% → 42%,78%]: Create [[new|#80b9ff]] proposal distributions centered at the samples.
- line #ffffff [4%,70% → 8%,78%]
- equation $5$ (36pt, #ffffff) [6%,73% → 6%,75%]
- image `test-23164.svg` [54%,21% → 88%,81%]
- rounded box (outline) [19%,81% → 28%,88%]
- text 36pt [20%,82% → 27%,87%]: REPEAT!
- text 36pt [62%,51% → 86%,63%]: {Perform multiple importance sampling with the final proposals.|#c0c0c0}
- **Builds:** click 1: text 36pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 90
_(Keynote: Lecture 11, slide 63)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: CROSS ENTROPY METHOD (ADAPTIVE IMPORTANCE SAMPLING)
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: MULTIPLE IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: POPULATION MONTE CARLO
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: SEQUENTIAL MONTE CARLO
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 91
_(Keynote: Lecture 11, slide 64)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-23382.svg` [31%,21% → 66%,82%]
- text 36pt [48%,13% → 52%,18%]: We want to move samples from the [[nominal distribution|#80b9ff]] {to the |#000000}[[failure distribution.|#000000]]
- vector icon `shape-aa0cab1e.svg` [47%,45% → 49%,47%]
- vector icon `shape-aa0cab1e.svg` [49%,49% → 50%,51%]
- vector icon `shape-aa0cab1e.svg` [49%,45% → 50%,47%]
- vector icon `shape-aa0cab1e.svg` [46%,49% → 48%,51%]
- vector icon `shape-aa0cab1e.svg` [47%,54% → 49%,56%]
- vector icon `shape-aa0cab1e.svg` [50%,54% → 51%,56%]
- vector icon `shape-aa0cab1e.svg` [48%,51% → 49%,53%]
- vector icon `shape-aa0cab1e.svg` [51%,49% → 52%,51%]
- vector icon `shape-aa0cab1e.svg` [50%,50% → 51%,52%]
- vector icon `shape-aa0cab1e.svg` [53%,51% → 55%,53%]
- vector icon `shape-aa0cab1e.svg` [53%,45% → 54%,47%]
- vector icon `shape-aa0cab1e.svg` [44%,51% → 45%,53%]
- vector icon `shape-aa0cab1e.svg` [42%,44% → 43%,46%]
- vector icon `shape-aa0cab1e.svg` [45%,43% → 47%,45%]
- vector icon `shape-aa0cab1e.svg` [46%,33% → 48%,35%]
- vector icon `shape-aa0cab1e.svg` [49%,39% → 50%,42%]
- vector icon `shape-aa0cab1e.svg` [50%,43% → 52%,45%]
- vector icon `shape-aa0cab1e.svg` [53%,37% → 54%,39%]
- vector icon `shape-aa0cab1e.svg` [58%,47% → 60%,49%]
- vector icon `shape-aa0cab1e.svg` [53%,55% → 54%,57%]
- vector icon `shape-aa0cab1e.svg` [49%,57% → 50%,59%]
- vector icon `shape-aa0cab1e.svg` [45%,59% → 46%,61%]
- vector icon `shape-aa0cab1e.svg` [55%,58% → 56%,60%]
- vector icon `shape-aa0cab1e.svg` [49%,60% → 51%,62%]
- vector icon `shape-aa0cab1e.svg` [47%,69% → 49%,71%]
- vector icon `shape-aa0cab1e.svg` [41%,55% → 42%,57%]
- vector icon `shape-aa0cab1e.svg` [41%,48% → 43%,50%]
- vector icon `shape-aa0cab1e.svg` [45%,47% → 47%,49%]
- vector icon `shape-aa0cab1e.svg` [45%,54% → 47%,56%]
- vector icon `shape-aa0cab1e.svg` [46%,52% → 48%,54%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 92
_(Keynote: Lecture 11, slide 65)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-23382.svg` [31%,21% → 66%,82%]
- text 36pt [48%,13% → 52%,18%]: We want to move samples from the [[nominal distribution|#80b9ff]] to the [[failure distribution|#fab0ae]].
- vector icon `shape-af5dfe6a.svg` [55%,38% → 56%,40%]
- vector icon `shape-af5dfe6a.svg` [56%,33% → 57%,35%]
- vector icon `shape-af5dfe6a.svg` [56%,29% → 57%,31%]
- vector icon `shape-af5dfe6a.svg` [56%,32% → 57%,34%]
- vector icon `shape-af5dfe6a.svg` [56%,36% → 58%,38%]
- vector icon `shape-af5dfe6a.svg` [56%,35% → 57%,37%]
- vector icon `shape-af5dfe6a.svg` [55%,29% → 56%,31%]
- vector icon `shape-af5dfe6a.svg` [60%,38% → 61%,40%]
- vector icon `shape-af5dfe6a.svg` [58%,27% → 59%,29%]
- vector icon `shape-af5dfe6a.svg` [57%,34% → 58%,36%]
- vector icon `shape-af5dfe6a.svg` [57%,38% → 58%,40%]
- vector icon `shape-af5dfe6a.svg` [55%,35% → 56%,37%]
- vector icon `shape-af5dfe6a.svg` [55%,31% → 56%,33%]
- vector icon `shape-af5dfe6a.svg` [57%,30% → 58%,33%]
- vector icon `shape-af5dfe6a.svg` [59%,32% → 60%,35%]
- vector icon `shape-af5dfe6a.svg` [58%,38% → 59%,40%]
- vector icon `shape-af5dfe6a.svg` [58%,37% → 60%,39%]
- vector icon `shape-af5dfe6a.svg` [57%,33% → 58%,35%]
- vector icon `shape-af5dfe6a.svg` [60%,36% → 61%,38%]
- vector icon `shape-af5dfe6a.svg` [55%,33% → 56%,35%]
- vector icon `shape-af5dfe6a.svg` [56%,31% → 57%,33%]
- vector icon `shape-af5dfe6a.svg` [56%,37% → 57%,39%]
- vector icon `shape-af5dfe6a.svg` [56%,35% → 57%,37%]
- vector icon `shape-af5dfe6a.svg` [55%,36% → 56%,39%]
- vector icon `shape-af5dfe6a.svg` [56%,34% → 57%,36%]
- vector icon `shape-af5dfe6a.svg` [56%,39% → 57%,41%]
- vector icon `shape-af5dfe6a.svg` [58%,35% → 59%,37%]
- vector icon `shape-af5dfe6a.svg` [57%,37% → 58%,39%]
- vector icon `shape-af5dfe6a.svg` [56%,37% → 57%,39%]
- vector icon `shape-af5dfe6a.svg` [55%,36% → 56%,38%]
- text 36pt [48%,86% → 52%,90%]: It turns out we can estimate the probability of failure based on the [[path|#c3b8ff]] that the samples take.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 93
_(Keynote: Lecture 11, slide 66)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-23382.svg` [31%,33% → 66%,95%]
- text 36pt [48%,13% → 52%,18%]: We want to move samples from the [[nominal distribution|#80b9ff]] to the [[failure distribution|#fab0ae]].
- vector icon `shape-af5dfe6a.svg` [55%,51% → 56%,53%]
- vector icon `shape-af5dfe6a.svg` [56%,45% → 57%,48%]
- vector icon `shape-af5dfe6a.svg` [56%,42% → 57%,44%]
- vector icon `shape-af5dfe6a.svg` [56%,45% → 57%,47%]
- vector icon `shape-af5dfe6a.svg` [56%,49% → 58%,51%]
- vector icon `shape-af5dfe6a.svg` [56%,48% → 57%,50%]
- vector icon `shape-af5dfe6a.svg` [55%,42% → 56%,44%]
- vector icon `shape-af5dfe6a.svg` [60%,50% → 61%,53%]
- vector icon `shape-af5dfe6a.svg` [58%,39% → 59%,42%]
- vector icon `shape-af5dfe6a.svg` [57%,47% → 58%,49%]
- vector icon `shape-af5dfe6a.svg` [57%,50% → 58%,53%]
- vector icon `shape-af5dfe6a.svg` [55%,47% → 56%,50%]
- vector icon `shape-af5dfe6a.svg` [55%,44% → 56%,46%]
- vector icon `shape-af5dfe6a.svg` [57%,43% → 58%,45%]
- vector icon `shape-af5dfe6a.svg` [59%,45% → 60%,47%]
- vector icon `shape-af5dfe6a.svg` [58%,51% → 59%,53%]
- vector icon `shape-af5dfe6a.svg` [58%,50% → 60%,52%]
- vector icon `shape-af5dfe6a.svg` [57%,46% → 58%,48%]
- vector icon `shape-af5dfe6a.svg` [60%,48% → 61%,50%]
- vector icon `shape-af5dfe6a.svg` [55%,46% → 56%,48%]
- vector icon `shape-af5dfe6a.svg` [56%,44% → 57%,46%]
- vector icon `shape-af5dfe6a.svg` [56%,50% → 57%,52%]
- vector icon `shape-af5dfe6a.svg` [56%,48% → 57%,50%]
- vector icon `shape-af5dfe6a.svg` [55%,49% → 56%,51%]
- vector icon `shape-af5dfe6a.svg` [56%,46% → 57%,49%]
- vector icon `shape-af5dfe6a.svg` [56%,51% → 57%,53%]
- vector icon `shape-af5dfe6a.svg` [58%,48% → 59%,50%]
- vector icon `shape-af5dfe6a.svg` [57%,50% → 58%,52%]
- vector icon `shape-af5dfe6a.svg` [56%,49% → 57%,52%]
- vector icon `shape-af5dfe6a.svg` [55%,48% → 56%,50%]
- text 36pt [20%,19% → 80%,24%]: We typically move the samples through a series of [[intermediate distributions|#c3b8ff]].
- text 36pt [27%,26% → 64%,30%]: How can we get these [[intermediate distributions|#c3b8ff]]?
- text 36pt [64%,26% → 76%,30%]: SMOOTHING!
- text on a #80b9ff filled box 32pt [72%,38% → 91%,46%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: text 36pt — slides in; click 2: text 36pt — slides in; click 3: text on a #80b9ff filled box 32pt — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 94
_(Keynote: Lecture 11, slide 67)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- text 36pt [48%,13% → 52%,18%]: We want to move samples from the [[nominal distribution|#80b9ff]] to the [[failure distribution|#fab0ae]].
- text 36pt [20%,19% → 80%,24%]: We typically move the samples through a series of [[intermediate distributions|#c3b8ff]].
- text 36pt [27%,26% → 64%,30%]: How can we get these [[intermediate distributions|#c3b8ff]]?
- text 36pt [64%,26% → 76%,30%]: SMOOTHING!
- text 36pt [50%,81% → 90%,89%]: We can also use the [[thresholding technique|#80b9ff]] similar to what we did for the cross entropy method.
- image `test-23618.svg` [14%,37% → 83%,78%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 95
_(Keynote: Lecture 11, slide 68)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- text 36pt [48%,13% → 52%,18%]: We want to move samples from the [[nominal distribution|#80b9ff]] to the [[failure distribution|#fab0ae]].
- text 36pt [20%,19% → 80%,24%]: We typically move the samples through a series of [[intermediate distributions|#c3b8ff]].
- text 36pt [113%,26% → 150%,30%]: How can we get these [[intermediate distributions|#c3b8ff]]?
- text 36pt [150%,26% → 162%,30%]: SMOOTHING!
- text 36pt [136%,81% → 176%,89%]: We can also use the [[thresholding technique|#80b9ff]] similar to what we did for the cross entropy method.
- image `test-23618.svg` [100%,37% → 169%,78%]
- text 36pt [24%,25% → 71%,30%]: How do we [[move samples|#c3b8ff]] from one distribution to the next?
- text 36pt [71%,26% → 78%,30%]: MCMC!
- **Builds:** click 1: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 96
_(Keynote: Lecture 11, slide 69)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-24193.svg` [29%,18% → 71%,92%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 97
_(Keynote: Lecture 11, slide 70)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-24193.svg` [29%,18% → 71%,92%]
- image `test-24199.svg` [29%,18% → 71%,92%]

## Slide 98
_(Keynote: Lecture 11, slide 71)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `g01-23759.svg` [29%,18% → 71%,92%]
- image `g02-23767.svg` [29%,18% → 71%,92%]
- image `g03-23758.svg` [29%,18% → 71%,92%]
- image `g04-23760.svg` [29%,18% → 71%,92%]
- image `g05-23770.svg` [29%,18% → 71%,92%]
- image `g06-23764.svg` [29%,18% → 71%,92%]
- image `g07-23762.svg` [29%,18% → 71%,92%]
- image `g08-23792.svg` [29%,18% → 71%,92%]
- image `g09-23772.svg` [29%,18% → 71%,92%]
- image `g10-23771.svg` [29%,18% → 71%,92%]
- image `g11-23777.svg` [29%,18% → 71%,92%]
- image `g12-23812.svg` [29%,18% → 71%,92%]
- image `g13-23813.svg` [29%,18% → 71%,92%]
- image `g14-23816.svg` [29%,18% → 71%,92%]
- image `g15-23808.svg` [29%,18% → 71%,92%]
- image `g16-23806.svg` [29%,18% → 71%,92%]
- image `g17-23775.svg` [29%,18% → 71%,92%]
- image `g18-23779.svg` [29%,18% → 71%,92%]
- image `g20-23794.svg` [29%,18% → 71%,92%]
- image `g21-23801.svg` [29%,18% → 71%,92%]
- image `g22-23839.svg` [29%,18% → 71%,92%]
- image `g23-23841.svg` [29%,18% → 71%,92%]
- image `g24-23823.svg` [29%,18% → 71%,92%]
- image `g25-23814.svg` [29%,18% → 71%,92%]
- image `g26-23817.svg` [29%,18% → 71%,92%]
- image `g27-23803.svg` [29%,18% → 71%,92%]
- image `g28-23802.svg` [29%,18% → 71%,92%]
- image `g29-23790.svg` [29%,18% → 71%,92%]
- image `g30-23781.svg` [29%,18% → 71%,92%]
- image `g31-23783.svg` [29%,18% → 71%,92%]
- image `g32-23782.svg` [29%,18% → 71%,92%]
- image `g33-23810.svg` [29%,18% → 71%,92%]
- image `g34-23836.svg` [29%,18% → 71%,92%]
- image `g35-23805.svg` [29%,18% → 71%,92%]
- image `g36-23804.svg` [29%,18% → 71%,92%]
- image `g38-23840.svg` [29%,18% → 71%,92%]
- image `g39-23819.svg` [29%,18% → 71%,92%]
- image `g40-23795.svg` [29%,18% → 71%,92%]
- image `g41-23793.svg` [29%,18% → 71%,92%]
- image `g42-23824.svg` [29%,18% → 71%,92%]
- image `g43-23815.svg` [29%,18% → 71%,92%]
- image `g44-23809.svg` [29%,18% → 71%,92%]
- image `g45-23807.svg` [29%,18% → 71%,92%]
- image `g46-23811.svg` [29%,18% → 71%,92%]
- image `g47-23821.svg` [29%,18% → 71%,92%]
- image `g48-23820.svg` [29%,18% → 71%,92%]
- image `g49-23818.svg` [29%,18% → 71%,92%]
- image `g50-23791.svg` [29%,18% → 71%,92%]
- image `g51-23785.svg` [29%,18% → 71%,92%]
- **Builds:** click 1: image `g02-23767.svg` — appears; then (0.05 s later): image `g03-23758.svg` — appears; then (0.05 s later): image `g04-23760.svg` — appears; then (0.05 s later): image `g05-23770.svg` — appears; then (0.05 s later): image `g06-23764.svg` — appears; then (0.05 s later): image `g07-23762.svg` — appears; then (0.05 s later): image `g08-23792.svg` — appears; then (0.05 s later): image `g09-23772.svg` — appears; then (0.05 s later): image `g10-23771.svg` — appears; then (0.05 s later): image `g11-23777.svg` — appears; then (0.05 s later): image `g12-23812.svg` — appears; then (0.05 s later): image `g13-23813.svg` — appears; then (0.05 s later): image `g14-23816.svg` — appears; then (0.05 s later): image `g15-23808.svg` — appears; then (0.05 s later): image `g16-23806.svg` — appears; then (0.05 s later): image `g17-23775.svg` — appears; then (0.05 s later): image `g18-23779.svg` — appears; then (0.05 s later): image `g20-23794.svg` — appears; then (0.05 s later): image `g21-23801.svg` — appears; then (0.05 s later): image `g22-23839.svg` — appears; then (0.05 s later): image `g23-23841.svg` — appears; then (0.05 s later): image `g24-23823.svg` — appears; then (0.05 s later): image `g25-23814.svg` — appears; then (0.05 s later): image `g26-23817.svg` — appears; then (0.05 s later): image `g27-23803.svg` — appears; then (0.05 s later): image `g28-23802.svg` — appears; then (0.05 s later): image `g29-23790.svg` — appears; then (0.05 s later): image `g30-23781.svg` — appears; then (0.05 s later): image `g31-23783.svg` — appears; then (0.05 s later): image `g32-23782.svg` — appears; then (0.05 s later): image `g33-23810.svg` — appears; then (0.05 s later): image `g34-23836.svg` — appears; then (0.05 s later): image `g35-23805.svg` — appears; then (0.05 s later): image `g36-23804.svg` — appears; then (0.05 s later): image `g38-23840.svg` — appears; then (0.05 s later): image `g39-23819.svg` — appears; then (0.05 s later): image `g40-23795.svg` — appears; then (0.05 s later): image `g41-23793.svg` — appears; then (0.05 s later): image `g42-23824.svg` — appears; then (0.05 s later): image `g43-23815.svg` — appears; then (0.05 s later): image `g44-23809.svg` — appears; then (0.05 s later): image `g45-23807.svg` — appears; then (0.05 s later): image `g46-23811.svg` — appears; then (0.05 s later): image `g47-23821.svg` — appears; then (0.05 s later): image `g48-23820.svg` — appears; then (0.05 s later): image `g49-23818.svg` — appears; then (0.05 s later): image `g50-23791.svg` — appears; then (0.05 s later): image `g51-23785.svg` — appears

## Slide 99
_(Keynote: Lecture 11, slide 72)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `g01-23872.svg` [29%,18% → 71%,92%]
- image `g02-23871.svg` [29%,18% → 71%,92%]
- image `g03-23873.svg` [29%,18% → 71%,92%]
- image `g04-23870.svg` [29%,18% → 71%,92%]
- image `g05-23878.svg` [29%,18% → 71%,92%]
- image `g06-23883.svg` [29%,18% → 71%,92%]
- image `g07-23877.svg` [29%,18% → 71%,92%]
- image `g08-23882.svg` [29%,18% → 71%,92%]
- image `g09-23940.svg` [29%,18% → 71%,92%]
- image `g10-23939.svg` [29%,18% → 71%,92%]
- image `g11-23945.svg` [29%,18% → 71%,92%]
- image `g12-23936.svg` [29%,18% → 71%,92%]
- image `g13-23933.svg` [29%,18% → 71%,92%]
- image `g14-23893.svg` [29%,18% → 71%,92%]
- image `g15-23891.svg` [29%,18% → 71%,92%]
- image `g16-23894.svg` [29%,18% → 71%,92%]
- image `g17-23948.svg` [29%,18% → 71%,92%]
- image `g18-23947.svg` [29%,18% → 71%,92%]
- image `g19-23949.svg` [29%,18% → 71%,92%]
- image `g20-23942.svg` [29%,18% → 71%,92%]
- image `g21-23941.svg` [29%,18% → 71%,92%]
- image `g22-23946.svg` [29%,18% → 71%,92%]
- image `g23-23943.svg` [29%,18% → 71%,92%]
- image `g24-23931.svg` [29%,18% → 71%,92%]
- image `g25-23938.svg` [29%,18% → 71%,92%]
- image `g26-23910.svg` [29%,18% → 71%,92%]
- image `g27-23899.svg` [29%,18% → 71%,92%]
- image `g28-23900.svg` [29%,18% → 71%,92%]
- image `g29-23912.svg` [29%,18% → 71%,92%]
- image `g30-23888.svg` [29%,18% → 71%,92%]
- image `g31-23935.svg` [29%,18% → 71%,92%]
- image `g32-23932.svg` [29%,18% → 71%,92%]
- image `g33-23885.svg` [29%,18% → 71%,92%]
- image `g34-23887.svg` [29%,18% → 71%,92%]
- image `g35-23927.svg` [29%,18% → 71%,92%]
- image `g36-23924.svg` [29%,18% → 71%,92%]
- image `g37-23923.svg` [29%,18% → 71%,92%]
- image `g38-23917.svg` [29%,18% → 71%,92%]
- image `g39-23918.svg` [29%,18% → 71%,92%]
- image `g40-23911.svg` [29%,18% → 71%,92%]
- image `g41-23903.svg` [29%,18% → 71%,92%]
- image `g42-23905.svg` [29%,18% → 71%,92%]
- image `g43-23902.svg` [29%,18% → 71%,92%]
- image `g44-23925.svg` [29%,18% → 71%,92%]
- image `g45-23920.svg` [29%,18% → 71%,92%]
- image `g46-23915.svg` [29%,18% → 71%,92%]
- image `g47-23913.svg` [29%,18% → 71%,92%]
- image `g48-23934.svg` [29%,18% → 71%,92%]
- image `g49-23922.svg` [29%,18% → 71%,92%]
- image `g50-23901.svg` [29%,18% → 71%,92%]
- image `g51-23898.svg` [29%,18% → 71%,92%]
- **Builds:** click 1: image `g02-23871.svg` — appears; then (0.05 s later): image `g03-23873.svg` — appears; then (0.05 s later): image `g04-23870.svg` — appears; then (0.05 s later): image `g05-23878.svg` — appears; then (0.05 s later): image `g06-23883.svg` — appears; then (0.05 s later): image `g07-23877.svg` — appears; then (0.05 s later): image `g08-23882.svg` — appears; then (0.05 s later): image `g09-23940.svg` — appears; then (0.05 s later): image `g10-23939.svg` — appears; then (0.05 s later): image `g11-23945.svg` — appears; then (0.05 s later): image `g12-23936.svg` — appears; then (0.05 s later): image `g13-23933.svg` — appears; then (0.05 s later): image `g14-23893.svg` — appears; then (0.05 s later): image `g15-23891.svg` — appears; then (0.05 s later): image `g16-23894.svg` — appears; then (0.05 s later): image `g17-23948.svg` — appears; then (0.05 s later): image `g18-23947.svg` — appears; then (0.05 s later): image `g19-23949.svg` — appears; then (0.05 s later): image `g20-23942.svg` — appears; then (0.05 s later): image `g21-23941.svg` — appears; then (0.05 s later): image `g22-23946.svg` — appears; then (0.05 s later): image `g23-23943.svg` — appears; then (0.05 s later): image `g24-23931.svg` — appears; then (0.05 s later): image `g25-23938.svg` — appears; then (0.05 s later): image `g26-23910.svg` — appears; then (0.05 s later): image `g27-23899.svg` — appears; then (0.05 s later): image `g28-23900.svg` — appears; then (0.05 s later): image `g29-23912.svg` — appears; then (0.05 s later): image `g30-23888.svg` — appears; then (0.05 s later): image `g31-23935.svg` — appears; then (0.05 s later): image `g32-23932.svg` — appears; then (0.05 s later): image `g33-23885.svg` — appears; then (0.05 s later): image `g34-23887.svg` — appears; then (0.05 s later): image `g35-23927.svg` — appears; then (0.05 s later): image `g36-23924.svg` — appears; then (0.05 s later): image `g37-23923.svg` — appears; then (0.05 s later): image `g38-23917.svg` — appears; then (0.05 s later): image `g39-23918.svg` — appears; then (0.05 s later): image `g40-23911.svg` — appears; then (0.05 s later): image `g41-23903.svg` — appears; then (0.05 s later): image `g42-23905.svg` — appears; then (0.05 s later): image `g43-23902.svg` — appears; then (0.05 s later): image `g44-23925.svg` — appears; then (0.05 s later): image `g45-23920.svg` — appears; then (0.05 s later): image `g46-23915.svg` — appears; then (0.05 s later): image `g47-23913.svg` — appears; then (0.05 s later): image `g48-23934.svg` — appears; then (0.05 s later): image `g49-23922.svg` — appears; then (0.05 s later): image `g50-23901.svg` — appears; then (0.05 s later): image `g51-23898.svg` — appears

## Slide 100
_(Keynote: Lecture 11, slide 73)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `g01-24084.svg` [29%,18% → 71%,92%]
- image `g02-24085.svg` [29%,18% → 71%,92%]
- image `g03-24088.svg` [29%,18% → 71%,92%]
- image `g04-24086.svg` [29%,18% → 71%,92%]
- image `g05-24087.svg` [29%,18% → 71%,92%]
- image `g06-24122.svg` [29%,18% → 71%,92%]
- image `g07-24119.svg` [29%,18% → 71%,92%]
- image `g08-24093.svg` [29%,18% → 71%,92%]
- image `g09-24090.svg` [29%,18% → 71%,92%]
- image `g10-24089.svg` [29%,18% → 71%,92%]
- image `g11-24092.svg` [29%,18% → 71%,92%]
- image `g12-24091.svg` [29%,18% → 71%,92%]
- image `g13-24151.svg` [29%,18% → 71%,92%]
- image `g14-24141.svg` [29%,18% → 71%,92%]
- image `g15-24149.svg` [29%,18% → 71%,92%]
- image `g16-24145.svg` [29%,18% → 71%,92%]
- image `g17-24134.svg` [29%,18% → 71%,92%]
- image `g18-24135.svg` [29%,18% → 71%,92%]
- image `g19-24128.svg` [29%,18% → 71%,92%]
- image `g20-24148.svg` [29%,18% → 71%,92%]
- image `g21-24137.svg` [29%,18% → 71%,92%]
- image `g22-24095.svg` [29%,18% → 71%,92%]
- image `g23-24096.svg` [29%,18% → 71%,92%]
- image `g24-24131.svg` [29%,18% → 71%,92%]
- image `g25-24124.svg` [29%,18% → 71%,92%]
- image `g26-24121.svg` [29%,18% → 71%,92%]
- image `g27-24118.svg` [29%,18% → 71%,92%]
- image `g28-24102.svg` [29%,18% → 71%,92%]
- image `g30-24094.svg` [29%,18% → 71%,92%]
- image `g31-24101.svg` [29%,18% → 71%,92%]
- image `g32-24098.svg` [29%,18% → 71%,92%]
- image `g33-24155.svg` [29%,18% → 71%,92%]
- image `g34-24152.svg` [29%,18% → 71%,92%]
- image `g35-24142.svg` [29%,18% → 71%,92%]
- image `g36-24147.svg` [29%,18% → 71%,92%]
- image `g37-24154.svg` [29%,18% → 71%,92%]
- image `g38-24156.svg` [29%,18% → 71%,92%]
- image `g39-24150.svg` [29%,18% → 71%,92%]
- image `g40-24153.svg` [29%,18% → 71%,92%]
- image `g41-24157.svg` [29%,18% → 71%,92%]
- image `g42-24132.svg` [29%,18% → 71%,92%]
- image `g43-24133.svg` [29%,18% → 71%,92%]
- image `g44-24117.svg` [29%,18% → 71%,92%]
- image `g45-24115.svg` [29%,18% → 71%,92%]
- image `g46-24120.svg` [29%,18% → 71%,92%]
- image `g47-24111.svg` [29%,18% → 71%,92%]
- image `g48-24136.svg` [29%,18% → 71%,92%]
- image `g49-24123.svg` [29%,18% → 71%,92%]
- image `g50-24110.svg` [29%,18% → 71%,92%]
- image `g51-24099.svg` [29%,18% → 71%,92%]
- **Builds:** click 1: image `g02-24085.svg` — appears; then (0.05 s later): image `g03-24088.svg` — appears; then (0.05 s later): image `g04-24086.svg` — appears; then (0.05 s later): image `g05-24087.svg` — appears; then (0.05 s later): image `g06-24122.svg` — appears; then (0.05 s later): image `g07-24119.svg` — appears; then (0.05 s later): image `g08-24093.svg` — appears; then (0.05 s later): image `g09-24090.svg` — appears; then (0.05 s later): image `g10-24089.svg` — appears; then (0.05 s later): image `g11-24092.svg` — appears; then (0.05 s later): image `g12-24091.svg` — appears; then (0.05 s later): image `g13-24151.svg` — appears; then (0.05 s later): image `g14-24141.svg` — appears; then (0.05 s later): image `g15-24149.svg` — appears; then (0.05 s later): image `g16-24145.svg` — appears; then (0.05 s later): image `g17-24134.svg` — appears; then (0.05 s later): image `g18-24135.svg` — appears; then (0.05 s later): image `g19-24128.svg` — appears; then (0.05 s later): image `g20-24148.svg` — appears; then (0.05 s later): image `g21-24137.svg` — appears; then (0.05 s later): image `g22-24095.svg` — appears; then (0.05 s later): image `g23-24096.svg` — appears; then (0.05 s later): image `g24-24131.svg` — appears; then (0.05 s later): image `g25-24124.svg` — appears; then (0.05 s later): image `g26-24121.svg` — appears; then (0.05 s later): image `g27-24118.svg` — appears; then (0.05 s later): image `g28-24102.svg` — appears; then (0.05 s later): image `g30-24094.svg` — appears; then (0.05 s later): image `g31-24101.svg` — appears; then (0.05 s later): image `g32-24098.svg` — appears; then (0.05 s later): image `g33-24155.svg` — appears; then (0.05 s later): image `g34-24152.svg` — appears; then (0.05 s later): image `g35-24142.svg` — appears; then (0.05 s later): image `g36-24147.svg` — appears; then (0.05 s later): image `g37-24154.svg` — appears; then (0.05 s later): image `g38-24156.svg` — appears; then (0.05 s later): image `g39-24150.svg` — appears; then (0.05 s later): image `g40-24153.svg` — appears; then (0.05 s later): image `g41-24157.svg` — appears; then (0.05 s later): image `g42-24132.svg` — appears; then (0.05 s later): image `g43-24133.svg` — appears; then (0.05 s later): image `g44-24117.svg` — appears; then (0.05 s later): image `g45-24115.svg` — appears; then (0.05 s later): image `g46-24120.svg` — appears; then (0.05 s later): image `g47-24111.svg` — appears; then (0.05 s later): image `g48-24136.svg` — appears; then (0.05 s later): image `g49-24123.svg` — appears; then (0.05 s later): image `g50-24110.svg` — appears; then (0.05 s later): image `g51-24099.svg` — appears

## Slide 101
_(Keynote: Lecture 11, slide 74)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- image `test-24184.svg` [29%,18% → 71%,92%]

## Slide 102
_(Keynote: Lecture 11, slide 75)_
- rounded box (outline) [17%,13% → 84%,25%]
- text 100pt [20%,13% → 26%,26%]: 🤔
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- text 36pt [27%,17% → 79%,22%]: Okay but how do we estimate the probability of failure from all this?
- image `test-24193.svg` [33%,34% → 65%,92%]
- equation $g_1$ (29pt, #80b9ff) [45%,49% → 46%,51%]
- equation $g_2$ (29pt, #c3b8ff) [52%,44% → 53%,46%]
- equation $g_3$ (29pt, #b787a1) [56%,41% → 57%,43%]
- equation $g_4$ (29pt, #fab0ae) [59%,38% → 60%,40%]
- equation $g_5$ (29pt, #fab0ae) [63%,33% → 64%,35%]
- **Builds:** click 1: equation $g_5$ — appears; with previous: equation $g_4$ — appears; with previous: equation $g_3$ — appears; with previous: equation $g_2$ — appears; with previous: equation $g_1$ — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 103
_(Keynote: Lecture 11, slide 76)_
- line #ffffff [55%,69% → 80%,86%]
- rounded box (outline) [17%,13% → 84%,25%]
- text 100pt [20%,13% → 26%,26%]: 🤔
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- text 36pt [27%,17% → 79%,22%]: Okay but how do we estimate the probability of failure from all this?
- image `test-24193.svg` [10%,34% → 43%,92%]
- equation $g_1$ (29pt, #80b9ff) [22%,49% → 24%,51%]
- equation $g_2$ (29pt, #c3b8ff) [30%,44% → 31%,46%]
- equation $g_3$ (29pt, #b787a1) [33%,41% → 34%,43%]
- equation $g_4$ (29pt, #fab0ae) [36%,38% → 38%,40%]
- equation $g_5$ (29pt, #fab0ae) [40%,33% → 41%,35%]
- text 36pt [52%,35% → 82%,40%]: Keep track of a weight for each sample:
- equation $w_i^{(\ell)} = w_i^{(\ell-1)} \frac{\bar g_{\ell+1}(\tau_i^{(\ell)})}{\bar g_{\ell}(\tau_i^{(\ell)})}$ (52pt, #ffffff) [54%,43% → 79%,57%]
- text 36pt [52%,61% → 84%,66%]: Average the weights at the final iteration:
- equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m w_i^{(n-1)}$ (52pt, #ffffff) [56%,71% → 78%,84%]
- **Builds:** click 1: text 36pt — appears; with previous: equation $\hat p_\text{fail} = \frac{1}{m} \sum_{i=1}^m w_i^{(n-1)}$ — appears; click 2: line #ffffff — com.apple.iWork.Keynote.LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 104
_(Keynote: Lecture 11, slide 77)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- text 36pt [9%,16% → 31%,20%]: A few other notes on SMC:
- group [11%,26% → 89%,54%]
  - rounded box (outline) [11%,26% → 89%,54%]
  - text 36pt [14%,28% → 87%,33%]: It is common to also do a [[resampling step|#80b9ff]] similar to population Monte Carlo for each transition.
  - group [41%,35% → 59%,45%]
    - rounded box (outline) [41%,35% → 59%,45%]
    - text 36pt [48%,38% → 52%,42%]: {Example 7.6|#000000}
  - text 36pt [28%,47% → 72%,51%]: {This process may allow us to perform fewer MCMC steps.|#80cfb9}
- group [11%,63% → 89%,79%]
  - text 36pt [29%,65% → 71%,70%]: SMC is {nonparametric|#80b9ff}, we do everything with samples.
  - text 36pt [18%,71% → 82%,76%]: {This feature allows it to perform well for complex, multimodal failure distributions.|#80cfb9}
  - rounded box (outline) [11%,63% → 89%,79%]
- **Builds:** click 1: group — appears; click 2: group — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 105
_(Keynote: Lecture 11, slide 78)_
- heading (spaced caps) 36pt [32%,5% → 68%,10%]: SEQUENTIAL MONTE CARLO
- group [11%,15% → 89%,31%]
  - text 36pt [29%,18% → 71%,22%]: SMC is {nonparametric|#80b9ff}, we do everything with samples.
  - text 36pt [18%,23% → 82%,28%]: {This feature allows it to perform well for complex, multimodal failure distributions.|#80cfb9}
  - rounded box (outline) [11%,15% → 89%,31%]
- image `test-24625.svg` [7%,39% → 87%,86%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 106
_(Keynote: Lecture 12, slide 2)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: RATIO OF NORMALIZING CONSTANTS
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: SELF-NORMALIZED IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: BRIDGE SAMPLING
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: MULTILEVEL SPLITTING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 107
_(Keynote: Lecture 12, slide 3)_
- heading (spaced caps) 36pt [27%,41% → 73%,46%]: RATIO OF NORMALIZING CONSTANTS
- text 36pt [14%,47% → 86%,55%]: It turns out that importance sampling is a [[special case|#80b9ff]] of a more [[general problem|#80b9ff]] of determining the ratio of the normalizing constants of two distributions.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 108
_(Keynote: Lecture 12, slide 4)_
- heading (spaced caps) 36pt [27%,6% → 73%,11%]: RATIO OF NORMALIZING CONSTANTS
- text 36pt [14%,12% → 86%,20%]: It turns out that importance sampling is a [[special case|#80b9ff]] of a more [[general problem|#80b9ff]] of determining the ratio of the normalizing constants of two distributions.
- image `test-24685.svg` [36%,25% → 64%,83%]
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (46pt, #fab0ae) [9%,34% → 34%,45%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (46pt, #80b9ff) [66%,34% → 91%,45%]
- **Builds:** click 1: equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ — slides in; with previous: equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 109
_(Keynote: Lecture 12, slide 5)_
- image `test-24685.svg` [5%,35% → 33%,93%]
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (31pt, #fab0ae) [11%,9% → 27%,17%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (31pt, #80b9ff) [11%,21% → 27%,29%]
- text 36pt [49%,11% → 92%,16%]: Imagine someone just came up to you and was like…
- vector icon `shape-e6a98bf6.svg` [47%,53% → 54%,89%]
- group [50%,20% → 96%,52%]
  - shape (outline) [53%,20% → 95%,52%]
- text 44pt [59%,27% → 90%,47%]: {I will give you a million dollars 💰 if you can get me an accurate estimate of |#c0c0c0}$z_1${$/$|#fab0ae}{$z_2$|#c0c0c0}{ u|#80b9ff}{sing only samples from |#c0c0c0}$g_2${.|#80b9ff}
- **Builds:** click 1: group — wipes in; click 2: text 44pt — sparkle
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 110
_(Keynote: Lecture 12, slide 6)_
- vector icon `shape-c3aad2da.svg` [6%,62% → 11%,84%]
- group [8%,40% → 37%,61%]
  - shape (outline) [10%,40% → 37%,61%]
- text 24pt [14%,44% → 34%,57%]: {I will give you a million dollars 💰 if you can get me an accurate estimate of |#c0c0c0}$z_1${$/$|#fab0ae}{$z_2$|#c0c0c0}{ u|#80b9ff}{sing only samples from |#c0c0c0}$g_2${.|#80b9ff}
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (31pt, #fab0ae) [11%,9% → 27%,17%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (31pt, #80b9ff) [11%,21% → 27%,29%]
- group [16%,18% → 16%,18%]
  - line #80b9ff [16%,17% → 20%,18%]
  - line #80b9ff [24%,17% → 26%,18%]
  - line #80b9ff [23%,20% → 28%,30%]
- group [18%,52% → 18%,52%]
  - line #80b9ff [15%,51% → 19%,57%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 111
_(Keynote: Lecture 12, slide 7)_
- equation $\frac{z_1}{z_2} = \mathbb E_{\tau \sim g_2(\cdot)} \left [ \frac{\bar g_1(\tau)}{\bar g_2(\tau)} \right ] \approx \frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_2(\tau)}$ (46pt, #ffffff) [53%,69% → 87%,81%]
- vector icon `shape-c3aad2da.svg` [6%,62% → 11%,84%]
- group [8%,40% → 37%,61%]
  - shape (outline) [10%,40% → 37%,61%]
- text 24pt [14%,44% → 34%,57%]: {I will give you a million dollars 💰 if you can get me an accurate estimate of |#c0c0c0}$z_1${$/$|#fab0ae}{$z_2$|#c0c0c0}{ u|#80b9ff}{sing only samples from |#c0c0c0}$g_2${.|#80b9ff}
- group [57%,10% → 83%,60%]
  - vector icon `shape-76810f17.svg` [57%,10% → 83%,60%]
  - image `val-page-183.svg` (cropped: show only 29–52% across and 19–41% down of the image) [58%,12% → 82%,59%]
- line #ff48cf [75%,68% → 88%,82%]
- line #ff48cf [59%,74% → 65%,78%]
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (31pt, #fab0ae) [11%,9% → 27%,17%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (31pt, #80b9ff) [11%,21% → 27%,29%]
- **Builds:** click 1: line #ff48cf — com.apple.iWork.Keynote.LineDraw; click 2: line #ff48cf — com.apple.iWork.Keynote.LineDraw
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 112
_(Keynote: Lecture 12, slide 8)_
- vector icon `shape-e6a98bf6.svg` [9%,49% → 17%,84%]
- group [13%,16% → 58%,48%]
  - shape (outline) [16%,16% → 58%,48%]
- text 44pt [21%,22% → 53%,43%]: {I will give you a million dollars 💰 if you can get me an accurate estimate of |#c0c0c0}$z_1${$/$|#fab0ae}{$z_2$|#c0c0c0}{ u|#80b9ff}{sing only samples from |#c0c0c0}$g_2${.|#80b9ff}
- group [49%,59% → 85%,75%]
  - rounded box (outline) [49%,59% → 85%,75%]
  - text 48pt [49%,61% → 85%,72%]: Sadly 😕, this scenario is probably never going to happen to you.
- text 36pt [48%,78% → 86%,82%]: So let’s get back to failure probability estimation…
- equation $\frac{z_1}{z_2} = \mathbb E_{\tau \sim g_2(\cdot)} \left [ \frac{\bar g_1(\tau)}{\bar g_2(\tau)} \right ] \approx \frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_2(\tau)}$ (46pt, #ffffff) [61%,26% → 95%,38%]
- text 36pt [73%,20% → 80%,25%]: {fireworks|#000000}
- **Builds:** click 1: text 36pt — fireworks; click 2: group — apple:dissolve; click 3: text 36pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 113
_(Keynote: Lecture 12, slide 9)_
- equation $\frac{z_1}{z_2} = \mathbb E_{\tau \sim g_2(\cdot)} \left [ \frac{\bar g_1(\tau)}{\bar g_2(\tau)} \right ] \approx \frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_2(\tau)}$ (46pt, #ffffff) [33%,21% → 67%,32%]
- text 48pt [19%,8% → 81%,14%]: Can we derive the importance sampling estimator from this?

## Slide 114
_(Keynote: Lecture 12, slide 10)_
- text 48pt [22%,8% → 78%,14%]: Quick aside: don’t do the opposite (i.e. estimate $1/p_\text{fail}$)
- image `screenshot-2025-10-15-at-4-01-44-pm.png` [14%,21% → 86%,101%]
- vector icon `shape-df24e860.svg` [66%,23% → 83%,29%]
- vector icon `shape-e43c2dee.svg` [16%,28% → 41%,34%]
- **Builds:** click 1: vector icon `shape-df24e860.svg` — wipes in; then: vector icon `shape-e43c2dee.svg` — wipes in

## Slide 115
_(Keynote: Lecture 12, slide 11)_
- image `test-24685.svg` [36%,32% → 64%,90%]
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (46pt, #fab0ae) [9%,41% → 34%,52%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (46pt, #80b9ff) [66%,41% → 91%,52%]
- text 48pt [19%,8% → 81%,14%]: What might be a problem with estimating this ratio using samples from $g_2$?
- vector icon `shape-644dbec6.svg` [58%,79% → 59%,81%]
- vector icon `shape-644dbec6.svg` [58%,79% → 60%,81%]
- vector icon `shape-644dbec6.svg` [59%,79% → 60%,81%]
- vector icon `shape-644dbec6.svg` [60%,79% → 61%,81%]
- vector icon `shape-644dbec6.svg` [61%,79% → 62%,81%]
- vector icon `shape-644dbec6.svg` [62%,79% → 64%,81%]
- vector icon `shape-644dbec6.svg` [58%,79% → 59%,81%]
- vector icon `shape-644dbec6.svg` [57%,79% → 58%,81%]
- vector icon `shape-644dbec6.svg` [57%,79% → 58%,81%]
- vector icon `shape-644dbec6.svg` [56%,79% → 57%,81%]
- vector icon `shape-644dbec6.svg` [54%,79% → 55%,81%]
- text 48pt [20%,16% → 80%,22%]: {It doesn’t work so great if $g_1$ and $g_2$ have very |#f3cf80}[[little overlap|#f3cf80]]{.|#f3cf80}
- text 48pt [43%,-9% → 57%,-4%]: The solution?
- **Builds:** click 1: vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; with previous (0.1 s later): vector icon `shape-644dbec6.svg` — apple:dissolve character; click 2: text 48pt — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 116
_(Keynote: Lecture 12, slide 12)_
- image `test-24685.svg` [36%,32% → 64%,90%]
- text 48pt [-77%,8% → -1%,14%]: What might be a problem with estimating this ratio using samples from $g_2$?
- text 48pt [-69%,16% → -10%,22%]: {It doesn’t work so great if $g_1$ and $g_2$ have very |#f3cf80}[[little overlap|#f3cf80]]{.|#f3cf80}
- text 48pt [43%,8% → 57%,14%]: The solution?
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (46pt, #fab0ae) [9%,41% → 34%,52%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (46pt, #80b9ff) [66%,41% → 91%,52%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 117
_(Keynote: Lecture 12, slide 13)_
- image `test-24685.svg` [36%,32% → 64%,90%]
- text 48pt [34%,8% → 48%,14%]: The solution?
- text 48pt [49%,8% → 69%,14%]: {Use an umbrella!☔|#c3b8ff}
- image `test-25047.svg` [36%,32% → 64%,90%]
- equation $\bar g_u(\tau)$ (46pt, #c3b8ff) [48%,74% → 52%,78%]
- equation $g_1(\tau) = \frac{\bar g_1(\tau)}{\int \bar g_1(\tau) d \tau} = \frac{\bar g_1(\tau)}{z_1}$ (46pt, #fab0ae) [9%,41% → 34%,52%]
- equation $g_2(\tau) = \frac{\bar g_2(\tau)}{\int \bar g_2(\tau) d \tau} = \frac{\bar g_2(\tau)}{z_2}$ (46pt, #80b9ff) [66%,41% → 91%,52%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 118
_(Keynote: Lecture 12, slide 14)_
- text 48pt [34%,8% → 48%,14%]: The solution?
- text 48pt [49%,8% → 69%,14%]: {Use an umbrella!☔|#c3b8ff}
- image `test-24685.svg` [9%,36% → 24%,68%]
- image `test-25047.svg` [9%,36% → 24%,68%]
- equation $\bar g_u(\tau)$ (25pt, #c3b8ff) [16%,59% → 18%,62%]
- equation $g_1(\tau)$ (25pt, #fab0ae) [7%,41% → 10%,43%]
- equation $g_2(\tau)$ (25pt, #80b9ff) [24%,41% → 26%,43%]
- equation $\frac{z_\alpha}{z_\beta} = \approx \frac{1}{m} \sum_{i=1}^m \frac{\bar g_\alpha(\tau)}{\bar g_\beta(\tau)}$ (46pt, #ffffff) [7%,10% → 26%,21%]
- text 36pt [15%,24% → 19%,29%]: Using samples from $g_\beta$
- line #ffffff [6%,9% → 28%,30%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 119
_(Keynote: Lecture 12, slide 15)_
- text 48pt [34%,8% → 48%,14%]: The solution?
- text 48pt [49%,8% → 69%,14%]: {Use an umbrella!☔|#c3b8ff}
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_u(\tau)}}{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_2(\tau)}{\bar g_u(\tau)}}$ (54pt, #ffffff) [40%,22% → 60%,42%]
- text 36pt [41%,45% → 59%,50%]: Using samples from $g_u$.
- line #ffffff [36%,20% → 64%,54%]
- rounded box (outline) [31%,58% → 69%,71%]
- text 100pt [32%,59% → 38%,72%]: 🤔
- text 36pt [39%,62% → 68%,67%]: What’s the optimal umbrella density?
- group [39%,75% → 61%,88%]
  - equation $\bar g^\ast_u(\tau) \propto \left | \bar g_1(\tau) - \frac{z_1}{z_2} \bar g_2(\tau) \right |$ (36pt, #c3b8ff) [40%,77% → 60%,86%]
  - line #c3b8ff [39%,75% → 61%,88%]
- **Builds:** click 1: text 100pt — fades up from dark; with previous: text 36pt — fades up from dark; with previous: rounded box (outline) — wipes in; click 2: group — apple:dissolve
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 120
_(Keynote: Lecture 12, slide 16)_
- text 48pt [34%,8% → 48%,14%]: The solution?
- text 48pt [49%,8% → 69%,14%]: {Use an umbrella!☔|#c3b8ff}
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_u(\tau)}}{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_2(\tau)}{\bar g_u(\tau)}}$ (54pt, #ffffff) [16%,22% → 36%,42%]
- text 36pt [17%,45% → 34%,50%]: Using samples from $g_u$.
- line #ffffff [12%,20% → 39%,54%]
- rounded box (outline) [6%,58% → 45%,71%]
- text 100pt [7%,59% → 13%,72%]: 🤔
- text 36pt [14%,62% → 43%,67%]: What’s the optimal umbrella density?
- group [15%,75% → 36%,88%]
  - equation $\bar g^\ast_u(\tau) \propto \left | \bar g_1(\tau) - \frac{z_1}{z_2} \bar g_2(\tau) \right |$ (36pt, #c3b8ff) [16%,77% → 35%,86%]
  - line #c3b8ff [15%,75% → 36%,88%]
- rounded box (outline) [52%,22% → 91%,35%]
- text 100pt [55%,22% → 61%,35%]: 🤔
- text 36pt [62%,24% → 88%,33%]: …but it is written in terms of the thing we want to estimate ($z_1 / z_2$).
- image `l12-pasted-movie-20620.png` [49%,37% → 94%,91%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 121
_(Keynote: Lecture 12, slide 17)_
- text 48pt [34%,8% → 48%,14%]: The solution?
- text 48pt [49%,8% → 69%,14%]: {Use an umbrella!☔|#c3b8ff}
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_u(\tau)}}{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_2(\tau)}{\bar g_u(\tau)}}$ (54pt, #ffffff) [16%,22% → 36%,42%]
- text 36pt [17%,45% → 34%,50%]: Using samples from $g_u$.
- line #ffffff [12%,20% → 39%,54%]
- rounded box (outline) [6%,58% → 45%,71%]
- text 100pt [7%,59% → 13%,72%]: 🤔
- text 36pt [14%,62% → 43%,67%]: What’s the optimal umbrella density?
- group [15%,75% → 36%,88%]
  - equation $\bar g^\ast_u(\tau) \propto \left | \bar g_1(\tau) - \frac{z_1}{z_2} \bar g_2(\tau) \right |$ (36pt, #c3b8ff) [16%,77% → 35%,86%]
  - line #c3b8ff [15%,75% → 36%,88%]
- rounded box (outline) [52%,22% → 91%,35%]
- text 100pt [55%,22% → 61%,35%]: 🤔
- text 36pt [62%,24% → 88%,33%]: …but it is written in terms of the thing we want to estimate ($z_1 / z_2$).
- image `l12-pasted-movie-20620.png` [49%,37% → 94%,91%]
- rounded box (outline) [18%,43% → 82%,62%]
- text 48pt [48%,50% → 52%,55%]: {In practice, we just try to get as close as possible.|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 122
_(Keynote: Lecture 12, slide 18)_
- rounded box (outline) [18%,6% → 82%,17%]
- text 48pt [25%,9% → 75%,14%]: {In practice, we just try to get as close as possible.|#000000}
- image `test-24685.svg` [36%,34% → 64%,92%]
- equation $\bar g_1(\tau)$ (46pt, #fab0ae) [32%,43% → 36%,47%]
- equation $\bar g_2(\tau)$ (46pt, #80b9ff) [64%,43% → 69%,47%]
- image `test-25047.svg` [36%,34% → 64%,92%]
- equation $\bar g_u(\tau)$ (46pt, #c3b8ff) [48%,77% → 52%,81%]
- text 36pt [17%,22% → 83%,27%]: A good umbrella distribution should [[cover|#c3b8ff]] [[regions of high likelihood|#c3b8ff]] in both distributions.
- vector icon `shape-66ca66f9.svg` [60%,81% → 61%,83%]
- vector icon `shape-66ca66f9.svg` [60%,81% → 61%,83%]
- vector icon `shape-66ca66f9.svg` [59%,81% → 60%,83%]
- vector icon `shape-66ca66f9.svg` [59%,81% → 60%,83%]
- text on a #c3b8ff filled box 32pt [58%,81% → 59%,83%]: c
- text on a #c3b8ff filled box 32pt [58%,81% → 59%,83%]: c
- text on a #c3b8ff filled box 32pt [57%,81% → 58%,83%]: c
- text on a #c3b8ff filled box 32pt [56%,81% → 57%,83%]: c
- text on a #c3b8ff filled box 32pt [54%,81% → 55%,83%]: c
- text on a #c3b8ff filled box 32pt [44%,81% → 45%,83%]: c
- text on a #c3b8ff filled box 32pt [45%,81% → 46%,83%]: c
- text on a #c3b8ff filled box 32pt [43%,81% → 44%,83%]: c
- text on a #c3b8ff filled box 32pt [42%,81% → 43%,83%]: c
- text on a #c3b8ff filled box 32pt [41%,81% → 42%,83%]: c
- text on a #c3b8ff filled box 32pt [41%,81% → 42%,83%]: c
- text on a #c3b8ff filled box 32pt [40%,81% → 41%,83%]: c
- text on a #c3b8ff filled box 32pt [39%,81% → 40%,83%]: c
- text on a #c3b8ff filled box 32pt [38%,81% → 39%,83%]: c
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 123
_(Keynote: Lecture 12, slide 19)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: RATIO OF NORMALIZING CONSTANTS
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: SELF-NORMALIZED IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: BRIDGE SAMPLING
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: MULTILEVEL SPLITTING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 124
_(Keynote: Lecture 12, slide 20)_
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_1(\tau)}{\bar g_u(\tau)}}{\frac{1}{m} \sum_{i=1}^m \frac{\bar g_2(\tau)}{\bar g_u(\tau)}}$ (54pt, #ffffff) [8%,10% → 28%,29%]
- text 36pt [9%,32% → 27%,37%]: Using samples from $g_u$.
- line #ffffff [5%,7% → 32%,41%]
- text 48pt [42%,5% → 86%,11%]: But what are we even doing with all of this ☔?
- text 48pt [34%,14% → 93%,25%]: Turns out we can use it to estimate the probability of failure using samples from an [[unnormalized proposal|#c3b8ff]]!
- equation $\bar g_1(\tau) = p(\tau) 1\{\tau \notin \psi\}$ (36pt, #fab0ae) [39%,38% → 54%,41%]
- equation $\bar g_2(\tau) = p(\tau)$ (36pt, #80b9ff) [63%,38% → 72%,42%]
- equation $\bar g_u(\tau) = \bar q(\tau)$ (36pt, #c3b8ff) [83%,38% → 92%,41%]
- text 36pt [35%,28% → 58%,36%]: {unnormalized failure distribution|#fab0ae}
- text 36pt [57%,28% → 78%,36%]: {nominal trajectory distribution|#80b9ff}
- text 36pt [77%,28% → 98%,36%]: {unnormalized proposal density|#c3b8ff}
- group [29%,9% → 29%,9%]
  - line #80b9ff [29%,9% → 31%,37%]
  - line #80b9ff [28%,9% → 30%,18%]
  - line #80b9ff [28%,21% → 29%,29%]
  - line #80b9ff [25%,22% → 25%,24%]
- group [83%,43% → 83%,43%]
  - line #80b9ff [83%,43% → 91%,43%]
- group [10%,13% → 10%,13%]
  - line #80b9ff [7%,12% → 12%,28%]
- **Builds:** click 1: text 48pt — apple:dissolve character; click 2: text 36pt — fades up from dark; with previous: text 36pt — fades up from dark; with previous: text 36pt — fades up from dark; with previous: equation $\bar g_u(\tau) = \bar q(\tau)$ — fades up from dark; with previous: equation $\bar g_1(\tau) = p(\tau) 1\{\tau \notin \psi\}$ — fades up from dark; with previous: equation $\bar g_2(\tau) = p(\tau)$ — fades up from dark
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 125
_(Keynote: Lecture 12, slide 21)_
- text 48pt [21%,4% → 79%,15%]: Turns out we can use it to estimate the probability of failure using samples from an [[unnormalized proposal|#c3b8ff]]!
- equation $\bar g_1(\tau) = p(\tau) 1\{\tau \notin \psi\}$ (36pt, #fab0ae) [22%,29% → 38%,32%]
- equation $\bar g_2(\tau) = p(\tau)$ (36pt, #80b9ff) [47%,29% → 55%,32%]
- equation $\bar g_u(\tau) = \bar q(\tau)$ (36pt, #c3b8ff) [67%,29% → 76%,32%]
- text 36pt [18%,18% → 42%,26%]: {unnormalized failure distribution|#fab0ae}
- text 36pt [40%,18% → 61%,26%]: {nominal trajectory distribution|#80b9ff}
- text 36pt [61%,18% → 82%,26%]: {unnormalized proposal density|#c3b8ff}
- line #ffffff [10%,37% → 90%,37%]
- text 48pt [21%,39% → 79%,50%]: This process results in the self-normalized importance sampling ([[self-IS|#c3b8ff]]) estimator:
- equation $p_\text{fail} \approx \frac{\frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}}{\frac{1}{m} \sum_{i=1}^m w_i}$ (44pt, #ffffff) [37%,55% → 63%,69%]
- line #ffffff [36%,53% → 64%,71%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 126
_(Keynote: Lecture 12, slide 22)_
- text 48pt [21%,4% → 79%,15%]: This process results in the self-normalized importance sampling ([[self-IS|#c3b8ff]]) estimator:
- equation $p_\text{fail} \approx \frac{\frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}}{\frac{1}{m} \sum_{i=1}^m w_i}$ (44pt, #ffffff) [37%,19% → 63%,33%]
- line #ffffff [36%,17% → 64%,35%]
- text 36pt [16%,66% → 84%,70%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- group [33%,41% → 53%,65%]
  - group [33%,41% → 53%,65%]
    - line #80b9ff [33%,63% → 35%,65%]
    - line #80b9ff [35%,59% → 38%,62%]
    - line #80b9ff [36%,41% → 53%,59%]
  - equation $p_\text{fail} \approx \frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}$ (25pt, #80b9ff) [38%,48% → 51%,54%]
- **Builds:** click 1: group — wipes in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 127
_(Keynote: Lecture 12, slide 23)_
- text 48pt [21%,4% → 79%,15%]: This process results in the self-normalized importance sampling ([[self-IS|#c3b8ff]]) estimator:
- equation $p_\text{fail} \approx \frac{\frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}}{\frac{1}{m} \sum_{i=1}^m w_i}$ (44pt, #ffffff) [37%,19% → 63%,33%]
- line #ffffff [36%,17% → 64%,35%]
- text 36pt [17%,39% → 83%,43%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- text 36pt [30%,47% → 70%,51%]: HOWEVER, the [[optimal proposal|#c3b8ff]] is very different…
- group [9%,68% → 30%,81%]
  - equation $\bar g^\ast_u(\tau) \propto \left | \bar g_1(\tau) - \frac{z_1}{z_2} \bar g_2(\tau) \right |$ (36pt, #c3b8ff) [10%,69% → 29%,79%]
  - line #c3b8ff [9%,68% → 30%,81%]
- equation $\bar g_1(\tau) = p(\tau) 1\{\tau \notin \psi\}$ (36pt, #fab0ae) [12%,56% → 27%,59%]
- equation $\bar g_2(\tau) = p(\tau)$ (36pt, #80b9ff) [15%,62% → 24%,65%]
- group [10%,85% → 10%,86%]
  - line #80b9ff [9%,82% → 31%,85%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 128
_(Keynote: Lecture 12, slide 24)_
- text 48pt [21%,4% → 79%,15%]: This process results in the self-normalized importance sampling ([[self-IS|#c3b8ff]]) estimator:
- equation $p_\text{fail} \approx \frac{\frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}}{\frac{1}{m} \sum_{i=1}^m w_i}$ (44pt, #ffffff) [37%,19% → 63%,33%]
- line #ffffff [36%,55% → 64%,64%]
- text 36pt [17%,39% → 83%,43%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- text 36pt [30%,47% → 70%,51%]: HOWEVER, the [[optimal proposal|#c3b8ff]] is very different…
- equation $q^\ast(\tau) \propto p(\tau) \left |1\{\tau \notin \psi\} - p_\text{fail} \right |$ (42pt, #ffffff) [36%,56% → 64%,62%]
- line #ffffff [36%,17% → 64%,35%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 129
_(Keynote: Lecture 12, slide 25)_
- text 48pt [21%,-33% → 79%,-22%]: This process results in the self-normalized importance sampling ([[self-IS|#c3b8ff]]) estimator:
- equation $p_\text{fail} \approx \frac{\frac{1}{m} \sum_{i=1}^m w_i 1\{\tau_i \notin \psi\}}{\frac{1}{m} \sum_{i=1}^m w_i}$ (44pt, #ffffff) [37%,-17% → 63%,-3%]
- line #ffffff [36%,18% → 64%,27%]
- text 36pt [17%,2% → 83%,7%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- text 36pt [30%,10% → 70%,15%]: HOWEVER, the [[optimal proposal|#c3b8ff]] is very different…
- equation $q^\ast(\tau) \propto p(\tau) \left |1\{\tau \notin \psi| - p_\text{fail} \right |$ (42pt, #ffffff) [36%,20% → 64%,26%]
- line #ffffff [36%,-19% → 64%,-1%]
- text 36pt [30%,31% → 70%,36%]: It should result in [[half|#fab0ae]] the samples coming from the [[failure distribution|#fab0ae]] and [[half|#80b9ff]] from the [[success distribution|#80b9ff]].
- group [35%,39% → 65%,96%]
  - vector icon `shape-d5fa9aa8.svg` [35%,41% → 65%,96%]
  - image `val-page-166.svg` (cropped: show only 68–91% across and 51–76% down of the image) [37%,39% → 63%,96%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 130
_(Keynote: Lecture 12, slide 26)_
- line #ffffff [36%,18% → 64%,27%]
- text 36pt [17%,2% → 83%,7%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- text 36pt [30%,10% → 70%,15%]: HOWEVER, the [[optimal proposal|#c3b8ff]] is very different…
- equation $q^\ast(\tau) \propto p(\tau) \left |1\{\tau \notin \psi| - p_\text{fail} \right |$ (42pt, #ffffff) [36%,20% → 64%,26%]
- text 36pt [30%,31% → 70%,36%]: It should result in [[half|#fab0ae]] the samples coming from the [[failure distribution|#fab0ae]] and [[half|#80b9ff]] from the [[success distribution|#80b9ff]].
- group [17%,39% → 47%,96%]
  - vector icon `shape-d5fa9aa8.svg` [17%,41% → 47%,96%]
  - image `val-page-166.svg` (cropped: show only 68–91% across and 51–76% down of the image) [19%,39% → 45%,96%]
- image `output-onlinepngtools-2.png` [60%,39% → 82%,96%]
- shape (outline) [51%,63% → 56%,70%]
- rounded box (outline) [-71%,38% → -2%,95%]
- text 36pt [-58%,41% → -16%,45%]: It can be tough to sample from this proposal though…
- image `test-25604.svg` [-68%,48% → -5%,93%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 131
_(Keynote: Lecture 12, slide 27)_
- rounded box (outline) [16%,38% → 84%,95%]
- line #ffffff [36%,18% → 64%,27%]
- text 36pt [17%,2% → 83%,7%]: It is kinda like [[regular importance sampling|#80b9ff]] — we just [[normalize the weights|#c3b8ff]] by their sum.
- text 36pt [30%,10% → 70%,15%]: HOWEVER, the [[optimal proposal|#c3b8ff]] is very different…
- equation $q^\ast(\tau) \propto p(\tau) \left |1\{\tau \notin \psi| - p_\text{fail} \right |$ (42pt, #ffffff) [36%,20% → 64%,26%]
- text 36pt [30%,31% → 70%,36%]: It should result in [[half|#fab0ae]] the samples coming from the [[failure distribution|#fab0ae]] and [[half|#80b9ff]] from the [[success distribution|#80b9ff]].
- group [104%,39% → 133%,96%]
  - vector icon `shape-d5fa9aa8.svg` [104%,41% → 133%,96%]
  - image `val-page-166.svg` (cropped: show only 68–91% across and 51–76% down of the image) [105%,39% → 132%,96%]
- image `output-onlinepngtools-2.png` [146%,39% → 169%,96%]
- shape (outline) [137%,63% → 142%,70%]
- text 36pt [29%,41% → 71%,45%]: It can be tough to sample from this proposal though…
- image `test-25604.svg` [19%,48% → 81%,93%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 132
_(Keynote: Lecture 12, slide 28)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: RATIO OF NORMALIZING CONSTANTS
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: SELF-NORMALIZED IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: BRIDGE SAMPLING
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: MULTILEVEL SPLITTING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 133
_(Keynote: Lecture 12, slide 29)_
- heading (spaced caps) 36pt [57%,22% → 130%,26%]: BRIDGE SAMPLING
- heading (spaced caps) 36pt [14%,22% → 87%,26%]: UMBRELLA SAMPLING
- image `test-24685.svg` [16%,34% → 39%,84%]
- equation $\bar g_1(\tau)$ (40pt, #fab0ae) [12%,42% → 16%,45%]
- equation $\bar g_2(\tau)$ (40pt, #80b9ff) [40%,42% → 44%,45%]
- image `test-25047.svg` [16%,34% → 39%,84%]
- equation $\bar g_u(\tau)$ (40pt, #c3b8ff) [25%,71% → 29%,74%]
- vector icon `shape-9c43d125.svg` [36%,75% → 37%,77%]
- vector icon `shape-9c43d125.svg` [36%,75% → 37%,77%]
- vector icon `shape-9c43d125.svg` [35%,75% → 36%,77%]
- vector icon `shape-9c43d125.svg` [35%,75% → 36%,77%]
- text on a #c3b8ff filled box 32pt [35%,75% → 36%,77%]: c
- text on a #c3b8ff filled box 32pt [34%,75% → 35%,77%]: c
- text on a #c3b8ff filled box 32pt [33%,75% → 34%,77%]: c
- text on a #c3b8ff filled box 32pt [32%,75% → 33%,77%]: c
- text on a #c3b8ff filled box 32pt [31%,75% → 32%,77%]: c
- text on a #c3b8ff filled box 32pt [22%,75% → 23%,77%]: c
- text on a #c3b8ff filled box 32pt [23%,75% → 24%,77%]: c
- text on a #c3b8ff filled box 32pt [21%,75% → 22%,77%]: c
- text on a #c3b8ff filled box 32pt [21%,75% → 22%,77%]: c
- text on a #c3b8ff filled box 32pt [20%,75% → 21%,77%]: c
- text on a #c3b8ff filled box 32pt [20%,75% → 21%,77%]: c
- text on a #c3b8ff filled box 32pt [19%,75% → 20%,77%]: c
- text on a #c3b8ff filled box 32pt [18%,75% → 19%,77%]: c
- text on a #c3b8ff filled box 32pt [17%,75% → 18%,77%]: c
- image `test-25640.svg` [57%,34% → 80%,84%]
- equation $\bar g_2(\tau)$ (40pt, #80b9ff) [79%,42% → 83%,45%]
- equation $\bar g_1(\tau)$ (40pt, #fab0ae) [55%,42% → 59%,45%]
- equation $\bar g_b(\tau)$ (40pt, #c3b8ff) [66%,35% → 70%,39%]
- vector icon `shape-02e1b091.svg` [78%,75% → 79%,77%]
- vector icon `shape-02e1b091.svg` [77%,75% → 78%,77%]
- vector icon `shape-02e1b091.svg` [77%,75% → 77%,77%]
- vector icon `shape-02e1b091.svg` [76%,75% → 77%,77%]
- vector icon `shape-02e1b091.svg` [75%,75% → 76%,77%]
- vector icon `shape-02e1b091.svg` [74%,75% → 75%,77%]
- vector icon `shape-02e1b091.svg` [75%,75% → 76%,77%]
- vector icon `shape-02e1b091.svg` [74%,75% → 75%,77%]
- vector icon `shape-02e1b091.svg` [72%,75% → 73%,77%]
- vector icon `shape-9f6eb8b4.svg` [63%,75% → 64%,77%]
- vector icon `shape-9f6eb8b4.svg` [62%,75% → 63%,77%]
- vector icon `shape-9f6eb8b4.svg` [61%,75% → 62%,77%]
- vector icon `shape-9f6eb8b4.svg` [61%,75% → 62%,77%]
- vector icon `shape-9f6eb8b4.svg` [60%,75% → 61%,77%]
- vector icon `shape-9f6eb8b4.svg` [61%,75% → 62%,77%]
- vector icon `shape-9f6eb8b4.svg` [60%,75% → 61%,77%]
- vector icon `shape-9f6eb8b4.svg` [59%,75% → 60%,77%]
- vector icon `shape-9f6eb8b4.svg` [57%,75% → 58%,77%]
- **Builds:** click 1: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-02e1b091.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character; with previous: vector icon `shape-9f6eb8b4.svg` — apple:dissolve character
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 134
_(Keynote: Lecture 12, slide 30)_
- heading (spaced caps) 36pt [5%,36% → 79%,41%]: BRIDGE SAMPLING
- image `test-25640.svg` [5%,49% → 29%,99%]
- equation $\bar g_2(\tau)$ (40pt, #80b9ff) [28%,57% → 32%,60%]
- equation $\bar g_1(\tau)$ (40pt, #fab0ae) [3%,57% → 7%,60%]
- equation $\bar g_b(\tau)$ (40pt, #c3b8ff) [15%,50% → 19%,53%]
- vector icon `shape-02e1b091.svg` [27%,89% → 28%,91%]
- vector icon `shape-02e1b091.svg` [26%,89% → 27%,91%]
- vector icon `shape-02e1b091.svg` [25%,89% → 26%,91%]
- vector icon `shape-02e1b091.svg` [25%,89% → 25%,91%]
- vector icon `shape-02e1b091.svg` [24%,89% → 25%,91%]
- vector icon `shape-02e1b091.svg` [23%,89% → 24%,91%]
- vector icon `shape-02e1b091.svg` [24%,89% → 25%,91%]
- vector icon `shape-02e1b091.svg` [22%,89% → 23%,91%]
- vector icon `shape-02e1b091.svg` [20%,89% → 21%,91%]
- vector icon `shape-9f6eb8b4.svg` [12%,89% → 13%,91%]
- vector icon `shape-9f6eb8b4.svg` [11%,89% → 11%,91%]
- vector icon `shape-9f6eb8b4.svg` [10%,89% → 11%,91%]
- vector icon `shape-9f6eb8b4.svg` [10%,89% → 11%,91%]
- vector icon `shape-9f6eb8b4.svg` [9%,89% → 10%,91%]
- vector icon `shape-9f6eb8b4.svg` [9%,89% → 10%,91%]
- vector icon `shape-9f6eb8b4.svg` [8%,89% → 9%,91%]
- vector icon `shape-9f6eb8b4.svg` [7%,89% → 8%,91%]
- vector icon `shape-9f6eb8b4.svg` [6%,89% → 7%,91%]
- equation $\frac{z_\alpha}{z_\beta} = \approx \frac{1}{m} \sum_{i=1}^m \frac{\bar g_\alpha(\tau)}{\bar g_\beta(\tau)}$ (46pt, #ffffff) [7%,10% → 26%,21%]
- text 36pt [15%,24% → 19%,29%]: Using samples from $g_\beta$
- line #ffffff [6%,9% → 28%,30%]
- group [19%,48% → 20%,49%]
  - line #80b9ff [14%,47% → 20%,56%]
- group [28%,8% → 28%,8%]
  - line #80b9ff [4%,5% → 30%,26%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 135
_(Keynote: Lecture 12, slide 31)_
- heading (spaced caps) 36pt [38%,6% → 112%,10%]: BRIDGE SAMPLING
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m_2} \sum_{i=1}^{m_2} \frac{\bar g_b(\tau)}{\bar g_2(\tau)}}{\frac{1}{m_1} \sum_{i=1}^{m_1} \frac{\bar g_b(\tau)}{\bar g_1(\tau)}}$ (54pt, #ffffff) [40%,24% → 60%,43%]
- text 36pt [38%,46% → 62%,51%]: Using samples from $g_1$ and $g_2$.
- line #ffffff [36%,21% → 64%,53%]
- rounded box (outline) [31%,57% → 69%,70%]
- text 100pt [32%,58% → 38%,71%]: 🤔
- text 36pt [39%,61% → 68%,66%]: What’s the optimal bridge density?
- group [39%,74% → 61%,87%]
  - equation $\bar g^\ast_b(\tau) \propto \frac{\bar g_1(\tau) \bar g_2(\tau)}{m_1 \bar g_1(\tau) + m_2 \frac{z_1}{z_2} \bar g_2(\tau)}$ (36pt, #c3b8ff) [39%,76% → 61%,85%]
  - line #c3b8ff [39%,74% → 61%,87%]
- **Builds:** click 1: group — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 136
_(Keynote: Lecture 12, slide 32)_
- heading (spaced caps) 36pt [38%,6% → 112%,10%]: BRIDGE SAMPLING
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m_2} \sum_{i=1}^{m_2} \frac{\bar g_b(\tau)}{\bar g_2(\tau)}}{\frac{1}{m_1} \sum_{i=1}^{m_1} \frac{\bar g_b(\tau)}{\bar g_1(\tau)}}$ (54pt, #ffffff) [13%,24% → 34%,43%]
- text 36pt [12%,46% → 35%,51%]: Using samples from $g_1$ and $g_2$.
- line #ffffff [10%,21% → 37%,53%]
- rounded box (outline) [5%,57% → 43%,70%]
- text 100pt [6%,58% → 11%,71%]: 🤔
- text 36pt [12%,61% → 41%,66%]: What’s the optimal bridge density?
- group [12%,74% → 35%,87%]
  - equation $\bar g^\ast_b(\tau) \propto \frac{\bar g_1(\tau) \bar g_2(\tau)}{m_1 \bar g_1(\tau) + m_2 \frac{z_1}{z_2} \bar g_2(\tau)}$ (36pt, #c3b8ff) [13%,76% → 35%,85%]
  - line #c3b8ff [12%,74% → 35%,87%]
- rounded box (outline) [52%,22% → 91%,35%]
- text 100pt [55%,22% → 61%,35%]: 🤔
- text 36pt [62%,24% → 88%,33%]: …but it is written in terms of the thing we want to estimate ($z_1 / z_2$).
- image `l12-pasted-movie-20620.png` [49%,37% → 94%,91%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 137
_(Keynote: Lecture 12, slide 33)_
- heading (spaced caps) 36pt [38%,6% → 112%,10%]: BRIDGE SAMPLING
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m_2} \sum_{i=1}^{m_2} \frac{\bar g_b(\tau)}{\bar g_2(\tau)}}{\frac{1}{m_1} \sum_{i=1}^{m_1} \frac{\bar g_b(\tau)}{\bar g_1(\tau)}}$ (54pt, #ffffff) [13%,24% → 34%,43%]
- text 36pt [12%,46% → 35%,51%]: Using samples from $g_1$ and $g_2$.
- line #ffffff [10%,21% → 37%,53%]
- rounded box (outline) [5%,57% → 43%,70%]
- text 100pt [6%,58% → 11%,71%]: 🤔
- text 36pt [12%,61% → 41%,66%]: What’s the optimal bridge density?
- group [12%,74% → 35%,87%]
  - equation $\bar g^\ast_b(\tau) \propto \frac{\bar g_1(\tau) \bar g_2(\tau)}{m_1 \bar g_1(\tau) + m_2 \frac{z_1}{z_2} \bar g_2(\tau)}$ (36pt, #c3b8ff) [13%,76% → 35%,85%]
  - line #c3b8ff [12%,74% → 35%,87%]
- rounded box (outline) [52%,22% → 91%,35%]
- text 100pt [55%,22% → 61%,35%]: 🤔
- text 36pt [62%,24% → 88%,33%]: …but it is written in terms of the thing we want to estimate ($z_1 / z_2$).
- image `l12-pasted-movie-20620.png` [49%,37% → 94%,91%]
- rounded box (outline) [18%,43% → 82%,62%]
- text 48pt [48%,50% → 52%,55%]: {In practice, we just try to get as close as possible.|#000000}
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 138
_(Keynote: Lecture 12, slide 34)_
- rounded box (outline) [18%,6% → 82%,17%]
- text 48pt [25%,9% → 75%,14%]: {In practice, we just try to get as close as possible.|#000000}
- text 36pt [17%,22% → 83%,27%]: A good bridge distribution should [[bridge the gap|#c3b8ff]] between both distributions.
- image `test-25640.svg` [36%,34% → 62%,91%]
- equation $\bar g_2(\tau)$ (45pt, #80b9ff) [62%,43% → 66%,47%]
- equation $\bar g_1(\tau)$ (45pt, #fab0ae) [34%,43% → 38%,47%]
- equation $\bar g_b(\tau)$ (45pt, #c3b8ff) [47%,35% → 51%,39%]
- vector icon `shape-cb103d0d.svg` [60%,80% → 61%,82%]
- vector icon `shape-cb103d0d.svg` [59%,80% → 61%,82%]
- vector icon `shape-cb103d0d.svg` [59%,80% → 60%,82%]
- vector icon `shape-cb103d0d.svg` [58%,80% → 59%,82%]
- vector icon `shape-cb103d0d.svg` [57%,80% → 58%,82%]
- vector icon `shape-cb103d0d.svg` [56%,80% → 57%,82%]
- vector icon `shape-cb103d0d.svg` [57%,80% → 58%,82%]
- vector icon `shape-cb103d0d.svg` [55%,80% → 56%,82%]
- vector icon `shape-cb103d0d.svg` [53%,80% → 54%,82%]
- vector icon `shape-c2d64f39.svg` [44%,80% → 45%,82%]
- vector icon `shape-c2d64f39.svg` [42%,80% → 43%,82%]
- vector icon `shape-c2d64f39.svg` [41%,80% → 42%,82%]
- vector icon `shape-c2d64f39.svg` [41%,80% → 42%,82%]
- vector icon `shape-c2d64f39.svg` [40%,80% → 41%,82%]
- vector icon `shape-c2d64f39.svg` [41%,80% → 42%,82%]
- vector icon `shape-c2d64f39.svg` [40%,80% → 41%,82%]
- vector icon `shape-c2d64f39.svg` [39%,80% → 40%,82%]
- vector icon `shape-c2d64f39.svg` [37%,80% → 38%,82%]
- group [68%,59% → 90%,73%]
  - rounded box (outline) [68%,59% → 90%,73%]
  - text 36pt [70%,60% → 88%,72%]: See algorithm 7.8 for a technique to estimate this density.
- **Builds:** click 1: group — apple:dissolve
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 139
_(Keynote: Lecture 12, slide 35)_
- text 48pt [22%,48% → 78%,52%]: Let’s get back to failure probability estimation again… what should we do now?
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 140
_(Keynote: Lecture 12, slide 36)_
- text 48pt [10%,7% → 90%,12%]: Let’s get back to failure probability estimation again… what should we do now?
- equation $\bar g_1(\tau) = p(\tau) 1\{\tau \notin \psi\}$ (36pt, #fab0ae) [22%,32% → 38%,35%]
- equation $\bar g_2(\tau) = p(\tau)$ (36pt, #80b9ff) [46%,32% → 55%,35%]
- equation $\bar g_b(\tau) = \bar q(\tau)$ (36pt, #c3b8ff) [67%,32% → 75%,35%]
- text 36pt [18%,22% → 42%,30%]: {unnormalized failure distribution|#fab0ae}
- text 36pt [40%,22% → 61%,30%]: {nominal trajectory distribution|#80b9ff}
- text 36pt [60%,22% → 81%,30%]: {unnormalized proposal density|#c3b8ff}
- line #f5615c [18%,23% → 82%,37%]
- line #f5615c [18%,23% → 82%,37%]
- text 48pt [34%,44% → 66%,50%]: {Turns out this is a horrible plan!|#f5615c}
- text 36pt [48%,53% → 52%,57%]: It ends up being no better than direct estimation.
- group [41%,60% → 59%,69%]
  - rounded box (outline) [41%,60% → 59%,69%]
  - text 36pt [48%,62% → 52%,67%]: {Example 7.9|#000000}
- text 48pt [10%,75% → 90%,80%]: Let’s do something even crazier!
- **Builds:** click 1: line #f5615c — draws in; then: line #f5615c — draws in; then: text 48pt — slides in; click 2: text 36pt — wipes in; click 3: group — apple:dissolve; click 4: text 48pt — comet
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 141
_(Keynote: Lecture 12, slide 37)_
- text 48pt [33%,6% → 67%,12%]: Let’s do something even crazier!
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m_2} \sum_{i=1}^{m_2} \frac{\bar g_b(\tau)}{\bar g_2(\tau)}}{\frac{1}{m_1} \sum_{i=1}^{m_1} \frac{\bar g_b(\tau)}{\bar g_1(\tau)}}$ (54pt, #ffffff) [7%,18% → 28%,38%]
- text 36pt [6%,41% → 29%,45%]: Using samples from $g_1$ and $g_2$.
- line #ffffff [4%,16% → 31%,48%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 142
_(Keynote: Lecture 12, slide 38)_
- text 48pt [33%,6% → 67%,12%]: Let’s do something even crazier!
- equation $\frac{z_1}{z_2} \approx \frac{\frac{1}{m_2} \sum_{i=1}^{m_2} \frac{\bar g_b(\tau)}{\bar g_2(\tau)}}{\frac{1}{m_1} \sum_{i=1}^{m_1} \frac{\bar g_b(\tau)}{\bar g_1(\tau)}}$ (54pt, #ffffff) [7%,18% → 28%,38%]
- text 36pt [6%,41% → 29%,45%]: Using samples from $g_1$ and $g_2$.
- line #ffffff [4%,16% → 31%,48%]
- equation $p_\text{fail} = \frac{z_{p(\tau \mid \tau \notin \psi)}}{z_{p(\tau)}} = \left(\frac{z_2}{z_{p(\tau)}}\right) \left(\frac{z_3}{z_2}\right)\cdots \left(\frac{z_{p(\tau \mid \tau \notin \psi)}}{z_{L-1}}\right)$ (36pt, #ffffff) [41%,18% → 76%,29%]
- text 36pt [33%,36% → 92%,40%]: Get a bunch of intermediate distributions and apply bridge sampling to them!
- image `test-23618.svg` [26%,50% → 96%,91%]
- **Builds:** click 1: image `test-23618.svg` — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 143
_(Keynote: Lecture 12, slide 39)_
- image `test-24193.svg` [29%,18% → 71%,92%]
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 144
_(Keynote: Lecture 12, slide 40)_
- image `test-24193.svg` [29%,18% → 71%,92%]
- image `test-24199.svg` [29%,18% → 71%,92%]

## Slide 145
_(Keynote: Lecture 12, slide 41)_
- image `g01-23759.svg` [29%,18% → 71%,92%]
- image `g02-23767.svg` [29%,18% → 71%,92%]
- image `g03-23758.svg` [29%,18% → 71%,92%]
- image `g04-23760.svg` [29%,18% → 71%,92%]
- image `g05-23770.svg` [29%,18% → 71%,92%]
- image `g06-23764.svg` [29%,18% → 71%,92%]
- image `g07-23762.svg` [29%,18% → 71%,92%]
- image `g08-23792.svg` [29%,18% → 71%,92%]
- image `g09-23772.svg` [29%,18% → 71%,92%]
- image `g10-23771.svg` [29%,18% → 71%,92%]
- image `g11-23777.svg` [29%,18% → 71%,92%]
- image `g12-23812.svg` [29%,18% → 71%,92%]
- image `g13-23813.svg` [29%,18% → 71%,92%]
- image `g14-23816.svg` [29%,18% → 71%,92%]
- image `g15-23808.svg` [29%,18% → 71%,92%]
- image `g16-23806.svg` [29%,18% → 71%,92%]
- image `g17-23775.svg` [29%,18% → 71%,92%]
- image `g18-23779.svg` [29%,18% → 71%,92%]
- image `g20-23794.svg` [29%,18% → 71%,92%]
- image `g21-23801.svg` [29%,18% → 71%,92%]
- image `g22-23839.svg` [29%,18% → 71%,92%]
- image `g23-23841.svg` [29%,18% → 71%,92%]
- image `g24-23823.svg` [29%,18% → 71%,92%]
- image `g25-23814.svg` [29%,18% → 71%,92%]
- image `g26-23817.svg` [29%,18% → 71%,92%]
- image `g27-23803.svg` [29%,18% → 71%,92%]
- image `g28-23802.svg` [29%,18% → 71%,92%]
- image `g29-23790.svg` [29%,18% → 71%,92%]
- image `g30-23781.svg` [29%,18% → 71%,92%]
- image `g31-23783.svg` [29%,18% → 71%,92%]
- image `g32-23782.svg` [29%,18% → 71%,92%]
- image `g33-23810.svg` [29%,18% → 71%,92%]
- image `g34-23836.svg` [29%,18% → 71%,92%]
- image `g35-23805.svg` [29%,18% → 71%,92%]
- image `g36-23804.svg` [29%,18% → 71%,92%]
- image `g38-23840.svg` [29%,18% → 71%,92%]
- image `g39-23819.svg` [29%,18% → 71%,92%]
- image `g40-23795.svg` [29%,18% → 71%,92%]
- image `g41-23793.svg` [29%,18% → 71%,92%]
- image `g42-23824.svg` [29%,18% → 71%,92%]
- image `g43-23815.svg` [29%,18% → 71%,92%]
- image `g44-23809.svg` [29%,18% → 71%,92%]
- image `g45-23807.svg` [29%,18% → 71%,92%]
- image `g46-23811.svg` [29%,18% → 71%,92%]
- image `g47-23821.svg` [29%,18% → 71%,92%]
- image `g48-23820.svg` [29%,18% → 71%,92%]
- image `g49-23818.svg` [29%,18% → 71%,92%]
- image `g50-23791.svg` [29%,18% → 71%,92%]
- image `g51-23785.svg` [29%,18% → 71%,92%]
- vector icon `shape-b1618fc1.svg` [48%,37% → 60%,57%]
- equation $\frac{z_2}{z_{p(\tau)}}$ (43pt, #ffffff) [74%,31% → 78%,40%]
- **Builds:** click 1: image `g02-23767.svg` — appears; then (0.05 s later): image `g03-23758.svg` — appears; then (0.05 s later): image `g04-23760.svg` — appears; then (0.05 s later): image `g05-23770.svg` — appears; then (0.05 s later): image `g06-23764.svg` — appears; then (0.05 s later): image `g07-23762.svg` — appears; then (0.05 s later): image `g08-23792.svg` — appears; then (0.05 s later): image `g09-23772.svg` — appears; then (0.05 s later): image `g10-23771.svg` — appears; then (0.05 s later): image `g11-23777.svg` — appears; then (0.05 s later): image `g12-23812.svg` — appears; then (0.05 s later): image `g13-23813.svg` — appears; then (0.05 s later): image `g14-23816.svg` — appears; then (0.05 s later): image `g15-23808.svg` — appears; then (0.05 s later): image `g16-23806.svg` — appears; then (0.05 s later): image `g17-23775.svg` — appears; then (0.05 s later): image `g18-23779.svg` — appears; then (0.05 s later): image `g20-23794.svg` — appears; then (0.05 s later): image `g21-23801.svg` — appears; then (0.05 s later): image `g22-23839.svg` — appears; then (0.05 s later): image `g23-23841.svg` — appears; then (0.05 s later): image `g24-23823.svg` — appears; then (0.05 s later): image `g25-23814.svg` — appears; then (0.05 s later): image `g26-23817.svg` — appears; then (0.05 s later): image `g27-23803.svg` — appears; then (0.05 s later): image `g28-23802.svg` — appears; then (0.05 s later): image `g29-23790.svg` — appears; then (0.05 s later): image `g30-23781.svg` — appears; then (0.05 s later): image `g31-23783.svg` — appears; then (0.05 s later): image `g32-23782.svg` — appears; then (0.05 s later): image `g33-23810.svg` — appears; then (0.05 s later): image `g34-23836.svg` — appears; then (0.05 s later): image `g35-23805.svg` — appears; then (0.05 s later): image `g36-23804.svg` — appears; then (0.05 s later): image `g38-23840.svg` — appears; then (0.05 s later): image `g39-23819.svg` — appears; then (0.05 s later): image `g40-23795.svg` — appears; then (0.05 s later): image `g41-23793.svg` — appears; then (0.05 s later): image `g42-23824.svg` — appears; then (0.05 s later): image `g43-23815.svg` — appears; then (0.05 s later): image `g44-23809.svg` — appears; then (0.05 s later): image `g45-23807.svg` — appears; then (0.05 s later): image `g46-23811.svg` — appears; then (0.05 s later): image `g47-23821.svg` — appears; then (0.05 s later): image `g48-23820.svg` — appears; then (0.05 s later): image `g49-23818.svg` — appears; then (0.05 s later): image `g50-23791.svg` — appears; then (0.05 s later): image `g51-23785.svg` — appears; click 2: vector icon `shape-b1618fc1.svg` — apple:dissolve character; click 3: equation $\frac{z_2}{z_{p(\tau)}}$ — apple:dissolve

## Slide 146
_(Keynote: Lecture 12, slide 42)_
- image `g01-23872.svg` [29%,18% → 71%,92%]
- image `g02-23871.svg` [29%,18% → 71%,92%]
- image `g03-23873.svg` [29%,18% → 71%,92%]
- image `g04-23870.svg` [29%,18% → 71%,92%]
- image `g05-23878.svg` [29%,18% → 71%,92%]
- image `g06-23883.svg` [29%,18% → 71%,92%]
- image `g07-23877.svg` [29%,18% → 71%,92%]
- image `g08-23882.svg` [29%,18% → 71%,92%]
- image `g09-23940.svg` [29%,18% → 71%,92%]
- image `g10-23939.svg` [29%,18% → 71%,92%]
- image `g11-23945.svg` [29%,18% → 71%,92%]
- image `g12-23936.svg` [29%,18% → 71%,92%]
- image `g13-23933.svg` [29%,18% → 71%,92%]
- image `g14-23893.svg` [29%,18% → 71%,92%]
- image `g15-23891.svg` [29%,18% → 71%,92%]
- image `g16-23894.svg` [29%,18% → 71%,92%]
- image `g17-23948.svg` [29%,18% → 71%,92%]
- image `g18-23947.svg` [29%,18% → 71%,92%]
- image `g19-23949.svg` [29%,18% → 71%,92%]
- image `g20-23942.svg` [29%,18% → 71%,92%]
- image `g21-23941.svg` [29%,18% → 71%,92%]
- image `g22-23946.svg` [29%,18% → 71%,92%]
- image `g23-23943.svg` [29%,18% → 71%,92%]
- image `g24-23931.svg` [29%,18% → 71%,92%]
- image `g25-23938.svg` [29%,18% → 71%,92%]
- image `g26-23910.svg` [29%,18% → 71%,92%]
- image `g27-23899.svg` [29%,18% → 71%,92%]
- image `g28-23900.svg` [29%,18% → 71%,92%]
- image `g29-23912.svg` [29%,18% → 71%,92%]
- image `g30-23888.svg` [29%,18% → 71%,92%]
- image `g31-23935.svg` [29%,18% → 71%,92%]
- image `g32-23932.svg` [29%,18% → 71%,92%]
- image `g33-23885.svg` [29%,18% → 71%,92%]
- image `g34-23887.svg` [29%,18% → 71%,92%]
- image `g35-23927.svg` [29%,18% → 71%,92%]
- image `g36-23924.svg` [29%,18% → 71%,92%]
- image `g37-23923.svg` [29%,18% → 71%,92%]
- image `g38-23917.svg` [29%,18% → 71%,92%]
- image `g39-23918.svg` [29%,18% → 71%,92%]
- image `g40-23911.svg` [29%,18% → 71%,92%]
- image `g41-23903.svg` [29%,18% → 71%,92%]
- image `g42-23905.svg` [29%,18% → 71%,92%]
- image `g43-23902.svg` [29%,18% → 71%,92%]
- image `g44-23925.svg` [29%,18% → 71%,92%]
- image `g45-23920.svg` [29%,18% → 71%,92%]
- image `g46-23915.svg` [29%,18% → 71%,92%]
- image `g47-23913.svg` [29%,18% → 71%,92%]
- image `g48-23934.svg` [29%,18% → 71%,92%]
- image `g49-23922.svg` [29%,18% → 71%,92%]
- image `g50-23901.svg` [29%,18% → 71%,92%]
- image `g51-23898.svg` [29%,18% → 71%,92%]
- vector icon `shape-b1618fc1.svg` [53%,29% → 65%,48%]
- equation $\frac{z_2}{z_{p(\tau)}}$ (43pt, #ffffff) [74%,31% → 78%,40%]
- equation $\times \frac{z_3}{z_2}$ (43pt, #ffffff) [79%,32% → 83%,40%]
- **Builds:** click 1: image `g02-23871.svg` — appears; then (0.05 s later): image `g03-23873.svg` — appears; then (0.05 s later): image `g04-23870.svg` — appears; then (0.05 s later): image `g05-23878.svg` — appears; then (0.05 s later): image `g06-23883.svg` — appears; then (0.05 s later): image `g07-23877.svg` — appears; then (0.05 s later): image `g08-23882.svg` — appears; then (0.05 s later): image `g09-23940.svg` — appears; then (0.05 s later): image `g10-23939.svg` — appears; then (0.05 s later): image `g11-23945.svg` — appears; then (0.05 s later): image `g12-23936.svg` — appears; then (0.05 s later): image `g13-23933.svg` — appears; then (0.05 s later): image `g14-23893.svg` — appears; then (0.05 s later): image `g15-23891.svg` — appears; then (0.05 s later): image `g16-23894.svg` — appears; then (0.05 s later): image `g17-23948.svg` — appears; then (0.05 s later): image `g18-23947.svg` — appears; then (0.05 s later): image `g19-23949.svg` — appears; then (0.05 s later): image `g20-23942.svg` — appears; then (0.05 s later): image `g21-23941.svg` — appears; then (0.05 s later): image `g22-23946.svg` — appears; then (0.05 s later): image `g23-23943.svg` — appears; then (0.05 s later): image `g24-23931.svg` — appears; then (0.05 s later): image `g25-23938.svg` — appears; then (0.05 s later): image `g26-23910.svg` — appears; then (0.05 s later): image `g27-23899.svg` — appears; then (0.05 s later): image `g28-23900.svg` — appears; then (0.05 s later): image `g29-23912.svg` — appears; then (0.05 s later): image `g30-23888.svg` — appears; then (0.05 s later): image `g31-23935.svg` — appears; then (0.05 s later): image `g32-23932.svg` — appears; then (0.05 s later): image `g33-23885.svg` — appears; then (0.05 s later): image `g34-23887.svg` — appears; then (0.05 s later): image `g35-23927.svg` — appears; then (0.05 s later): image `g36-23924.svg` — appears; then (0.05 s later): image `g37-23923.svg` — appears; then (0.05 s later): image `g38-23917.svg` — appears; then (0.05 s later): image `g39-23918.svg` — appears; then (0.05 s later): image `g40-23911.svg` — appears; then (0.05 s later): image `g41-23903.svg` — appears; then (0.05 s later): image `g42-23905.svg` — appears; then (0.05 s later): image `g43-23902.svg` — appears; then (0.05 s later): image `g44-23925.svg` — appears; then (0.05 s later): image `g45-23920.svg` — appears; then (0.05 s later): image `g46-23915.svg` — appears; then (0.05 s later): image `g47-23913.svg` — appears; then (0.05 s later): image `g48-23934.svg` — appears; then (0.05 s later): image `g49-23922.svg` — appears; then (0.05 s later): image `g50-23901.svg` — appears; then (0.05 s later): image `g51-23898.svg` — appears; click 2: vector icon `shape-b1618fc1.svg` — apple:dissolve character; click 3: equation $\times \frac{z_3}{z_2}$ — slides in

## Slide 147
_(Keynote: Lecture 12, slide 43)_
- image `g01-24084.svg` [29%,18% → 71%,92%]
- image `g02-24085.svg` [29%,18% → 71%,92%]
- image `g03-24088.svg` [29%,18% → 71%,92%]
- image `g04-24086.svg` [29%,18% → 71%,92%]
- image `g05-24087.svg` [29%,18% → 71%,92%]
- image `g06-24122.svg` [29%,18% → 71%,92%]
- image `g07-24119.svg` [29%,18% → 71%,92%]
- image `g08-24093.svg` [29%,18% → 71%,92%]
- image `g09-24090.svg` [29%,18% → 71%,92%]
- image `g10-24089.svg` [29%,18% → 71%,92%]
- image `g11-24092.svg` [29%,18% → 71%,92%]
- image `g12-24091.svg` [29%,18% → 71%,92%]
- image `g13-24151.svg` [29%,18% → 71%,92%]
- image `g14-24141.svg` [29%,18% → 71%,92%]
- image `g15-24149.svg` [29%,18% → 71%,92%]
- image `g16-24145.svg` [29%,18% → 71%,92%]
- image `g17-24134.svg` [29%,18% → 71%,92%]
- image `g18-24135.svg` [29%,18% → 71%,92%]
- image `g19-24128.svg` [29%,18% → 71%,92%]
- image `g20-24148.svg` [29%,18% → 71%,92%]
- image `g21-24137.svg` [29%,18% → 71%,92%]
- image `g22-24095.svg` [29%,18% → 71%,92%]
- image `g23-24096.svg` [29%,18% → 71%,92%]
- image `g24-24131.svg` [29%,18% → 71%,92%]
- image `g25-24124.svg` [29%,18% → 71%,92%]
- image `g26-24121.svg` [29%,18% → 71%,92%]
- image `g27-24118.svg` [29%,18% → 71%,92%]
- image `g28-24102.svg` [29%,18% → 71%,92%]
- image `g30-24094.svg` [29%,18% → 71%,92%]
- image `g31-24101.svg` [29%,18% → 71%,92%]
- image `g32-24098.svg` [29%,18% → 71%,92%]
- image `g33-24155.svg` [29%,18% → 71%,92%]
- image `g34-24152.svg` [29%,18% → 71%,92%]
- image `g35-24142.svg` [29%,18% → 71%,92%]
- image `g36-24147.svg` [29%,18% → 71%,92%]
- image `g37-24154.svg` [29%,18% → 71%,92%]
- image `g38-24156.svg` [29%,18% → 71%,92%]
- image `g39-24150.svg` [29%,18% → 71%,92%]
- image `g40-24153.svg` [29%,18% → 71%,92%]
- image `g41-24157.svg` [29%,18% → 71%,92%]
- image `g42-24132.svg` [29%,18% → 71%,92%]
- image `g43-24133.svg` [29%,18% → 71%,92%]
- image `g44-24117.svg` [29%,18% → 71%,92%]
- image `g45-24115.svg` [29%,18% → 71%,92%]
- image `g46-24120.svg` [29%,18% → 71%,92%]
- image `g47-24111.svg` [29%,18% → 71%,92%]
- image `g48-24136.svg` [29%,18% → 71%,92%]
- image `g49-24123.svg` [29%,18% → 71%,92%]
- image `g50-24110.svg` [29%,18% → 71%,92%]
- image `g51-24099.svg` [29%,18% → 71%,92%]
- vector icon `shape-b1618fc1.svg` [58%,20% → 70%,40%]
- equation $\frac{z_2}{z_{p(\tau)}}$ (43pt, #ffffff) [74%,31% → 78%,40%]
- equation $\times \frac{z_3}{z_2}$ (43pt, #ffffff) [79%,32% → 83%,40%]
- equation $\times \frac{z_4}{z_3}$ (43pt, #ffffff) [84%,32% → 88%,40%]
- **Builds:** click 1: image `g02-24085.svg` — appears; then (0.05 s later): image `g03-24088.svg` — appears; then (0.05 s later): image `g04-24086.svg` — appears; then (0.05 s later): image `g05-24087.svg` — appears; then (0.05 s later): image `g06-24122.svg` — appears; then (0.05 s later): image `g07-24119.svg` — appears; then (0.05 s later): image `g08-24093.svg` — appears; then (0.05 s later): image `g09-24090.svg` — appears; then (0.05 s later): image `g10-24089.svg` — appears; then (0.05 s later): image `g11-24092.svg` — appears; then (0.05 s later): image `g12-24091.svg` — appears; then (0.05 s later): image `g13-24151.svg` — appears; then (0.05 s later): image `g14-24141.svg` — appears; then (0.05 s later): image `g15-24149.svg` — appears; then (0.05 s later): image `g16-24145.svg` — appears; then (0.05 s later): image `g17-24134.svg` — appears; then (0.05 s later): image `g18-24135.svg` — appears; then (0.05 s later): image `g19-24128.svg` — appears; then (0.05 s later): image `g20-24148.svg` — appears; then (0.05 s later): image `g21-24137.svg` — appears; then (0.05 s later): image `g22-24095.svg` — appears; then (0.05 s later): image `g23-24096.svg` — appears; then (0.05 s later): image `g24-24131.svg` — appears; then (0.05 s later): image `g25-24124.svg` — appears; then (0.05 s later): image `g26-24121.svg` — appears; then (0.05 s later): image `g27-24118.svg` — appears; then (0.05 s later): image `g28-24102.svg` — appears; then (0.05 s later): image `g30-24094.svg` — appears; then (0.05 s later): image `g31-24101.svg` — appears; then (0.05 s later): image `g32-24098.svg` — appears; then (0.05 s later): image `g33-24155.svg` — appears; then (0.05 s later): image `g34-24152.svg` — appears; then (0.05 s later): image `g35-24142.svg` — appears; then (0.05 s later): image `g36-24147.svg` — appears; then (0.05 s later): image `g37-24154.svg` — appears; then (0.05 s later): image `g38-24156.svg` — appears; then (0.05 s later): image `g39-24150.svg` — appears; then (0.05 s later): image `g40-24153.svg` — appears; then (0.05 s later): image `g41-24157.svg` — appears; then (0.05 s later): image `g42-24132.svg` — appears; then (0.05 s later): image `g43-24133.svg` — appears; then (0.05 s later): image `g44-24117.svg` — appears; then (0.05 s later): image `g45-24115.svg` — appears; then (0.05 s later): image `g46-24120.svg` — appears; then (0.05 s later): image `g47-24111.svg` — appears; then (0.05 s later): image `g48-24136.svg` — appears; then (0.05 s later): image `g49-24123.svg` — appears; then (0.05 s later): image `g50-24110.svg` — appears; then (0.05 s later): image `g51-24099.svg` — appears; click 2: vector icon `shape-b1618fc1.svg` — apple:dissolve character; click 3: equation $\times \frac{z_4}{z_3}$ — slides in

## Slide 148
_(Keynote: Lecture 12, slide 44)_
- image `test-24184.svg` [29%,18% → 71%,92%]
- vector icon `shape-b1618fc1.svg` [60%,16% → 72%,36%]
- equation $\frac{z_2}{z_{p(\tau)}}$ (43pt, #ffffff) [74%,31% → 78%,40%]
- equation $\times \frac{z_3}{z_2}$ (43pt, #ffffff) [79%,32% → 83%,40%]
- equation $\times \frac{z_4}{z_3}$ (43pt, #ffffff) [84%,32% → 88%,40%]
- equation $\times \frac{z_{p(\tau \mid \tau \notin \psi)}}{z_4}$ (43pt, #ffffff) [89%,31% → 98%,40%]
- line #f5615c [75%,30% → 78%,35%]
- line #f5615c [80%,36% → 83%,41%]
- line #f5615c [80%,30% → 83%,35%]
- line #f5615c [86%,37% → 89%,41%]
- line #f5615c [86%,30% → 88%,35%]
- line #f5615c [93%,37% → 96%,41%]
- equation $= \frac{z_{p(\tau \mid \tau \notin \psi)}}{z_{p(\tau)}} = \frac{p_\text{fail}}{1} = p_\text{fail}$ (43pt, #ffffff) [74%,47% → 96%,57%]
- text on a #80b9ff filled box 32pt [6%,76% → 25%,84%]: {Pluto Notebook!|#000000}
- **Builds:** click 1: vector icon `shape-b1618fc1.svg` — apple:dissolve character; click 2: equation $\times \frac{z_{p(\tau \mid \tau \notin \psi)}}{z_4}$ — slides in; click 3: line #f5615c — draws in; with previous: line #f5615c — draws in; click 4: line #f5615c — draws in; with previous: line #f5615c — draws in; click 5: line #f5615c — draws in; with previous: line #f5615c — draws in; click 6: equation $= \frac{z_{p(\tau \mid \tau \notin \psi)}}{z_{p(\tau)}} = \frac{p_\text{fail}}{1} = p_\text{fail}$ — slides in; click 7: text on a #80b9ff filled box 32pt — fades up from dark

## Slide 149
_(Keynote: Lecture 12, slide 45)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: RATIO OF NORMALIZING CONSTANTS
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: SELF-NORMALIZED IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: BRIDGE SAMPLING
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: MULTILEVEL SPLITTING
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 150
_(Keynote: Lecture 12, slide 46)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- text 36pt [29%,18% → 71%,23%]: Pick a notion of [[distance to failure $f(\tau)$ |#80b9ff]](e.g. robustness)
- text 36pt [37%,30% → 63%,39%]: We will require that {$f(\tau) \leq 0$|#fab0ae} for failure trajectories such that
- equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ (36pt, #ffffff) [39%,40% → 61%,43%]
- rounded box (outline) [34%,29% → 66%,46%]
- equation $f(\tau) \leq 0$ (37pt, #fab0ae) [53%,31% → 60%,34%]
- line #ffffff [22%,17% → 27%,24%]
- equation $1$ (36pt, #ffffff) [24%,20% → 25%,22%]
- line #ffffff [22%,52% → 27%,60%]
- equation $2$ (36pt, #ffffff) [24%,55% → 25%,57%]
- text 36pt [29%,53% → 71%,58%]: Pick a series of thresholds $\gamma_i$ for the distance to failure ranging from $\infty$ to $0$.
- **Builds:** click 1: line #ffffff — appears; with previous: equation $1$ — appears; with previous: text 36pt — appears; click 2: text 36pt — fades up from dark; with previous: equation $p(\tau \mid \tau \notin \psi) = p(\tau \mid f(\tau) \leq 0)$ — fades up from dark; with previous: rounded box (outline) — fades up from dark; with previous: equation $f(\tau) \leq 0$ — fades up from dark; click 3: line #ffffff — appears; with previous: equation $2$ — appears; with previous: text 36pt — appears
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 151
_(Keynote: Lecture 12, slide 47)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- text 36pt [29%,18% → 71%,23%]: Pick a notion of [[distance to failure $f(\tau)$ |#80b9ff]](e.g. robustness)
- line #ffffff [22%,17% → 27%,24%]
- equation $1$ (36pt, #ffffff) [24%,20% → 25%,22%]
- line #ffffff [22%,28% → 27%,36%]
- equation $2$ (36pt, #ffffff) [24%,31% → 25%,33%]
- text 36pt [29%,28% → 71%,37%]: Pick a series of thresholds $\gamma_i$ for the distance to failure ranging from $\infty$ to $0$.
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 152
_(Keynote: Lecture 12, slide 48)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- text 36pt [29%,18% → 71%,23%]: Pick a notion of [[distance to failure $f(\tau)$ |#80b9ff]](e.g. robustness)
- line #ffffff [22%,17% → 27%,24%]
- equation $1$ (36pt, #ffffff) [24%,20% → 25%,22%]
- line #ffffff [22%,28% → 27%,36%]
- equation $2$ (36pt, #ffffff) [24%,31% → 25%,33%]
- text 36pt [29%,28% → 71%,37%]: Pick a series of thresholds $\gamma_i$ for the distance to failure ranging from $\infty$ to $0$.
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [38%,46% → 65%,54%]
- line #ffffff [37%,43% → 66%,57%]
- text 36pt [42%,66% → 75%,74%]: {If these probabilities are large enough, we can estimate them using direct sampling!|#80b9ff}
- arrow #80b9ff [59%,53% → 59%,65%]
- text 36pt [26%,77% → 91%,81%]: We can ensure that these probabilities are large enough by [[selecting them adaptively|#80cfb9]].
- **Builds:** click 1: arrow #80b9ff — draws in; with previous: text 36pt — fades up from dark; click 2: text 36pt — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 153
_(Keynote: Lecture 12, slide 49)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (42pt, #80b9ff) [36%,28% → 58%,31%]
- equation $=$ (42pt, #80b9ff) [59%,29% → 60%,30%]
- equation $0.5$ (42pt, #80b9ff) [62%,28% → 64%,31%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [31%,49% → 36%,51%]
- equation $\gamma_2 = 0.67$ (36pt, #80b9ff) [31%,52% → 38%,55%]
- **Builds:** click 1: image `test-26328.svg` — apple:dissolve; click 2: equation $\gamma_1 = \infty$ — apple:dissolve; with previous: equation $\gamma_2 = 0.67$ — apple:dissolve; click 3: equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ — apple:dissolve; click 4: equation $0.5$ — slides in; with previous: equation $=$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 154
_(Keynote: Lecture 12, slide 50)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [29%,49% → 36%,52%]
- equation $\gamma_3 = 0.62$ (36pt, #80b9ff) [29%,53% → 36%,56%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (42pt, #80b9ff) [36%,28% → 60%,31%]
- equation $=$ (42pt, #80b9ff) [61%,29% → 62%,30%]
- equation $0.5$ (42pt, #80b9ff) [63%,28% → 66%,31%]
- line #ffffff [12%,21% → 12%,93%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (13pt, #80b9ff) [16%,24% → 23%,25%]
- equation $0.5$ (47pt, #80b9ff) [18%,26% → 21%,29%]
- **Builds:** click 1: image `test-26419.svg` — apple:dissolve; with previous: equation $\gamma_3 = 0.62$ — apple:dissolve; click 2: equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ — apple:dissolve; click 3: equation $0.5$ — slides in; with previous: equation $=$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 155
_(Keynote: Lecture 12, slide 51)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (13pt, #80b9ff) [16%,24% → 23%,25%]
- equation $0.5$ (47pt, #80b9ff) [18%,26% → 21%,29%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- line #ffffff [12%,21% → 12%,93%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [4%,31% → 10%,34%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (14pt, #80b9ff) [23%,24% → 31%,25%]
- equation $0.5$ (42pt, #80b9ff) [26%,26% → 29%,29%]
- image `test-26466.svg` [21%,38% → 75%,96%]
- image `test-26473.svg` [21%,38% → 75%,96%]
- equation $\gamma_3 = 0.62$ (36pt, #d6d6d6) [29%,48% → 36%,52%]
- equation $\gamma_4 = 0.59$ (36pt, #80b9ff) [29%,53% → 36%,56%]
- equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ (42pt, #80b9ff) [36%,28% → 60%,31%]
- equation $=$ (42pt, #80b9ff) [61%,29% → 62%,30%]
- equation $0.5$ (42pt, #80b9ff) [63%,28% → 66%,31%]
- **Builds:** then: equation $\gamma_4 = 0.59$ — apple:dissolve; with previous: image `test-26473.svg` — apple:dissolve; click 1: equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ — apple:dissolve; click 2: equation $0.5$ — slides in; with previous: equation $=$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 156
_(Keynote: Lecture 12, slide 52)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (13pt, #80b9ff) [16%,24% → 23%,25%]
- equation $0.5$ (47pt, #80b9ff) [18%,26% → 21%,29%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- line #ffffff [12%,21% → 12%,93%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [4%,31% → 10%,34%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (14pt, #80b9ff) [23%,24% → 31%,25%]
- equation $0.5$ (42pt, #80b9ff) [26%,26% → 29%,29%]
- image `test-26466.svg` [21%,38% → 75%,96%]
- image `test-26473.svg` [21%,38% → 75%,96%]
- equation $\gamma_3 = 0.62$ (36pt, #d6d6d6) [4%,35% → 10%,38%]
- equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ (14pt, #80b9ff) [32%,24% → 40%,25%]
- equation $0.5$ (42pt, #80b9ff) [35%,27% → 37%,29%]
- image `test-26513.svg` [21%,38% → 75%,96%]
- image `test-26524.svg` [21%,38% → 75%,96%]
- equation $\gamma_4 = 0.59$ (36pt, #d6d6d6) [29%,48% → 36%,52%]
- equation $\gamma_5 = 0.56$ (36pt, #80b9ff) [29%,52% → 36%,56%]
- equation $p(f(\tau) \leq 0.56 \mid f(\tau) \leq 0.59)$ (42pt, #80b9ff) [36%,32% → 60%,35%]
- equation $=$ (42pt, #80b9ff) [61%,33% → 62%,34%]
- equation $0.5$ (42pt, #80b9ff) [63%,32% → 66%,35%]
- **Builds:** then: equation $\gamma_5 = 0.56$ — apple:dissolve; with previous: image `test-26524.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.56 \mid f(\tau) \leq 0.59)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $=$ — apple:dissolve
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 157
_(Keynote: Lecture 12, slide 53)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (13pt, #80b9ff) [16%,24% → 23%,25%]
- equation $0.5$ (47pt, #80b9ff) [18%,26% → 21%,29%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- line #ffffff [12%,21% → 12%,93%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [4%,31% → 10%,34%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (14pt, #80b9ff) [23%,24% → 31%,25%]
- equation $0.5$ (42pt, #80b9ff) [26%,26% → 29%,29%]
- image `test-26466.svg` [21%,38% → 75%,96%]
- image `test-26473.svg` [21%,38% → 75%,96%]
- equation $\gamma_3 = 0.62$ (36pt, #d6d6d6) [4%,35% → 10%,38%]
- image `test-26513.svg` [21%,37% → 75%,96%]
- image `test-26524.svg` [21%,38% → 75%,96%]
- equation $\gamma_4 = 0.59$ (36pt, #d6d6d6) [4%,40% → 10%,43%]
- equation $p(f(\tau) \leq 0.56 \mid f(\tau) \leq 0.59)$ (14pt, #80b9ff) [41%,24% → 49%,25%]
- equation $0.5$ (42pt, #80b9ff) [44%,27% → 46%,29%]
- equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ (14pt, #80b9ff) [32%,24% → 40%,25%]
- equation $0.5$ (42pt, #80b9ff) [35%,27% → 37%,29%]
- equation $p(f(\tau) \leq 0.53 \mid f(\tau) \leq 0.56)$ (42pt, #80b9ff) [36%,32% → 60%,35%]
- equation $=$ (42pt, #80b9ff) [61%,33% → 62%,34%]
- equation $0.5$ (42pt, #80b9ff) [63%,32% → 66%,35%]
- image `test-26565.svg` [21%,38% → 75%,96%]
- image `test-26581.svg` [21%,38% → 75%,96%]
- equation $\gamma_5 = 0.56$ (36pt, #d6d6d6) [29%,48% → 36%,52%]
- equation $\gamma_6 = 0.53$ (36pt, #80b9ff) [29%,52% → 36%,55%]
- **Builds:** then: equation $\gamma_6 = 0.53$ — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.53 \mid f(\tau) \leq 0.56)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $=$ — apple:dissolve; with previous: image `test-26581.svg` — apple:dissolve
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 158
_(Keynote: Lecture 12, slide 54)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- line #ffffff [12%,21% → 12%,93%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [4%,31% → 10%,34%]
- image `test-26466.svg` [21%,38% → 75%,96%]
- image `test-26473.svg` [21%,38% → 75%,96%]
- equation $\gamma_3 = 0.62$ (36pt, #d6d6d6) [4%,35% → 10%,38%]
- image `test-26513.svg` [21%,37% → 75%,96%]
- image `test-26524.svg` [21%,38% → 75%,96%]
- equation $\gamma_4 = 0.59$ (36pt, #d6d6d6) [4%,40% → 10%,43%]
- image `test-26565.svg` [21%,38% → 75%,96%]
- image `test-26581.svg` [21%,38% → 75%,96%]
- equation $\gamma_5 = 0.56$ (36pt, #d6d6d6) [4%,44% → 10%,48%]
- equation $\gamma_6 = 0.53$ (36pt, #d6d6d6) [4%,49% → 10%,52%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (10pt, #80b9ff) [14%,25% → 20%,25%]
- equation $0.5$ (36pt, #80b9ff) [16%,26% → 18%,29%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (11pt, #80b9ff) [20%,24% → 27%,25%]
- equation $0.5$ (33pt, #80b9ff) [23%,26% → 25%,29%]
- equation $p(f(\tau) \leq 0.56 \mid f(\tau) \leq 0.59)$ (11pt, #80b9ff) [34%,24% → 40%,25%]
- equation $0.5$ (33pt, #80b9ff) [36%,27% → 38%,29%]
- equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ (11pt, #80b9ff) [27%,24% → 34%,25%]
- equation $0.5$ (33pt, #80b9ff) [29%,27% → 31%,29%]
- equation $p(f(\tau) \leq 0.53 \mid f(\tau) \leq 0.56)$ (11pt, #80b9ff) [41%,24% → 47%,25%]
- equation $0.5$ (33pt, #80b9ff) [43%,26% → 45%,29%]
- equation $\gamma_7 = 0.49$ (36pt, #d6d6d6) [4%,54% → 10%,57%]
- equation $\gamma_8 = 0.45$ (36pt, #d6d6d6) [4%,58% → 10%,61%]
- equation $\gamma_9 = 0.40$ (36pt, #d6d6d6) [4%,62% → 11%,65%]
- equation $\gamma_{10} = 0.21$ (36pt, #d6d6d6) [3%,66% → 10%,70%]
- equation $\gamma_{11} = 0.11$ (36pt, #d6d6d6) [3%,71% → 10%,74%]
- equation $\gamma_{12} = 0.02$ (36pt, #d6d6d6) [3%,75% → 10%,78%]
- equation $p(f(\tau) \leq 0.49 \mid f(\tau) \leq 0.53)$ (10pt, #80b9ff) [47%,24% → 53%,25%]
- equation $0.5$ (36pt, #80b9ff) [49%,26% → 51%,28%]
- equation $p(f(\tau) \leq 0.45 \mid f(\tau) \leq 0.49)$ (11pt, #80b9ff) [53%,24% → 60%,25%]
- equation $0.5$ (33pt, #80b9ff) [55%,26% → 57%,28%]
- equation $p(f(\tau) \leq 0.21 \mid f(\tau) \leq 0.40)$ (11pt, #80b9ff) [67%,24% → 73%,25%]
- equation $0.5$ (33pt, #80b9ff) [69%,26% → 71%,28%]
- equation $p(f(\tau) \leq 0.40 \mid f(\tau) \leq 0.45)$ (11pt, #80b9ff) [60%,24% → 67%,25%]
- equation $0.5$ (33pt, #80b9ff) [62%,26% → 64%,28%]
- equation $p(f(\tau) \leq 0.11 \mid f(\tau) \leq 0.21)$ (11pt, #80b9ff) [73%,24% → 80%,25%]
- equation $0.5$ (33pt, #80b9ff) [76%,26% → 78%,28%]
- equation $p(f(\tau) \leq 0.02 \mid f(\tau) \leq 0.11)$ (11pt, #80b9ff) [80%,24% → 87%,25%]
- equation $0.5$ (33pt, #80b9ff) [83%,26% → 85%,28%]
- equation $p(f(\tau) \leq 0.0 \mid f(\tau) \leq 0.02)$ (24pt, #80b9ff) [40%,34% → 53%,36%]
- equation $0.92$ (25pt, #80b9ff) [56%,35% → 58%,36%]
- image `test-26748.svg` [21%,38% → 75%,96%]
- image `test-26753.svg` [21%,38% → 75%,96%]
- image `test-26763.svg` [21%,38% → 75%,96%]
- image `test-26769.svg` [21%,38% → 75%,96%]
- image `test-26774.svg` [21%,38% → 75%,96%]
- image `test-26779.svg` [21%,38% → 75%,96%]
- image `test-26787.svg` [21%,38% → 75%,96%]
- equation $\gamma_{13} = 0.00$ (36pt, #80b9ff) [30%,49% → 37%,52%]
- equation $=$ (25pt, #80b9ff) [54%,35% → 55%,36%]
- **Builds:** click 1: image `test-26753.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.49 \mid f(\tau) \leq 0.53)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_7 = 0.49$ — apple:dissolve; click 2: image `test-26763.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.45 \mid f(\tau) \leq 0.49)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_8 = 0.45$ — apple:dissolve; click 3: image `test-26769.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.40 \mid f(\tau) \leq 0.45)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_9 = 0.40$ — apple:dissolve; click 4: image `test-26774.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.21 \mid f(\tau) \leq 0.40)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_{10} = 0.21$ — apple:dissolve; click 5: image `test-26779.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.11 \mid f(\tau) \leq 0.21)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_{11} = 0.11$ — apple:dissolve; click 6: image `test-26787.svg` — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.02 \mid f(\tau) \leq 0.11)$ — apple:dissolve; with previous: equation $0.5$ — apple:dissolve; with previous: equation $\gamma_{12} = 0.02$ — apple:dissolve; click 7: equation $\gamma_{13} = 0.00$ — apple:dissolve; click 8: equation $=$ — apple:dissolve; with previous: equation $p(f(\tau) \leq 0.0 \mid f(\tau) \leq 0.02)$ — apple:dissolve; with previous: equation $0.92$ — apple:dissolve
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 159
_(Keynote: Lecture 12, slide 55)_
- heading (spaced caps) 36pt [35%,5% → 108%,10%]: MULTILEVEL SPLITTING
- image `test-26276.svg` [21%,38% → 75%,96%]
- equation $p_\text{fail} = \prod_{\ell=2}^{n} P(f(\tau) \leq \gamma_{\ell} \mid f(\tau) \leq \gamma_{\ell-1})$ (36pt, #ffffff) [4%,7% → 31%,16%]
- line #ffffff [3%,4% → 31%,18%]
- image `test-26328.svg` [21%,38% → 75%,96%]
- equation $\gamma_1 = \infty$ (36pt, #d6d6d6) [4%,27% → 9%,29%]
- line #ffffff [12%,21% → 12%,93%]
- image `test-26408.svg` [21%,38% → 75%,96%]
- image `test-26419.svg` [21%,38% → 75%,96%]
- equation $\gamma_2 = 0.67$ (36pt, #d6d6d6) [4%,31% → 10%,34%]
- image `test-26466.svg` [21%,38% → 75%,96%]
- image `test-26473.svg` [21%,38% → 75%,96%]
- equation $\gamma_3 = 0.62$ (36pt, #d6d6d6) [4%,35% → 10%,38%]
- image `test-26513.svg` [21%,37% → 75%,96%]
- image `test-26524.svg` [21%,38% → 75%,96%]
- equation $\gamma_4 = 0.59$ (36pt, #d6d6d6) [4%,40% → 10%,43%]
- image `test-26565.svg` [21%,38% → 75%,96%]
- image `test-26581.svg` [21%,38% → 75%,96%]
- equation $\gamma_5 = 0.56$ (36pt, #d6d6d6) [4%,44% → 10%,48%]
- equation $\gamma_6 = 0.53$ (36pt, #d6d6d6) [4%,49% → 10%,52%]
- equation $p(f(\tau) \leq 0.67 \mid f(\tau) \leq \infty)$ (10pt, #80b9ff) [14%,25% → 20%,25%]
- equation $0.5$ (36pt, #80b9ff) [16%,26% → 18%,29%]
- equation $p(f(\tau) \leq 0.62 \mid f(\tau) \leq 0.67)$ (11pt, #80b9ff) [20%,24% → 27%,25%]
- equation $0.5$ (33pt, #80b9ff) [23%,26% → 25%,29%]
- equation $p(f(\tau) \leq 0.56 \mid f(\tau) \leq 0.59)$ (11pt, #80b9ff) [34%,24% → 40%,25%]
- equation $0.5$ (33pt, #80b9ff) [36%,27% → 38%,29%]
- equation $p(f(\tau) \leq 0.59 \mid f(\tau) \leq 0.62)$ (11pt, #80b9ff) [27%,24% → 34%,25%]
- equation $0.5$ (33pt, #80b9ff) [29%,27% → 31%,29%]
- equation $p(f(\tau) \leq 0.53 \mid f(\tau) \leq 0.56)$ (11pt, #80b9ff) [41%,24% → 47%,25%]
- equation $0.5$ (33pt, #80b9ff) [43%,26% → 45%,29%]
- equation $\gamma_7 = 0.49$ (36pt, #d6d6d6) [4%,54% → 10%,57%]
- equation $\gamma_8 = 0.45$ (36pt, #d6d6d6) [4%,58% → 10%,61%]
- equation $\gamma_9 = 0.40$ (36pt, #d6d6d6) [4%,62% → 11%,65%]
- equation $\gamma_{10} = 0.21$ (36pt, #d6d6d6) [3%,66% → 10%,70%]
- equation $\gamma_{11} = 0.11$ (36pt, #d6d6d6) [3%,71% → 10%,74%]
- equation $\gamma_{12} = 0.02$ (36pt, #d6d6d6) [3%,75% → 10%,78%]
- equation $p(f(\tau) \leq 0.49 \mid f(\tau) \leq 0.53)$ (10pt, #80b9ff) [47%,24% → 53%,25%]
- equation $0.5$ (36pt, #80b9ff) [49%,26% → 51%,28%]
- equation $p(f(\tau) \leq 0.45 \mid f(\tau) \leq 0.49)$ (11pt, #80b9ff) [53%,24% → 60%,25%]
- equation $0.5$ (33pt, #80b9ff) [55%,26% → 57%,28%]
- equation $p(f(\tau) \leq 0.21 \mid f(\tau) \leq 0.40)$ (11pt, #80b9ff) [67%,24% → 73%,25%]
- equation $0.5$ (33pt, #80b9ff) [69%,26% → 71%,28%]
- equation $p(f(\tau) \leq 0.40 \mid f(\tau) \leq 0.45)$ (11pt, #80b9ff) [60%,24% → 67%,25%]
- equation $0.5$ (33pt, #80b9ff) [62%,26% → 64%,28%]
- equation $p(f(\tau) \leq 0.11 \mid f(\tau) \leq 0.21)$ (11pt, #80b9ff) [73%,24% → 80%,25%]
- equation $0.5$ (33pt, #80b9ff) [76%,26% → 78%,28%]
- equation $p(f(\tau) \leq 0.02 \mid f(\tau) \leq 0.11)$ (11pt, #80b9ff) [80%,24% → 87%,25%]
- equation $0.5$ (33pt, #80b9ff) [83%,26% → 85%,28%]
- equation $p(f(\tau) \leq 0.0 \mid f(\tau) \leq 0.02)$ (11pt, #80b9ff) [87%,24% → 94%,25%]
- equation $0.92$ (33pt, #80b9ff) [88%,26% → 91%,28%]
- image `test-26748.svg` [21%,38% → 75%,96%]
- image `test-26753.svg` [21%,38% → 75%,96%]
- image `test-26763.svg` [21%,38% → 75%,96%]
- image `test-26769.svg` [21%,38% → 75%,96%]
- image `test-26774.svg` [21%,38% → 75%,96%]
- image `test-26779.svg` [21%,38% → 75%,96%]
- image `test-26787.svg` [21%,38% → 75%,96%]
- equation $\gamma_{13} = 0.00$ (36pt, #d6d6d6) [3%,80% → 10%,83%]
- equation $\times$ (36pt, #ffffff) [20%,27% → 21%,29%]
- equation $\times$ (36pt, #ffffff) [26%,27% → 27%,29%]
- equation $\times$ (36pt, #ffffff) [33%,27% → 34%,29%]
- equation $\times$ (36pt, #ffffff) [40%,27% → 41%,29%]
- equation $\times$ (36pt, #ffffff) [46%,27% → 47%,28%]
- equation $\times$ (36pt, #ffffff) [53%,26% → 54%,28%]
- equation $\times$ (36pt, #ffffff) [59%,27% → 60%,28%]
- equation $\times$ (36pt, #ffffff) [66%,27% → 67%,28%]
- equation $\times$ (36pt, #ffffff) [73%,27% → 74%,28%]
- equation $\times$ (36pt, #ffffff) [80%,27% → 81%,29%]
- equation $\times$ (36pt, #ffffff) [86%,27% → 87%,28%]
- equation $\hat p_\text{fail} = 0.00046$ (36pt, #ffffff) [44%,31% → 56%,35%]
- **Builds:** click 1: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; with previous: equation $\times$ — apple:dissolve; click 2: equation $\hat p_\text{fail} = 0.00046$ — slides in
- **Transition to next:** Magic Move (shared objects glide; others fade)

## Slide 160
_(Keynote: Lecture 12, slide 56)_
- text on a #80b9ff filled box 32pt [7%,24% → 11%,31%]: {1|#000000}
- text on a #80b9ff filled box 32pt [7%,37% → 11%,44%]: {2|#000000}
- line #ffffff [7%,17% → 40%,17%]
- heading (spaced caps) 36pt [13%,25% → 92%,30%]: RATIO OF NORMALIZING CONSTANTS
- heading (spaced caps) 36pt [13%,39% → 87%,43%]: SELF-NORMALIZED IMPORTANCE SAMPLING
- text on a #80b9ff filled box 32pt [7%,51% → 11%,58%]: {3|#000000}
- heading (spaced caps) 36pt [13%,52% → 87%,57%]: BRIDGE SAMPLING
- heading (spaced caps) 50pt [-14%,9% → 62%,15%]: PLAN FOR TODAY
- text on a #80b9ff filled box 32pt [7%,64% → 11%,71%]: {4|#000000}
- heading (spaced caps) 36pt [13%,65% → 86%,70%]: MULTILEVEL SPLITTING
- **Transition to next:** Magic Move (shared objects glide; others fade)
