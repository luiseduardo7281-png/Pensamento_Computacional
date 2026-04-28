Você foi contratado para desenvolver a lógica de um sistema de iluminação automática para uma sala técnica. Essa sala precisa manter uma sinalização visual 
conforme a quantidade de luz do ambiente. Para simular essa leitura, será utilizado um LDR, que identifica se o ambiente está claro, com iluminação média ou 
escuro. O sistema também terá um LED RGB, responsável por indicar visualmente a condição do ambiente.

Quando o ambiente estiver claro, o LED RGB deve ficar verde. Quando a iluminação estiver média, o LED RGB deve ficar amarelo. Quando o ambiente estiver escuro, 
o LED RGB deve ficar vermelho, indicando necessidade de atenção.

Além disso, o sistema possui três botões. O primeiro botão ativa o modo automático, em que o LED RGB responde ao LDR. O segundo botão ativa o modo manual de 
alerta, deixando o LED RGB vermelho independentemente da leitura do LDR. O terceiro botão desliga o sistema, apagando todos os LEDs. 

Durante os testes, foi observado que o operador pode pressionar mais de um botão ao mesmo tempo. O sistema deve tratar essa situação, evitando estados 
inconsistentes.


**1) Identifique as entradas e saídas do sistema:** As entradas são a luz da sala e os 3 botões que acionam o gatilho para ativar certas condições do sistema. 
As saidas é o resultado do LED RGB de acordo com a luz da sala que será medido pelo LDR(Verde para claro, Amerelo para média e Vermelho para escuro), o
primeiro botão que ativa o modo normal do LDR, o segundo botão que deixa o LED RGB vermelho independente do LDR e o terceiro botão que apaga todos os LEDS.
  
**2) Apresente todos os componentes do sistema e para que eles servem:** LDR serve para identificar a luz da sala onde o circuito está atualmente, LED RGB
serve para sinalizar o estado de iluminação do quarto identificado pelo LDR, os botões ativam os modos do sistema e também um deles pode desligar o sistema.

**3) Apresente as regras de funcionamento a serem implementadas:** Quando o programa iniciar, o sistema estará no modo automático, utilizando o LDR para
identificar a luz do ambiente para definir que cor o LED RGB estará no momento. Ao apertar no primeiro botão, ele entrará no modo automático, que é o modo
padrão do sistema. Se já estiver no modo automático, continua no mesmo modo. O segundo botão ativa o modo manual, onde o LED RGB estará sempre na cor 
vermelha, independente do que o LDR está identificando. O terceiro botão irá desligar o sistema, apagando o LED RGB até outro botão ser pressionado. Se
acontecer de mais de um botão for pressionado, o sistema deverá apagar o LED RGB e esperar até outro botão ser pressionado para um dos modos serem ativados.

**4) Explique como você utilizaria estruturas if para controlar o sistema:** A estrutura IF será usada na entrada do LDR e nos botões, identificando o valor 
que será entregue pelo estado da luz e o estado do programa respectivimente. Se(IF) a luz estiver no estado claro(Valor X), acenderá a luz de cor verde. Se(IF)
a luz estiver no estado médio(Valor Y), acenderá a luz de cor amarela. Se(IF) a luz estiver no estado escuro(Valor Z), acenderá a luz de cor vermelha. Se(IF) 
botão 1 for pressionado, ativará o modo onde o LDR identificará a luz e acenderá as luz de acordo com o estado da luz. Se(IF) botão 2 for pressionado, ativará
a luz vermelha no LED RGB, ignorando a entrada do LDR. Se(IF) botão 3 for pressionado, o LED RGB se desligará e ignorará a entrada do LDR. Se(IF) mais de um
botão for pressionado, o LED RGB se desligará.
