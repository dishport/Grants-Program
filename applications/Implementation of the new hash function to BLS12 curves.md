# W3F Grant Proposal

- **Project Name:** Implementation of the new hash function to BLS12 curves
- **Team Name:** Dmitrii Koshelev
- **Payment Address:** With your permission, I would prefer provide my Bitcoin payment address after I won the grant
- **[Level](https://github.com/w3f/Grants-Program/tree/master#level_slider-levels):** 1

## Project Overview :page_facing_up:

### Overview

Please provide the following:

- If the name of your project is not descriptive, a tag line (one sentence summary).

Implementation in one of programming languages of my hash function to pairing-friendly curves BLS12 (for example, BLS12-381 or BLS12-377).
  
- A brief description of your project.

Recently, my article https://link.springer.com/article/10.1007/s10623-022-01012-8 was published in the quite prestigious cryptographic journal "Designs, Codes and Cryptography". This article provides a new hash function (indifferentiable from a random oracle) to the subgroup G1 of pairing-friendly elliptic curves BLS12-381 and BLS12-377 (Barreto-Lynn-Scott). These curves and such hash functions are actively used in blockchains, namely in the BLS (Boneh-Lynn-Shacham) aggregate signature. My hash function is much faster than previous state-of-the-art ones, including the Wahby-Boneh indirect map. For instance, BLS12-377 is defined over a highly 2-adic finite field Fp (of characteristic p), hence the indifferentiable Wahby-Boneh hash function requires to apply twice the slow Tonelli-Shanks algorithm for extracting two square roots in the basic field. In comparison, the new hash function extracts only one cubic root, which can be expressed via one exponentiation in Fp. I have already checked the correctness of my results in the computer algebra system Magma. The project is dedicated to implementing the new hash function in one of industrial programming languages (according to my wish or yours).
  
- An indication of how your project relates to / integrates into Substrate / Polkadot / Kusama.

According to the web page https://wiki.polkadot.network/docs/learn-keys, the BLS signature will be in particular used in Polkadot.
  
- An indication of why your team is interested in creating this project.

Because I want to demonstrate to the blockchain society that my research has an immediate practical value. 
  
### Project Details

- PoC/MVP or other relevant prior work or research on the topic

My article https://link.springer.com/article/10.1007/s10623-022-01012-8 under the name "Indifferentiable hashing to ordinary elliptic Fq-curves of j=0 with the cost of one exponentiation in Fq".

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?

Hashing to elliptic curves in the BLS (Boneh-Lynn-Shacham) aggregate signature.

- Who is your target audience (parachain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?

Developers who will use my hash function already implemented.

- Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

I don't know, because my project is quite extraordinary, in my opinion. Maybe, similar projects (based on recent results of mathematical cryptography) periodically arise in the Ethereum Foundation grants program.

## Team :busts_in_silhouette:

### Team members

- Name of team leader

Dmitrii Koshelev

- Names of team members

There are no other members.

### Contact

- **Contact Name:** Dmitrii Koshelev
- **Contact Email:** dimitri.koshelev@gmail.com
- **Website:** https://www.researchgate.net/profile/Dimitri-Koshelev

### Legal Structure

- **Registered Address:** 27B boulevard Jourdan, app. 317, Paris, France
- **Registered Legal Entity:** In this project I am an individual, but I work as a postdoctoral researcher in Telecom Paris (Polytechnic Institute of Paris).

### Team's experience

There is the regularly updated CFRG draft on hashing to elliptic curves: https://datatracker.ietf.org/doc/draft-irtf-cfrg-hash-to-curve/. As for me, at the beginning
of the last year, as said in https://blog.ethereum.org/2021/11/04/esp-allocation-update-q2-2021/, I won an Ethereum Foundation grant to derive a fast hash function to the subgroup G2 of the pairing-friendly curve BLS12-381. As an outcome of this grant, in Section 1.2 of https://eprint.iacr.org/2021/1082 I prove that for hashing to G2 the Wahby-Boneh map applied only once (not twice) is sufficient to act as a random oracle. Thus we get rid of one exponentiation in the quadratic extension Fp2 or, equivalently, of two exponentiations in the prime field Fp. Besides, I constructed a series of hash functions to other elliptic curves in the articles https://eprint.iacr.org/2021/1034 (accepted in SIAM Journal on Applied Algebra and Geometry), https://link.springer.com/article/10.1007/s12095-021-00478-y (published in Cryptography and Communications), https://eprint.iacr.org/2021/1604 (submitted to Journal of Mathematical Cryptology). 


### Team Code Repos

- https://github.com/dishport

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/dimitri-koshelev/

## Development Status :open_book:

- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,

https://ethresear.ch/t/indifferentiable-hashing-to-ordinary-elliptic-fq-curves-of-j-0-with-the-cost-of-one-exponentiation-in-fq/8867

https://github.com/cfrg/draft-irtf-cfrg-hash-to-curve/issues/316

https://github.com/dishport/Indifferentiable-hashing-to-ordinary-elliptic-curves-of-j-0-with-the-cost-of-one-exponentiation

https://link.springer.com/article/10.1007/s10623-022-01012-8

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 6 months
- **Full-Time Equivalent (FTE):** 1 FTE
- **Total Costs:** 10,000 USD


### Milestone 1 — Learning the syntax of the desired programming language (in fact, the advance payment for the milestone 2)

- **Estimated duration:** 3 months
- **FTE:**  1
- **Costs:** 5,000 USD  


### Milestone 2 — Implementation of the new hash function

- **Estimated Duration:** 3 months
- **FTE:**  1
- **Costs:** 5,000 USD

...


## Future Plans

The new hash function appears to be optimal, because it performs only one exponentiation in the basic field Fp. In other words, since it is highly unlikely that there is a hash function to an elliptic curve without exponentiations at all (even if it is supersingular), the result of my article seems to be unimprovable. Thus I hope that the implementation of my hash function will be interesting not only to you, but also to all blockchain projects that involve the BLS signature.

## Additional Information :heavy_plus_sign:

**How did you hear about the Grants Program?** Web3 Foundation Website

- If there are any other teams who have already contributed (financially) to the project.

No

- Previous grants you may have applied for.

An Ethereum Foundation grant called "fast hash-to-curve research" and represented on the web page https://blog.ethereum.org/2021/11/04/esp-allocation-update-q2-2021/
