Applying SVR to earlier problem, where I tried to predict an applicant's salary based on his role/designation.

The differences are that SVR needs feature scaling, because unlike linear regression models where the coefficients of the variables take care of the scaling part somewhat, the same doesn't happen in SVR. 

SVR has an inbuilt equation, with Epsilon Insensitive Tube, that overlooks errors within the tube. And those above and below the tube boundaries are taken into account as Epsilon(i) and Epsilon(i) star.

<img width="244" alt="Screenshot 2021-10-31 at 3 11 20 PM" src="https://user-images.githubusercontent.com/61674750/139576538-7c8787bb-2040-412a-b705-4b5ca127e2b4.png">

<img width="369" alt="Screenshot 2021-10-31 at 3 12 58 PM" src="https://user-images.githubusercontent.com/61674750/139576592-9f828032-65e9-4c86-8810-de189058247f.png">

We are using the non-linear Gaussian RBF as a kernel. Other options also available. 
<img width="582" alt="Screenshot 2021-10-31 at 4 26 06 PM" src="https://user-images.githubusercontent.com/61674750/139579530-b228c397-61ac-4396-9b06-e4dbb99c0165.png">


Points to note :- 
Poly Reg might overfit but treats outliers well and doesn't exclude any.
SVR on the other hand ignores the extreme outliers, those that lie outside the epsilon tube
