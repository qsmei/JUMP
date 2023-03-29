# JUMP
A Julia Package for genomic selection(prediction) with BLUP and Bayesian methods! Some functions are under releasing! Here is the simple usage of JUMP:

``` {.r}


../JUMPCompiled/bin/JUMP  --phe_file phe.txt --ped_file ped.txt 
			  --model PBLUP_A  --trait_pos 6 --fix_pos 3
			  --ran_pos 5 --cov_pos 8

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
