# Classificação de Fraturas Ósseas com Transfer Learning

Este projeto foi desenvolvido com o objetivo de classificar radiografias entre dois tipos de fraturas: **fratura simples** e **fratura cominutiva**, utilizando redes neurais convolucionais e técnicas de **Transfer Learning**.

## 🩻 Dataset

O conjunto de dados utilizado foi o **[Simple vs Comminuted Fractures X-ray Data](https://www.kaggle.com/datasets/your-link-aqui)**, publicado no Kaggle em **dezembro de 2024**. O dataset é composto por imagens radiográficas organizadas em duas categorias:

### 📊 Distribuição das Imagens

**Fratura Simples:**
- Imagens Originais: 1.211  
- Imagens Aumentadas: 6.311  
- **Total**: 7.522  

**Fratura Cominutiva:**
- Imagens Originais: 1.173  
- Imagens Aumentadas: 7.366  
- **Total**: 8.539  

**Total geral:** 16.061 imagens no formato JPG.

As imagens aumentadas (data augmentation) foram fornecidas no próprio dataset, facilitando o aprendizado da rede ao aumentar a diversidade visual de cada classe.

---

## 🧠 Abordagem com Redes Neurais

Utilizamos técnicas de **Transfer Learning** para aproveitar modelos pré-treinados em grandes datasets e adaptá-los à nossa tarefa específica de classificação de fraturas.

### Estratégias de Transfer Learning Aplicadas

1. **Congelamento de Camadas**  
   Inicialmente, as camadas convolucionais da base foram congeladas e apenas as camadas superiores (dense layers) foram treinadas. Isso permitiu adaptar o classificador ao nosso dataset sem perder o conhecimento aprendido previamente.

2. **Fine-tuning (Ajuste Fino)**  
   Após o treinamento inicial, as últimas camadas convolucionais da base foram descongeladas para realizar um ajuste fino da rede. Com isso, o modelo se adaptou melhor às especificidades visuais das radiografias de fraturas.

### Modelos Base Utilizados

- ✅ **EfficientNetB2** (pré-treinada no ImageNet)

Outros modelos foram considerados para comparação, mas a EfficientNetB2 apresentou uma boa relação entre desempenho e custo computacional.

---

## ⚙️ Tecnologias Utilizadas

- **Python**  
- **Keras / TensorFlow**  
- **Google Colab** (ambiente de treino)  
- **NumPy, Pandas, Matplotlib, Seaborn** (para análise e visualização de dados)

---

## 📈 Resultados Esperados

Nosso objetivo principal foi:

- Avaliar a acurácia da rede para distinguir entre fraturas simples e cominutivas
- Observar o impacto de estratégias de transfer learning no desempenho final
- Identificar possíveis padrões visuais que influenciam a classificação

> *Os resultados e métricas detalhadas podem ser conferidos nos notebooks do repositório.*

---

---

## 👥 Integrantes do Projeto

- Gabriel Assmann Schafer 
- Isabela Cunha
- Gabriel Heyde


<!-- English version-->

# Bone Fracture Classification using Transfer Learning

This project focuses on the classification of X-ray images into two types of bone fractures: **simple fractures** and **comminuted fractures**, using convolutional neural networks and **transfer learning techniques**.

## 🩻 Dataset

We used the **[Simple vs Comminuted Fractures X-ray Data](https://www.kaggle.com/datasets/your-link-here)** published on Kaggle in **December 2024**. The dataset contains labeled X-ray images divided into two categories and includes augmented images to improve model learning.

### 📊 Dataset Summary

**Simple Fracture:**
- Original Images: 1,211  
- Augmented Images: 6,311  
- **Total**: 7,522  

**Comminuted Fracture:**
- Original Images: 1,173  
- Augmented Images: 7,366  
- **Total**: 8,539  

**Overall Total:** 16,061 JPG images.

The dataset includes augmented images (already pre-processed), which help enhance the model’s ability to generalize by increasing visual diversity.

---

## 🧠 Neural Network Approach

We applied **transfer learning** to fine-tune pre-trained models on our fracture classification task.

### Transfer Learning Strategies

1. **Layer Freezing**  
   We initially froze the convolutional base and trained only the new classifier layers (Dense layers), allowing the model to adapt without overwriting previously learned features.

2. **Fine-Tuning**  
   After initial training, we unfroze the top layers of the convolutional base and retrained the model with a very low learning rate, allowing it to better adjust to the specific features of fracture X-rays.

### Pre-trained Model Used

- ✅ **EfficientNetB2** (pre-trained on ImageNet)

Other models were considered, but EfficientNetB2 provided a good balance between performance and computational cost.

---

## ⚙️ Technologies Used

- **Python**  
- **Keras / TensorFlow**  
- **Google Colab** (for training environment)  
- **NumPy, Pandas, Matplotlib, Seaborn** (for data analysis and visualization)

---

## 📈 Project Goals

The main goals of the project were:

- To build a robust neural network model capable of classifying bone fractures accurately.
- To evaluate the performance impact of different transfer learning strategies.
- To identify and analyze key visual features distinguishing the fracture types.

> *For detailed results and evaluation metrics, please check the notebooks in the repository.*

---
## 👥 Team

- Gabriel Assmann  
- Isabela Cunha
- Gabriel Heyde




