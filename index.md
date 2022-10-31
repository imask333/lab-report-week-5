**grep**


## 1. grep -l ##

Example 1:
```
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -l "base pair" technich/docsearch$ al/plos/*.txt > plos-results.txt        
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ sort plos-results.txt      
technical/plos/journal.pbio.0020190.txt 
technical/plos/journal.pbio.0020223.txt 
```
This lines searches in all the files in the technical/plos/*.txt path to see if any string in each file contains the "base pair", then it moves the matching files to a new file called plos-results.txt. the sort returns the found files in order to how many line(s) each file has that matches the "base pair", bottom to top implicated low to high lines each file contains; for example: ournal.pbio.0020223.txt has 1 line that contains "base pair" while journal.pbio.0020190.txt has two. It's useful to find keywords, and to compare the definitions of them. 

Example 2:
```
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -l "base pair" technical/9
11report/*.txt >911report.txt
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ sort 911report.txt
```
Searches for "base pair" in all the files in 911report, and if there's any, put them in a new file called 911report.txt, but the result returns nothing since no files in it contains "base pair". This is useful when we want to find a keyword or a definition much faster, like ctrl+f. 

Example 3:
~~~
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -l "Indiana" technical/government/About_LSC/*.txt > government.txt  
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ sort government.txt
technical/government/About_LSC/Comments_on_semiannual.txt
technical/government/About_LSC/Progress_report.txt
technical/government/About_LSC/Special_report_to_congress.txt
technical/government/About_LSC/State_Planning_Report.txt
technical/government/About_LSC/State_Planning_Special_Report.txt
technical/government/About_LSC/Strategic_report.txt
technical/government/About_LSC/commission_report.txt
technical/government/About_LSC/conference_highlights.txt
~~~
This searches for the term "Indiana" in all txt files of About_LSC and puts all of them into a new file called government.txt. It then sorts them from least to most lines that contain "Indinana" from bottom to top. It's useful for searching info about "Indiana".

## 2. grep -c ##
Example 1:
grep -c
~~~
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -c "characteristics" techn
ical/biomed//1471-2202-3-20.txt
2
~~~
This is printing out the number of liens that match the given string "characteristics", which is 2. Grep- c is useful for diplaying the count of number of matches. 

Example 2:
~~~
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -c "Antihypertensive" technical/biomed/1468-6708-3-7.txt              ihypertensive" technical/biomed/1468-6708-3-7.txt 
2
~~~
grep-c prints out the lines in technical/biomed/1468-6708-3-10.txt that match with "Antihypertensive", which is 2. 

Example 3:
~~~
h/docsearch$ grep -c "2001" technical/911report/*.txt
technical/911report/chapter-1.txt:5     
technical/911report/chapter-10.txt:5    
technical/911report/chapter-11.txt:17   
technical/911report/chapter-12.txt:8    
technical/911report/chapter-13.1.txt:2  
technical/911report/chapter-13.2.txt:286technical/911report/chapter-13.3.txt:91 
technical/911report/chapter-13.4.txt:305technical/911report/chapter-13.5.txt:407technical/911report/chapter-2.txt:1     
technical/911report/chapter-3.txt:12    
technical/911report/chapter-5.txt:5     
technical/911report/chapter-6.txt:26    
technical/911report/chapter-7.txt:42    
technical/911report/chapter-8.txt:41    
technical/911report/chapter-9.txt:5     
technical/911report/preface.txt:2     
~~~
grep-c prints out all the lines in all the files .txt in 911report that contain "2001"

## 3: grep -n  ##

Example 1:
~~~
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -n "2001" technical/911report/preface.txt
11:                September 11, 2001, was a day of unprecedented shock and suffering in the history of
18:                relating to the terrorist attacks of September 11, 2001," including those relating
~~~
grep - n shows the line number of file technical/911/preface.txt that contain "2001", which are line 11 and line 18.

Example 2:
~~~
phtn33@DESKTOP-VOADGL0:/mnt/c/Users/phanh/docsearch$ grep -n "MAdCAM-1" technical/biomed/*.txt
technical/biomed/1471-230X-1-5.txt:6:   
     MAdCAM-1 is a 60 kD endothelial cell adhesion molecule
technical/biomed/1471-230X-1-5.txt:8:   
     gut, and in Peyers patches. MAdCAM-1 is expressed basally
technical/biomed/1471-230X-1-5.txt:11:  
      Crohn's disease, MAdCAM-1 acts as 
the main ligand for
technical/biomed/1471-230X-1-5.txt:15:  
      support an absolute requirement for both MAdCAM-1 and a4b7
technical/biomed/1471-230X-1-5.txt:16:  
      in the production of immune models of colitis. MAdCAM-1 is
technical/biomed/1471-230X-1-5.txt:20:  
      MAdCAM-1 are still not well understood. However, since
technical/biomed/1471-230X-1-5.txt:21:  
      MAdCAM-1 is induced by Th1 cytokines, like TNF-α and IL-1b,
technical/biomed/1471-230X-1-5.txt:39:  
      Here, we examine the induction of 
MAdCAM-1 by TNF-α, and
technical/biomed/1471-230X-1-5.txt:44:  
      or eNOS), does not significantly influence MAdCAM-1
technical/biomed/1471-230X-1-5.txt:46:  
      donors can potently inhibit the expression of MAdCAM-1 and
technical/biomed/1471-230X-1-5.txt:81:  
        MAdCAM-1 message in response to 
TNF-α and blockers was
technical/biomed/1471-230X-1-5.txt:105: 
         normalize mRNA levels, the density of the MAdCAM-1 and
technical/biomed/1471-230X-1-5.txt:114: 
         MAdCAM-1 densities were determined using the Instat™
technical/biomed/1471-230X-1-5.txt:137: 
         Jolla, CA). The density of MAdCAM-1 staining was measured
technical/biomed/1471-230X-1-5.txt:142: 
         of density. Significant changes in MAdCAM-1 densities
technical/biomed/1471-230X-1-5.txt:177: 
         addressin-1 (MAdCAM-1), as well as VCAM-1, L-selectin and
technical/biomed/1471-230X-1-5.txt:206: 
         Effect of NO on MAdCAM-1 in SVEC
technical/biomed/1471-230X-1-5.txt:208: 
         TNF-α-induced MAdCAM-1 message 
in SVEC by RT-PCR. Figure
technical/biomed/1471-230X-1-5.txt:210: 
         amplify the first and second IgG-like domain of MAdCAM-1
technical/biomed/1471-230X-1-5.txt:211: 
         [ 7]. A strong band is detected as MAdCAM-1 transcript
technical/biomed/1471-230X-1-5.txt:214: 
         (20 ng/ml, 12 h) induced MAdCAM-1 transcript (37.3% of
technical/biomed/1471-230X-1-5.txt:219: 
         TNF-α induces MAdCAM-1 protein 
expression which is
technical/biomed/1471-230X-1-5.txt:221: 
         TNF-α (20 ng/ml) induced MAdCAM-1 expression is
technical/biomed/1471-230X-1-5.txt:224: 
         significantly reduces MAdCAM-1 
expression at 100 and 1000
technical/biomed/1471-230X-1-5.txt:226: 
         significantly reduced MAdCAM-1 
at a only 1/10 the
technical/biomed/1471-230X-1-5.txt:227: 
         concentration of SperNO needed 
to reduce MAdCAM-1
technical/biomed/1471-230X-1-5.txt:229: 
         MAdCAM-1 expresssion).
technical/biomed/1471-230X-1-5.txt:243: 
         TNF-α induced MAdCAM-1 expression
technical/biomed/1471-230X-1-5.txt:244: 
         TNF-α induced MAdCAM-1 was not 
affected by either a
technical/biomed/1471-230X-1-5.txt:250: 
         Adhesion of a4b7 expressing lymphocytes to MAdCAM-1
technical/biomed/1471-230X-1-5.txt:253: 
         regulation of MAdCAM-1 expression by endothelial cells,
technical/biomed/1471-230X-1-5.txt:261: 
         monolayers with anti-MAdCAM-1 antibody. MAdCAM-1 antibody
technical/biomed/1471-230X-1-5.txt:264: 
         lymphocyte adhesion in this model was MAdCAM-1 dependent.
technical/biomed/1471-230X-1-5.txt:286: 
       glycoprotein, the mucosal vascular addressin MAdCAM-1 [ 12,
technical/biomed/1471-230X-1-5.txt:288: 
       MAdCAM-1 is expressed on endothelial cells in mesenteric
technical/biomed/1471-230X-1-5.txt:291: 
       expression of MAdCAM-1 on murine 
endothelial cells can be
technical/biomed/1471-230X-1-5.txt:293: 
       MAdCAM-1 has also been detected at high levels on colonic
technical/biomed/1471-230X-1-5.txt:297: 
       integrin on a subset of T cells, 
with its ligand, MAdCAM-1,
technical/biomed/1471-230X-1-5.txt:303: 
       MAdCAM-1/B7 integrin bond is essential to produce colitis.
technical/biomed/1471-230X-1-5.txt:307: 
       recipient animals with either MAdCAM-1, or α4β7 specific
technical/biomed/1471-230X-1-5.txt:311: 
       MAdCAM-1 expression in IBD, and likely that the control of
technical/biomed/1471-230X-1-5.txt:312: 
       MAdCAM-1 expression may be an effective potential treatment
technical/biomed/1471-230X-1-5.txt:357: 
       In this present study, we investigated how MAdCAM-1
technical/biomed/1471-230X-1-5.txt:363: 
       significantly reduce TNF-α-induced expression of MAdCAM-1
technical/biomed/1471-230X-1-5.txt:366: 
       nuclear translocation of NF-kB. The MAdCAM-1 promoter has
technical/biomed/1471-230X-1-5.txt:368: 
       induce MAdCAM-1 expression. Both 
a short and long acting NO
technical/biomed/1471-230X-1-5.txt:369: 
       donor blocked MAdCAM-1 induction, but the slow-releasing NO
technical/biomed/1471-230X-1-5.txt:392: 
       mediated MAdCAM-1 regulation by cytokines. [ 35] have
technical/biomed/1471-230X-1-5.txt:401: 
       MAdCAM-1 in IBD and design effective therapies to treat
technical/biomed/1471-230X-1-5.txt:410: 
       MAdCAM-1 (mucosal addressin cell 
adhesion
technical/biomed/1471-230X-3-3.txt:15:  
      expression of ECAMs like ICAM-1, VCAM-1, and MAdCAM-1
technical/biomed/1471-230X-3-3.txt:21:  
      MAdCAM-1, the mucosal cell adhesion molecule, is thought to
technical/biomed/1471-230X-3-3.txt:23:  
      inflammation. MAdCAM-1 is normally expressed in the gut,
technical/biomed/1471-230X-3-3.txt:26:  
      increased appearance of MAdCAM-1 in IBD is supported by
technical/biomed/1471-230X-3-3.txt:28:  
      either MAdCAM-1 or its ligand, the α4β7 integrin, attenuate
technical/biomed/1471-230X-3-3.txt:33:  
      the literature suggests that MAdCAM-1 is probably
technical/biomed/1471-230X-3-3.txt:38:  
      especially that of MAdCAM-1, might help to devise improved
technical/biomed/1471-230X-3-3.txt:63:  
      block the expression of MAdCAM-1 in response to TNF-α, and
technical/biomed/1471-230X-3-3.txt:68:  
      through an IL-10 expression vector attenuates MAdCAM-1
technical/biomed/1471-230X-3-3.txt:129: 
         powder in PBS). Primary rat anti-mouse MAdCAM-1 mAb was
technical/biomed/1471-230X-3-3.txt:137: 
         (Amersham, La Jolla, CA). The density of MAdCAM-1
technical/biomed/1471-230X-3-3.txt:157: 
         mucosal addressin-1 (MAdCAM-1), as well as VCAM-1,
technical/biomed/1471-230X-3-3.txt:160: 
         at least 50% MAdCAM-1 dependent [ 41 ] . SVEC monolayers
technical/biomed/1471-230X-3-3.txt:206: 
         MAdCAM-1 expression in IL-10 gene transfected
technical/biomed/1471-230X-3-3.txt:211: 
         adhesion molecule MAdCAM-1 induced by TNF-α (1 ng/ml, 24
technical/biomed/1471-230X-3-3.txt:212: 
         h). TNF-α strongly induced expression of MAdCAM-1. This
technical/biomed/1471-230X-3-3.txt:215: 
         had no effect on MAdCAM-1 expression.
technical/biomed/1471-230X-3-3.txt:222: 
         endothelial MAdCAM-1 induction, we next examined the
technical/biomed/1471-230X-3-3.txt:236: 
       MAdCAM-1 is a 60 kDa endothelial 
cell surface molecule
technical/biomed/1471-230X-3-3.txt:240: 
       MAdCAM-1 has also been reported in the brain, and in the
technical/biomed/1471-230X-3-3.txt:242: 
       suggested that MAdCAM-1 might play roles in chronic
technical/biomed/1471-230X-3-3.txt:244: 
       With respect to inflammatory bowel disease, MAdCAM-1
technical/biomed/1471-230X-3-3.txt:247: 
       Since MAdCAM-1 is normally expressed mainly within the gut
technical/biomed/1471-230X-3-3.txt:249: 
       it has been suggested that increased MAdCAM-1 expression
technical/biomed/1471-230X-3-3.txt:253: 
       directed against either MAdCAM-1, or its lymphocyte ligand,
technical/biomed/1471-230X-3-3.txt:299: 
       expression of MAdCAM-1, and also 
blocks lymphocyte adhesion
technical/biomed/1471-230X-3-3.txt:302: 
       Interestingly, the low basal levels of MAdCAM-1 expressed
technical/biomed/1471-230X-3-3.txt:305: 
       of MAdCAM-1, is IL-10 independent, while cytokine
technical/biomed/1471-230X-3-3.txt:306: 
       stimulated MAdCAM-1
technical/biomed/1471-230X-3-3.txt:336: 
       binding mediated by TNF-α induced MAdCAM-1 expression. In
technical/biomed/1471-230X-3-3.txt:338: 
       efficiently blocked TNF-α induced MAdCAM-1 expression and
technical/biomed/1471-230X-3-3.txt:341: 
       several ECAMs including ICAM-1, VCAM-1 and MAdCAM-1 [ 60 ]
technical/biomed/1471-230X-3-3.txt:346: 
       through ICAM-1 as well MAdCAM-1, 
but not VCAM-1, since an
technical/biomed/1471-230X-3-3.txt:347: 
       antibody against MAdCAM-1 reduced adhesion to 27 ± 4.6% of
technical/biomed/1471-230X-3-3.txt:352: 
       that adhesion in this system is mostly MAdCAM-1
technical/biomed/1471-230X-3-3.txt:354: 
       IL-10 transfection of endothelial cells reduced MAdCAM-1
technical/biomed/1471-230X-3-3.txt:358: 
       (42%/50%) MAdCAM-1 dependent, and that the remaining 16% of
technical/biomed/1471-230X-3-3.txt:366: 
       associated with IBD which are mediated by MAdCAM-1
technical/biomed/1471-230X-3-3.txt:371: 
       MAdCAM-1 (mucosal addressin cell 
adhesion molecule-1),
technical/biomed/1471-2407-2-11.txt:459 
        addressins GlyCAM-1 and MAdCAM- 
 are expressed in
 ~~~
 prints out the line number of the .txt files in biomed that contain "MAdCAM", for example from top to bottom6, 8, 11, 15, 16, etc. 

 Example 3:
~~~
h/docsearch$ grep -n "Five independent Salt Lake" technical/plos/*.txt
~~~
This prints out nothing since no txt files in plos contain "Five independent Salt Lake"
