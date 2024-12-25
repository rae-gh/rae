# To do

- **Util** Make a util that takes a pdb file and returns the same but all the atom positions adjusted to the maxima  
  - **Analysis** Use this to run the analysis for C:O against CA:C:N+1 (tau+1) and show no correlation in pdb but correlation on adjusted maxima
  - N.b. I have this in C++ but not sure about python. Do I want to use my C++ tool or re-write?  Could I make it a singularity image?
   
- **Util** make a util that returns  
  - a) the coords of structures with similar features (pdb search)  
  - b) the adjusted maxima of those  
  - c) Superposes either adjusted or none adjusted slices  
  - **Analysis** use this to look at hydrogen bonds mentioned in lit review
 
- **Analysis** iron in different formations

- **Analysis** and **Util** is my Laplacian calculation correct? I had a hessian before which I lost, in part because the method I used disappeared from the internet, resurrect all of that and ensure correctness.
