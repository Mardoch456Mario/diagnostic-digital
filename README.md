# 🚀 Digital Quest — Diagnostic Transformation Digitale

> Outil de diagnostic gamifié, 100% gratuit, déployé sur internet.

🌐 **Site en ligne** : [https://mardoch456mario.github.io/diagnostic-digital/](https://mardoch456mario.github.io/diagnostic-digital/)

---

## ✨ Fonctionnalités

- 🎮 **Gamification complète** : XP, niveaux, combo, badges à débloquer
- 📊 **5 dimensions** : Stratégie, Expérience Client, Données & IA, Processus, Culture
- 🏆 **10 badges** débloquables selon vos performances
- 📈 **Radar chart** de maturité digitale
- 📍 **Percentile** : votre position parmi les autres entreprises
- 🎯 **Plan d'action** prioritaire personnalisé
- ✉️ **Rapport par email** (via EmailJS)
- 📅 **Réservation d'appel** consultant (via Calendly)
- 🎊 **Confetti** et animations à la fin du diagnostic
- 📱 **Responsive** mobile/desktop

---

## ⚙️ Configuration en 3 étapes

### Étape 1 — Configurer EmailJS (envoi du rapport par mail)

1. Créez un compte gratuit sur [emailjs.com](https://www.emailjs.com/)
2. Ajoutez un **Email Service** (Gmail, Outlook, etc.)
3. Créez un **Email Template** avec les variables suivantes :
   - `{{to_email}}` — email du destinataire
   - `{{to_name}}` — prénom et nom
   - `{{company}}` — nom de l'entreprise
   - `{{global_score}}` — score global /100
   - `{{level}}` — niveau de maturité
   - `{{score_strategy}}` — score Stratégie
   - `{{score_customer}}` — score Expérience Client
   - `{{score_data}}` — score Données & IA
   - `{{score_process}}` — score Processus
   - `{{score_culture}}` — score Culture
   - `{{badges}}` — badges débloqués
   - `{{xp_total}}` — XP total
   - `{{recommendations}}` — recommandations prioritaires
4. Récupérez votre **Public Key**, **Service ID** et **Template ID**
5. Dans `index.html`, remplacez :
```js
const EMAILJS_PUBLIC_KEY = 'YOUR_PUBLIC_KEY';
const EMAILJS_SERVICE_ID = 'YOUR_SERVICE_ID';
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';
```

### Étape 2 — Configurer Calendly (réservation d'appel)

1. Créez un compte sur [calendly.com](https://calendly.com/)
2. Créez un événement "Appel Diagnostic Digital - 30 min"
3. Copiez votre lien Calendly (ex: `https://calendly.com/votre-nom/diagnostic`)
4. Dans `index.html`, remplacez :
```js
const CALENDLY_URL = 'https://calendly.com/votre-lien';
```

### Étape 3 — Déployer les modifications

Après avoir modifié `index.html`, commitez sur GitHub. Le site se met à jour automatiquement via GitHub Pages.

---

## 🗂️ Structure du projet

```
diagnostic-digital/
├── index.html    # Application complète (HTML + CSS + JS)
└── logo.png      # Logo de la marque
```

---

## 📬 Template email suggéré (à copier dans EmailJS)

**Objet** : 🚀 Votre rapport de maturité digitale — {{company}}

```
Bonjour {{to_name}},

Voici votre rapport de diagnostic de transformation digitale pour {{company}}.

📊 SCORE GLOBAL : {{global_score}}/100 — {{level}}
⭐ XP accumulés : {{xp_total}}
🏆 Badges : {{badges}}

SCORES PAR DIMENSION :
• Stratégie & Leadership : {{score_strategy}}%
• Expérience Client : {{score_customer}}%
• Données & IA : {{score_data}}%
• Processus & Automatisation : {{score_process}}%
• Culture & Compétences : {{score_culture}}%

🎯 RECOMMANDATIONS PRIORITAIRES :
{{recommendations}}

Pour aller plus loin, réservez votre appel gratuit avec un consultant :
https://calendly.com/votre-lien

À bientôt !
L'équipe Digital Quest
```

---

## 🧰 Stack technique

| Composant | Outil | Coût |
|-----------|-------|------|
| Frontend | HTML/CSS/JS vanilla | Gratuit |
| Charts | Chart.js CDN | Gratuit |
| Confetti | canvas-confetti | Gratuit |
| Fonts | Google Fonts (Inter) | Gratuit |
| Hébergement | GitHub Pages | Gratuit |
| Email | EmailJS | Gratuit (200 emails/mois) |
| Réservation | Calendly | Gratuit |

---

## 📄 Licence

MIT — Libre d'utilisation, modification et distribution.
