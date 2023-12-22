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
De forma geral, todos os sistemas ICM apresentam os mesmos processos de construção dividido em etapas, como mostrado na ilustração baixo.
<br>

<p align="center">
  <img src= /../main/Imagens/Fig_1.png  width="600" >
</p>

Na aquisição de sinais, onde ocorre a coleta de sinais obtidos por eletrodos que percebem uma atividade cerebral em decorrência de um estímulo interno ou externo. Em seguida, no pré-processamento, esses sinais são filtrados e modelados para atender o formato desejado para processamento. Na extração de características, aplicam-se tecnicas e métodos para evidenciar os aspectos de cada sinal e que vão auxiliar a classificação dos sinais. A etapa de classificação tem o objetivo atribuir o conjunto de dados a grupos e categoriza-los de acordo com atividade cerebral a qual eles são deveriam ser relacionados. Por fim, os sinais classificados são convertidos em sinais de comandos e enviados para a aplicação que volta como um feedback para o usuário.
<br><br>
Cada sistema ICM se diferencia com o tipo de método de aquisição e tipo de sinal que se utiliza e também o tipo de estímulo que é aplicado. Por consequência, as técnicas e métodos aplicadas variam com essas escolhas. Em relação ao tipo de sinal, o mais comum encontrado nas literaturas é o Eletroencefalograma ou EEG que trabalha com a atividade elétrica cerebral. Apesar de ser bastante suscetível, suscetível a interferências no sinal, o seu uso se justifica por ser mais barato, fácil de trabalhar e utiliza eletrodos em contato com a pele seguindo um padrão de posicionamento como o representado na figura abaixo.

<p align="center">
  <img src= /../main/Imagens/Fig_2.png width="600" >
</p>

