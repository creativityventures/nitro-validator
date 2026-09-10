# 04 — P-384 et malleabilite

Les attestations AWS emploient ECDSA P-384, verifiee par une implementation adaptee a Solidity.
Le depot indique que la forme low-S n est pas imposee car AWS ne l emet pas ainsi.
La signature admet donc un jumeau malleable `(r, n-s)` qui valide le meme message.
Cette propriete ne casse pas l authenticite, mais interdit d utiliser les octets de signature comme identifiant unique.
La deduplication doit porter sur les champs canoniques de l attestation et le contexte de challenge.
Les coordonnees, scalaires, hash et message signes doivent rester lies au meme chemin de validation.
Sources : [`src/P384Verifier.sol`](https://github.com/base/nitro-validator/blob/main/src/P384Verifier.sol) et [`README.md`](https://github.com/base/nitro-validator/blob/main/README.md).

[Suite : fraicheur](05-fraicheur-et-checklist.md)
