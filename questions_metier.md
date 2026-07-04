# Questions métier - Analyse Ventes Supermarché

## Question 1 — Statistiques de base
**Code :** `df['revenue'].sum()`, `df['revenue'].mean()`, `df['revenue'].max()`, `df['revenue'].min()`, `len(df)`
**Interprétation :** Vue d'ensemble du chiffre d'affaires global du supermarché.

## Question 2 — Chiffre d'affaires par catégorie de produit
**Code :** `df.groupby('product_line')['revenue'].sum().sort_values().plot(kind='barh')`
**Interprétation :** Identifie les catégories les plus rentables pour orienter les décisions commerciales.

## Question 3 — Ventes totales par moyen de paiement
**Code :** `df.groupby('payment_method')['revenue'].sum().plot(kind='bar')`
**Interprétation :** Montre les préférences de paiement des clients.

## Question 4 — Note moyenne des clients par ville
**Code :** `df.groupby('city')['rating'].mean().plot(kind='bar')`
**Interprétation :** Évalue la satisfaction client selon la localisation.

## Question 5 — Répartition des ventes par genre
**Code :** `df.groupby('gender_customer')['revenue'].sum().plot(kind='pie')`
**Interprétation :** Analyse le comportement d'achat selon le genre.

## Question 6 — Quantité vendue par catégorie de produit
**Code :** `df.groupby('product_line')['quantity'].sum().sort_values().plot(kind='barh')`
**Interprétation :** Identifie les catégories les plus vendues en volume.

## Question 7 — CA moyen par moyen de paiement
**Code :** `df.groupby('payment_method')['revenue'].mean().plot(kind='bar')`
**Interprétation :** Compare le panier moyen selon le moyen de paiement.

## Question 8 — Top 3 des catégories les plus rentables
**Code :** `df.groupby('product_line')['revenue'].sum().sort_values(ascending=False).head(3)`
**Interprétation :** Identifie les 3 catégories générant le plus de chiffre d'affaires.