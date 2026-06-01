# Class mapping used in the dissertation experiments.

The keys correspond to the class identifiers and to the output indices of the models. For example, index 0 in the model output vector corresponds to "Nucleoplasm", index 1 corresponds to "Nuclear membrane", and so on.

## The dictionaries below provide:

- classes_map: original class names in English;
- classes_map_pt: Portuguese translations used in the dissertation;
- classes_map_paper: Portuguese labels with panel letters used in figures;
- classes_abrev: abbreviated labels used only in figures and tables.

```
classes_map = {
    0: "Nucleoplasm",
    1: "Nuclear membrane",
    2: "Nucleoli",
    3: "Nucleoli fibrillar center",
    4: "Nuclear speckles",
    5: "Nuclear bodies",
    6: "Endoplasmic reticulum",
    7: "Golgi apparatus",
    8: "Intermediate filaments",
    9: "Actin filaments",
    10: "Microtubules",
    11: "Mitotic spindle",
    12: "Centrosome",
    13: "Plasma membrane",
    14: "Mitochondria",
    15: "Aggresome",
    16: "Cytosol",
    17: "Vesicles and punctate cytosolic patterns",
    18: "Negative",
}
```

```
classes_map_paper = {
    0: "(a) Nucleoplasma",
    1: "(b) Membrana nuclear",
    2: "(c) Nucléolos",
    3: "(d) Centro fibrilar do nucléolo",
    4: "(e) Pontuações nucleares (nuclear speckles)",
    5: "(f) Corpos nucleares",
    6: "(g) Retículo endoplasmático",
    7: "(h) Aparelho de Golgi",
    8: "(i) Filamentos intermediários",
    9: "(j) Filamentos de actina",
    10: "(k) Microtúbulos",
    11: "(l) Fuso mitótico",
    12: "(m) Centrossomo",
    13: "(n) Membrana plasmática",
    14: "(o) Mitocôndrias",
    15: "(p) Agressoma",
    16: "(q) Citosol",
    17: "(r) Vesículas e padrões citosólicos pontilhados",
    18: "(s) Negativo",
}
```

```
classes_map_pt = {
    0: "Nucleoplasma",
    1: "Membrana nuclear",
    2: "Nucléolos",
    3: "Centro fibrilar do nucléolo",
    4: "Pontilhados nucleares",
    5: "Corpos nucleares",
    6: "Retículo endoplasmático",
    7: "Aparelho de Golgi",
    8: "Filamentos intermediários",
    9: "Filamentos de actina",
    10: "Microtúbulos",
    11: "Fuso mitótico",
    12: "Centrossomo",
    13: "Membrana plasmática",
    14: "Mitocôndrias",
    15: "Agressoma",
    16: "Citosol",
    17: "Vesículas e padrões citosólicos pontilhados",
    18: "Negativo",
}
```

```
classes_abrev = {
    0:  "Nucleopl.",        # Nucleoplasma
    1:  "Mem. Nuc.",        # Membrana nuclear
    2:  "Nucl.",            # Nucléolos
    3:  "C. Fibr.",         # Centro fibrilar do nucléolo
    4:  "Pont. Nuc.",       # Pontilhados nucleares
    5:  "Cor. Nuc.",        # Corpos nucleares
    6:  "R. E.",            # Retículo endoplasmático
    7:  "Golgi",            # Aparelho de Golgi
    8:  "F. Int.",          # Filamentos intermediários
    9:  "F. Act.",          # Filamentos de actina
    10: "Micr.",            # Microtúbulos
    11: "Fuso M.",          # Fuso mitótico
    12: "Centr.",           # Centrossomo
    13: "Mem. Plas.",       # Membrana plasmática
    14: "Mit.",             # Mitocôndrias
    15: "Agr.",             # Agressoma
    16: "Cit.",             # Citosol
    17: "Ves.",             # Vesículas e padrões citosólicos pontilhados
    18: "Neg.",             # Negativo
}
```