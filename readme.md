### \subfloat command error: Undefined control sequence.
Delete package 'subfig', and use package 'subcaption'

### Error: Use of \label@optarg doesn't match its definition.
Delete the 'subcaption' package and add:
```
\usepackage[caption=false,labelformat=simple]{subfig}
\renewcommand\thesubfigure{(\alph{subfigure})}
```
### Could not establish a connection to "hostname".
(1) Open the command panel on VS code (Ctrl+Shift+P for Windows and Cmd+Shift+P for Mac).
(2) Search for Kill VS Code Server on Host, click it - it will be automatically deleted.
(3) Reload VS Code and establish the connection again.

### Package natbib Warning: There were undefined citations.
natbib automatically loads achemso package, so change the command: \bibliographystyle{achemso}

### Load markdown after the enumitem package: Undefined control sequence error.
The order of loading these two packages matters. Should first load markdown and then load enumitem.
The reason MIGHT BE the markdown package redefines the enumerate and itemize environment, thus incurring a conflict.

### Error for \usepackage[dvipsnames]{xcolor} in an acmart documentclass
Use \PassOptionsToPackage{prologue,dvipsnames}{xcolor} before \documentclass, and then add \usepackage[dvipsnames]{xcolor}.

### Import markdown package: LaTeX Error: Command `\Bbbk' already defined.
\let\Bbbk\relax
\usepackage{markdown}

### Script file ./output.markdown.lua not found

