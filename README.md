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

