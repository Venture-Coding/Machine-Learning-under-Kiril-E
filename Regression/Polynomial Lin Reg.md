Here, we try to predict the Salary based on the Designation of the applicant.
The data is varying across different positions and hence the relation across input/ouput isn't linear but rather exponential in some sorts.

Hence, we try to fit a better regression curve by going beyond the Lin Reg in single degree and employing multiple degrees of freedom.
Effectively getting y = b0 + b1x1 +b2x1^2 +..... + bnx1^n

Poly Reg might overfit but treats outliers well and doesn't exclude any.
SVR on the other hand ignores the extreme outliers, those that lie outside the epsilon tube.
