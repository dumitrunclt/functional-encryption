#  Functional Encryption (FE) & Multi-Party Functional Encryption (MPFE)

A curated list of open-source libraries, software implementations, frameworks, and foundational papers for Functional Encryption (FE), Multi-Input Functional Encryption (MIFE), Multi-Party Functional Encryption (MPFE), and Decentralized Multi-Client FE (DMCFE).

Functional Encryption (FE) generalizes public-key cryptography by allowing private key holders to evaluate specific functions over encrypted data without decrypting the full plaintext. Multi-Party Functional Encryption (MPFE) and Multi-Input FE (MIFE) extend this to multi-user environments, enabling computation over ciphertexts and keys originating from distributed sources.

## Contents
- [Libraries](#libraries)
    - [Dedicated FE and MIFE Libraries](#dedicated-fe-and-mife-libraries)
    - [Attribute-Based & Identity-Based Libraries](#attribute-based-abe--identity-based-ibe-libraries)
    - [Lightweight & IoT-Focused Libraries](#lightweight--iot-focused-libraries)
    - [Hardware-Assisted & Specialized Implementations](#hardware-assisted--specialized-implementations)
    - [General Cryptographic & Math Libraries](#general-cryptographic--math-libraries)
- [Foundational Papers for Implementations](#foundational-papers-for-implementations)
- [Related Awesome Lists](#related-awesome-lists)


## Libraries

Comprehensive collection of software implementations, libraries, and frameworks supporting Functional Encryption paradigms.

### Dedicated FE and MIFE Libraries

Libraries specifically designed to implement core Functional Encryption (FE), Multi-Input Functional Encryption (MIFE), and Decentralized Multi-Client Functional Encryption (DMCFE) schemes.

- [**dmcfe**](https://github.com/Cosmian/dmcfe) (`Rust` / `C`) - Implementation of Decentralized Multi-Client Functional Encryption (DMCFE) and Multi-Client Functional Encryption (MCFE) over the BLS12-381 elliptic curve.
- [**GoFE**](https://github.com/fentec-project/gofe) (`Go`) - Developed by the EU FENTEC project. Implements Inner-Product FE (IPFE) and Quadratic FE schemes.
  - [gofe-wasm] - WebAssembly bindings to execute GoFE functions in JavaScript/browser environments.
  - [abe-wrappers] - Language wrappers for integrating GoFE into other programming environments.
- [**CiFEr**](https://github.com/fentec-project/CiFEr) (`C`) - Developed by the FENTEC project. A C library for Inner-Product Functional Encryption schemes.
- [**PyMIFE**](https://github.com/MechFroG88/PyMIFE) (`Python`) - Python library dedicated to Multi-Input Functional Encryption (MIFE) prototyping and experimental evaluation.
- [**PyFE**](https://github.com/OpenMined/PyFE) (`Python`) - OpenMined library implementing Functional Encryption schemes in Python.
- [**FHIPE**](https://github.com/kevinlewi/fhipe) (`C` / `Python`) - Implementation of Function-Hiding Inner Product Encryption (FHIPE) by Kevin Lewi.

### Attribute-Based (ABE) & Identity-Based (IBE) Libraries

Libraries and software frameworks dedicated to implementing Attribute-Based Encryption (CP-ABE, KP-ABE) and Identity-Based Encryption (IBE) schemes.

- [**OpenABE**](https://github.com/zeutro/OpenABE) (`C` / `C++`) - Developed by Zeutro. A suite for Attribute-Based Encryption (CP-ABE, KP-ABE) and Identity-Based Encryption.
- [**Rabe**](https://github.com/Fraunhofer-AISEC/Rabe) (`Rust`) - Developed by Fraunhofer AISEC. A memory-safe Rust library for Attribute-Based Encryption.
- [**Charm-Crypto**](https://github.com/JHUISI/charm) (`Python`) - Developed by JHU Security and Crypto Lab. Framework for rapid prototyping of advanced cryptosystems including ABE, IBE, and commitment schemes.

### Lightweight & IoT-Focused Libraries

Software implementations specifically optimized to deploy Functional Encryption on resource-constrained devices, embedded systems, and ARM Cortex microcontrollers.

- **sumFE / sumFE v2** (`C` / `Embedded`) - Lightweight Functional Encryption implementation optimized for IoT and resource-constrained microcontrollers.

### Hardware-Assisted & Specialized Implementations

Frameworks leveraging specialized secure hardware enclaves to evaluate arbitrary functions over encrypted data.

- **Iron** (`C` / `C++`) - Functional Encryption using Intel SGX hardware enclaves to support arbitrary functions efficiently via isolated execution.

### General Cryptographic & Math Libraries

Underlying mathematical and pairing libraries that do not implement FE natively but are frequently used as the algebraic foundations for constructing FE, IBE, and ABE schemes.

- [**FLINT (Fast Library for Number Theory)**](https://flintlib.org/) (`C`) 
  - **Description:** Highly optimized C library for number theory, providing efficient algorithms for polynomial arithmetic, matrix operations, finite field arithmetic, and multiprecision integer computations.
- [**PBC (Pairing-Based Cryptography)**](https://crypto.stanford.edu/pbc/) (C)
  - **Description:** C library built on top of GMP that provides abstract mathematical operations for bilinear pairings over elliptic curves, forming the core algebraic primitive required for pairing-based FE, IBE, and ABE schemes.

## Foundational Papers for Implementations

Academic research papers and technical specifications that explicitly introduce, underpin, or evaluate the specific software libraries and implementations listed in this repository.

* **Decentralized Multi-Client Functional Encryption (DMCFE)** 
  - Chotard et al., *"Decentralized Multi-Client Functional Encryption for Inner Product"*, ASIACRYPT 2018\. [ePrint 2018/699](https://eprint.iacr.org/2018/699) — *Underlies the Cosmian DMCFE implementation.*
* **GoFE &amp; FENTEC Framework**
  - FENTEC Consortium, *"Functional ENcryption TEChnologies (FENTEC)"*, EU H2020 Project. [fentec.eu](https://fentec.eu/) — *Underlies GoFE and CiFEr.*
* **Intel SGX Hardware-Assisted FE (Iron)**
  - Fisch et al., *"Iron: Functional Encryption using Intel SGX"*, ACM CCS 2017\. [ACM DL](https://dl.acm.org/doi/10.1145/3133956.3134106) — *Underlies the Iron enclave framework.*
* **Lightweight FE for IoT (sumFE)**
  - Frimpong et al., *"Need for Speed: Leveraging the Power of Functional Encryption for Resource-Constrained Devices"*, IoTBD 2024\. — *Underlies the sumFE library.*
* **Inner-Product Functional Encryption Foundations**
  - Abdalla et al., *"Simple Functional Encryption Schemes for Inner Products"*, CRYPTO 2015\. [ePrint 2015/017](https://eprint.iacr.org/2015/017) — *Foundational paper for IPFE implemented across GoFE, CiFEr, and dmcfe.*
* **FE Libraries for Machine Learning &amp; Survey**
  - Panzade et al., *"Privacy-Preserving Machine Learning Using Functional Encryption: Opportunities and Challenges"*, IEEE Internet of Things Journal, 2023\. — *Analyzes performance and utility of FLINT, PBC, GoFE, and PyFE for PPML.*

## Related Awesome Lists

Curated repositories and community collections focusing on adjacent privacy-preserving cryptographic primitives and multi-party computation paradigms:

* [**awesome-mpc**](https://github.com/rdragos/awesome-mpc) \- Curated list of Multi-Party Computation (MPC) frameworks and libraries.
* [**awesome-zama**](https://github.com/zama-ai/awesome-zama) \- Resources and tools for Fully Homomorphic Encryption (FHE).
* [**awesome-cryptography**](https://github.com/sobolevn/awesome-cryptography) \- Comprehensive collection of cryptography tools, code, and resources.

## Acknowledgements

This list was developed as part of the [PATTERN](https://chistera-pattern.github.io/) research project.
