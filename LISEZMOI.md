<!--
  Nom      : LISEZMOI.md
  Objet    : Présentation du dépôt sstv (émission, réception et diagnostic SSTV)
  Auteur   : Eric PERRET
  Date     : 2026-10-17
  Licence  : CC BY-NC 4.0
-->

# 📻 SSTV

🇬🇧 [English version: README.md](README.md)

Télévision à balayage lent (SSTV) dans le navigateur : émission d'une image en fichier audio, décodage d'un fichier ou du son en direct, diagnostic d'un enregistrement. Trois fichiers HTML autonomes, aucune librairie, aucune installation. Interfaces en français (diagnostic en anglais).

▶️ **[Page d'accueil des outils](https://ericperret.github.io/sstv/index2.html)**

| Outil | Lancer |
|---|---|
| Émetteur SSTV multi-mode v4 | ▶️ **[sstv_tx_multimode_v4.html](https://ericperret.github.io/sstv/sstv_tx_multimode_v4.html)** |
| SSTV Decoder Ultimate | ▶️ **[sstv_decoder_ultimate.html](https://ericperret.github.io/sstv/sstv_decoder_ultimate.html)** |
| SSTV Diagnostic | ▶️ **[sstv_diagnostic.html](https://ericperret.github.io/sstv/sstv_diagnostic.html)** |

---

## Émetteur SSTV multi-mode v4

![Émetteur SSTV multi-mode v4](screenshot_sstv_tx_multimode_v4.png)

| Fonction | Description |
|---|---|
| Image | Chargement d'une image, mise à l'échelle du mode choisi |
| Modes | Robot36 couleur et N&B, Robot72, Martin M1 / M2, Scottie S1 / S2, PD120, PD180 (durée affichée) |
| Signal | Échantillonnage 44,1 / 48 / 22,05 kHz, filtre passe-bas, lissage des transitions de ligne |
| En-tête | Code VIS (auto-détection à la réception), mire de calibration 1 s à 1 900 Hz |
| Sortie | Fichier WAV téléchargé, à diffuser par un émetteur ou un haut-parleur |

## SSTV Decoder Ultimate

![SSTV Decoder Ultimate](screenshot_sstv_decoder_ultimate.png)

| Fonction | Description |
|---|---|
| Sources | Fichier WAV, ou audio en direct (micro, autorisation demandée) |
| Modes | Détection automatique par code VIS, ou forcé : Robot36 / 72, Martin M1 / M2, Scottie S1 / S2, PD90 à PD240 |
| Synchronisation | PLL sur les impulsions de synchronisation, AFC automatique, décalage Doppler manuel, correction d'inclinaison (slant) |
| Analyse | Analyse du signal, affichage de l'image au fil du décodage, journal de débogage |
| Sortie | Export PNG de l'image décodée |

## SSTV Diagnostic

![SSTV Diagnostic](screenshot_sstv_diagnostic.png)

| Fonction | Description |
|---|---|
| Entrée | Fichier WAV |
| Recherches | Code VIS, impulsions de synchronisation, mesure de la durée de ligne |
| Tracé | Fréquence instantanée, mesure au clic |
| Résultats | Marqueurs détectés, analyse des temps, journal |

---

## Radioamateurisme

La SSTV sert aux radioamateurs pour transmettre des images en HF / VHF. Ces outils permettent d'expérimenter sans émetteur, par câble audio ou couplage acoustique ; l'émission sur les bandes radioamateurs reste soumise à licence.

## Historique

| Version | Évolution |
|---|---|
| 2026-10-17 | Fichiers renommés sans suffixe de copie, cartouches, page d'accueil corrigée, README / LISEZMOI réécrits |

## Licence

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/deed.fr) — voir [LICENSE (CC BY-NC 4.0)](<LICENSE (CC BY-NC 4.0)>).

## Auteur

**Eric PERRET** — [GitHub](https://github.com/ericperret)
