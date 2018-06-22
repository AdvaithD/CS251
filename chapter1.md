# First Chapter

### Chapter 1: Introduction to Cryptography & Cryptocurrencies

* All currencies need some way to control supply and enforce various security properties to prevent cheating
* Fiat - Central banks control supply. Law enforcement required.
* Crypto - Security measures to prevent people from tampering with the state of the system
  * Alice bob analogy
  * Cryptography provides a mechanism for encoding rules of a cryptocurrency system in itself
  * Cryptocurrencies make use of hash functions and digital signatures.

### 1.1 Cryptographic Hash Functions

* Mathematical function
  * Input can be any string of any size
  * Produces fixed size output. \(Assuming 256-bit here\)
  * Efficiently computable\(figure out output in a reasonable amount of time\)
    * Computing hash of an n-bit string should have a running time O\(_n_\)
* Hash functions can be used to build a data structure such as a hash table
* Secure hash function
  * Collision resistance
    * Collision occurs when two distinct inputs produce same output.
    * Formally: hash function H is resistant to collisions if it is infeasible to find x and y, x!= y, but H\(x\) = H\(y\)
    * Nobody can find a collision but collisions do exist
      * Input space larger than output space
      * Pigeonhole principle
    * Birthday paradox: picking more inputs than possible outputs
  * Hiding
    * If given the hash y = H\(x\) theres no feasible way to figure out the input x.
    * A hash function is hiding when a secret value r is chosen from a probability distribution  that has high min-entropy. Then given H\(r \|\| x\) it is infeasible to find x.
    * **min-entropy: **Measure of how predictable an outcome is. High min-entropy implies that the distribution is spread out.
  * puzzle friendliness
* Message digests
  * x and y unique =&gt; H\(x\) and H\(y\) are unique.
    * If  someone knew x and y that were unique, but have the same hash, that would violate our assumption that H is collision resistance
  * SecureBox - authenticated online file storage system
    * Upload files and ensure integrity using hashes.



