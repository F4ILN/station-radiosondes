# Station de réception de radiosondes météo

Manuel de montage et d'exploitation, en français, d'une station de réception de
radiosondes météorologiques. Un Raspberry Pi, une clé SDR, une antenne, et les
trames des sondes lâchées deux fois par jour par les centres météo sont décodées
et remontées automatiquement vers [SondeHub](https://sondehub.org).

Le manuel va du déballage du matériel à la première sonde décodée, puis au-delà :
suivre une sonde en mobile, la retrouver au sol, améliorer la réception, et
reprogrammer une sonde récupérée pour en faire une balise radioamateur.

**[→ Télécharger le manuel (PDF)](../../releases/latest/download/manuel-station-radiosondes.pdf)**
 · [version Word](../../releases/latest/download/manuel-station-radiosondes.docx)
 · [toutes les versions](../../releases)

Environ 100 pages, illustrées. Format A4.

## Ce que couvre le manuel

**Installer.** Le matériel et le choix du Raspberry Pi, puis l'installation en dix
étapes : préparer la carte SD, régler le WiFi, écarter le pilote TV natif,
installer Docker, tester la clé SDR, écrire le fichier de configuration, lancer le
décodeur et attendre la première sonde. Comptez une heure.

**Exploiter.** La maintenance et les mises à jour, la lecture des journaux, et de
quoi comprendre ce que l'on entend : à quoi ressemble la modulation d'une RS41,
d'une M20 ou d'une DFM à l'oreille.

**Chasser.** Suivre une sonde en voiture et la retrouver au sol : ChaseMapper, le
TTGO T-Beam sous rdzTTGOsonde, MySondy GO, le portatif Quansheng qui décode les
trames et affiche la position, et la radiogoniométrie à l'ancienne par décalage en
fréquence — la méthode qui fonctionne encore quand tous les récepteurs saturent.

**Recevoir mieux.** Préamplificateurs, antennes du commerce et antennes à
fabriquer : ground plane 403 MHz pas à pas, dipôle, Slim Jim, colinéaire COCO,
avec le bilan de liaison qui explique ce qu'on peut raisonnablement espérer.

**Reprogrammer.** Une annexe pas à pas pour transformer une sonde récupérée en
balise : RS41 sous RS41ng ou RS41-NFW, M20 et M10, avec le brochage, les cibles de
compilation et les pièges de chaque génération de carte.

**Références.** Tous les réglages de `station.cfg` et du firmware du TTGO, les
alternatives à `radiosonde_auto_rx`, la réglementation, le dépannage, un glossaire
et les liens utiles.

## Le matériel décrit

- Raspberry Pi 3, 4 ou 5 — la procédure est identique sur les trois
- Carte micro-SD de 16 Go minimum
- Clé RTL-SDR Blog V4
- Antenne 403 MHz, du bout de fil pour les premiers essais à l'antenne fabriquée
- Câble coaxial 50 Ω
- Un PC sur le même réseau pour la configuration

En option, pour la chasse : un TTGO T-Beam, un préamplificateur, un portatif.

## Signaler une erreur, proposer un complément

Ce manuel s'est construit par relectures successives et il reste perfectible.
Si vous relevez une erreur, une valeur qui ne correspond pas à ce que vous
mesurez, un lien mort, ou s'il vous manque quelque chose : ouvrez une
[issue](../../issues). Les retours de terrain sont les plus utiles — une
manipulation qui échoue sur votre matériel en dit plus long que n'importe quelle
relecture.

Les chapitres qui n'ont pas encore été vérifiés sur le terrain sont signalés comme
tels dans le manuel, au chapitre « Sources et crédits », avec la documentation sur
laquelle ils s'appuient.

## Sources et crédits

Le manuel cite ses sources chapitre par chapitre. Il doit beaucoup au projet
[radiosonde_auto_rx](https://github.com/projecthorus/radiosonde_auto_rx) de
Project Horus et à son wiki, au firmware
[rdzTTGOsonde](https://github.com/dl9rdz/rdz_ttgo_sonde) de DL9RDZ, à
[RS41ng](https://github.com/mikaelnousiainen/RS41ng) de Mikael Nousiainen, et aux
travaux publiés par de nombreux radioamateurs — F1LVT, F0GYS, F5ZJ, F4DKA, F4CQA,
F5BEZ, F4HWN, KF6ZEO, PH1M, OM3BC et d'autres, tous nommés dans le chapitre
correspondant.

## Licence

Le texte et les figures de l'auteur sont sous licence
[CC BY-NC-SA 4.0](LICENSE) : réutilisation libre en citant la source, pas d'usage
commercial, partage dans les mêmes conditions. Certaines illustrations
proviennent de tiers et restent la propriété de leurs auteurs — voir le fichier
[LICENSE](LICENSE).

## Auteur

Daniel GUIRAUD — F4ILN
