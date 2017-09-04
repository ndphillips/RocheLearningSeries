---
title       : Fast and Frugal Trees (FFTrees)
subtitle    : Experiences developing a tool to create, visualise, and evaluate a machine learning based classifier model 
author      : Dr. Nathaniel Phillips
job         : Roche EU Learning Series
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---&twocol


## Roche Internship

***=left


- Task: Create an interactive tool for exploring and visualising PRO (Patient Reported Outcome) data. 


<img src="images/pro_cartoon.gif" title="plot of chunk unnamed-chunk-1" alt="plot of chunk unnamed-chunk-1" width="90%" style="display: block; margin: auto;" />


***=right

- Status: Most underlying code for visualizations is complete. To be integrated into Adrian Waddel's Teal framework

### Teal (Adrian Waddell)


<img src="images/tealss.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" width="100%" style="display: block; margin: auto;" />

---

<q>How can people make good decisions based on limited, noisy information?</q>







---  .nobackground

## Limited Time. Limited information.

<br>


<img src="images/threeexamples.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" width="100%" style="display: block; margin: auto;" />


---&twocol .nobackground


## Cook County Hospital, 1996

***=left
<img src="images/crowdedemergency.jpg" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" width="100%" style="display: block; margin: auto;" />

***=right


"As the city’s principal public hospital, Cook County was the place of last resort for the hundreds of thousands of Chicagoans without health insurance. Resources were stretched to the limit. The hospital’s cavernous wards were built for another century. There were no private rooms, and patients were separated by flimsy plywood dividers. [\...] Doctors once trained a homeless man to do routine lab tests because there was no one else available." Malcolm Gladwell, Blink.



---&twocol

## Heart Attack Diagnosis

***=left

<img src="images/paindecision.png" title="plot of chunk unnamed-chunk-6" alt="plot of chunk unnamed-chunk-6" width="60%" style="display: block; margin: auto;" />

***=right

<img src="images/doctordeciding.jpg" title="plot of chunk unnamed-chunk-7" alt="plot of chunk unnamed-chunk-7" width="90%" style="display: block; margin: auto;" />

- In a Michigan hospital, doctors sent 90% of patients to the ICU, although only 25%  were actually having a heart attack.

---&twocol

## Emergency Room Solution: a fast-and-frugal tree (FFT)

***=left

- A fast-and-frugal decision tree (FFT) developed by Green & Mehr (1997).
- Tree cut the false-alarm rate in half
- Tree is transparent, easy to modify, and accepted by physicians (unlike regression).

### What is a fast-and-frugal decision tree (FFT)?

***=right

<img src="images/GreenMehrFFT.png" title="plot of chunk unnamed-chunk-8" alt="plot of chunk unnamed-chunk-8" width="65%" style="display: block; margin: auto;" />

Green & Mehr (1997) "What alters physicians' decisions to admit to the coronary care unit?"


---&twocol

***=left
## Fast-and-Frugal Decision Tree (FFT)

- An FFT is a decision tree with exactly two branches from each node, where one (or in the case of the final node, both) of the branches are exit branches (Martignon et al., 2008)


<!-- #### Descriptive Uses -->

<!-- - Inference (Gigerenzer & Goldstein, 1996) -->
<!-- - Judge's bailing decisions (Dhami, 2003) -->
<!-- - Fish mating (Dugatkin & Godin, 1996) -->

<!-- #### Prescriptive Uses -->

<!-- - Terrorist attacks (Garcia, 2016) -->
<!-- - Bank failure (Neth et al., 2014) -->
<!-- - Depression diagnosis (Jenny et al., 2013) -->

<img src="images/martignon2008_ss.png" title="plot of chunk unnamed-chunk-9" alt="plot of chunk unnamed-chunk-9" width="100%" style="display: block; margin: auto;" />



***=right

### An example FFT
<img src="images/heartfft.png" title="plot of chunk unnamed-chunk-10" alt="plot of chunk unnamed-chunk-10" width="80%" style="display: block; margin: auto;" />

- Easily communicated.
- Fast to implement
- Requires little information


---
## Why a simple algorithm?


<img src="images/simplevcomplex.png" title="plot of chunk unnamed-chunk-11" alt="plot of chunk unnamed-chunk-11" width="80%" style="display: block; margin: auto;" />





---





<img src="figure/unnamed-chunk-13-1.png" title="plot of chunk unnamed-chunk-13" alt="plot of chunk unnamed-chunk-13" width="90%" style="display: block; margin: auto;" />




---

<img src="figure/unnamed-chunk-14-1.png" title="plot of chunk unnamed-chunk-14" alt="plot of chunk unnamed-chunk-14" width="90%" style="display: block; margin: auto;" />


---

<img src="figure/unnamed-chunk-15-1.png" title="plot of chunk unnamed-chunk-15" alt="plot of chunk unnamed-chunk-15" width="90%" style="display: block; margin: auto;" />






---

<img src="figure/unnamed-chunk-16-1.png" title="plot of chunk unnamed-chunk-16" alt="plot of chunk unnamed-chunk-16" width="90%" style="display: block; margin: auto;" />



---

<img src="figure/unnamed-chunk-17-1.png" title="plot of chunk unnamed-chunk-17" alt="plot of chunk unnamed-chunk-17" width="90%" style="display: block; margin: auto;" />



---

## Weapons of Math Destruction


![asdf](images/oneilted.png)

---

## Weapons of Math Destruction

> Algorithms are opinions embedded in code. [Most people think] algorithms are objective and true and scientific. That's a marketing trick. It's also a marketing trick to intimidate you with algorithms, to make you trust and fear algorithms because you trust and fear mathematics. A lot can go wrong when we put blind faith in big data.

> When [algorithms] are secret, important and destructive, I've coined a term for these algorithms:  <span class = 'red'>Weapons of math desctruction</span>
 
 
- Cathy O'Neil 
<img src="images/oneilted.png" title="plot of chunk unnamed-chunk-18" alt="plot of chunk unnamed-chunk-18" width="40%" style="display: block; margin: auto;" />


--- &twocol

## Weapons of Math Destruction

***=left

<br>

Getting a car to drive [autonomously] was an impressive feat. But it’s also a bit unsettling, since it isn’t completely clear how the car makes its decisions. [..] [W]hat if one day it did something unexpected—crashed into a tree, or sat at a green light? [...] The system is so complicated that even the engineers who designed it may struggle to isolate the reason for any single action. 

~ Will Knight, MIT Technology Review, April 2017

***=right

<img src="images/darksecretcar.png" title="plot of chunk unnamed-chunk-19" alt="plot of chunk unnamed-chunk-19" width="60%" style="display: block; margin: auto;" />



--- &twocol

## Weapons of Math Destruction

***=left


**Whether it’s an investment decision, a medical decision, or maybe a military decision, you don’t want to just rely on a ‘black box’ method**.” ~ Tommi Jaakkola, MIT professor of machine learning

<br>
<br>

### What is the alternative to a black box algorithm?

***=right

<img src="images/jaakkola.jpg" title="plot of chunk unnamed-chunk-20" alt="plot of chunk unnamed-chunk-20" width="80%" style="display: block; margin: auto;" />


--- &twocol

## Simple Heuristics that make us smart

***=left


Rather than using black box algorithms we can use simple heuristics


<img src="images/gigerenzer.jpg" title="plot of chunk unnamed-chunk-21" alt="plot of chunk unnamed-chunk-21" width="80%" style="display: block; margin: auto;" />

"The mind can use less information and computation or take less time and nevertheless achieve better performance." ~ Gigerenzer & Brighton, 2009


***=right

<img src="images/simpleheuristicscover.png" title="plot of chunk unnamed-chunk-22" alt="plot of chunk unnamed-chunk-22" width="80%" style="display: block; margin: auto;" />

--- &twocol

## Catching a Ball

***=left

### Complex


"A baseball outfielder behaves as if he had solved a set of differential equations in predicting the trajectory of the ball [...] something functionally equivalent to the mathematical calculations is going on" (Dawkins, 1989)

<img src="images/baseballequation.jpg" title="plot of chunk unnamed-chunk-23" alt="plot of chunk unnamed-chunk-23" width="80%" style="display: block; margin: auto;" />


***=right

### Heuristic


Gaze Heuristic (Gigerenzer, 2007)

1. Fix your gaze on the ball
2. Start running
2. Adjust your running speed so that the angle of gaze remains constant.

<img src="images/gazeheuristic.jpg" title="plot of chunk unnamed-chunk-24" alt="plot of chunk unnamed-chunk-24" width="70%" style="display: block; margin: auto;" />


--- &twocol

## Investment

***=left

### Complex

Nobel prize winning Harry Markowitz model: 

Selects the most efficient portfolio by analyzing various possible portfolios of different securities

<img src="images/riskreturngraph.jpg" title="plot of chunk unnamed-chunk-25" alt="plot of chunk unnamed-chunk-25" width="100%" style="display: block; margin: auto;" />


***=right

### Heuristic

1 / N Heuristic: 

Equally distribute funds across all N assets

<br>

<img src="images/pie.png" title="plot of chunk unnamed-chunk-26" alt="plot of chunk unnamed-chunk-26" width="70%" style="display: block; margin: auto;" />


--- &twocol

## Investment

***=left

### Complex


Nobel prize winning Harry Markowitz model:

Selects the most efficient portfolio by analyzing various possible portfolios of different securities

<img src="images/riskreturngraph.jpg" title="plot of chunk unnamed-chunk-27" alt="plot of chunk unnamed-chunk-27" width="100%" style="display: block; margin: auto;" />


***=right

### Heuristic


1 / N Heuristic: 

Equally distribute funds across N assets

<br>

<img src="images/markowitzpie.png" title="plot of chunk unnamed-chunk-28" alt="plot of chunk unnamed-chunk-28" width="70%" style="display: block; margin: auto;" />



--- &twocol

***=left

## Why Heuristics?

<br>

<br>


- Discover and tell meaningful stories from your data.

- Focus on what is important, ignore what is not.

- Give a realistic assessment of uncertainty and risk.
    - i.e.; No overfitting


***=right

<br>


<img src="images/simplicitymaze.png" title="plot of chunk unnamed-chunk-29" alt="plot of chunk unnamed-chunk-29" width="80%" style="display: block; margin: auto;" />


<br>

<i>Simplicity is the ultimate sophistication</i> ~ Leonardo da Vinci

<br>

*The art of being wise is the art of knowing what to overlook* ~ William James


<br>

<!-- > If [an algorithm] that measures up very well on the performance criterion is nevertheless totally incomprehensible to a human expert, can it be described as knowledge? Under the common-sense definition of this term […] it is not ~ Quinlan (1999) -->


---&twocol
## FFTrees

***=left

- A toolbox to create fast-and-frugal decision trees (FFTs) for binary classification decisions.

- Any kind of data.

- Minimal to no programming, extensive examples and guides. 

<img src="images/FFTrees_Logo.jpg" title="plot of chunk unnamed-chunk-30" alt="plot of chunk unnamed-chunk-30" width="60%" style="display: block; margin: auto;" />


***=right

### Manuscript

- Phillips, Neth, Woike & Gaissmaier. (2017). FFTrees: A toolbox to create, visualize, and evaluate fast-and-frugal decision trees.

<img src="images/FFTManuscriptP2.png" title="plot of chunk unnamed-chunk-31" alt="plot of chunk unnamed-chunk-31" width="100%" style="display: block; margin: auto;" />







---
## Tutorial and Documentation

<img src="images/FFTrees_Tutorial_SS.png" title="plot of chunk unnamed-chunk-32" alt="plot of chunk unnamed-chunk-32" width="90%" style="display: block; margin: auto;" />


---

## Example: Heart Disease



| age| sex|cp | trestbps| chol| fbs|restecg     | thalach| exang| oldpeak|slope | ca|thal   | diagnosis|
|---:|---:|:--|--------:|----:|---:|:-----------|-------:|-----:|-------:|:-----|--:|:------|---------:|
|  63|   1|ta |      145|  233|   1|hypertrophy |     150|     0|     2.3|down  |  0|fd     |         0|
|  67|   1|a  |      160|  286|   0|hypertrophy |     108|     1|     1.5|flat  |  3|normal |         1|
|  67|   1|a  |      120|  229|   0|hypertrophy |     129|     1|     2.6|flat  |  2|rd     |         1|
|  37|   1|np |      130|  250|   0|normal      |     187|     0|     3.5|down  |  0|normal |         0|
|  41|   0|aa |      130|  204|   0|hypertrophy |     172|     0|     1.4|up    |  0|normal |         0|
|  56|   1|aa |      120|  236|   0|normal      |     178|     0|     0.8|up    |  0|normal |         0|


### Goal: Predict binary diagnosis classification



---

## The FFTrees() function


```r
# Step 1: Install and load FFTrees (v.1.3.2)
install.packages("FFTrees")
library("FFTrees")

# Step 2: Create FFTs
heart.fft <- FFTrees(formula = diagnosis ~.,  # Formula
                     data = heart.train,      # Training data
                     data.test = heart.test,  # Test data
                     main = "Heart Disease",  # Optional labels
                     decision.labels = c("Low-Risk", "High-Risk"))
```


---


```r
plot(heart.fft, data = "test")  # Training data
```

<img src="figure/unnamed-chunk-35-1.png" title="plot of chunk unnamed-chunk-35" alt="plot of chunk unnamed-chunk-35" width="55%" style="display: block; margin: auto;" />



--- &twocol

## Example: Diagnosing muscle disorders


***=left


- Problem: How to diagnose children as having one of two muscle disorders?

- Data: 147 children with ~ 10 different medical measurements.

- Collaboration between Dr. Patricia Haefner (University of Basel) and Matthew Pitt (NHS, UK)

<img src="images/backmuscles.jpg" title="plot of chunk unnamed-chunk-36" alt="plot of chunk unnamed-chunk-36" width="50%" style="display: block; margin: auto;" />


***=right

### Muscle Disorder FFT

<img src="images/muscledisordersfft.png" title="plot of chunk unnamed-chunk-37" alt="plot of chunk unnamed-chunk-37" width="100%" style="display: block; margin: auto;" />

---&twocol

## Additional FFTrees features

***=left

- Specify a tree directly 'in words'


```r
my.tree = 
'If age > 50, predict FALSE.
 If sex = {m}, predict TRUE.
 If ca > 1, predict TRUE, otherwise, FALSE')
```

- Give differential weight to sensitivity (avoiding misses) and specificity (avoiding false-alarms)
- Incorporate cue costs in evaluating and/or building trees.

***=right


<img src="images/medicaltestcost.jpg" title="plot of chunk unnamed-chunk-39" alt="plot of chunk unnamed-chunk-39" width="60%" style="display: block; margin: auto;" />



<img src="images/roc.jpg" title="plot of chunk unnamed-chunk-40" alt="plot of chunk unnamed-chunk-40" width="70%" style="display: block; margin: auto;" />




---
## ShinyFFTrees

- A point-and click (no programming), web-based version of FFTrees with around 90% of the functionality of FFTrees
- Link: http://econpsychbasel.shinyapps.io/ShinyFFTrees/

<img src="images/shinyfftrees_ss.png" title="plot of chunk unnamed-chunk-41" alt="plot of chunk unnamed-chunk-41" width="50%" style="display: block; margin: auto;" />



---

<q>How well can simple FFTs compete with classical rational models and cutting-edge machine learning algorithms?</q>


---&twocol

***=left

## Prediction Simulation
<br>
<br>

- 10 datasets from the UCI Machine Learning Database.
- 50% Training, 50% Testing
- FFTrees vs rpart, regression, random forests...
- Criterion: Balanced accuracy
    - `mean(sensitivity, specificity)`

***=right

<img src="images/datacollage.png" title="plot of chunk unnamed-chunk-42" alt="plot of chunk unnamed-chunk-42" width="90%" style="display: block; margin: auto;" />



<!-- --- -->
<!-- ```{r out.width = "60%", echo = FALSE} -->
<!-- titanic.fft <- FFTrees(survived ~., data = titanic, main = "Titanic", decision.labels = c("Died", "Survived")) -->
<!-- plot(titanic.fft) -->
<!-- ``` -->



<!-- --- -->

<!-- ```{r out.width = "60%", echo = FALSE, message = FALSE, warning = FALSE} -->
<!-- set.seed(100) -->
<!-- forestfires$area <- forestfires$area > 0 -->
<!-- forest.fft <- FFTrees(area ~., data = forestfires, main = "Forest Fires", decision.labels = c("None", "Fire"), train.p = .5) -->
<!-- plot(forest.fft, "train") -->
<!-- ``` -->

<!-- --- -->

<!-- ```{r out.width = "60%", echo = FALSE} -->
<!-- plot(forest.fft, "test") -->
<!-- ``` -->


<!-- --- -->

<!-- ```{r out.width = "60%", echo = FALSE} -->
<!-- plot(forest.fft, what = "cues") -->
<!-- ``` -->



--- .class #id 
## Prediction Accuracy

<img src="figure/unnamed-chunk-43-1.png" title="plot of chunk unnamed-chunk-43" alt="plot of chunk unnamed-chunk-43" width="80%" style="display: block; margin: auto;" />



--- .class #id 

<img src="images/MLR_Simulation_Trees.jpg" title="plot of chunk unnamed-chunk-44" alt="plot of chunk unnamed-chunk-44" width="72%" style="display: block; margin: auto;" />




--- .class #id 
## Speed and frugality


<img src="figure/unnamed-chunk-45-1.png" title="plot of chunk unnamed-chunk-45" alt="plot of chunk unnamed-chunk-45" width="60%" style="display: block; margin: auto;" />


--- .class #id 
## Speed and frugality


<img src="figure/unnamed-chunk-46-1.png" title="plot of chunk unnamed-chunk-46" alt="plot of chunk unnamed-chunk-46" width="60%" style="display: block; margin: auto;" />





---
<img src="figure/unnamed-chunk-47-1.png" title="plot of chunk unnamed-chunk-47" alt="plot of chunk unnamed-chunk-47" width="60%" style="display: block; margin: auto;" />



---
<img src="figure/unnamed-chunk-48-1.png" title="plot of chunk unnamed-chunk-48" alt="plot of chunk unnamed-chunk-48" width="60%" style="display: block; margin: auto;" />






---&twocol

## Conclusion

***=left

- I have personally been amazed by how well fast-and-frugal trees can predict data.

- Try FFTrees, you might be surprised by how well it works, and generate meaningful insights.

- When using an algorithm, ask yourself two questions:

    - "What did I learn from an algorithm that I didn't know before?"
    - "If, suddenly, the algorithm consistently fails, will I be able to know why?"

***=right


<img src="figure/unnamed-chunk-49-1.png" title="plot of chunk unnamed-chunk-49" alt="plot of chunk unnamed-chunk-49" width="100%" style="display: block; margin: auto;" />


---&twocol

## Thank you!

***=left

Email: Nathaniel.D.Phillips.is@gmail.com

Website: http://ndphillips.github.io

FFTrees R package:

- `install.packages("FFTrees")`

ShinyFFTrees: https://econpsychbasel.shinyapps.io/ShinyFFTrees


***=right


<img src="figure/unnamed-chunk-50-1.png" title="plot of chunk unnamed-chunk-50" alt="plot of chunk unnamed-chunk-50" width="100%" style="display: block; margin: auto;" />




---
## FFTrees


<img src="images/fftreeshex.png" title="plot of chunk unnamed-chunk-51" alt="plot of chunk unnamed-chunk-51" width="100%" style="display: block; margin: auto;" />



---

## Why simple algorithms?

- Simple algorithms can tell compelling stories. Black box algorithms don't.







--- 

## Less Is more


<img src="images/londontemp_A.png" title="plot of chunk unnamed-chunk-52" alt="plot of chunk unnamed-chunk-52" width="100%" style="display: block; margin: auto;" />


--- 

## Less Is more

<img src="images/londontemp_B.png" title="plot of chunk unnamed-chunk-53" alt="plot of chunk unnamed-chunk-53" width="100%" style="display: block; margin: auto;" />

--- 

## Less Is more

<img src="images/londontemp_C.png" title="plot of chunk unnamed-chunk-54" alt="plot of chunk unnamed-chunk-54" width="100%" style="display: block; margin: auto;" />

