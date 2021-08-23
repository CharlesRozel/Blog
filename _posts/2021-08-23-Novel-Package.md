I typeset books and design book covers for indie authors. In the main, I use Scrivener and LaTeX for print books. Recently, I discovered the Novel Package on CTAN, and used it to typeset the paperback edition of _Richmond: Scenes in the Life of a Bow Street Runner_. I was very pleased with the result, and decided to use the Novel package to typeset all my print books.

However, when I had nearly finished typesetting a second book, the package packed up on me with the message ‘novel.cls not found’.

On `tex.stackexchange.com` I read an exchange of emails in June 2017 regarding the same error message. In the email exchange, the author of the package explained:

“Due to some change in one or more other LaTeX packages, novel now crashes. This behavior is as of the last couple of weeks. Novel certainly did not crash prior to that. The crash is fundamental, in that the user's document content does not matter. It is not due to any change in novel.. twice I have had to revise code, to compensate for changes in another package…It seems that the package(s) causing the crash are not necessary for novel's purpose, but they are automatically loaded whether novel likes it or not; then novel crashes. I have requested that CTAN remove novel…It may be that some users will find that novel compiles, only to discover that it fails after TeX update.”

I assume that the package crashed on me following a Tex update.

As at the date of this blogpost the package is still on CTAN.

It seems to me that the package crashing due to other packages demonstrates a problem with LaTeX relying on packages from various developers. 
So I installed Context which was developed for typesetting and does not rely on packages. I installed the LMTX version on a MacBook Air with the M1 chip.
After installing LMTX I was about to delete the Novel package when I found that it was working again. I can only think that the installation of LMTX kickstarted the Novel package. Both LMTX and the Novel package use Lua.

So, if you use the Novel package and it crashed on you, try installing Context.

Charles Rozel

PS: I am learning Context, but it is a hard slog as there is no up-to-date manual.
