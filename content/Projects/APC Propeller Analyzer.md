---
date: 2026-09-28
draft: false
---

During the last semesters of my bachelor studies I often encountered the need to compare propeller performance for electric propulsion systems for small aircraft. Although many tools existed to both design and size power train systems as a whole, I was mostly interested in understanding the performance of propellers individually before integrating them into the overall system design.

As my theoretical basis I was able to find a pretty good book dedicated only to fixed pitch propellers, with the small caveat that it was approaching the 90 year mark since its publishing (incidentally the last time fixed-pitch propellers were a dominant means of propulsion). Fred E. Weick's [Aircraft Propeller Design](https://openlibrary.org/books/OL6751986M/Aircraft_propeller_design) is nevertheless a very informative and also historically interesting read. Armed with the teachings of this historical document I was better prepared to compare all the performance plots I could find.

The obvious issue becomes then, where to find good performance plots for small propellers meant up to until recently for model aircraft rather than full on engineering systems. Luckily, one of the main suppliers of propellers we used in my university, [APC propellers](https://www.apcprop.com/) publishes an extensive simulation data set for all the propellers they sell. These data files have some caveats, some parsing needs to be done to bring them into what I would call a useful format and if you are part of the globalized world and prefer to work in the metric system, most units need to be converted as well.

Most of the scripts in this [repository](https://github.com/JARC99/apc-prop-analyzer) are centered in these tasks. Once developed I was able to put them to work in both my capstone project and during the design of out SAE Aero Design aircraft with good results, if I may say so myself.

Here is an example of the types of performance plots you can generate using the scripts:
![[Pasted image 20260928170934.png]]
