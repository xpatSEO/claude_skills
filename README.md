# claude_skills

Collection de skills pour Claude Code.

## Skill: /frontend-design

Le skill `/frontend-design` permet de générer des designs frontend modernes et responsives avec des technologies web actuelles.

### Installation

#### Prérequis

- Claude Code CLI installé
- Node.js 18+ (optionnel, pour le preview local)

#### Étapes d'installation

1. **Cloner le repository**
   ```bash
   git clone https://github.com/xpatSEO/claude_skills.git
   cd claude_skills
   ```

2. **Configurer le skill dans Claude Code**

   Ajoutez le chemin du skill dans votre configuration Claude Code :
   ```bash
   claude config add skill /chemin/vers/claude_skills/frontend-design
   ```

   Ou ajoutez manuellement dans votre fichier de configuration `~/.claude/config.json` :
   ```json
   {
     "skills": [
       "/chemin/vers/claude_skills/frontend-design"
     ]
   }
   ```

3. **Vérifier l'installation**
   ```bash
   claude skills list
   ```

   Vous devriez voir `/frontend-design` dans la liste des skills disponibles.

### Utilisation

Une fois installé, invoquez le skill avec la commande :

```
/frontend-design [description de votre design]
```

#### Exemples

```
/frontend-design landing page moderne pour une startup SaaS
```

```
/frontend-design formulaire de contact avec validation
```

```
/frontend-design dashboard admin avec sidebar et graphiques
```

### Fonctionnalités

- **HTML5 sémantique** : Structure accessible et bien organisée
- **CSS moderne** : Flexbox, Grid, variables CSS, animations
- **Responsive Design** : Adapté mobile, tablette et desktop
- **Composants réutilisables** : Boutons, cartes, formulaires, navigation
- **Mode sombre** : Support du dark mode intégré
- **Accessibilité** : Conformité WCAG 2.1

### Structure générée

Le skill génère typiquement :

```
output/
├── index.html          # Page principale
├── styles/
│   ├── main.css        # Styles principaux
│   ├── variables.css   # Variables CSS (couleurs, espacements)
│   └── responsive.css  # Media queries
├── scripts/
│   └── main.js         # Interactions JavaScript (si nécessaire)
└── assets/
    └── images/         # Placeholder pour les images
```

### Configuration avancée

Vous pouvez personnaliser le comportement du skill avec un fichier `.frontend-design.json` à la racine de votre projet :

```json
{
  "framework": "vanilla",
  "cssPreprocessor": "none",
  "includeJS": true,
  "colorScheme": "auto",
  "language": "fr"
}
```

Options disponibles :
- `framework`: `"vanilla"` | `"tailwind"` | `"bootstrap"`
- `cssPreprocessor`: `"none"` | `"sass"` | `"less"`
- `includeJS`: `true` | `false`
- `colorScheme`: `"light"` | `"dark"` | `"auto"`
- `language`: `"fr"` | `"en"`

### Dépannage

#### Le skill n'apparaît pas dans la liste

Vérifiez que le chemin dans votre configuration est correct et que le dossier contient bien le fichier `skill.json`.

#### Erreur de permissions

```bash
chmod +x /chemin/vers/claude_skills/frontend-design/run.sh
```

### Support

Pour signaler un bug ou demander une fonctionnalité :
- Ouvrez une issue sur [GitHub](https://github.com/xpatSEO/claude_skills/issues)

## Licence

MIT