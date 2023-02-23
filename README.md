# Série perfis: Whindersson Nunes

A [Série Perfis, do O POVO+](https://mais.opovo.com.br/reportagens-especiais/serie-perfis/), explora personagens famosos e anônimos para destacar histórias de vida.

Este repositório contém os códigos criados para coletar dados utilizados no episódio sobre o comediante, youtuber, cantor, compositor e ator Whindersson Nunes.

Para auxiliar a redação do texto jornalístico, foram coletadas estatísticas de acessos a músicas e vídeos do artista no Spotify e no YouTube nos perfis em que ele se identifica como Whindersson Nunes e pelo pseudônimo Lil Whind.

## Coleta

### YouTube

Para ter acesso às APIs do Google com Python, é necessário instalar a seguinte biblioteca, via pip:
```
!pip install --upgrade google-api-python-client
```

Além disso, é preciso criar uma chave de API seguindo a [documentação específica](https://developers.google.com/youtube/registering_an_application?hl=pt-br).

Uma vez conectado à API do YouTube, foram realizadas a consulta e a coleta das estatísticas dos canais de Whindersson Nunes e Lil Whind — contendo visualizações, número de inscritos e número de vídeos —, assim como os dados sobre as playlists e os vídeos.

Foram coletados, por exemplo, quantidade de curtidas, visualizações e comentários, além de quantas vezes cada vídeo foi marcado como "favorito". A partir disso, foram feitos rankings dos 10 destaques em cada "categoria".

O notebook com o código desenvolvido está disponível em [`consulta_API_YouTube.ipynb`](https://github.com/opovomais/perfil-whindersson-nunes/blob/main/consulta_API_YouTube.ipynb). Já os dataframes gerados a partir dessa consulta estão na pasta [`dataYoutube`](https://github.com/opovomais/perfil-whindersson-nunes/tree/main/dataYoutube).

### Spotify

Para acessar a API do Spotify, foi utilizada a biblioteca python [spotipy](https://spotipy.readthedocs.io/en/2.22.1/), que pode ser instalada via pip:
```
!pip install spotipy --upgrade
```

É preciso criar um id e uma senha para que as aplicações possam conectar-se à API. Para conhecer o passo a passo, deve-se checar a [documentação do Spotify](https://developer.spotify.com/documentation/general/guides/authorization/app-settings/).

Tanto para o perfil do Whindersson Nunes quanto para o perfil do Lil Whind, foram extraídos dados sobre números de seguidores, popularidade, gêneros musicais, artistas relacinados, álbuns e top 10 das músicas mais populares no momento.

O notebook com o código desenvolvido está disponível em [`consulta_spotify.ipynb`](https://github.com/opovomais/perfil-whindersson-nunes/blob/main/consulta_spotify.ipynb). Já os dataframes gerados a partir dessa consulta estão na pasta [`dataSpotify`](https://github.com/opovomais/perfil-whindersson-nunes/tree/main/dataSpotify).
