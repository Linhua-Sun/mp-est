The MP-EST method estimates species trees from a set of gene trees by maximizing a pseudo-likelihood function. The program is written in C. The parallel version of the program can run independent searches (chains) in parallel. Each chain starts with a different seed. The program will find the estimate of the species tree with the largest likelihood score across chains. To use MP-EST, you need to create two files; a gene tree file and a control file.

The gene tree file contains rooted ML gene trees. Because mp-est can only take gene trees with branch lengths, please make sure that all gene trees have branch lengths, though mp-est does not use branch length information to reconstruct species trees. Unrooted ML gene trees (with branch lengths) can be estimated from sequences using  phylogenetic programs (phyml, phylip). The unrooted ML trees can be rooted in phybase using the outgroup. The control file contains necessary parameters for running MP-EST (for example, seed, number of species, user tree).

Precisely, you need to follow the following steps to construct MP-EST trees.

1. Estimate ML gene trees (w/o branch lengths) from phylogenetic programs (phyml, phylip, paup).

2. Root ML gene trees (gene trees estimated from phyml are unrooted trees).

3. Put the rooted ML gene trees (phylip format) into a single file (this is the gene tree file).

4. Create a control file for running MP-EST (see Manual for how to create a control file).

5. Type “mpest control” (if the control file is named "control ") to run mp-est on the terminal window (DOS command window on PC)

!!!!! Check out the new web server for MP-EST at  http://bioinformatics.publichealth.uga.edu

!!!!! The new version MP-EST 1.5 is available at http://faculty.franklin.uga.edu/lliu/content/software
