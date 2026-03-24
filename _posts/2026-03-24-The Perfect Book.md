The Golden Canon

Jan Tschichold, the legendary typographer and book designer, described the Golden Canon as a method to produce the perfect book.

A page in the perfect book should be overlaid, notionally, with a 9 x 9 grid so that the width is made up of 9 rows of 9 equal rectangles and the height is made up of 9 rows of 9 equal rectangles.

On a recto page the textblock is then postioned 1/9th from the top and the inside of the page and 2/9th from the outside and botton of the page. The postioning is reversed on a verso page.

The ratio of the grid is then 2:3. There is harmonious because the height of the textblock equals the width of the page.

I had to design a range of bulletpoint booklets, on the subject of UK employment law, for Worklaw, a company which advises employers. It occurred to me that such a boring topic might be more readable if the booklets were designed to follow the Golden Canon.

The booklets are 6 by 9 inches. 
I did not change the font from Computer Modern which, I think, can look fine in non-fiction.

Below, is the LaTeX code to print two pages of one of the booklets.

	\documentclass[twoside,openany]{book}
	%\usepackage{showframe}
	\pagestyle{plain}
	\usepackage[paperwidth=6in, paperheight=9in, top=1in, outer=2in, bottom=2in, inner=1in]{geometry}
	\usepackage{enumitem}
	\usepackage{csquotes}
	\usepackage{microtype}
	\usepackage[compact]{titlesec}
	\usepackage[none]{hyphenat}
	\usepackage{xspace}
	\setlist{nosep}
	\setlist[itemize]{leftmargin=*}
	\setlist[enumerate]{leftmargin=*}
	\begin{document}
	\newpage
	\section*{Defending}
	To defend a claim to an employment tribunal you need to fill out the response form (an ET3) and then organise the following: 
	\begin{itemize}
	\item relevant documents;
	\item written statements from any witnesses. 
	\end{itemize}
	That’s it!\\
	The rest of it is knowing a bit about how an employment tribunal operates. 
	\subsection*{Relevant documents}
	As a general rule, employment tribunals regard documents made at the time of the event in question (a contemporaneous document) as more reliable than 		what a witness says in evidence, particularly if the witness did not write their witness statement until many months after the event.
	As soon as an employer knows or suspects that they might face a claim to an employment tribunal they should collect together anything in writing, both 	printed and electronic, which might be relevant, including handwritten documents which have been typed up (they should keep both the original handwritten document and the typed copy).\\ 
	Some claims have few relevant documents, but the following will still be relevant: 
	\begin{itemize}
	\item the employee’s employment contract;
	\item the company’s written disciplinary procedure;
	\item previous disciplinary documents, if any. 
	\end{itemize}
	Other cases might involve hundreds of investigation documents. 
	\section*{Witness statements}
	It follows from the above that a witness should write up a statement of what they saw or heard.\\
	Employment tribunals used to be called industrial tribunals.\\ 
	Previously, an employment tribunal comprised an employment judge and 2 lay persons (\emph{lay person} meaning a person who is not a lawyer).\\
	Nowadays, most cases in an employment tribunal are decided by an employment judge sitting alone.\\ 
	However, some cases still require 2 lay persons in addition to the employment judge. For example, discrimination cases and \emph{whistleblowing} cases are heard by a judge and 2 lay persons. The lay persons are an employee (often a member a trade union) and an employer (often a member of an employer's organisation such as The Federation of Small Businesses).\\ 
	Employment tribunal procedure is designed to be less intimidating than in a court. For example, witnesses give evidence sitting at a table instead of standing in a witness box. However, employment tribunals have strict procedural rules with which both parties must comply. In particular, time limits laid down by the tribunal must be adhered to otherwise the party in default risks their case being dismissed and judgment given in favour of the other party.\\ 
	To keep this booklet as simple as possible we will assume that the parties comply with all time limits laid down by the tribunal, and that it is not necessary to consider such matters as \emph{unless orders}, \emph{strike-out applications}, etc. If any such matters do arise then the affected party should take professional advice as a matter of urgency. 
	\end{document}

I have a confession to make: the client said a purchaser might think thay were being sold too much white space.so I had to change the geometry to:

top=1in, outer=1.333in, bottom=2in, inner=1in.

Albeit based on a modified version of the Golden Canon, the design still looks good and the print versions outsell the epub versions.

