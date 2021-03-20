
.texinfo.html:
	$(MAKEINFO) --html $<

.texi.html:
	$(MAKEINFO) --html $<

# The automatically-generated target "pdf" is not working...  Not sure why not?
sysadmin_manual.pdf:	sysadmin_manual.texi
	texi2dvi --pdf --batch --output=sysadmin_manual.pdf sysadmin_manual.texi

sysadmin_manual.html:	sysadmin_manual.texi
	makeinfo --html sysadmin_manual.texi

# makeinfo --html is not making the html when called from automake
all:	$(TARGETS) sysadmin_manual.pdf
#	cp quip.pdf ../docs/quip_manual.pdf
#	cp -R quip.html ../docs/quip_web_manual
#	BUG ../docs/quip_web_manual must exist!
#	cp -R quip/*.html ../docs/quip_web_manual

.PHONY:	html
html:	version.texi $(HTML_DOCS)

