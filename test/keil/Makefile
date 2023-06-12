# Do NOT use parenthesis on Windows project dir names
PROJECTS ?= $(wildcard ../../examples/stm32/nucleo-*-keil-*)

MAKEFILEPATH := $(dir $(word $(words $(MAKEFILE_LIST)),$(MAKEFILE_LIST)))
BATPATH := $(subst /,\,$(MAKEFILEPATH))

all: $(PROJECTS)
	
# Need to test inside .bat to check and transfer errors
$(PROJECTS): FORCE
	$(BATPATH)unitest.bat $(subst /,\,$@)

FORCE:
