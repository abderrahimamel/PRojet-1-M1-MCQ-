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

# 3)Filtrer les sequences avec une Longueur supérieure à 10
print("*************Filtrage avec Longueur **************","\n")

filtered_df = df[df["Longueur"] > 10]
print(filtered_df, "\n","\n")

# 4)Calculer la moyenne du pourcentage de GC
print("************* Calcul de la moyenne *************,"\n")

average_gc = df["Pourcentage GC"].mean()
print(f"Pourcentage moyen de GC :{average_gc:3f}%","\n","\n")

# 5) Ajouter une nouvelle colonne avec des calculs 
print("************* Ajout d'une nouvelle colonne *************")

#Ajouter une nouvelle colonne " catégorisée "
print ("******************Ajouter une colonne Catégorie GC ***************" "\n")

df["Catégorie GC"] = df["Pourcentage GC"].apply(lambda x: "rich" if x>55 else "weak")
print(df, "\n")

df["Catégorie GC"] = df["Pourcentage GC"].apply(lambda x: "means"if 45<x<55 else "auther")
print(df,"\n")

df["Catégorie GC"] = df["Pourcentage GC"].apply(lambda x: "weak" if x<45 else "rich")
print(df, "\n")

# 6)ajouter une colonne donnant le nombre de"G" dans chaque séquence

df ["Nombre de G"] =
df["Séquence"].str.count("G")
print ("****** Nombre de "G" Ajoutés ****************", "\n")
print (df,"\n")


# 7)Calcul de l'écart-type du %GC et de la longueur des séquences

#print("******* l'écart-type de %GC et de la longueur des séquences*******","\n")

#l'écart-type de %GC

S_gc = df["Pourcentage GC"].mean()
print(f"écart-type de GC : {S_gc:.3f}%","\n","\n")

#l'écart-type de longueur 

S_gc = df["Longueur"].mean()
print(f"écart-type de longueur: {S_gc:.3f}%","\n","\n")


# 8)Sauvegarde et chargement des données avec panda
#Sauvegarder le DataFrame dans un fichier CSV
df.to_csv("tableau_sequences.csv", index=False)



