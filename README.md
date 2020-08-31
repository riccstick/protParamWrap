# protParamWrap
wrapper to submit multiple sequences to analyze with protParam tool
# Requirements
- [Julia](https://julialang.org/)
  - module [protParam](https://github.com/zmactep/ProtParam.jl) *(the package has to be included into julia)*
  - module BioSequences *(the package has to be included into julia)*
- Installation of Julia and modules can be found [here](https://medium.com/@erikbreslmayr/protparam-standalone-bfa38932e946).
## Workflow
- `.fasta` files are seperated into single files
- `.protParam.jl` files are generated for each sequence 
- `.jl` files are processed by julia and protParam
- results are saved in the `summary.txt` file (*Important: For my needs I only save pI, Molecular weight, number of Amino acids and Instability Index values; However, of course a lot more data can be extracted from the results of protParam by adding more variables in the getData function...*)
# Installation
Bash script, just make it executable and run
## SourceCode compiling with Argbash - argument parser generator
template file can be changed and converted to executable code (tested with argbash_2.8.1; Ubuntu_16.04)

`argbash protParamWrap_template -o protParamWrap`
### Problems
- Fasta file must look like this:

<img src="fasta.png" alt="sample .fasta file"
	title="sample .fasta file" width="600" />
- Amino acid sequence in the .fasta file can only include standard amino acids like `'RHKDESTNQCGPAVILMFYW'`; otherwise protParam crashes!
