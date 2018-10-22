PROJECT=ABIITheor

all:  ${PROJECT}
${PROJECT}: build/${PROJECT}.pdf 

build/${PROJECT}.pdf: build/${PROJECT}.bbl
	lualatex --output-directory=build ${PROJECT}
	lualatex --output-directory=build ${PROJECT}

build/${PROJECT}.bbl: build/${PROJECT}.bcf
	biber build/${PROJECT}

build/${PROJECT}.bcf: ${PROJECT}.tex
	lualatex --output-directory=build ${PROJECT}

clean:
	rm -f build/*

