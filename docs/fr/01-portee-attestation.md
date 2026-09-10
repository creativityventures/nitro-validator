# 01 — Ce que prouve une attestation Nitro

Une attestation Nitro relie un document signe a une chaine de certificats AWS et a des mesures d enclave.
Le validateur Solidity verifie structure, certificats et signature avant de remettre les champs au contrat consommateur.
Cette authenticite ne prouve pas a elle seule la fraicheur, l unicite ou l adequation des mesures a une politique applicative.
Le consommateur doit comparer les PCR attendus et definir les champs obligatoires pour son usage.
Une attestation valide peut donc rester inacceptable pour une session ou une version de code donnee.
La valeur du composant tient autant a cette frontiere explicite qu a la verification cryptographique.
Source : [`src/NitroValidator.sol`](https://github.com/base/nitro-validator/blob/main/src/NitroValidator.sol).

[Suite : CBOR](02-cbor-et-bornes.md)
