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


#3)Filtrer les sequences avec une longeure est supriere a 10
print("*************Filtrage avec longeure *************","\n")

filtred_df["longeure"] > 10]
print(filtred_df,"\n")

#4)Calculer la moyen du pourcentage de GC
print("************* Calcul de la moyen *************,"\n")

average_gc - df["Pourcentage GC"].mean()
print(f"Pourcentage moyen de GC :{average_gc:3f}%")

#5) Ajouter une nouvelle colonne avec des calculs 
print("************* Ajout d'une nouvelle colonne *************")

#Ajouter une nouvelle colonne " longueur catégorisée "
df["catégorie longueur"] = df ["longueur "] apply (Laubde x : "longue" if × 10 else 
print (df)

#6)Ajout une colonne comptant les "G"
df ["Nombre de G] =["Séquence"]str.count("G")

print ("***** Nombre de Ajout *****)
print (df,"\n").

#7) calculer l'ecrant-type du % de GC et de ka longueur 
ecart-type-gc = df ['pourcentage GC'] std()

ecart_type_longueur = df ['Longueur'] std()
print ("\n7 ecart_type:")
print (f"Écart_type GC:ecart_tyoe_gc: .3f)
print(f"Écart_type longureur:{ecart_type_lingueur: .3f}")

#___8)sauvegarder le tableau final dans un fichier CSV___
#L'argument index =False permet de ne pas écrire l'indese de pandas.
df.to _CSV('resultats_adn_final.CSV', index=False)

print("\n###8 sauvrgarde###")
print ("Le tableau final(avec les nouvelles colonnes)a été savaugardé dans 'resultats _adn_final.CSV'.")


