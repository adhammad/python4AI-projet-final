# Python4AI

Mini projet d'initiation a l'intelligence artificielle autour d'un mini reseau de neurones, applique au probleme XOR.

Ce depot sert de base de TP pour comprendre, pas a pas, comment construire et entrainer un modele simple avec NumPy.

## Sommaire

- [Presentation](#presentation)
- [Structure du projet](#structure-du-projet)
- [Prerequis](#prerequis)
- [Installation rapide](#installation-rapide)
- [Execution du notebook](#execution-du-notebook)
- [Deroule pedagogique du TP](#deroule-pedagogique-du-tp)
- [Resultats attendus](#resultats-attendus)
- [Livrables conseilles](#livrables-conseilles)
- [Depannage](#depannage)

## Presentation

Le probleme XOR est un classique de l'apprentissage machine. Il montre qu'un modele lineaire simple ne suffit pas et qu'une architecture a couches cachees est necessaire.

Dans ce TP, vous allez :

- manipuler des donnees et des vecteurs avec NumPy ;
- utiliser des fonctions d'activation ;
- implementer un mini reseau de neurones ;
- observer l'apprentissage via la perte et les predictions ;
- visualiser des resultats avec Matplotlib.

## Structure du projet

- `notebooks/TP_mini_reseau_neurones_XOR.ipynb` : notebook principal du TP.
- `reports/` : dossier pour comptes rendus, exports et captures.
- `TP_NumPy_Matplotlib_Fonction_Activation_Mini_Reseau_Neurone_XOR.pdf` : enonce/support du TP.

## Prerequis

- Python 3.10 ou plus
- `pip`
- (optionnel mais recommande) environnement virtuel `venv`

Dependances Python utilisees dans le notebook :

- `numpy`
- `matplotlib`
- `scipy`
- `jupyter` (ou `notebook`)

## Installation rapide

Depuis la racine du projet :

```bash
python -m venv venv
```

### Activation de l'environnement virtuel

Sous PowerShell :

```powershell
.\venv\Scripts\Activate.ps1
```

Sous Git Bash :

```bash
source venv/Scripts/activate
```

### Installation des packages

```bash
pip install numpy matplotlib scipy notebook
```

## Execution du notebook

Lancez Jupyter depuis la racine du projet :

```bash
jupyter notebook
```

Puis ouvrez :

- `notebooks/TP_mini_reseau_neurones_XOR.ipynb`

Conseil : executez les cellules dans l'ordre pour garder un etat coherent.

## Deroule pedagogique du TP

1. Chargement des bibliotheques et configuration.
2. Definition des donnees XOR.
3. Construction de la structure du mini reseau.
4. Initialisation des poids et biais.
5. Propagation avant (forward pass).
6. Calcul de la perte.
7. Retropropagation et mise a jour des parametres.
8. Evaluation finale sur les entrees XOR.
9. Visualisation et interpretation des resultats.

## Resultats attendus

A la fin du notebook, vous devriez etre capable de :

- expliquer pourquoi XOR n'est pas lineairement separable ;
- decrire le role des couches et activations ;
- justifier l'effet du taux d'apprentissage ;
- obtenir des predictions coherentes sur les 4 cas XOR.

## Livrables conseilles

Vous pouvez placer dans `reports/` :

- un compte rendu court (methodologie + observations) ;
- des captures de courbes (perte, evolution des sorties) ;
- une conclusion avec pistes d'amelioration.

## Depannage

### `jupyter` non reconnu

Installez notebook dans l'environnement actif :

```bash
pip install notebook
```

### Kernel introuvable dans le notebook

Verifiez que le venv est bien active, puis installez ipykernel :

```bash
pip install ipykernel
python -m ipykernel install --user --name python4ai
```

### Erreur d'import (`numpy`, `matplotlib`, `scipy`)

Installez les packages manquants dans le meme environnement que celui du notebook :

```bash
pip install numpy matplotlib scipy
```

---