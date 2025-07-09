# Detector de Pinturas Rupestres: Uma Abordagem com Redes Neurais Convolucionais

---

## Slide 1: Título e Apresentação

* **Título:** Detector de Pinturas Rupestres: Uma Abordagem com Redes Neurais Convolucionais
* [Seu Nome]
* **Matéria:** Visão Computacional
* [Data]

---

## Slide 2: Contexto, Objetivo e Desafios

* **Contexto:** A relevância da preservação e estudo das pinturas rupestres como patrimônio cultural.
* **Objetivo:** Desenvolver um sistema automatizado para a **detecção e classificação** de pinturas rupestres, focando em elementos humanos e animais.
* **Desafios:**
    * Variações de iluminação e textura das superfícies.
    * Formas irregulares e camuflagem natural das pinturas.
    * Qualidade e tamanho dos datasets disponíveis.
    * Alta precisão necessária para diferenciação entre classes (humanos/animais).

---

## Slide 3: Metodologia e Abordagens

* **Modelos de Detecção:**
    * **Faster R-CNN:** Arquitetura de duas etapas, conhecida pela **alta precisão**.
    * **YOLOv5:** Arquitetura de etapa única, focada em **velocidade e eficiência**.
* **Estratégias de Treinamento (Transfer Learning):**
    * **Faster R-CNN:**
        * Experimento 1: Treinamento com 1 classe (**Pintura Rupestre**).
        * Experimento 2: Fine-tuning do modelo de 1 classe para 2 classes (**Humanos** e **Animais**).
    * **YOLOv5:**
        * Base: Modelo pré-treinado em um detector de petroglifos.
        * Experimento 1: Fine-tuning para 1 classe (**Pintura Rupestre**).
        * Experimento 2: Fine-tuning do modelo de 1 classe para 2 classes (**Humanos** e **Animais**).
        * Experimento 3 (Adicional): Fine-tuning **direto** do modelo de petroglifos para 2 classes (sem passar pela etapa de 1 classe).
* **Por que Faster R-CNN e YOLOv5?**
    * **Faster R-CNN:** Para estabelecer um baseline de alta precisão.
    * **YOLOv5:** Pela sua eficiência e por ser a arquitetura base do detector de petroglifos (facilitando o transfer learning).

---

## Slide 4: Dataset e Pré-processamento

* **Composição:** Combinação de múltiplos datasets de pinturas rupestres.
    * *Mencionar e, se possível, mostrar thumbnails representativos.*
* **Desafios do Dataset:**
    * Dataset inicial pequeno e desequilibrado.
    * Seleção e anotação manual e minuciosa das imagens e rótulos.
* **Estratégias de Data Augmentation:**
    * **Técnicas Aplicadas:** Rotação, espelhamento, ajustes de brilho/contraste, zoom.
    * **Objetivo:** Ampliar a diversidade e o volume do dataset, aumentando a robustez dos modelos.
    * **Exemplo Visual:** Imagem original vs. Imagem com augmentation (destacar a mudança).

---

## Slide 5: Detalhes do Treinamento

* **Configurações Comuns:** Otimizadores, taxa de aprendizado inicial e agendadores de taxa de aprendizado (`learning rate schedulers`), peso (`weight decay`).
* **Treinamento Faster R-CNN:**
    * Principais parâmetros e estratégias de fine-tuning para o modelo de 2 classes.
* **Treinamento YOLOv5:**
    * Processo de fine-tuning a partir do modelo de petroglifos.
    * Principais parâmetros e ajuste de hiperparâmetros-chave.

---

## Slide 6: Resultados Qualitativos: Exemplos de Detecção

* **Visualização:** Apresentar imagens de validação com as caixas delimitadoras e classificações dos modelos.
* **Comparação Visual:** Mostrar e discutir a capacidade de Faster R-CNN e YOLOv5 em identificar as pinturas e distinguir entre humanos e animais.
* **Análise:** Incluir exemplos de detecções bem-sucedidas e, se apropriado, alguns erros ou falsos positivos para discussão.

---

## Slide 7: Resultados Quantitativos: Métricas de Avaliação

* **Métricas Utilizadas:** Precisão, Recall, F1-Score e mAP (mean Average Precision).
* **Apresentação:** Utilizar **gráficos comparativos** ou **tabelas claras** para visualizar o desempenho.
* **Comparação Abrangente:**
    * **Faster R-CNN:** 1 classe vs. 2 classes.
    * **YOLOv5:** 1 classe vs. 2 classes (a partir de 1 classe e direto de petroglifos).
* **Discussão:** Análise do melhor desempenho geral e por classe para cada abordagem.

---

## Slide 8: Conclusões e Limitações

* **Análise dos Resultados:**
    * Identificação de **overfitting** ou **estagnação** (se ocorreram).
    * Tendências no desempenho dos modelos (e.g., melhor desempenho para uma classe específica).
    * **O que funcionou bem:** Pontos fortes de cada abordagem.
    * **O que não funcionou tão bem:** Desafios persistentes, classes com pior desempenho.
* **Limitações do Trabalho:**
    * Tamanho e diversidade do dataset.
    * Variações de iluminação e oclusão em ambientes reais.
    * Complexidade das formas das pinturas.
* **Próximos Passos:** Sugestões para trabalhos futuros e melhorias.

---

## Slide 9: Recursos e Contribuições

* **GitHub do Projeto:** [Link direto para o seu repositório]
    * Organização do código, modelos treinados (se disponíveis), scripts de treinamento e avaliação.
* **Datasets Utilizados:** [Mencionar e incluir links, se forem públicos]
* **Resultados Detalhados:** (Se houver um local específico para gráficos e métricas adicionais, como um relatório PDF complementar).

---

## Slide 10: Agradecimentos e Perguntas

* Agradecimento à audiência.
* Espaço para perguntas.
* Contato: [Seu e-mail (opcional)]
