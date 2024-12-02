# AuthBJJCredential

AuthBJJCredential is a primary credential for each identity. It represents an authorization operational key.
Hex of the current auth claim schema is _ca938857241db9451ea329256b9c06e5_.
This claim must be presented in most circuits for identity verification.


A Baby Jubjub key uses a specific elliptic curve defined over the large prime subgroup of the BN128 elliptic curve. To know more about the bjj key, you can [visit this page](https://iden3-docs.readthedocs.io/en/latest/_downloads/33717d75ab84e11313cc0d8a090b636f/Baby-Jubjub.pdf).

X and Y values of the bjj public key are part of the Index data slots [I_2] and [I_3].

You can find below an example of a claim entry:

```
Index:
 i_0: [ 128 bits] 269270088098491255471307608775043319525 // auth schema (big integer from ca938857241db9451ea329256b9c06e5)
      [ 32 bits ] 00010000000000000000 // header flags: first 000 - self claim 1 - expiration is set. 
      [ 32 bits ] 0
      [ 61 bits ] 0 
 i_1: [ 253 bits] 0
 i_2: [ 253 bits] 15730379921066174438220083697399546667862601297001890929936158339406931652649 // x part of BJJ pubkey
 i_3: [ 253 bits] 5635420193976628435572861747946801377895543276711153351053385881432935772762  // y part of BJJ pubkey
Value:
 v_0: [ 64 bits ] 2484496687 // revocation nonce
      [ 64 bits ] 1679670808 // expiration timestamp
      [ 125 bits] 0
 v_1: [ 253 bits] 0
 v_2: [ 253 bits] 0
 v_3: [ 253 bits] 0
```

