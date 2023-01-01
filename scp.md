## CORRENTES

corrente de excitação - corrente que é aplicada ao circuito de campo de uma máquina elétrica, como um motor ou gerador. Essa corrente é usada para controlar o campo magnético da máquina e, portanto, afeta sua operação. Por exemplo, em um motor de corrente alternada, a corrente de excitação é aplicada ao circuito de campo através de um conjunto de bobinas ou um enrolamento de campo. A corrente de excitação pode ser controlada por meio de dispositivos como reguladores de corrente ou inversores de frequência, e é usada para controlar a velocidade e torque da máquina.

Correntes Ia, Ib e Ic - correntes de referência em quadratura do espaço da máquina controlada pelo conversor de potência VSC. Elas são utilizadas no controlador DTC para calcular os sinais de PWM para os dispositivos de potência do VSC, a fim de controlar a torque e a velocidade do motor elétrico. As correntes ia*, ib* e ic* são obtidas a partir da transformação das correntes de saída do VSC para o espaço da máquina, ou seja, são as correntes de saída do VSC na base da máquina. Elas são importantes porque permitem ao controlador DTC considerar os efeitos da estática e dinâmica do conversor de potência e da máquina elétrica na determinação dos sinais de PWM.



## VETORES

Space vector - vetor que é representado no espaço de tensão trifásica (isto é, no espaço formado pelas três tensões trifásicas do conversor). O "vetor espacial" é determinado a partir das três tensões trifásicas de saída desejadas, e é utilizado para calcular os "duty cycles" dos transistores do conversor de forma a produzir a tensão de saída desejada.

## MÉTODOS DE CONTROLO

Direct Torque Control (DTC):

* método de controlo de torque para máquinas elétricas de rotação. 
* Controlar o torque da máquina elétrica de forma precisa, ao mesmo tempo que minimiza o erro de velocidade. 
* mede o torque atual da máquina elétrica e compara com o torque desejado. O controlador ajusta então os sinais de comando dos inversores de potência de acordo com a diferença entre o torque atual e o torque desejado.
* método de controlo robusto e de alta precisão

* pode ter um desempenho ligeiramente inferior em comparação com outros métodos de controlo de torque, como o Flux Vector Control (FVC). 
* DTC é mais simples de implementar e pode ser mais eficiente em termos de consumo de energia em comparação com o FVC.

FOC (Flux-Oriented Control):
* método de controlo de motores elétricos de corrente alternada (AC)
* permite controlar o torque e o ângulo de fase da máquina AC através do controlo da corrente de excitação da máquina.
* baseado no controlo da componente direta e da componente de quadratura da corrente de excitação, que são ajustadas de forma a produzir o torque desejado na máquina.
* método de controlo de alta performance que é amplamente utilizado em aplicações de alto rendimento, como sistemas de tração elétrica e geradores síncronos.
O controlo da tensão em PWM no FOC:
* é um método de controlo de máquinas elétricas rotativas que utiliza a modulação por PWM para controlar a tensão aplicada ao circuito de excitação da máquina.
* objetivo é controlar a intensidade do fluxo magnético do rotor, que por sua vez controla a torque e a velocidade da máquina.
* utiliza sensores de posição e velocidade para medir o estado atual da máquina e gerar sinais de controlo para os conversores de potência que alimentam a máquina. O controlador utiliza estes sinais para gerar sinais de PWM que são aplicados aos semicondutores dos conversores de potência para controlar a tensão aplicada ao circuito de excitação da máquina.
* permite obter uma boa resposta dinâmica e uma excelente qualidade da tensão aplicada ao circuito de excitação da máquina.
* amplamente utilizado em aplicações de controlo de velocidade e torque em máquinas elétricas rotativas.

Rotor Flux-Oriented Control (RFOC):
* método de controlo de motores AC que visa controlar a orientação do fluxo de rotor do motor.
* baseado na medição da tensão e corrente nos enrolamentos do estator e no cálculo da orientação do fluxo de rotor através de um observador de estado.
* permite um controlo preciso da velocidade e torque do motor, mesmo em condições de carga dinâmica, pois não depende de modelos matemáticos do motor.

Space Vector Modulation (SVM): 
* método para controlar a tensão de saída de um conversor de potência de três fases (como um inversor de frequência de corrente alternada). 
* baseado na modulação da tensão de saída do conversor através do ajuste dos "duty cycles" dos diferentes transistores que formam o conversor. 
No caso de um conversor de potência, o "duty cycle" de cada transistor é ajustado de forma a controlar a tensão de saída.
* No SVM, a tensão de saída do conversor é controlada através da seleção de um "space vector" que representa a tensão de saída desejada.




## OUTROS

Duty cycles - medida da duração do sinal de saída em relação ao período do sinal. Por exemplo, um sinal com um "duty cycle" de 50% ficaria ligado por metade do período e desligado por metade do período.

VSC - (Variador de Semicondutores) é um tipo de conversor de potência que permite converter a corrente elétrica de uma forma para outra, por exemplo, para converter corrente alternada em corrente contínua ou vice-versa.





Campo rotórico - vetor magnético que é gerado pelo movimento de rotação de um motor elétrico. Este vetor magnético é gerado pelas correntes que fluem pelas bobinas do estator e é responsável por produzir a força magnética que aciona o rotor do motor. O campo rotórico é uma grandeza importante no controle de motores elétricos, pois pode ser medido e controlado para produzir uma torque desejado.

Componente direta - componente da corrente que é paralela ao vetor de fluxo de campo. Ela é responsável por produzir torque e contribui para a magnetização do motor. Em um sistema de controle de torque direto (DTC), a componente direta é controlada de forma a seguir uma referência de fluxo de campo.

Componente de quadratura - refere-se ao componente da corrente ou da tensão que está 90 graus de fase adiante ou atras da componente fundamental. A componente de quadratura é usada para controlar a posição angular do rotor em um motor elétrico, pois é proporcional à velocidade angular do rotor. A componente de quadratura é geralmente gerada por meio de um sistema de controle de corrente de quadratura, que utiliza um sistema de controle de corrente de campo orientado para produzir correntes de quadratura nas fases do motor.

Componente de referência de corrente - corrente que é desejada no estator do motor, e é usada como referência para o controlador de torque. O controlador de torque usa a componente de referência de corrente para calcular o torque e a potência que devem ser entregues pelo motor. A componente de referência de corrente é geralmente definida pelo controlador de velocidade do motor, que usa a velocidade desejada como entrada para calcular a componente de referência de corrente.

Amplificador de corrente: este bloco amplifica a diferença entre a corrente da máquina medida e a referência de corrente. O amplificador pode ser um controlador PID ou um controlador de histerese.

Comparador de histerese: este bloco compara a saída do amplificador de corrente com os limites de histerese superior e inferior. Quando a saída do amplificador de corrente ultrapassa um dos limites, o comparador gera um sinal para ativar ou desativar um dos semicondutores do VSC.

Semicondutores do VSC: os semicondutores são controlados pelos sinais gerados pelo comparador de histerese. Quando um semicondutor é ativado, ele conduz corrente para o enrolamento da máquina, aumentando a corrente da máquina. Quando um semicondutor é desativado, ele é isolado do enrolamento da máquina, diminuindo a corrente da máquina.

Histerese - fenômeno que ocorre em sistemas que possuem um estado de equilíbrio instável, onde o sistema oscila entre dois estados de equilíbrio diferentes conforme o sinal de entrada varia em torno de um determinado valor de corte. Por exemplo, em um interruptor de pressão, o sistema pode oscilar entre dois estados diferentes conforme a pressão aplicada aumenta ou diminui em torno de um determinado valor de corte. No contexto do controlo, o termo histerese também é usado para se referir a um controlador que utiliza uma faixa de tolerância em torno de um ponto de setpoint para determinar quando ativar ou desativar uma ação de controle. Por exemplo, um controlador de temperatura pode ser projetado para ativar o aquecedor quando a temperatura cai abaixo de um determinado valor de setpoint e desativá-lo quando a temperatura aumenta acima de um outro valor de setpoint, criando assim uma faixa de histerese em torno do ponto de setpoint.
Os controladores de corrente baseados no método de histerese são um tipo de controlador utilizado para controlar a corrente em uma máquina elétrica. Eles funcionam comparando a corrente medida com uma referência de corrente, e ajustando a saída do controlador de acordo para manter a corrente dentro de um intervalo especificado.

O método de histerese é um tipo específico de controlador de corrente que utiliza uma técnica de feedback baseada em um intervalo de tolerância, conhecido como "histerese". Quando a corrente medida está dentro deste intervalo, o controlador mantém a saída constante. Quando a corrente ultrapassa o limite superior ou inferior do intervalo, o controlador ajusta a saída para trazer a corrente de volta para dentro do intervalo.
Um diagrama de blocos para um controlador de corrente baseado no método de histerese geralmente inclui os seguintes componentes:

    Amplificador de corrente: responsável por ampliar a corrente medida para um nível utilizável pelo controlador.

    Comparador de corrente: comparar a corrente medida com a referência de corrente e gerar um sinal de erro.

    Circuito de histerese: responsável por estabelecer o intervalo de tolerância (histerese) e gerar um sinal de saída para o amplificador de corrente quando o erro ultrapassa os limites superior ou inferior do intervalo.

    Amplificador de saída: responsável por ampliar a saída do circuito de histerese para um nível utilizável pelos semicondutores do conversor de potência.

O rotor da máquina síncrona de imanes permanentes é composto por imanes permanentes, o que lhe confere o seu nome.
A máquina síncrona de imanes permanentes gera um torque proporcional à diferença entre a velocidade do rotor e a velocidade do campo gerado pelo estator.
A máquina síncrona de imanes permanentes é controlada através da variação da corrente de excitação do estator, o que permite controlar a velocidade do rotor.
A máquina síncrona de imanes permanentes é utilizada em aplicações de elevada qualidade de torque, como na geração de energia e na propulsão de veículos eléctricos.

