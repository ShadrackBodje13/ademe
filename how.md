Fork le projet sur ma machine

Pip install -r requirements.txt 

<!-- Pour installer ma librairie -->
pip freeze > requirements.txt

<!-- Lancer mon feature qui cree mon fichier csv -->
Python .\script\features.py 

<!-- Si erreur, KeyError: 'I' choisir de supprimer ou rajouter la Colonne -->
print(data['etiquette_dpe'].unique())
print(data['etiquette_dpe'].value_counts())
Ce que je peux faire, c'est soit rajouter le I soit supprimer le I
- Pour supprimer : il faut en bas de target_encoding
if 'I' in target_encoding:
    del target_encoding['I']
- Sinon rajouter I dans les données
    target_encoding = {"A": 1, "B": 2, "C": 3, "D": 4, "E": 5, "F": 6, "G": 7, "I":8}

Puis run > Python .\script\features.py

<!-- Run train.py -->
Mettre en commentaire la librairie sur MLFLOW
python .\script\train.py

