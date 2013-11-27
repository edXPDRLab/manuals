
.PHONY: html

Q_FLAG =

ifeq ($(quiet), true)
Q_FLAG = quiet=true
endif

html:
	cd $(CURDIR)/course_authors && make html $(Q_FLAG)
	cd $(CURDIR)/lms && make html $(Q_FLAG)
	cd $(CURDIR)/howto-slideshare && make html $(Q_FLAG)

latex:
	cd $(CURDIR)/course_authors && make latex $(Q_FLAG)
	cd $(CURDIR)/lms && make latex $(Q_FLAG)
	cd $(CURDIR)/howto-slideshare && make latex $(Q_FLAG)
