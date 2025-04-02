# UCIA-CLUSTERSPOTIFY

Uma análise da base de dados das Músicas mais "Streamadas" em 2024.

Como o nome sugere, é uma base direta ao ponto em sua utilidade, que é uma grande compilação das músicas mais tocadas no ano passado, 2024. Ela oferece uma visualização sólida de variados atributos de uma track, sejam eles mais técnicos como o próprio ISRC, que basicamente funciona como um "CPF" da música, e também informações a respeito da popularidade em diversos streamings; algo que é curioso, pois à princípio eu imaginava que o dataset conteria apenas dados exclusivos do Spotify, mas o arquivo é completo ao ponto de também apresentar informações de outras plataformas, certamente estas adições são bem-vindas. 

Acredito que essa base de dados seja uma fonte riquíssima de conteúdo para que as agências, empresas e artistas tenham noção real do impacto do seu produto. O dataset até lista a quantidade de vezes que uma certa música foi utilizada em posts do TikTok, e para mim isso é algo imprescindível de saber, atualmente o TikTok é um fator chave se um artista quer que sua música estoure, tanto que vemos exemplos disso com o surgimento de tracks cada vez mais curtas, com o propósito de encaixar num vídeo pequeno.

Isso me leva à minha proposta de análise dessa base de dados, escolhi usar o método de agrupamento, o clustering. A ideia principal é identificar e agrupar grupos de músicas com características semelhantes, avaliar o desempenho em diferentes plataformas e tentar entender quais são os fatores que contribuem para o seu sucesso. 

A base de dados utilizada nessa análise está disponível aqui: https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024

# Músicas Virais

Aproveitando o que já foi dito anteriormente sobre a importância do TikTok, um cluster seria dedicado à ele, um grupo com as "músicas virais no TikTok", que levaria em conta características como:

Visualizações, likes e posts do TikTok, dando atenção para aquelas que tiverem todos esses 3 atributos muito altos;
Visualizações do YouTube, para ter uma noção se o artista já é conhecido;

Esse cluster funcionaria para avaliar caso certas músicas explodiram por trends ou desafios na plataforma.

# Músicas de Playlist

Outro cluster seria formado pensando na eficiência do próprio algoritmo dessas plataformas musicais, o Spotify por exemplo costuma criar playlists com os top hits do dia, da semana, também costuma criar playlists específicas para cada usuário baseando-se em seus gostos, esse grupo levaria em conta características como:

Streams, alcance da playlist e número de playlists do Spotify, isso também poderia ser aplicado ao Deezer e ao Apple Music;
Visualizações do TikTok, se forem baixas, isso mostra que essas músicas não dependem dessa rede para bombar;
Visualizações do Youtube, para saber se existe um clipe, se o artista é conhecido, etc;


# Músicas "Hits"

Pode parecer semelhante ao conceito de músicas virais, mas esse cluster seria muito mais abrangente. Ele verificaria a popularidade da música em todas as plataformas, as características principais seriam baseadas em altas visualizações e no desempenho geral, incluindo até mesmo a rádio. São hits globais de artistas provavelmente já consolidados, uma track que todo mundo já ouviu pelo menos uma vez.


# Finalização

Mais clusters poderiam ser criados para alcançar outros objetivos, um que avaliaria a popularidade de músicas explícitas e não explícitas seria interessante. Acredito que esse método de agrupamento seja perfeito justamente por se alinhar com as estratégias reais da indústria, que analisam o que está bombando em diferentes plataformas, permitindo que os artistas, agências e empresas ajustem o marketing e a promoção com base nos clusters. É prático e funcional.

Penso que usar o algoritmo K-means seria bom, pelo menos no ínicio, por conta de sua simplicidade. Como ele divide os dados em clusters baseados em similaridades, é ideal para um dataset como esse que contém um volume muito grande de dados númericos como as visualizações, likes, streams, entre outros.
