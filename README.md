# roberto.github.io
Static version of the excellent minitel simulator from minipavi.fr and Zigazou (https://github.com/Zigazou)

---

# Émulateur Minitel (MiniPavi)

Cet émulateur Minitel est une version légèrement modifiée de celui
réalisé et proposé par **Frédéric Bisson**.

L'émulateur d'origine, incluant un éditeur de pages vidéotex,
est disponible ici :

👉 https://github.com/Zigazou/miedit

## Fonctionnalités spécifiques à cette version

Cette version ajoute les fonctionnalités suivantes :

- Correction de petits bugs mineurs
- Support du **WebMedia** de MiniPavi
- Mise en pause du flux de données
- Enregistrement du flux de données
- Réponse à la demande d'identification en tant que modèle **EmU**
- Support de séquences **PRO2** spécifiques pour :
  - le changement de vitesse de l'émulateur
  - le changement du mode d'affichage (couleur / noir et blanc) de l'émulateur

## Séquences PRO2 spécifiques à l'émulateur

### Vitesse de transmission

| Séquence | Vitesse |
|--------|--------|
| `PRO2 / 0x10 / 0x41` | 1200 bds |
| `PRO2 / 0x10 / 0x42` | 4800 bds |
| `PRO2 / 0x10 / 0x43` | 9600 bds |
| `PRO2 / 0x10 / 0x44` | Vitesse maximale |

### Mode d'affichage

| Séquence | Mode |
|--------|------|
| `PRO2 / 0x11 / 0x41` | Noir et blanc |
| `PRO2 / 0x11 / 0x42` | Couleur |

### Rappel

```text
PRO2 = 0x1B 0x3A
