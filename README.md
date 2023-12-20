<p align="center">
  <img src="/../main/Imagens/Brasao_UFPA.png" width="100" style="margin-right: 10px;">
  <img src="/../main/Imagens/Logo_CAMTUC.png" width="100" style="margin-right: 10px;">
  <img src="/../main/Imagens/Logo_Faculdade.jpg" width="160">
</p>
<br>
<p align="center"><strong>Universidade Federal do Pará || Campus Universitário de Tucuruí || Faculdade de Engenharia Elétrica</strong>
<br>
<strong>Sávio Milhomens de Sousa || Fablena K. N. Dias || Dr. Cleison Daniel Silva</strong></p>

<br>

# Aplicação da Análise de Correlação Canônica em sistemas ICM baseados em SSVEP

## Resumo
Este trabalho aborda a apresentação do artigo intitulado “Aplicação da Análise de Correlação Canônica em Sistemas ICM Baseados em SSVEP”, desenvolvido durante o período de Abril de 2023 a Setembro de 2023, durante a execução do projeto de pesquisa, sob orientação do Professor Dr. Cleison Daniel Silva e apresentado na III Escola Regional de Aprendizado de Máquina e Inteligência Artificial Norte 2. 
<br><br>
O sistema ICM (Interface Cérebro Máquina) é uma  tecnologia capaz de realizar comunicações entre seres humanos e máquinas através da atividade cerebral em resposta a estímulos visuais, imaginários ou somatossensoriais. Essa atividade é aquisitada, por meio de métodos como o eletroencefalograma (EEG), processada e convertida em sinais de comando. O estudo do artigo se concentra no processamento de informações usando o método de Análise de Correlação Canônica (CCA) para auxiliar na classificação de sinais em sistemas ICM’s baseados em SSVEP (Potencial Evocado Visualmente em Estado Estável).
<br><br>
Como metodologia, foram realizadas cinco abordagens do método CCA, em ambiente Python, usando o mesmo conjunto de dados e mesma técnica de processamento e classificação de sinais, alterando apenas a forma como os dados são tratados no método. Os dados usados são provenientes de um repositório de domínio público contendo sinais de EEG de quatro sujeitos em presença de estímulos de SSVEP em frequências de $8 Hz$, $14 Hz$ e $28 Hz$. Em adição ao CCA, utilizou-se do periodograma como tecnica para maximizar a extração de características dos sinais resultantes da aplicação do método.  Na etapa de classificação os sinais foram agrupados em três combinações binárias entre as frequências de estímulo, e para cada par, foi aplicado a Análise do Discriminante Linear (LDA). Ao final, a acurácia do classificador foi utilizada como parâmetro para discussões e conclusões de cada abordagem. De forma geral, notou-se que os resultados variam entre os indivíduos numa faixa de $38$*%* a $100$*%* de acurácia. A partir da lógica de construção e dos resultados da abordagem E, conclui-se que essa é propícia para aplicação em um sistema real.<br><br>

## Introdução
A Interface Cérebro Máquina (ICM) é uma tecnologia que permite a comunicação entre o cérebro humano e um dispositivo externo, como por exemplo as máquinas eletrônicas, através dos impulsos elétricos emitidos pelos neurônios. A ICM é capaz de transformar a atividade cerebral em ações reproduzidas por máquinas, permitindo que indivíduos com diferentes graus de deficiência motora possam desempenhar ações como controlar computadores, dirigir cadeiras de rodas, manipular braços robóticos, entre outras.
<br><br>
De forma geral, todos os sistemas ICM apresentam os mesmos processos de construção dividido em etapas, como mostrado na Figura 1.
<br>

<br><br>
<p align="center">
  <img src= /../main/Imagens/Fig_1.png>
</p>
