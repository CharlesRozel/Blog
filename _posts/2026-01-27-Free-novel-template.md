Below is a LaTeX template which you copy and use to typeset your novel for free.

Just replace the body text and title text with your text.

If you are unfamiliar with LaTeX it is a computerised text-processing system, first developed by a mathematician, Donald Knuth, who called the system TeX. The name is written with a capital T, a lowercase e, and a capital X. It was further developed by another mathematician, Leslie Lamport, and is now called LaTeX.

Use LaTeX to print your book and you will be using the best computerised typesetting system.

You can print any document from a replica medieval manuscript to a flyer for a village fête.

Your book will look professional.

LaTeX produces plaintext documents, which means it would be very difficult, if not impossible, to hide malicious code in LaTeX.

LaTeX does the formatting and leaves the content to you.

You can copy the code from the template or download the code from [QuaystoneBooks.com][1]

You do not need to understand the code, but you will need a free LaTeX editor to process the code.

Use Google (or your favourite search engine) to find a free editor for Windows, Mac or Linux.

A free editor called [TexStudio][2] is recommended for Windows.

I use Macs and a free editor called [TeXShop](), which is also recommended for Linux users.

If you are a programmer you can use VSCode or Vim.

Alternatively, you can use an online editor such as [Overleaf][4] or [Crixit][5] both of which oﬀer a free plan and tutorials.

The text editor you choose will offer different settings to process the typesetting; you should choose as XeLaTeX. This setting allows you to use the two fonts mentioned in the next sentence.

The fonts used in the templates are EB Garamond for the body text and Bangers for the title text. both of which fonts can be downloaded from [Google Fonts][6] and are licensed for commercial use
.
If you have a problem using the template send me a message and I will try to help.

	\documentclass[openany]{book}
	\usepackage[paperwidth=5.5in, paperheight=8.5in,
	top=0.75in, outer=0.8in, bottom=1in, inner=1in]
	{geometry}
	\usepackage{xspace}
	\usepackage{microtype}
	\usepackage{graphicx,pifont}
	\usepackage{lipsum}
	\usepackage{fancyhdr}
	\pagestyle{fancy}
	\fancyhf{}
	\fancyhead[CE]{\bangers Book Title}
	\fancyhead[CO]{\rightmark}
	\renewcommand{\headrulewidth}{0pt}
	\renewcommand{\chaptermark}[1]
	{\markboth{}{\bangers{#1}}}
	\fancyfoot[C]{\thepage}
	\setlength{\headheight}{12pt}
	\setlength{\headsep}{12pt}
	\usepackage{titlesec}
	\usepackage{lettrine}
	\titlespacing*{\chapter}
	{0pt}      
	{60pt}     
	{40pt}     
	\titleformat{\chapter}[display]
	{}                              
	{}                               
	{0pt}                            
	{\centering\Huge\bangers} 
	[]   
	\usepackage{fontspec}
	\newfontfamily\bangers{Bangers}
	\setmainfont{Crimson Pro}
	\begin{document}
	\frontmatter
	\newpage
	\thispagestyle{empty}
	\begin{center}
	\vspace*{120pt}
	{\Huge\bangers\scalebox{1.75}{Book Title}\\}
	\vspace{40pt}
	{\huge\bangers\scalebox{1.50}{ Book subtitle}\\}
	\vspace{45pt}
	{\LARGE\bangers\scalebox{1.25}{Your Author Name}}
	\vfill
	\newpage
	\thispagestyle{empty}
	\vspace*{140pt}
	{\LARGE\bangers Book Title}\\
	\vspace{8pt}
	{\small
	\copyright{} Your Author Name 2026\\
	all rights reserved.\\
	\vspace{0.04in}               
	\noindent\hfill\rule{0.5in}{0.4pt}\hfill
	\vspace{0.07in}\\
	All characters in this book are fictitious\\
	and any resemblance
	to real persons,\\living or dead,\\
	is entirely coincidental.\\
	\vspace{0.04in}               
	\noindent\hfill\rule{0.5in}{0.4pt}\hfill
	\vspace{0.07in}\\
	Imprint: Your Publishing Company\\
	ISBN: Your number}
	\end{center}
	\mainmatter
	\chapter{First Chapter}
	\vspace{-25pt}
	\lettrine[lines=3,
	loversize=0.2,
	findent=0.5em,
	nindent=0.2em,]{\bangers A}{olor} sit amet,
	consectetur adipiscing elit.
	\lipsum[1-10]
	\chapter{Second Chapter}
	\vspace{-25pt}
	\lettrine[lines=3,
	loversize=0.2,
	findent=0.5em,
	nindent=0.2em,]{\bangers B}{olor} sit amet,
	consectetur adipiscing elit. 
	\lipsum[1]
	\end{document}






[1]:	https:%5C%5Cwww.quaystonebooks.com
[2]:	https://www.texstudio.org
[4]:	https://www.overleaf.com
[5]:	https://crixet.com
[6]:	https://fonts.google.com