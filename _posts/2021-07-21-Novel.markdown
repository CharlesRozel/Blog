---
layout: post
title:  "How I typeset a novel called Dead Guy using LaTeX"
date:   2021-07-21
categories:
---
#How I typeset a novel called Dead Guy using LaTeX
I used a MacBook Air with an M1 chip running Big Sur to download the _TexShop.app_ and the _Novel Package_ from [CTAN].
The author of the _Novel Package_ stopped its development in or about 2018, but it still works.
The _Novel Package_ is in a folder called _Novel_. Inside this folder is a folder called _Doc_ with the explanatory notes in a document called _novel-documentation.html_. The explanatory notes are an excellent general guide to how to typeset a book, and make clear that the _Novel Package_ is designed  for fiction and similar books such as a biography. You cannot use the package to produce an epub.
The _Novel_ folder contains a large number of other documents most of which are beyond me as I am not a programmer. I extracted the following code from the _Novel_ folder and adapted it for my novel using trial and error.
START CODE
% !TeX TS-program = LuaLaTeX
% !TeX encoding = UTF-8
\documentclass{novel} % See list of class options; usually none needed.
%%% METADATA (FILE DATA):
\SetTitle{DEAD GUY} % Required for PDF/X.
\SetSubtitle{A COMEDY THRILLER} % Default: empty.
\SetAuthor{CHARLES ROZEL} % Default: empty.
\SetApplication{LuaLaTeX with novel and microtype}
\SetProducer{LuaLaTeX with novel-pdfx and hyperref}
\SetPDFX[CGATSTR001]{X-1a:2001}
%%% DIMENSIONS:
\SetTrimSize{5.5in}{8.5in} % Sets width, height of your book.
% Default Media Size equals Trim Size.
% Rarely-used over-ride, except for cover artwork:
% \SetMediaSize[alignment]{width}{height}
% Default margins vary with Trim Size. Defaults for {5.5in}{8.5in}:
\SetMargins{0.5in}{0.5in}{0.5in}{0.75in}
%%% GENERAL FONTS:
% Percent at end of line is necessary, when writing font settings multi-line:
\SetParentFont[%
SmallCapsFeatures={Renderer=Basic},% Effective when small caps requested locally.
Kerning=On, %
Ligatures=TeX, %
]{EB Garamond}
% Main text font automatically adds Numbers=OldStyle,Ligatures=Common.
% Default main font size is based on other layout settings.
% Varies from 11pt to 12pt. With all default layouts, value is 11.4pt.
% You may manually choose a different main font size:
% \SetFontSize{length}
% Default lines per page (main textblock) is calculated from other layout settings.
% When using all defaults, the calculated value is 35.
% If used, \SetLinesPerPage manually chooses the value:
% \SetLinesPerPage{integer}
\SetDecoFont{NovelDeco.otf}
\setsansfont{Libertinus Sans}
\setmonofont{Libertinus Mono}
\setmathfont{Libertinus Math} % unicode-math
%%% HEADERS/FOOTERS:
\SetHeadFootStyle{1} % This style has headers only.
\SetHeadJump{1.5}
\SetFootJump{1.5}
\SetLooseHead{50}
\SetEmblems{}{} % Default blanks.
\SetHeadFont[\parentfontfeatures,Letters=SmallCaps,Scale=0.92]{\parentfontname}
\SetPageNumberStyle{\thepage}
\SetVersoHeadText{Charles Rozel}
\SetRectoHeadText{Dead Guy}
%%% CHAPTERS:
\SetChapterStartStyle{footer} % Equivalent to empty, when style has no footer.
\SetChapterStartHeight{10}
\SetChapterFont[Scale=1.6]{\parentfontname}
\SetSubchFont[Numbers=Lining,Scale=1.2]{Libertinus Sans}
\SetScenebreakIndent{false}
%%% CUSTOM FONTS:
\NewFontFamily\booktitlefont{QTMagicMarker}
\NewFontFamily\regencyfont{QTMagicMarker}
% \NewFontFace[]{} % Optional command.
% \CreateFontFeature{}{} % Optional command.
%%% OTHER:
\setdefaultlanguage[variant=american]{english} % polyglossia
\microtypesetup{config=novel-microtype,stretch=20,shrink=20,final} % microtype
%%% BEGIN DOCUMENT:
\begin{document}
\frontmatter % Required.
% Typically six pages of front matter, but could be more.

% iii. Full Title page:
\thispagestyle{empty}
\vspace*{7\nbs}
\begin{center}
\charscale[3.6]{\booktitlefont DEAD GUY}\par
\vspace*{6\nbs}
\charscale[2.5]{\regencyfont a comedy}\par
\null
\charscale[2.5]{\regencyfont thriller}\par
\vspace*{6\nbs}
\charscale[2.5]{\regencyfont Charles Rozel}\par
\vfill
\end{center} 
\clearpage

\thispagestyle{empty}
\vspace*{2\nbs}
\begin{center}
DEAD GUY\par
\null
Copyright © Charles Rozel 2018\\
This hardback edition: 2021\\
All rights reserved.\par
\null
Charles Rozel has asserted his right under the Copyright, Designs\\
and Patents Act 1988 to be identified as the author of this work.\par
\null
This book is a work of fiction. Names, characters, places,\\
 incidents either are the product of the author’s imagination\\
 or are used fictitiously, and any resemblance to actual persons,\\
 living or dead, businesses, companies, events, or locales\\
  is entirely coincidental.\par
\null
ISBN-978-1-9196257-0-6\par
Imprint: Quaystone Books, Norfolk, England.\par
 \null
Typeset by Quaystone Books\\
Cover by Pulp Web Design\par
 \null
website: thrillers.pub\par
email: charlesrozel@thrillers.pub\par

\end{center}
\clearpage

% v. Epigraph, Dedication, Table of Contents, or repeated Half-Title.
% In this case, an Epigraph:

\thispagestyle{empty}
\vspace*{7\nbs}

\begin{adjustwidth}{5em}{5em}
\noindent \textit{One should not speak ill of the dead.\\
But what if the dead speak ill of the living?}
\par
\end{adjustwidth}

\clearpage

\thispagestyle{empty}
\begin{toc}[-0.1]{2.5em}
{\centering
CHAPTERS\par
\null
\tocitem*[1]{a voice from the coffin}{1}
\tocitem*[2]{In mortal fear}{2}}\par
\end{toc}

\cleartorecto % here, inserts blank, so mainmatter begins recto

\mainmatter % Required

\begin{ChapterStart}[9]
\vspace{5\nbs}
\ChapterTitle[l]{one}
\vspace{0.5\nbs}
\hrule\par
\vspace{0.5\nbs}
\ChapterSubtitle[r] {a voice from the coffin}
\vspace{\nbs}
\end{ChapterStart}

The funeral started as normal. A coffin rested in peace in front of the altar. The few mourners shuffled into pews as the organist played. Bats clattered in the belfry. Mice scuttled in the crypt. A rat watched through the leper’s squint. 

The vicar cleared his throat. ‘We are gathered here today\ldots’ 

‘I was murdered.’\\
REST OF CHAPTER


% Chapter Two:
\clearpage % next chapter may begin recto or verso
\begin{ChapterStart}[9]
\vspace{5\nbs}
\ChapterTitle[l]{two}
\vspace{0.5\nbs}
\hrule\par
\vspace{0.5\nbs}
\ChapterSubtitle[r] {Sarah Wilde}
\vspace{\nbs}
\end{ChapterStart}

‘Dead and buried. Case closed.’

‘I still think Parkin was murdered. Ouch!’

‘Sorry. I don’t know why Playtex can’t invent a bra catch a bloke can undo.’\\
REST OF CHAPTER\\
REST OF NOVEL\\
....A book closed.’
\vspace{0.5\nbs}
\begin{center}
THE END
\end{center}
\end{document}


If you run the above code in _TextShop_ it should produce a PDF.
Remember to use _LuaLaTeX_ (not LaTeX) from the dropdown menu in TexShop.
You can then adapt the code to produce your book.
I published _Dead Guy_ on Amazon in epub format using Vellum and in paperback format using Scrivener. I used the _Novel Package_ to produce the hardback. To date, I have produced one other book using the Novel Package being _Richmond: Scenes in the Life of a Bow Street Runner_. I now intend to produce most of my books using the _Novel Package_.
If you have any problems or questions send me an email.
Regards
Charles Rozel
PS: The author of the Novel Package is listed on CTAN as Robert Allgeyer but I can find no contact details for him ( I would like to thank him for a brilliant LaTeX package).
