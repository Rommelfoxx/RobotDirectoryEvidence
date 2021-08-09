# RobotDirectoryEvidence
Code in Robot framework for generate evidence in folder with the name of the Suite and Test 


Library  SeleniumLibrary
Library  String

Pegar o nome da suite de teste
	${suiteName}=	Get Variable Value	${SUITE NAME}
	${suiteName}=	Replace String	${suiteName}	${SPACE}	_
	${suiteName}=	Replace String	${suiteName}	.	_
	${suiteName}=	Replace String	${suiteName}	(	_
	${suiteName}=	Replace String	${suiteName}	)	_
	${suiteName}=	Replace String	${suiteName}	\"	_
	${suiteName}=	Replace String	${suiteName}	:	_
	${suiteName}=	Replace String	${suiteName}	\'	_
    [Return]        ${suiteName}

Pegar o nome do test-case
    ${testName}=	Get Variable Value	${TEST NAME}
	${testName}=	Replace String	${testName}	${SPACE}	_
	${testName}=	Replace String	${testName}	(	_
	${testName}=	Replace String	${testName}	)	_
	${testName}=	Replace String	${testName}	\"	_
	${testName}=	Replace String	${testName}	:	_
	${testName}=	Replace String	${testName}	\'	_
    [Return]        ${testName}

Gerar evidencia teste
    ${suite}=        Pegar o nome da suite de teste
    ${teste}=        Pegar o nome do test-case
    Set Screenshot Directory     results\\${suite}\\${teste}
    Capture Page Screenshot	 
    


Pegar o nome da suite de teste
	${suiteName}=	Get Variable Value	${SUITE NAME}
	${suiteName}=	Replace String	${suiteName}	${SPACE}	_
	${suiteName}=	Replace String	${suiteName}	.	_
	${suiteName}=	Replace String	${suiteName}	(	_
	${suiteName}=	Replace String	${suiteName}	)	_
	${suiteName}=	Replace String	${suiteName}	\"	_
	${suiteName}=	Replace String	${suiteName}	:	_
	${suiteName}=	Replace String	${suiteName}	\'	_
    [Return]        ${suiteName}

Pegar o nome do test-case
    ${testName}=	Get Variable Value	${TEST NAME}
	${testName}=	Replace String	${testName}	${SPACE}	_
	${testName}=	Replace String	${testName}	(	_
	${testName}=	Replace String	${testName}	)	_
	${testName}=	Replace String	${testName}	\"	_
	${testName}=	Replace String	${testName}	:	_
	${testName}=	Replace String	${testName}	\'	_
    [Return]        ${testName}

Gerar evidencia teste
    ${suite}=        Pegar o nome da suite de teste
    ${teste}=        Pegar o nome do test-case
    Set Screenshot Directory     results\\${suite}\\${teste}
    Capture Page Screenshot	 
    
