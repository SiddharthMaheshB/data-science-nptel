### Confusion Matrix
![[Pasted image 20240921164540.png]]
- **True Positive**: Correct identification of positive labels
- **True Negative**: Correct identification of negative labels
- **False Positive**: Incorrect identification of positive labels
- **False Negative**: Incorrect identification of negative labels

**Accuracy** using a confusion matrix can be defined by $A = \frac{TP + TN}{N}$ 
**Sensitivity**: $S_e = \frac {TP}{TP + FN}$
**Specificity**: $S_p = \frac{TN}{FP + TN}$
**Balanced Accuracy**: BA = $(sensitivity + specificity)/2$
**Prevalence**: $P = \frac{TP + FN}{N}$
**Positive Prevalence Value**: $PPV = \frac{sensitivity * prevalence}{((sensitivity* prevalence) + ((1-specificity)*(1-prevalence)))}$
**Negative Prevalence Value**: $NPV = \frac{sensitivity *(1- prevalence)}{(((1-sensitivity)* prevalence) + ((specificity)*(1-prevalence)))}$
**Detection Rate**: $DR = \frac{TP}{N}$
**Detection prevalence**: $DR = \frac{TP + FP}{N}$
**Kappa**: $Kappa = \frac{observed accuracy - expected accuracy}{1 - expected accuracy}$
**Observed accuracy**: $OA = \frac{TP + TN}{N}$
**Expected accuracy**: $OA = \frac{(TP + FN)(TP + FP) + (FP + TN)(FN + TN)}{N}$

- ROC curve can be used to see classifier performance at different threshold levels (don't  ask what it is I have no idea)
