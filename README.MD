# Installation

Il faut avoir python et pip ( gestionnaire des packages )

Commence par créer un  ```venv```

```bash
python -m venv .venv/
```

Active le ```venv```

```bash
 ./.venv/bin/activate
```

D'abord installe les packages

```bash
pip install -r requirements.txt
```

Ensuite copie .env.example a .env

```bash
cp .env.example .env
```

Tu met la clé api gpt 
```ini
OPENAI_KEY=<ici la clé>
```

Met ton fichier pdf a la racine du projet, et exécute 

```bash
python app.py
```

Tu devrais avoir le pptx a la racine du projet aussi

## Step up

Joue sur le prompt a la ligne 

```python
    prompt = (
        "Tu es un expert en rédaction technique. Voici un document que je souhaite résumer sous forme de présentation PowerPoint.\n"
        "Génère un JSON contenant une liste de slides avec : un titre, un sous-titre, un contenu et une URL d'image pertinente.\n\n"
        f"Document : {texte_pdf}\n\n"
        "Réponds uniquement avec un JSON bien structuré sous cette forme :\n"
        '{ "slides": [ { "titre": "...", "sous_titre": "...", "contenu": "...", "image": "..." } ] }'
    )
```

Pour voir ce qui te correspond, good luck dude 