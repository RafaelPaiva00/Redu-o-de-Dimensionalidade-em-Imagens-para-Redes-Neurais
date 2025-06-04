# 🎨 Processamento Básico de Imagens: Tons de Cinza e Binarização

Este projeto explora operações fundamentais no processamento digital de imagens: a conversão de uma imagem colorida para tons de cinza e, posteriormente, a binarização (transformação em preto e branco).

O diferencial desta implementação reside na construção da **lógica principal das transformações de pixels a partir do zero**, sem a utilização de bibliotecas de processamento de imagem de alto nível, como `OpenCV` ou `Pillow`, para os cálculos centrais. Esta abordagem visa aprofundar o entendimento dos algoritmos subjacentes. A biblioteca `Pillow` é empregada apenas para as funcionalidades de carregamento e exibição das imagens.

## Conceitos Abordados:

1.  **Conversão para Tons de Cinza (Grayscale):**
    Uma imagem colorida é composta por canais Vermelho (R), Verde (G) e Azul (B). Para convertê-la para tons de cinza, o valor de intensidade de cada pixel é calculado com base em uma média ponderada desses canais. A fórmula de luminância utilizada é:
    $L = 0.299 \times R + 0.587 \times G + 0.114 \times B$
    Onde $L$ é o valor do pixel em tons de cinza (0 a 255).

2.  **Binarização (Preto e Branco):**
    Após a conversão para tons de cinza, a imagem pode ser simplificada para conter apenas duas cores: preto (0) e branco (255). Este processo envolve a aplicação de um **limiar (threshold)**:
    * Se o valor de um pixel em tons de cinza for **menor** que o limiar definido, ele se torna **preto (0)**.
    * Se for **igual ou maior** que o limiar, ele se torna **branco (255)**.
    A escolha do limiar é crucial para o resultado da imagem binarizada.

## Estrutura e Execução:

O código é composto por funções Python que operam diretamente sobre representações de pixels em listas (matrizes de valores).

* `converter_para_tons_de_cinza(imagem_colorida_pixels)`: Transforma uma matriz de pixels RGB em uma matriz de pixels em tons de cinza.
* `binarizar_imagem(imagem_cinza_pixels, limiar)`: Converte uma matriz de pixels em tons de cinza para uma matriz binarizada (0 ou 255) com base em um limiar.

O script principal realiza o carregamento da imagem (`14.jpg`) utilizando a `Pillow`, extrai seus dados de pixel, aplica as funções de processamento desenvolvidas e, por fim, exibe as imagens resultantes (original, em tons de cinza e binarizada) no ambiente de execução.

### Como Executar:

1.  Faça o upload da imagem `14.jpg` para o diretório do projeto (ou para o ambiente do Google Colab).
2.  Instale a biblioteca `Pillow` (se necessário):
    ```bash
    pip install Pillow
    ```
3.  Execute o script Python.

As imagens processadas serão exibidas.

link: [https://colab.research.google.com/drive/1wfoZJ0WhcyKeWTD-3YdQGMpqCQN9_YMj?usp=sharing](https://colab.research.google.com/drive/1wfoZJ0WhcyKeWTD-3YdQGMpqCQN9_YMj?usp=sharing)
