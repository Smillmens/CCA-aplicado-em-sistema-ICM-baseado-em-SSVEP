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

Neste projeto, foi desenvolvido um estudo sobre a aplicação do método da Análise de Correlação Canônica (CCA) em um sistema de Interface Cérebro Máquina (ICM) baseado em Potêncial Evocado Visualmente em Estado Estável (SSVEP).

A motivação para a produção deste artigo surgiu da necessidade de uma ferramenta que pudesse destacar as características dos sinais de EEG, auxiliando o processo de classificação e aprimorando a acurácia do classificador. A habilidade do método CCA em capturar as interações complexas entre os sinais de EEG e os estímulos foi um dos principais motivos para sua utilização. Espera-se que essa abordagem contribua significativamente para aumentar a acurácia geral do processo de classificação.
<br><br>

## Navegação pelo repositório
- `Abordagens` Pasta com os códigos utlizados em cada abordagem;
- `Dataset_ICM_SSVEP` Pasta com os sinais de EGG utilizados.
<br><br>

## Projeto
### Resumo
Este trabalho aborda a apresentação do artigo intitulado “Aplicação da Análise de Correlação Canônica em Sistemas ICM Baseados em SSVEP”, desenvolvido durante o período de Abril de 2023 a Setembro de 2023, durante a execução do projeto de pesquisa, sob orientação do Professor Dr. Cleison Daniel Silva e apresentado na III Escola Regional de Aprendizado de Máquina e Inteligência Artificial Norte 2. O estudo deste trabalho se concentra no processamento de informações usando o método de Análise de Correlação Canônica (CCA) para auxiliar na classificação de sinais em sistemas ICM’s baseados em SSVEP (Potencial Evocado Visualmente em Estado Estável).

Como metodologia, foram realizadas cinco abordagens do método CCA, em ambiente Python, usando o mesmo conjunto de dados e mesma técnica de processamento e classificação de sinais, alterando apenas a forma como os dados são tratados no método. Os dados usados são provenientes de um repositório de domínio público contendo sinais de EEG de quatro sujeitos em presença de estímulos de SSVEP em frequências de $8 Hz$, $14 Hz$ e $28 Hz$. Em adição ao CCA, utilizou-se do periodograma como tecnica para maximizar a extração de características dos sinais resultantes da aplicação do método.  Na etapa de classificação os sinais foram agrupados em três combinações binárias entre as frequências de estímulo, e para cada par, foi aplicado a Análise do Discriminante Linear (LDA). Ao final, a acurácia do classificador foi utilizada como parâmetro para discussões e conclusões de cada abordagem. De forma geral, notou-se que os resultados variam entre os indivíduos numa faixa de $38$*%* a $100$*%* de acurácia. A partir da lógica de construção e dos resultados da abordagem E, conclui-se que essa é propícia para aplicação em um sistema real.
<br><br>

## Revisão Bibliográfica
A Interface Cérebro Máquina (ICM) é uma tecnologia que permite a comunicação entre o cérebro humano e um dispositivo externo, como por exemplo as máquinas eletrônicas, através dos impulsos elétricos emitidos pelos neurônios. A ICM é capaz de transformar a atividade cerebral em ações reproduzidas por máquinas, permitindo que indivíduos com diferentes graus de deficiência motora possam desempenhar ações como controlar computadores, dirigir cadeiras de rodas, manipular braços robóticos, entre outras.

De forma geral, todos os sistemas ICM apresentam os mesmos processos de construção dividido em etapas, como mostrado na ilustração baixo.
<br>

<p align="center">
  <img src= /../main/Imagens/Fig_1.png  width="600" >
</p>

Na aquisição de sinais, onde ocorre a coleta de sinais obtidos por eletrodos que percebem uma atividade cerebral em decorrência de um estímulo interno ou externo. Em seguida, no pré-processamento, esses sinais são filtrados e modelados para atender o formato desejado para processamento. Na extração de características, aplicam-se tecnicas e métodos para evidenciar os aspectos de cada sinal e que vão auxiliar a classificação dos sinais. A etapa de classificação tem o objetivo atribuir o conjunto de dados a grupos e categoriza-los de acordo com atividade cerebral a qual eles são deveriam ser relacionados. Por fim, os sinais classificados são convertidos em sinais de comandos e enviados para a aplicação que volta como um feedback para o usuário.

Cada sistema ICM se diferencia com o tipo de método de aquisição e tipo de sinal que se utiliza e também o tipo de estímulo que é aplicado. Por consequência, as técnicas e métodos aplicadas variam com essas escolhas. Em relação ao tipo de sinal, o mais comum encontrado nas literaturas é o Eletroencefalograma ou EEG que trabalha com a atividade elétrica cerebral. Apesar de ser bastante suscetível, suscetível a interferências no sinal, o seu uso se justifica por ser mais barato, fácil de trabalhar e utiliza eletrodos em contato com a pele seguindo um padrão de posicionamento como o representado na figura abaixo.

<p align="center">
  <img src= /../main/Imagens/Fig_3.png width="400" >
</p>

Em relação ao estímulo, sua origem pode se apresenta de forma visual, imaginária ou somatossensorial. Cada uma dessas está associada a uma região do cérebro, onde a resposta cerebral relacionada ao tipo de estímulo se encontra mais densa. A Figura a seguir mostra a divisão dessas regiões, chamadas de lobos cerebrais. 

<p align="center">
  <img src= /../main/Imagens/Fig_2.png width="400" >
</p>

Em sistemas ICM baseados em SSVEP, a frequência do estímulo visual ao qual uma pessoa mantém o olhar atento está ligada a uma resposta potencial contínua no córtex cerebral. Eletrodos coletam essa resposta, representada como um sinal de eletroencefalograma (EEG), e processam para se transformar em um sinal de controle. Um exemplo de estímulo de SSVEP e da aplicação desse sistema é mostrado nas imagens a baixo.

<p align="center">
  <img src="/../main/Imagens/Fig_4.gif" width="250" style="margin-right: 10px;">
  <img src="/../main/Imagens/Fig_5.png" width="400">
</p>

O artigo apresentado neste trabalho é resultado do projeto de pesquisa intitulado 'Otimização Bayesiana aplicada a sistemas de Interface Cérebro-Máquina', orientado pelo professor Cleison Daniel no período de 01 de abril de 2023 a 31 de agosto de 2023. Após uma revisão bibliográfica sobre o sistema ICM e os estímulos e eventos do SSVEP, deu-se início ao processo de aplicação do método CCA, em ambiente Python, na fase de extração de características de um sistema ICM baseado em SSVEP em desenvolvimento. Um dos aspectos mais relevantes do artigo é a maneira como os dados são tratados no método CCA, sendo uma informação pouco apresentada nos estudos existentes.

O método CCA busca matrizes de peso que maximizam a correlação entre dois conjuntos de dados. Aplicado em sistemas SSVEP, um dos conjuntos de dados é composto por sinais de interesse, referente aos sinais aquisitados, e o outro por sinais de referências criados e como a mesma frequencia dos estímulos utilizados no sistema. Dessa forma, esperasse que os sinais de mesma frequência tenham uma correlação maior que sinais de frequencia diferentes.
<br><br>

## Visão geral do projeto
### Metodologia
Para o desenvolvimento do estudo, utilizou-se de um banco de dados de um [repositório de domínio público](http://www.bakardjian.com/work/ssvep_data_Bakardjian.html) que contém sinais de EEG de cento e vinte e sete eletrodos, seguindo o padrão $10-10$, de quatro sujeitos em presença de estímulos de SSVEP nas frequências de $8 Hz$, $14 Hz$ e $28 Hz$. Utilizando um filtro passa faixa de $2 Hz$ em torno de cada frequência dos estímulos, cada conjunto de sinais foram filtrados nas três bandas resultando em nove conjunto de sinais. Em seguida foi realizado uma segmentação dos sinais em janelas de tempo de um segundo e por fim, os sinais de três eletrodos formam selecionados para as etapas seguintes. 

O método CCA busca matrizes de peso $w_x$ e $w_y$ que maximizam a correlação entre conjuntos de dados $X$ e $Y$ ao resolver a equação:

$$\max_{w_x,w_y} \rho = \frac{w^T_xXY^Tw_y}{\sqrt{w^T_xXX^Tw_xw^T_yYY^Tw_y}}$$



O método do CCA foi aplicado na etapa de extração de características utilizando a biblioteca *`sklearn.cross_decomposition.CCA2`* da linguagem de programação *Python* seguindo cinco abordagens . Em cada abordagem se manteve as mesmas configurações utilizadas em todas as etapas se diferenciando apenas na forma como os conjuntos de dados são organizados e entregues às funções da biblioteca.
<br><br>

### Resultados?
<br><br>

### Conclusões?
Em todas as abordagens, se mostrou evidente que a seleção de cada parâmetro do sistema tem um impacto direto nos resultados. Os canais representam a principal fonte de dados, carregando informações referentes às atividades cerebrais nas diferentes regiões do cérebro, portanto, a escolha de cada canal deve cuidadosamente considerada para extrair as informações mais relevantes para o tipo de ICM utilizado. Além disso, notou-se que os resultados variam entre os indivíduos devido às diferentes respostas cerebrais aos estímulos em cada pessoa. Cada abordagem seguiu lógicas de estruturação dos dados diferentes, gerando respostas similares nas abordagens B e E e singulares para as demais.

## Referências
<br><br>

## Sobre nós















