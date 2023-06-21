# Exemplo_Transformacao

*Conversão de imagem RGB em imagem Grayscale*<br>
O código acima utiliza a biblioteca OpenCV para processar imagens e a biblioteca NumPy para operações numéricas. Ele também usa a biblioteca Matplotlib para exibir gráficos e imagens.
A linha import cv2 importa a biblioteca OpenCV, enquanto import numpy as np importa a biblioteca NumPy. A linha import matplotlib.pyplot as plt importa a biblioteca Matplotlib.
A linha from google.colab.patches import cv2_imshow é específica para o ambiente de programação Google Colab e permite exibir imagens usando a função cv2_imshow.
Em seguida, a imagem 't1.jpg' é lida usando cv2.imread('t1.jpg', 1), onde o número 1 indica que a imagem deve ser carregada em cores.
A função cv2_imshow(img) exibe a imagem carregada no Google Colab.
Depois, há um trecho de código comentado que mostra como exibir a imagem em um ambiente Python comum, usando as funções cv2.imshow(), cv2.waitKey(0) e cv2.destroyAllWindows().
A seguir, é aplicada a conversão ponderada para converter a imagem colorida em uma imagem em preto e branco. A imagem é dividida em seus componentes de cor (B, G, R) usando cv2.split(img).
A conversão ponderada é aplicada multiplicando cada componente de cor pelos valores de ponderação (0,299 para o canal Azul, 0,587 para o canal Verde e 0,114 para o canal Vermelho) e somando-os. O resultado é armazenado na variável img_grayscale_pondered.
Em seguida, a matriz é convertida em um array NumPy com o tipo de dados uint8 usando np.array(img_grayscale_pondered, dtype=np.uint8).
Por fim, a função cv2_imshow(img_grayscale_pondered) é usada para exibir a imagem convertida em tons de cinza ponderados no Google Colab.
