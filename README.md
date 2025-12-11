# PRojet-1-M1-MCQ-
# Le chef de Projet : Abderrahim Amel , M1 MCQ,le (11/12/2025)
# Messaoudi Wissam Douaa 
# Meziane Ahlem Rouida
# Torchi Bouchra 

import pandas as pd

# Données : Séquences ADN, Longueur, Pourcentage de GC
data = { 
    "Séquence":["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCGTAAGT","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"],
    "Longueur":[12,12,12,10,11,10,10],
    "Pourcentage GC":[50,60.67,58.33,40,45.45,60,50]
}

# Création d'un DataFrame (tableau pandas)
df = pd.DataFrame(data)
print("**************** Creation et affichage *****************")

# 1) Affichage du tableau
print("Tableau des séquences ADN :")
print(df,"\n","\n")

# Opérations sur les tableaux:
print("******************* Operations *********************")
# 2) Sélectionner la colonne "longueur"
sequences =df["Longueur"]
print(sequences,"\n","\n" )


