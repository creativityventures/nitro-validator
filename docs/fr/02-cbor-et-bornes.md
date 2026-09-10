# 02 — CBOR, COSE et bornes de parsing

Le document d attestation utilise CBOR et une enveloppe COSE, deux couches que Solidity doit decoder sans ambiguite.
Les longueurs, types majeurs, offsets et limites du buffer sont des invariants de securite avant toute interpretation.
Un parseur ne doit pas accepter des champs dupliques ou des representations alternatives lorsque la politique exige une forme canonique.
Chaque tranche transmise au verificateur doit etre liee aux octets exacts signes par AWS.
Les erreurs de parsing doivent provoquer un rejet, jamais une valeur par defaut confondue avec un champ absent.
La revue suit octets, element CBOR, champ semantique puis usage applicatif.
Source : [`src/CborDecode.sol`](https://github.com/base/nitro-validator/blob/main/src/CborDecode.sol).

[Suite : certificats](03-certificats-et-revocation.md)
