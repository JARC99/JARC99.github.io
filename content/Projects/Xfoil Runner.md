---
date: 2026-09-28
draft: false
---

Back when I was starting work in my capstone project I decided I wanted to use some metaheuristic optimization techniques to design at least some parts of the aircraft. I had recently read [Aircraft Aerodynamic Design: Geometry and Optimization](https://www.google.de/books/edition/Aircraft_Aerodynamic_Design/wqTCBwAAQBAJ?hl=en&gbpv=0) from  András Sóbester and Alexander I. J. Forrester, a great book altogether and for me a gret source of inspiration.

One of the optimization routines I ended up implementing was a genetic algorithm to optimize the airfoils of all lifting surfaces based on the parameterized NACA-4 digit series of airfoils. In order to evaluate the fitness of the individuals during the optimization process I decided to use Mark Drela's [Xfoil](https://web.mit.edu/drela/Public/web/xfoil/) panel solver to evaluate the performance of each airfoil at the expected flight conditions. Since I was running all the optimization process using a Python script I needed a way to call Xfoil from within Python in order to automate, the process. That was the motivation behind this short Python script whose GitHub repository can be found [here](https://github.com/JARC99/xfoil-runner).

I even ended up making a short tutorial video explaining its use:
![](https://www.youtube.com/watch?v=zGZin_PPLdc&t=4s)