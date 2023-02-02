
Compilation of C

-   Pre-Processing

    -    All the statements starting with the # symbol in a C program are processed by the [[pre_processing|pre-processor]], and it converts our program file into an intermediate file with no # statements


-   Compiling

    -   Compiling phase in C uses an inbuilt [[nibm.dse.pf.compiler]] software to convert the intermediate (.i) file into an Assembly file (.s) having assembly level instructions (low-level code)


-   Assembling

    -   Assembly level code (.s file) is converted into a machine-understandable code (in binary/hexadecimal form) using an [[nibm.dse.pf.assembler]]


-   Linking

    -   A program called the [[nibm.dse.pf.linker]] is used to combines all the files like library files and others files into a single self included executable which can be executed in doesn't need any external dependency

