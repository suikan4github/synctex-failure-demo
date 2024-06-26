# SyncTeX-failure-demo
Demonstration of the SyncTex failure on TeX Live 2024

# Details
This is a demonstration of SyncTeX failure of TeX Live 2024. 

You can build the a main.pdf file from the main.tex and fox.tex. Then, you can see the chapter 2 "Fox" is unable to link with LaTeX source for both forward and backward. 

This problem was found when I switched from pLaTeX to LuaLaTeX. The original problem was found in a large document bigger than 100pages. 

This demonstration is shrank from that document. 

# Procedure to reproduce the problem

1. Run following command to build the PDF file. 
   - ```lualatex -synctex=1 main.tex```
1. Open the PDF and go to chapter 2 "Fox". 
1. Try the link with LaTeX source by clicking chapter 2.
1. You will see the chapter 2 is unable to link.    

You can also see the problem with the pre-build main.pdf and main.synctex.gz in this repository. 

# Reproduced  Environment
## Common condition
- Ubuntu 22.04 LTS
- TeX Live 2024 ( from install-tl-unx.tar.gz )
- LuaLaTeX (LuaHBTex 1.18.0 )
- Document class : 
  - book
  - jlreq

## WSL
- VS Code 1.88.1 + LaTeX Workshop 9.20.0

## Desktop Linux
- KDE Plasma 6
- TeX Works 

# Contents of this repository 
File name       | Description
----------------|------------------
main.tex        | Main source of LaTeX.
rain.tex        | Chapter 1.
fox.tex         | Chapter 2.
fig.png         | demo figure.
main.pdf        | pre-build PDF for demo. 
main.synctex.gz | pre-build synctex file for demo. 



# Consideration 
This problem seems to be a problem of LuaLaTeX or SyncTeX rather than viewer, because both LaTeX workshop and TeX works can reproduce in different OS environment. 

# License
The contents of this repository is delivered under [MIT LICENSE](./LICENSE).