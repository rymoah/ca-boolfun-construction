# Construction of Boolean functions with Cellular Automata
GitHub repository for the source code and the experimental data of the paper:

L. Mariot, M. Saletta, A. Leporati, L. Manzoni: Exploring Semi-bent Boolean Functions Arising from Cellular Automata (2020)

Compiling
---------
To compile the Java code, just run javac */*.java from inside the directory src/

Running
-------

The Java classes that can be run are the following:

- boolfun.TestSingleBoolFunProp -> Test the cryptographic properties of a single Boolean function
- ca.TestGenerateSBoxAllCA -> Loop over all local rules of a specified diameter and generate the corresponding CA-based S-boxes, testing their cryptographic properties
- ca.TestQuadraticCASbox -> Loop over all quadratic local rules of a specified diameter and test if the CA construction produces semi-bent function up to a specified number of variables
- ca.TestQuadraticCASboxFile -> Same as the class above, but loop instead over a list of quadratic rules contained in a file
- ca.TestSingleCASbox -> Test the CA construction up to a specified number of variables on a single local rule

Invoking each class without arguments prints a helper with information on how to use the class. The class ca.TestQuadraticCASbox is the one implementing the search-ANF algorithm described in section 4 of the paper, in the particular case where the degree is 2 (i.e., we only consider quadratic functions as in the experiments presented in section 5).
