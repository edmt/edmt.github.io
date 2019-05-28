---

title: Common rules in cryptography
date: 2019-05-17 03:26 UTC
tags: Software

---

> While cryptographic security is precisely defined, this paper asks the question whether developers who use cryptographic APIs achieve this notion of security. Using cryptographic primitives correctly can be challenging. In particular, any application that violates one of the following six rules cannot be secure.
>
>__Rule 1: Do not use ECB mode for encryption.__
>
>A significant problem with ECB mode is that identical messages encrypt to identical ciphertexts. Such a leak of information is often intolerable.
>
>__Rule 2: Do not use a non-random IV for CBC encryption.__
>
>In essence, CBC$ shouldalways be used. Unfortunately, it is common to initializethe IV with a constant, e.g., all zeros. A constant IV results in a deterministic, stateless cipher.
>
>__Rule 3: Do not use constant encryption keys.__
>
>Intuitively, a constant key hard-coded in publicly available software is not a secret key, thus the resulting encryption does not provide privacy. 
>
>__Rule 4: Do not use constant salts for PBE.__
>__Rule 5: Do not use fewer than 1,000 iterations for PBE.__
>
>Rule 4 and Rule 5 are both recommended best practices for PBE schemes.
>
>__Rule 6: Do not use static seeds to seed SecureRandom()__

_Reference: M. Egele, D. Brumley, Y. Fratantonio, and C. Kruegel. An Empirical Study of Cryptographic Misuse in Android Applications._
