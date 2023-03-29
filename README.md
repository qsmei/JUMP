# JUMP
A Julia Package (binary version) for genomic selection(prediction) with BLUP and Bayesian methods! In the current stage, i just use this to achieve my analysis. Some functions are under releasing, speed and memory performance would be the next step target! 
Here is the simple usage of JUMP:

``` {.r}


../JUMPCompiled/bin/JUMP  --phe_file phe.txt --ped_file ped.txt 
			  --model PBLUP_A  --trait_pos 6 --fix_pos 3
			  --ran_pos 5 --cov_pos 8

```                         
 
 The output log is: 
``` {.c++} 
Start the PBLUP_A analysis of T1
300 animals with phenotpe and 5000 animals with pedigree will be used in this analysis
Start construct pedigree additive relationship matrix......
Complete construct pedigree additive relationship matrix!
Estimate variance components by REML......
Iteration(FS)=1         ;∇Litter²=1656.2349 ;∇g²=456.3620  ;∇e²=1472.6871 ;σLitter²=1657.2349 (0.452907);σg²=457.3620  (0.532790);σe²=1473.6871 (0.468833)
Iteration(AI)=2         ;∇Litter²=16.5209   ;∇g²=125.2068  ;∇e²=91.2086   ;σLitter²=1640.7140 (558.833749);σg²=582.5688  (464.746953);σe²=1382.4785 (521.748636)
Iteration(AI)=3         ;∇Litter²=6.1949    ;∇g²=4.8878    ;∇e²=0.3501    ;σLitter²=1646.9089 (551.353023);σg²=577.6810  (510.294004);σe²=1382.8286 (522.787160)
Iteration(AI)=4         ;∇Litter²=0.1063    ;∇g²=0.5554    ;∇e²=0.5592    ;σLitter²=1647.0152 (551.103728);σg²=578.2363  (508.985402);σe²=1382.2694 (521.829681)
Iteration(AI)=5         ;∇Litter²=0.0522    ;∇g²=0.0567    ;∇e²=0.0027    ;σLitter²=1647.0674 (551.033281);σg²=578.1796  (509.187025);σe²=1382.2721 (521.786574)
Iteration(AI)=6         ;∇Litter²=0.0005    ;∇g²=0.0060    ;∇e²=0.0055    ;σLitter²=1647.0679 (551.027637);σg²=578.1857  (509.168389);σe²=1382.2666 (521.773863)
Iteration(AI)=7         ;∇Litter²=0.0005    ;∇g²=0.0006    ;∇e²=0.0001    ;σLitter²=1647.0684 (551.026993);σg²=578.1850  (509.170549);σe²=1382.2667 (521.773559)
Iteration(AI)=8         ;∇Litter²=0.0000    ;∇g²=0.0001    ;∇e²=0.0001    ;σLitter²=1647.0684 (551.026944);σg²=578.1851  (509.170343);σe²=1382.2666 (521.773437)
Convergence!
Log-Likelihood Is: -1371.9736350575317
Estimate Fiexed Effect And Random Effect 
h2 and standard error of the above random effects are: 0.457(0.143), 0.16(0.138), 0.383(0.15) respectively!
Analysis done within 11.8005s
EBVs and Residuals of Individuals are saved as JUMP.PBLUP_A.T1.ebv.csv and JUMP.PBLUP_A.T1.res.csv in the current path:
 ```
 
 Parameters:
 ``` {.r}
 --phe_file:     file name of phenotype data(with colnames)
 --ped_file:     file name of pedigree data(with colnames)
 --model   :     analysis model
 --trait_pos:    postion of trait name in the colnames of phenotype
 --fix_pos:      postion of fixed effects name in the  colnames of phenotype
 --ran_pos:      postion of randome effects name in the colnames of phenotype (animal effect position not included in ran_pos)
 --cov_pos:      postion of covariate effects name in the colnames of phenotype
                           
```  
