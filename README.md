# Website Optimization project
====================================
### How I set up the working environment for this project:
  1. Cloned original repo from https://github.com/udacity/frontend-nanodegree-mobile-portfolio
  2. Opted for GitHub pages in order to host the web site for analysis: https://oearikan.github.io/website-optimization-project/ (I find the incorporation of extra tools such as ngrok, grunt, gulp etc... distracting while I'm already struggling to learn a new skill, so I avoid them whenever I can. However, I appreciate that time will come that I'll find them handy. Just taking my time)
  
**Important Note:** Since at the time of me working on this project, *Timeline* tool was deprecated in favor of *Performance* tool by Google chrome, it felt a little off. Also possible due to updates happening since the time of recording, bits of code were not running as they were supposed to. For instance, my pizzas never moved since the beginning.

### Objective 1: PageSpeed Score
- Initial Score => Mobile: Poor(27/100); Desktop: Poor(29/100)
- Below you can find each action taken and corresponding effect on the score. Changes were made to ```index.html``` when necessary (see comments in this file for exact changes):

|Change|Mobile|Desktop|
|------|---------|-----|
|Initial score|27/100|29/100|
|Changed *pizzeria.jpg* with a lower resolution *pizzeria_oea.jpg*| 68/100|79/100|
|Commented out the google web fonts as suggested by CP|72/100|81/100|
|Further compressed images at pizzeria and profilepic (provided by google pagespeed Insigt service)|77/100|90/100|
|Asynced the google analytics script; added ```media = 'print' ``` in front of *print.css*|87/100|94/100|
|Inlined entire CSS|95/100|96/100|

- I stop at this point although several other optimization steps are recommended.

### Objective 2: Getting Rid of Jank

- All the changes are made to ```views/js/main.js``` file for the *Frame rate* and *Computational efficiency* part. Please see the *comments in code* itself to see what the exact changes were.

##### 2.1: Frame Rate
- Optimized the ```updatePositions()``` function.
- Reduced the number of moving pizzas from 200 to 48 which are created once the page loads.

##### 2.2: Computational Efficiency
- Optmized the ```changePizzaSizes()``` function.
