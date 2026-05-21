**
readme_fusion = """# Ventec KPI Dashboard — Streamlit Wrapper

Tableau de Bord KPI pour **Ventec Industries** (filiale Ventec Groupe), spécialisée dans la fabrication de gaines de ventilation. Application Streamlit intégrant une interface HTML/CSS/JS complète pour le pilotage du système de management QSE (ISO 9001 · ISO 45001 · ISO 14001).

---

## 🔧 Fix apporté

**Problème** : Les fonctions comme "Gérer mes KPIs" semblaient cassées après déploiement Streamlit.

**Cause** : La hauteur excessive de l'iframe Streamlit faisait disparaître les éléments CSS `position: fixed` (modales, notifications) loin dans le scroll.

**Solution** : Hauteur d'iframe fixée à `930px` — suffisant pour le viewport sans casser le positionnement fixed.

```python
components.html(html_code, height=930, scrolling=True)
```

---

## 📁 Fichiers

| Fichier | Rôle |
|---------|------|
| `app.py` | Application Streamlit (wrapper + config page) |
| `index.html` | Interface complète HTML/CSS/JS (dashboard KPI) |
| `requirements.txt` | Dépendance : `streamlit` |

---

## 🚀 Déploiement

### Local

```bash
pip install -r requirements.txt
streamlit run app.py
```

### Streamlit Cloud

```
Main file path: app.py
```

---

## 🔐 Accès

**Code login** : `ventec2026`

| Profil | Département | Processus |
|--------|-------------|-----------|
| Directeur Général | DG | Management Général (MPM1) |
| Responsable QSE | QSE | Management QSE (MPM2) |
| Chef Service RH | RH | Management RH (MPM3) |
| Directeur Technique | Production | Production (MPR4) |
| Chef Service Achats | Achats | Achats (MPS1) |
| Resp. Logistique | Logistique | Logistique (MPS2) |
| Chef Service SI | SI | Systèmes d'information (MPS4) |
| Chef Service MG | Moyens Généraux | Moyens Généraux (MPS5) |

---

## 📊 Modules

- **Accueil** — Vue d'ensemble et statistiques KPI
- **Politique QSE** — Lettre d'engagement et engagements direction
- **Cartographie** — Carte interactive des processus
- **Axes & Objectifs** — Objectifs stratégiques par processus
- **Tableau de Bord KPI** — Suivi temps réel avec code couleur
- **Calculateur KPI** — Outil de calcul interactif
- **Visualisation** — Graphiques Chart.js (barres, lignes, aires)
- **Tableau Excel** — Saisie, calculs auto, export Excel
- **Rapport de Processus** — Rapport détaillé par période
- **Suivi des Actions** — Actions correctives (Ouvert/En cours/Clôturé)

---

## 🛠️ Stack technique

- **Backend** : Python + Streamlit
- **Frontend** : HTML5, CSS3, Vanilla JS
- **Graphiques** : Chart.js 4.4.1 (CDN)
- **Export Excel** : xlsx-js-style (CDN)

---

## 👤 Auteur

**Abirdrissi** — [GitHub](https://github.com/Abirdrissi)

---

*Version 2026 — Ventec Industries*
"""

output_path = "/mnt/agents/output/README.md"
with open(output_path, "w", encoding="utf-8") as f:
    f.write(readme_fusion)

print("README fusionné généré avec succès !")
print(f"Taille : {len(readme_fusion)} caractères")
**
