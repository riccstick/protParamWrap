# protParamWrap
wrapper to submit multiple sequences to analyze with protParam tool
# Requirements
- [Julia](https://julialang.org/)
  - module [protParam](https://github.com/zmactep/ProtParam.jl) *(the package has to be included into julia)*
  - module BioSequences *(the package has to be included into julia)*
- Installation of Julia and modules can be found [here](https://medium.com/@erikbreslmayr/protparam-standalone-bfa38932e946).
# Installation
Bash script, just make it executable and run
## SourceCode compiling with Argbash - argument parser generator
template file can be changed and converted to executable code (tested with argbash_2.8.1; Ubuntu_16.04)

`argbash protParamWrap_template -o protParamWrap`
### Problems
- .fasta file must look like this:
> \>seq1
>MQLI...
>RYLI...
- Amino acid sequence in the .fasta file can only include standard amino acids like 'RHKDESTNQCGPAVILMFYW'; otherwise protParam crashes!
