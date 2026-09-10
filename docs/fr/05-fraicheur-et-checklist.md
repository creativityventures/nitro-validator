# 05 — Fraicheur, rejeu et checklist

Le validateur ne compare pas automatiquement le timestamp en millisecondes a `block.timestamp` en secondes et ne lie pas le nonce a un challenge.
Le consommateur doit donc definir fenetre temporelle, challenge unique, destinataire et contexte de chaine.
1. Verifier la chaine de certificats et la politique PCR attendue.
2. Convertir les unites de temps explicitement et refuser futur ou ancien hors fenetre.
3. Marquer chaque challenge consomme avant tout effet externe rejouable.
4. Ne jamais dedupliquer par signature ECDSA brute.
5. Surveiller transferts de role et evenements de revocation.
Ce parcours est documentaire, pas un audit. Aucune installation, compilation ou execution de tests n a ete effectuee.
Source de verification future : [`test`](https://github.com/base/nitro-validator/tree/main/test).

[Retour au sommaire](README.md)
