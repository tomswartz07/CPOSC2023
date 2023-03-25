######################
#      Makefile      #
######################

filename=cposc2023

all: pdf clean-artifacts

clean-artifacts:
	@rm -f ${filename}.{ps,log,aux,html,out,dvi,bbl,blg,snm,toc,nav,vrb}

pdf: 
	pdflatex -halt-on-error ${filename} 
	# Run twice to update Table-of-Contents and other items
	pdflatex -halt-on-error ${filename} 

xe-pdf:
	xelatex -halt-on-error ${filename}

text: html
	html2text -width 100 -style pretty ${filename}/${filename}.html | sed -n '/./,$$p' | head -n-2 >${filename}.txt

html:
	@#latex2html -split +0 -info "" -no_navigation ${filename}
	htlatex ${filename}

view:
	while inotifywait --event modify,move_self,close_write ${filename}.tex; \
		do pdflatex -halt-on-error ${filename} && xelatex -halt-on-error \
		${filename}; done

clean:
	rm -f ${filename}.{ps,pdf,log,aux,html,out,dvi,bbl,blg,snm,toc,nav,vrb}
