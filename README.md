# Tradutor de Libras 🤟📷

Este projeto é um sistema de visão computacional capaz de reconhecer e traduzir gestos da Língua Brasileira de Sinais (LIBRAS) em tempo real ou através de imagens estáticas. Ele utiliza técnicas de processamento de imagem e aprendizado de máquina para identificar os sinais das mãos.

## 🚀 Funcionalidades

- **Coleta de Dados**: Script automatizado para capturar imagens das mãos e criar uma base de dados personalizada.
- **Processamento de Dataset**: Conversão das imagens capturadas em pontos de referência (landmarks) das mãos.
- **Treinamento de Modelo**: Algoritmo de Classificação (Machine Learning) para aprender a diferenciar os gestos.
- **Tradução em Tempo Real**: Utiliza a webcam para detectar e exibir a tradução do sinal.

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido inteiramente em **Python** utilizando as seguintes bibliotecas:

- **[OpenCV](https://opencv.org/)**
- **[MediaPipe](https://developers.google.com/mediapipe)**
- **[Scikit-learn](https://scikit-learn.org/)**
- **[Numpy](https://numpy.org/)**
- **Pickle**

## 📂 Estrutura do Projeto

```bash
├── data/
├── images/
├── collect_imgs.py
├── create_dataset.py
├── training.py
├── testing.py
├── testing_imgs.py
├── model.p
└── data.pickle
```

## ⚙️ Como Rodar o Projeto

### 1. Pré-requisitos

Instale as dependências necessárias:

```bash
pip install opencv-python mediapipe scikit-learn numpy
```

### 2. Coleta de Dados (Opcional)

Execute o script para coletar imagens pela webcam:

```bash
python collect_imgs.py
```

### 3. Criando o Dataset

Gere o arquivo `data.pickle` a partir das imagens coletadas:

```bash
python create_dataset.py
```

### 4. Treinando o Modelo

Treine o modelo de machine learning e gere o arquivo `model.p`:

```bash
python training.py
```

### 5. Testando em Tempo Real

Inicie a tradução dos gestos em tempo real usando a webcam:

```bash
python testing.py
```

## 🤝 Contribuição

Contribuições são bem-vindas!  
Sinta-se à vontade para abrir uma **Issue** ou enviar um **Pull Request**.

## 📄 Licença

Este projeto está sob a licença **MIT**.

---

Desenvolvido por **Derick Bessa**
