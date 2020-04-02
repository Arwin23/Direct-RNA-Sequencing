# **ONT-RNA-Sequencing**

### Workflow

#### 1. RNA Extraction
  - Qiagen
  - LifeS
#### 2. Barcoding 
  - Barcoding the cDNA - [CDC Protocol](https://github.com/helix-phoenix/SARS-CoV-2_Sequencing/blob/master/protocols/CDC-Comprehensive/CDC_SARS-CoV-2_Sequencing_200325-2.pdf)
  - Barcoding the RNA (is this possible?)
#### 3. Adaptor Ligation
#### 4. Sequencing
#### 5. Bioinformatics
  
 
  








--------------------------------------










### References

The following ONT sequencing protocols, checklists and job-aids are primarily designed for the Oxford Nanopore [MinION](https://nanoporetech.com/products/minion), and have been kindly shared by research groups throughout the world (please see individual protocols for attribution and citing purposes). Even so, most of these protocols should scale to larger ONT instruments without significant modifications.

#### a) CDC NCIRD/DVD ONT Sequencing Protocol
This protocol was developed, tuned and validated by the Viral Discovery laboratory at CDC/NCIRD, where it was used to generate the first 16 SARS-CoV-2 genome sequences from the United States. In practice, it has been used for situations with a relatively low or predictable volume of samples, and is often used in conjunction with Sanger-based tiling to resolve any potential sequencing or assembly issues.
- [Singleplex and Multiplex Protocols for ONT/Illumina](./protocols/CDC-Comprehensive)

#### b) [ARTIC Network nCoV-2019 Sequencing Protocol](https://artic.network/ncov-2019)
This protocol was developed and released by the fine folks at [ARTIC Network](https://artic.network), and was subsequently refined based on comments from [Itokawa et al](https://www.biorxiv.org/content/10.1101/2020.03.10.985150v1.full.pdf), which identified potential issues and proposed an alternate L18 primer.

- [Sequencing protocol](https://www.protocols.io/view/ncov-2019-sequencing-protocol-bbmuik6w) / [Single sample sequencing protocol](https://www.protocols.io/view/ncov-2019-sequencing-protocol-single-sample-bdbfi2jn)

- [Stepwise simplified protocol from ONT*](./protocols/ONT-COVID-19_Tiling)

- Primer schemes: [V1](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V1) / [V2](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V2) [(ref)](https://www.biorxiv.org/content/10.1101/2020.03.10.985150v1.full.pdf) / [V3](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019/V3)

- [ARTIC on Illumina - Complete Walk-through - Grubaugh/Andersen/Loman labs](https://docs.google.com/document/d/1PilT4w5jHO-ROsE8TL5WBGa0wSCdTHAsNl1LIOYiTgk/mobilebasic)

- Integrated bioinformatics (RAMPART) - documentation below under bioinformatics methods.

#### c) Doherty Institute VIDRL Sequencing Protocols
The Victorian Infectious Diseases Reference Laboratory ([VIDRL](https://www.vidrl.org.au/)) at the [Peter Doherty Institute for Infection and Immunity](https://www.doherty.edu.au/) released two protocols for the ONT MinION, which they successfully used to sequence early Australian SARS-CoV-2 samples.
- [Native RNA Sequencing Protocol](./protocols/ONT-Native_RNA) [(ref)](https://www.biorxiv.org/content/10.1101/2020.03.05.976167v1.full.pdf)

- [SISPA Sequencing Protocol](./protocols/ONT-SISPA)





