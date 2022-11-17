# ProgramacaoLogica
-------------------------------------------------------------------------------------------------------------------------
# Aplicação Bagof:
  Para  resolver  estes  exercícios  você  pode,  ou  não  desenvolver  seus  próprios  predicados.  Se  olptar  por  não, 
  todas  as  queries  criadas  para  responder  a  questão  devem  estar,  na  forma  de  comentários,  no  final  do  seu 
  arquivo  no Swish Prolog, online. Se optar por desenvolver suas próprias regras, os queries  para a chamada 
  destas  regras  deve  estar  especificado, em  forma  de  comentário,  no  fim  do  seu  código.  A  entrega  deve  ser 
  apenas o link para o ambiente Swish onde está a sua solução. Considere a base de conhecimento a seguir: 
 
  cidade(curitiba, parana, brasil). 
  cidade(blumenau, santa_catarina, brasil). 
  cidade(joenville, santa_catarina, brasil). 
  cidade(foz_do_iguaçu, parana, brasil). 
  cidade(londrina, parana, brasil). 
  cidade(maringa, parana, brasil). 
  cidade(ushuaia, terra_do_fogo, argentina). 
  cidade(santa_rosa, la_pampa, argentina). 
  cidade(cordoba, cordoba, argentina). 
  
  1) Encontre uma lista ordenada com todas as cidades da Argentina. 
  Resp esperada:  
  Cidades = [cordoba, santa_rosa, ushuaia]. 
 
  2) Encontre uma lista com as cidades de cada estado do Brasil. 
  Resp esperada:  
  Cidades = [curitiba, foz_do_iguaçu, londrina, maringa], 
  Estado = parana; 
  Cidades = [blumenau, joenville], 
  Estado = santa_catarina. 
 
  3) Encontre uma lista ordenada das cidades de cada estado da base de conhecimento. 
  Resp esperada:  
  Cidades = [cordoba], 
  Estado = cordoba 
  Cidades = [santa_rosa], 
  Estado = la_pampa 
  Cidades = [curitiba, foz_do_iguaçu, londrina, maringa], 
  Estado = parana 
  Cidades = [blumenau, joenville], 
  Estado = santa_catarina 
  Cidades = [ushuaia], 
  Estado = terra_do_fogo. 
 
  4) Encontre uma lista ordenada dos estados de cada país da base de conhecimento. 
  Resp esperada:  
  Estados = [cordoba, la_pampa, terra_do_fogo], 
  Pais = argentina 
  Estados = [parana, santa_catarina], 
  Pais = brasil 
 
  5) Encontre uma lista com repetições e não ordenada dos estados de cada país da base de conhecimento. 
  Resp esperada:  
  Estados = [terra_do_fogo, la_pampa, cordoba], 
  Pais = argentina 
  Estados = [parana, santa_catarina, santa_catarina, parana, parana, parana], 
  Pais = brasil 
 
  6) Encontre uma lista com todas as cidades do Uruguai. 
  Resp esperada:  
  Cidades = []. 
  Pais = uruguai 
 
  7) Encontre uma lista com todas as cidades, de um determinado estado e país.
  Resp esperada:  
  Cidades = [cordoba], 
  Estado = cordoba, 
  Pais = argentina 
  Cidades = [santa_rosa], 
  Estado = la_pampa, 
  Pais = argentina 
  Cidades = [curitiba, foz_do_iguaçu, londrina, maringa], 
  Estado = parana, 
  Pais = brasil 
  Cidades = [blumenau, joenville], 
  Estado = santa_catarina, 
  Pais = brasil 
  Cidades = [ushuaia], 
  Estado = terra_do_fogo, 
  Pais = argentina 
-------------------------------------------------------------------------------------------------------------------------
# ArvoreProlog:
  1) Considere a seguinte lista de fatos dada por::  
  𝑝𝑎𝑖(𝑎,𝑏). 
  𝑝𝑎𝑖(𝑎,𝑐). 
  𝑝𝑎𝑖(𝑏,𝑑). 
  𝑝𝑎𝑖(𝑏,𝑒). 
  𝑝𝑎𝑖(𝑐,𝑓). 
  a) Defina um predicado irmao que seja verdadeiro se X e Y forem irmãos; 
  b) Defina um predicado primo que seja verdadeiro se X e Y forem primos; 
  c)  Defina um predicado neto se X for neto de Y. 
 
    DICA  MUITO  IMPORTANTE:  você  pode  usar  not(X)  para  negar  uma  variável,  constante, 
    predicado ou o resultado de uma operação entre estes artefatos.  1.  Considere a seguinte lista de fatos dada por::  
    𝑝𝑎𝑖(𝑎,𝑏). 
    𝑝𝑎𝑖(𝑎,𝑐). 
    𝑝𝑎𝑖(𝑏,𝑑). 
    𝑝𝑎𝑖(𝑏,𝑒). 
    𝑝𝑎𝑖(𝑐,𝑓). 
    a) Defina um predicado irmao que seja verdadeiro se X e Y forem irmãos; 
    b) Defina um predicado primo que seja verdadeiro se X e Y forem primos; 
    c)  Defina um predicado neto se X for neto de Y. 
 
    DICA  MUITO  IMPORTANTE:  você  pode  usar  not(X)  para  negar  uma  variável,  constante, 
    predicado ou o resultado de uma operação entre estes artefatos.  
  
  2) Você  deve  procurar,  implementar  e  explicar,  um  predicado 𝑞𝑢𝑖𝑐𝑘𝑠𝑜𝑟𝑡(𝐿,𝐾) no  qual,  dada 
  uma  lista  de  inteiros  𝐿,  devolve  uma  lista  𝐾 com  estes  inteiros  ordenados  segundo  o 
  algoritmo de quick sort. 
  
  3) Você deve procurar, implementar e explicar, um predicado 𝑚𝑒𝑟𝑔𝑒𝑠𝑜𝑟𝑡(𝐿,𝐾) no qual, dada 
  uma  lista  de  inteiros  𝐿,  devolve  uma  lista  𝐾 com  estes  inteiros  ordenados  segundo  o 
  algoritmo de merge sort. 
-------------------------------------------------------------------------------------------------------------------------
# CaminhoMaisCurto:
  1) Já  vimos  como  usar  o  Prolog  para encontrar todos  os  caminhos  entre dois  vértices  em um 
     grafo, este é um passo importante para resolver um dos problemas fundamentais da análise 
     de  grafos,  encontrar  o  caminho  mais  curto.  Sem  usar  os  algoritmos  consagrados  para  esta 
     tarefa  (Dijsktra,  Bellman-Floyd,  etc.)  escreva  um  programa  em  Prolog  que  encontre  o 
      caminho mais curto entre dois vértices quaisquer, considerando que o grafo é não direcional. 
     Para isso você deverá criar um banco de dados usando o predicado aresta/2 que contenha as 
     arestas de um grafo de, no mínimo, 20 vértices.  
-------------------------------------------------------------------------------------------------------------------------
# Cinema: 
  No link: https://swish.swi-prolog.org/p/Cinema_PUC_2022-1.plLinks to an external site.

   Existe um banco de dados com informações sobre os filmes de Hollywood. Neste link também estão as considerações referentes a criação 
  deste banco de dados, inclusive explicando como foram criados os fatos que relacionam os átomos envolvidos. 
  
  1) Sua tarefa será criar regras para atender as questões apresentadas no link acima e publicar, como resposta, o link do seu arquivo,
  contendo o banco, e as regras que você criou. 
-------------------------------------------------------------------------------------------------------------------------
# CutProlog:
  1.  Usando o banco de dados a seguir:  
  ℎ𝑜𝑚𝑒𝑚(𝑎𝑙𝑏𝑒𝑟𝑡). 
  ℎ𝑜𝑚𝑒𝑚(𝑏𝑜𝑏). 
  ℎ𝑜𝑚𝑒𝑚(𝑒𝑑𝑤𝑎𝑟𝑑).  
  𝑚𝑢𝑙ℎ𝑒𝑟(𝑎𝑙𝑖𝑐𝑒). 
  𝑚𝑢𝑙ℎ𝑒𝑟(𝑣𝑖𝑐𝑡𝑜𝑟𝑖𝑎). 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑎𝑙𝑏𝑒𝑟𝑡,𝑒𝑑𝑤𝑎𝑟𝑑).%𝑎𝑙𝑏𝑒𝑟𝑡 é 𝑝𝑎𝑖 𝑑𝑒 𝑒𝑑𝑢𝑎𝑟𝑑 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑣𝑖𝑐𝑡𝑜𝑟𝑖𝑎,𝑒𝑑𝑤𝑎𝑟𝑑). 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑎𝑙𝑏𝑒𝑟𝑡,𝑎𝑙𝑖𝑐𝑒). 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑣𝑖𝑐𝑡𝑜𝑟𝑖𝑎,𝑎𝑙𝑖𝑐𝑒). 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑎𝑙𝑏𝑒𝑟𝑡,𝑏𝑜𝑏). 
  𝑝𝑟𝑜𝑔𝑒𝑛𝑖𝑡𝑜𝑟(𝑣𝑖𝑐𝑡𝑜𝑟𝑖𝑎,𝑏𝑜𝑏). 
  
  Escreva uma regra que indique, entre os termos apresentados aqueles que são 
  filhos e uma outra regra que indique, entre os termos apresentados, aqueles que são 
  primos.  
 
    DICA MUITO IMPORTANTE: suas regras, obrigatoriamente precisam usar o cut (!).
-------------------------------------------------------------------------------------------------------------------------
# DFS - BFS: 
  1) Existem  dois  algoritmos  muito  importantes  na  busca  de  informações  em  grafos,  o  BFS  e  o 
  DFS.  Sua  pesquisa  será  explicar  estes  algoritmos  e  buscar  uma  implementação  destes 
  algoritmos em prolog. Lembre-se que deverá explicar como o código prolog está 
  funcionando. A prova de funcionamento deve ser realizada com um grafo composto de, pelo 
  menos, 10 arestas.
-------------------------------------------------------------------------------------------------------------------------
# Matrizes: 
  1) Pesquisar  a  existência  de  predicados  para  a  multiplicação  de  matrizes  e  para  o  cálculo  de 
  determinantes.  Seu  trabalho  será  explicar  estes  predicados,  caso  eles  existam,  ou  criar  os 
  predicados, caso eles não existam.
-------------------------------------------------------------------------------------------------------------------------
# ProblemaDoCaminho:
  1) Considerando a base de conhecimento apresentadas a seguir, que representa os caminhos possíveis em um 
  labirinto  na  forma  de  uma  lista  de  adjacências  mostrando  que  pontos  deste  labirinto  são  conectados. 
  Considere também que todos os caminhos são unidirecionais. Ou seja, você pode ir do ponto 1 para o ponto 
  2 mas não pode ir do ponto 2 para o ponto 1. Escreva os predicados necessários para determinar, a partir de 
  um  ponto  de  origem,  os  outros  pontos  que  você  pode  atingir  no  labirinto.  E,  se  necessário,  as  regras  que 
  respondam: que pontos você pode atingir a partir do ponto 1? Ou a partir do 13? 
  conectado(1,2). 
  conectado(3,4). 
  conectado(5,6). 
  conectado(7,8). 
  conectado(9,10). 
  conectado(12,13). 
  conectado(13,14). 
  conectado(15,16). 
  conectado(17,18). 
  conectado(19,20). 
  conectado(4,1). 
  conectado(6,3). 
  conectado(4,7). 
  conectado(6,11). 
  conectado(14,9). 
  conectado(11,15). 
  conectado(16,12). 
  conectado(14,17). 
  conectado(16,19)
  
  2.  Escreva  um  conjunto  de  fatos,  regras  e  predicados  que  possam  ser  usados  para  validar  uma  ordem  de 
  compra. Considere que uma ordem de compra é válida, se o cliente existir, se o cliente tiver um bom nível de 
  crédito e se existirem itens suficientes no estoque para atender esta ordem. Sendo assim, uma ordem deverá 
  conter,  no  mínimo,  nome  do  cliente,  item,  quantidade,  e  valor  total.  Cabe  a  você  criar  uma  base  de 
  conhecimento que permita validar, ou não estas ordens. 
 
  3.  Crie  um  conjunto    de  regras  em  prolog  que  permita  transformar  temperaturas  em  graus  Celsius  para 
  Fahrenheit e de Fahrenheit para Celsius. 
-------------------------------------------------------------------------------------------------------------------------
# ProblemaDoAvo: 
  1) A  história  a  seguir  está  no  trabalho  de  N.  Wirth  (1976)  Algorithms  +  data  structures  =  programs.  Leia 
  cuidadosamente: Casei com uma viúva (vamos chamá-la de W) que tem uma filha adulta (chame-a de D). Meu 
  pai (F), que nos visitava com bastante frequência, apaixonou-se pela minha enteada e casou-se com ela. Por 
  isso, meu pai se tornou meu genro e minha enteada se tornou minha madrasta. Alguns meses depois, minha 
  esposa deu à luz um filho (S1), que se tornou cunhado do meu pai, e meu tio. A esposa do meu pai, ou seja, 
  minha enteada, também teve um filho (S2). Usando o conhecimento de lógica, proposicional e predicativa, 
  que você já tem, represente a situação descrita por Wirth e, usando prolog ou a lógica matemática, prove que 
  é o narrador pode ser considerado como sendo seu próprio avô.   
-------------------------------------------------------------------------------------------------------------------------
