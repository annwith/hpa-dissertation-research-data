Códigos-fonte:

Baseline: https://github.com/annwith/wsss-hpa/tree/main

Conformal Prediction: https://github.com/annwith/hpa-individual-cell-classifier

<!-- 
Commit usado na dissertação:
<hash do commit> 
-->

DINO: https://github.com/annwith/dino-hpa/tree/dinov2-update

Colocar os códigos do git do segundo lugar e da segmentação, e os notebooks de inferência e de melhoria da segmentação.
revisar pra ver se as training configs tão certinhas
as tabelas de validação foram feitas do mesmo jeito?
rs50 batch size + step não é igual do segundo lugar.
pos weight 1, 0,1 e 10

Dados brutos:
Os dados brutos do Human Protein Atlas/Kaggle não são redistribuídos neste depósito.
Eles devem ser obtidos nas fontes originais.

Conteúdo deste depósito:
- divisões de treino/validação/teste
- mapeamento de classes
- predições dos modelos
- métricas experimentais
- configurações de treinamento e inferência
- dados-fonte das figuras e tabelas da dissertação

## Class mapping

The file `class_mapping.csv` defines the mapping between model output indices and subcellular localization classes. The column `class_id` corresponds to the index of each class in the model output vector. Portuguese labels and abbreviations are provided for consistency with the dissertation text and figures.