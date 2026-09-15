# WoW Forever — Group Planner

Outil de composition de groupe pour **WoW Forever** (5 joueurs, partageable via URL).

🔗 **[Ouvrir le planificateur](https://ton-compte.github.io/wow-forever-group-planner/)**
*(remplace `ton-compte` par ton pseudo GitHub après déploiement)*

---

## Fonctionnement

1. **Joueur 1** ouvre le site, choisit la faction (Horde ou Alliance), et reçoit une URL unique.
2. Il remplit son pseudo, sa race, sa classe et ses deux spécialisations, puis **copie le lien** et l'envoie au Joueur 2.
3. Chaque joueur suivant ouvre le lien, remplit son slot et passe le lien enrichi au suivant.
4. Une fois les 5 slots remplis, la **page d'audit** s'affiche automatiquement avec :
   - La composition visuelle du groupe (icônes de classe, rôles)
   - Le score de versatilité du groupe
   - Une checklist complète des utilitaires (Bloodlust, Battle Rez, CC, Interrupts, Buffs…)

**Zéro backend** — tout l'état est encodé dans le fragment `#` de l'URL. Aucune donnée n'est envoyée à un serveur.

---

## Races et classes disponibles (WoW Forever)

### Horde
| Race | Classes |
|---|---|
| Orc | Warrior, Hunter, **Mage** *(nouveau)*, Rogue, Warlock, Shaman |
| Tauren | Warrior, Hunter, Druid, Shaman |
| Troll | Warrior, Hunter, Mage, Rogue, Priest, **Warlock** *(nouveau)*, Shaman |
| Undead | Warrior, Mage, Rogue, Priest, Warlock, **Paladin** *(nouveau)* |
| Skyborne (Horde) | Warrior, Hunter, Rogue, Druid, **Shaman** |

### Alliance
| Race | Classes |
|---|---|
| Gnome | Warrior, Mage, Rogue, **Priest** *(nouveau)*, Warlock |
| Human | Warrior, **Hunter** *(nouveau)*, Mage, Rogue, Priest, Warlock, Paladin |
| Night Elf | Warrior, Hunter, Rogue, Priest, Druid |
| Dwarf | Warrior, Hunter, Rogue, Priest, Paladin, **Shaman** *(nouveau)* |
| Skyborne (Alliance) | Warrior, Hunter, **Mage**, Rogue, Druid |

---

## Déploiement sur GitHub Pages

1. Crée un nouveau dépôt public sur GitHub (ex : `wow-forever-group-planner`)
2. Pousse ce répertoire sur la branche `main`
3. Dans **Settings → Pages**, sélectionne **Branch: main / root**
4. Après quelques secondes, le site est accessible sur `https://<ton-compte>.github.io/wow-forever-group-planner/`

```bash
git init
git add index.html README.md
git commit -m "Initial commit — WoW Forever Group Planner"
git branch -M main
git remote add origin https://github.com/<ton-compte>/wow-forever-group-planner.git
git push -u origin main
```

---

## Hébergement

- **GitHub Pages** — gratuit, aucun serveur requis
- Fichier unique `index.html` (~800 lignes) — HTML + CSS + JS inline
- Aucune dépendance npm, aucun build tool
