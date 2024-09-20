### Preliminaries
- Sample mean: $\bar x = \frac{\sum x_i}{n}$ 
- Sample variance $S_{xx}$ = $1\over n \sum{(x_i-\bar x)^2}$ 
- Sample covariance $S_{xy}$ = $1\over n \sum (x_i-\bar x)(y_i-\bar y)$ 

### Correlation
- **Correlation** is the strength of association between two variables
- this does not mean that the variables are functionally related

**Pearson's Correlation**:
$$r_{xy} = \frac {\sum x_iy_i -n\bar x \bar y}{\sqrt {\sum x_i^2-n\bar x^2}\sqrt {\sum y_i^2-n\bar y^2}} = \frac {S_{xy}}{\sqrt {S_{xx}} \sqrt {S_{yy}}}$$
$r_xy$ takes a value between -1 (negative correlation) and 1 (positive correlation)
- sample size: 20-30 for good estimate
- only works for linear values
- robustness: outliers can lead to misleading values

**Spearman Rank Correlation**:
$$r_s = 1 - \frac {6 \sum d_i^2}{n(n^2-1)}$$

**Kendall rank correlation**:
$$\tau  = \frac{number of concodrant pairs - number of discordant pairs}{ n(n-1)/2}$$
- a concordant pair is when $x_1>x_2$ and the corresponding $y_1 > y_2$ or vice versa
- a discordant pair is when $x_1>x_2$ and the corresponding $y_1 < y_2$ or vice versa 
- the pair for which $x_1 = x_2$ and $y_1 = y_2$ are not classified as concordant or discordant and are ignored
![[Pasted image 20240920174838.png]]