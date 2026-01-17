def presentation(nom, age):
    print(f"Je m'appelle {nom} et j'ai {age} ans.")

# Appels avec différentes valeurs
presentation("Alice", 25)
presentation("Marc", 34)
def afficher_message(message, prefixe="[INFO]"):
    print(f"{prefixe} {message}")

# Utilisation par défaut
afficher_message("Le système a démarré.") 
# Résultat : [INFO] Le système a démarré.

# Utilisation avec un préfixe personnalisé
afficher_message("Connexion perdue", prefixe="[ERREUR]")
# Résultat : [ERREUR] Connexion perdue
def produit(*args):
    resultat = 1
    for valeur in args:
        resultat *= valeur
    return resultat

print(produit(2, 3, 4)) # Résultat : 24
print(produit())        # Résultat : 1
def rapport(notes, bonus=0, seuil=10, titre="Rapport des notes"):
    print(f"--- {titre} ---")
    
    # 1. Appliquer le bonus
    notes_avec_bonus = appliquer_bonus(notes, bonus)
    
    # 2. Filtrer les notes validées
    notes_valides = filtrer_notes(notes_avec_bonus, seuil)
    
    # 3. Calculer la moyenne
    moy = moyenne(notes_valides)
    
    print(f"Moyenne des notes validées : {moy:.2f}")
    return moy
