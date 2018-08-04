# SMP2018 (1st prize)-Ensemble-Guide

A combination of Model Ensembling methods that is extremely useful for increasing accuracy of this contest.
</br >More details see [Entire Project](https://github.com/Quincy1994/smp2018)

## Task description
Given an article, we need to create algorithms that judge types of authors (automatic summary, machine translation, robot writer or human writer). 
More details see [SMP EUPT 2018](https://www.biendata.com/competition/smpeupt2018/)

## 1.Requirements
* lightgbm
* gensim
* scikit-learn
* pickle
* numpy

## 2.Models
We have improved the traditional [Stacking](https://zhuanlan.zhihu.com/p/26890738 "悬停显示") method, concating the probability vectors generated by each classifier, and reclassifying them with Lightgbm.

    $ python3 smp_sta_all_vec.py
Performing the Blending method on the stitched probability vector.

    $ python3 smp_lgb_blending.py


## 3.Parameter Description
|  | Parameter |Description  |
| ------------ | ------------ | ------------ |
|1|num_class| 4 |
|2|n_estimators| 5000 |
|3|objective| multiclass |
|4|learning_rate| 0.005 |
|5|num_leaves| 65 |
|6|n_jobs| -1 |

## 4.Acknowledgment
Thanks for all the efforts of my teammates in `GDUFS-iiip` 
</br> We hope that more people will join in our labs: `Data Mining Lab in GDUFS(广外数据挖掘实验室）`


