BuildDir = ./build
Compiler = gmcs
# Documentation
DocDir = $(BuildDir)/docs/api
# Log
LogDir = ./log

all: doc

doc: FORCE
	-mkdir -p $(DocDir)
	rm -R -f $(DocDir)
	doxygen Doxyfile 2> $(LogDir)/Doxygen.log
	src/main/res/script/doxygen.postprocess.sh $(DocDir)

clean:
	-rm -R $(LogDir)
	-rm -R $(DocDir)

FORCE:
	-mkdir -p $(LogDir)
	-mkdir -p $(DocDir)
