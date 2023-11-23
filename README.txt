Este arquivo possui algumas orientações quanto a como se pode criar os datasets de treinamento e teste para
se conseguir executar o algoritmo presente neste repositório.

Passos para o desenvolvimento de um dataset de treinamento:

1. Deve-se realizar a coleta das imagens que se deseja utilizar no treinamento da rede neural de um determinado software
sendo que as escolhas dessas imagens dependem da finalidade que se deseja atribuir ao software. No caso deste algoritmo, foi 
desenvolvido um treinamento para que a rede neural, presente no modelo de detecção de objetos (YOLO), deixasse de detectar objetos para 
começar a detectar os dois estados de sonolência considerados ("acordado" e "sonolento") para a finalidade dada à ela. A quantidade de 
imagens que deve ser considerada, para que seja possível realizar um bom treinamento para a rede deste modelo, é cerca de 1500 imagens 
por classe. Portanto, no caso deste projeto, seriam necessárias cerca de 3000 imagens presentes neste dataset de treinamento.

2. Depois de coletada todas as imagens e inseridas dentro de uma nova pasta, deve-se rotular cada uma delas para um 
formato específico cujo qual, neste caso, é o formato "YOLO" por conta de ser o único formato de rotulação específico
aceito pela rede deste modelo (YOLO). Esse processo de rotulação é possível de ser feito por uma ferramenta chamada 
"LabelImg". A instalação desta ferramenta já é feita pelas células de código do tópico 5 presente no algoritmo que está
contido neste repositório. Caso se desconheça esta ferramenta, é recomendável que pesquise sobre.

3. Após feita a devida rotulação, deve-se indicar os caminhos ("Paths") de acesso a este dataset de treinamento para que 
a rede neural do modelo consiga acessar cada uma dessas imagens presentes neste dataset sendo que, este devido "Path" 
é configurado dentro de um arquivo epecífico chamado de "dataset.yaml". Depois de feita esta configuração (além de configurar 
algumas outras condições), o treinamento é executado sendo que a célula de código que o executa também está presente no tópico 
5 existente neste algoritmo (no caso, é a última célula de código presente neste tópico).

Para o dataset de teste, o processo de criação é mais fácil e exatamente o mesmo, porém não há necessidade de realizar
a parte de rotulação nas imagens, apenas é essencial gerar este dataset criando uma nova pasta e inserindo todas as 
imagens que se deseja considerar, para este conjunto de dados de teste, dentro desta pasta (lembrando que as imagens
consideradas para o dataset de teste devem ser diferentes das imagens utilizadas no dataset de treinamento). Essas imagens 
de teste só são possíveis de serem devidamente testadas através dos testes demonstrados no tópico 7 presente no código deste 
software que está inserido neste repositório, onde só é possível testar e passar as imagens por dentro da rede (depois de treinada)
uma por vez, verificando a devida inferência realizada pela mesma.

Caso a descrição de cada uma dessas etapas para a criação de um novo dataset de treinamento e teste não tenha ficado clara,
recomenda-se assistir o seguinte vídeo a partir do minuto "30:05": https://www.youtube.com/watch?v=tFNJGim3FXw&t=3291s.

Caso se queira compreender melhor cada uma das partes deste algoritmo referente ao Sistema de Detecção de Sonolência e tenha 
interesse em querer rodar o algoritmo deste software, recomenda-se assistir o vídeo, do link acima, por completo, pois foi com base 
nele que este software foi desenvolvido!!!

