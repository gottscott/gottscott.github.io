---
layout: post
title: How to insert citations with LaTeX using Bibdesk and the Google Scholar Button
---

Citations using LaTeX are easy! To follow these instructions, I'll assume that you have a working installation of LaTeX [for Windows](http://miktex.org/) or [for MacOS](https://tug.org/mactex/).
 I use [Bibdesk](http://bibdesk.sourceforge.net/) to manage my references. 
[JabRef](https://www.jabref.org/) is alternative for Windows. You can also keep all your references in a text file, but it might be hard to search through them. 

If you already use LaTeX, this process is simple. Download a citation, save it to a reference manager or paste it into a new file, figure out its cite key, and type \cite{cite-key} (where cite-key is whatever your cite key is).
Then add the bibliography by typing \bibliography{my-bibliography.bib} (change my-bibliography to the filepath and name of the bibliography). Compile using LaTeX, BibTex, and then LaTeX, and you're done.  

More detailed instructions are below: 

# Step 1: Download a citation

Most journals have download options for citations. If you're not sure where this is, hit control+F and search for 'citation' or 'export' or even 'download'. 
For example, on an Elsevier journal, it looks like this: 
![Downloading an Elsevier citation](/downloads/images/bibtex/save_citation.jpg)


You can also install the Google Scholar button [for Chrome](chrome.google.com/webstore/detail/google-scholar-button/) or [for Firefox](https://addons.mozilla.org/en-us/firefox/addon/google-scholar-button/) to your web browser. 
Click on the scholar hat button and hit the quote button: 
![The google scholar button in a web browser](/downloads/images/bibtex/usinggooglescholarbutton1.jpg)

Then select BibTeX as the format: 

![The google scholar buton in a web browser](/downloads/images/bibtex/usinggooglescholarbutton2.jpg)

This will open a new window that looks like: 

![The google scholar buton in a web browser](/downloads/images/bibtex/usinggooglescholarbutton3.jpg)
  
Copy the text (or download the page). 

# Step 2: Save the citation to your reference manager
A reference manager is a fancy word for an electronic bibliography database. This could be as simple as a text file with all your citations.
If you use BibDesk, you can drag and drop your file into a new bibliography. You can also import it. However you do this, the final product looks like: :

![The final bibliography result](/downloads/images/bibtex/bibdesk.jpg)

If you used the Google Scholar button, just paste the text into the bibliography. 
Again, you can also just copy all these citations into a single text file. If you do this, save this with the extension `.bib`.  

# Step 3: Cite your reference by typing \cite{}
Every citation that you download will have an id or cite key, found at the beginning of the file directly after `@article` (or @book, or @techreport for other formats). In Bibdesk, the cite key is listed in the database: 

![The cite key column in Bibdesk](/downloads/images/bibtex/bibdesk2.jpg)

In our case, this is Graham2016. To cite any reference, we merely type `\cite{cite key}` . 
For this paper, it would look like: 

> Previous literature shows that urban form can effect ambulance calls \cite{Graham2016}. Urban planning is also an important component for urban economies... 

# Step 4: Add the bibliography and compile 

Now that we have added references to our paper, we need to add our bibliography. We do this by specifying a citation style (using \bibliographystyle{}), and then adding the bibliography using \bibliography{}. 

```latex
 \bibliographystyle{ametsoc2014}
 \bibliography{YourFileLocation/YourBibliographyName}
```

# Step 5: Compile with LaTeX, with Bibtex, then with LaTex again 

Now we need to compile our document. Either type on the command line: 

```bash
latex ourdocument.tex 
bibtex ourdocument.tex 
latex ourdocument.tex 
```
or use the 'play' button in your LaTeX editor, compile with LaTeX, Bibtex, and LaTeX again: 


![Change the compiler in TeXShop](/downloads/images/bibtex/compile.png)


This generates all the citations, and in particular generates a .bib file for your document. 
Once you've compiled the references, you'll only need to run bibtex again if you edit the reference list. 
