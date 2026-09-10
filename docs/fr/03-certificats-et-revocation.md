# 03 — Chaine de certificats et revocation

Le gestionnaire de certificats ancre la confiance dans une racine et suit les certificats revoques.
La verification d une chaine doit lier chaque emetteur, periode, cle et signature jusqu a l ancre configuree.
La revocation est un etat administratif critique : proprietaire, revoker et evenements doivent etre surveilles.
Une modification legitime mais inattendue peut invalider ou elargir toutes les attestations acceptees.
Un timelock, une separation de roles et un runbook de rotation reduisent le risque operationnel.
Les caches doivent etre indexes par des champs canoniques, pas par une signature malleable.
Source : [`src/CertManager.sol`](https://github.com/base/nitro-validator/blob/main/src/CertManager.sol).

[Suite : P-384](04-p384-et-malleabilite.md)
