---
layout: post
title: Introduction to Zero-Knowledge
categories: [ZK]
description: It is the note of 1st lecture of the zk-learning course.
keywords: Zero-Knowledge
---

# Lecture 1. Introduction and History of ZKP

video: https://www.youtube.com/watch?v=uchjTIlPzFo

## NP-Language:

**Definition**:  $$\mathcal{L}$$ is an NP-language (or NP-decision problem) if there is a $$poly(|x|)$$ time verifier $$V$$where:

- Completeness: true claims have short proofs, s.t. if $$x\in \mathcal{L}$$ then there is a $$poly(|x|)$$ size witness $$w \in \{0,1\}^*$$ such that $$V(x,w) = 1$$.
- Soundness: false theorems have no proofs, s.t. if $$x \notin \mathcal{L}$$ then there is no witness, so $$\forall w \in \{0,1\}^*$$, we have $$V(x,w) = 0.$$

## [critical thinking]

Is there any  one-prover-many-verifiers or many-provers-one-verifier or many-provers-many-verifiers?





## Proof System

video: https://www.youtube.com/watch?v=6uGimDYZPMw

![image-20230601203511202](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601203511202.png)

## NP Proof System:

![image-20230601203801640](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601203801640.png)

example 1: Boolean Satisfiability:

![image-20230601204505823](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601204505823.png)

 example 2: Linear Equations:

![image-20230601204646512](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601204646512.png)

## The class P (ploynomial)

![image-20230601204908634](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601204908634.png)

example3 : Quadratic Residuosity:

![image-20230601205058262](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601205058262.png)

## Interactive Proof:

  ![image-20230601205747401](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601205747401.png)

![image-20230601210029320](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601210029320.png)

the power of IP:

![image-20230601210349697](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601210349697.png)

## Zero-Knowledge Proof

### Definition of "no knowledge leaked"

![image-20230601210801401](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601210801401.png)

## Definition of "Honest Verifier Zero-Knowledge"

![image-20230601211312870](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601211312870.png)

a zero-knowledge proof for QR_N:

![image-20230601212108673](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601212108673.png)

### Definition of "Perfect Zero-knowledge"

video : https://www.youtube.com/watch?v=cQ-BI1WWzjU

![image-20230601212732851](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601212732851.png)

### Definition of "Statistical Zero-knowledge"

![image-20230601214218535](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601214218535.png)

### Definition of "Computational Zero-knowledge"

![image-20230601214152295](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601214152295.png)

## Commitment Scheme

statistically-binding:

![image-20230601214739334](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230601214739334.png)



## Zero-Knowledge Proofs of Knowledge

##### Yehuada Lindell 

##### Bar-llan University

video: https://www.youtube.com/watch?v=RvGsjnoYRRg



# Lecture 2. Overview of Modern SNARK Constructions 

video: https://www.youtube.com/watch?v=bGEXYpt3sj0

##### SNARK:

succint: "short" and "fast"

##### zk-SNARK:

succint and reveal nothing

## What is SNARK:

### arithmetic circuit:

![image-20230605210044017](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605210044017.png)

![image-20230605210406437](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605210406437.png)

### NARK:

![image-20230605220013501](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605220013501.png)

### SNARK:

![image-20230605220410180](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605220410180.png)

![image-20230605220448420](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605220448420.png)

## Types of Preprocessing Setup

![image-20230605221016341](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605221016341.png)

better from top to bottom

## Significant Progress

## ![image-20230605221325636](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230605221325636.png)

(for a circuit with about $$2^{20}$$gates) (prover time is almost linear $$|C|$$)

## Building an efficient SNARK

## Paradigm:

![image-20230606092939832](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606092939832.png)

### functional commitment:

![image-20230606090950534](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606090950534.png)

e.g. 

![image-20230606091304961](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606091304961.png)

## Fiat-Shamir Transform

![image-20230606092745398](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606092745398.png)

## Functional-IOP:

![image-20230606093131440](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606093131440.png)

![image-20230606093409219](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606093409219.png)

## SNARK in Practive

![image-20230606094953374](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606094953374.png)



# Lecture 3. Programming ZKPs

## paradigm:

![image-20230606133524855](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606133524855.png)

![image-20230606135559688](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606135559688.png)

e.g.

![image-20230606135534776](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606135534776.png)

## ZKP programmability:

### Arithmetic Circuits:

![image-20230606134336718](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606134336718.png)

![image-20230606134408412](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606134408412.png)

# R1CS

![image-20230606134948481](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606134948481.png)

![image-20230606135035624](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606135035624.png)

### write an AC as R1CS:

![image-20230606135232376](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606135232376.png)

## 1. HDL： Hardware Description Language

 ![image-20230606141957517](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606141957517.png)

e.g. 

![image-20230606142230491](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606142230491.png)

### Circom：

#### base language:

![image-20230606142620937](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606142620937.png)

![image-20230606142855928](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606142855928.png)

![image-20230606143221593](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606143221593.png)

## 2. A Library for R1CS:

![image-20230606143641594](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606143641594.png)

![image-20230606144014486](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144014486.png)

![image-20230606144221335](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144221335.png)

![image-20230606144443799](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144443799.png)

![image-20230606144523557](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144523557.png)

#### witness computation:

![image-20230606144621007](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144621007.png)

## 3. High Programming Language:

### Zokrages:

![image-20230606144816618](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144816618.png)

![image-20230606144934840](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606144934840.png)

#### witness computation:

![image-20230606145029313](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145029313.png)

## ZKP Toolchain

### Toolchain types:

![image-20230606145143975](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145143975.png)

![image-20230606145230232](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145230232.png)

![image-20230606145519998](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145519998.png)

![image-20230606145622257](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145622257.png)

![image-20230606145710861](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606145710861.png)



# Lecture 4. Interactive Proof.

![image-20230709161645521](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709161645521.png)

## Definition of IP

![image-20230606195839064](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606195839064.png)

### soundness vs knowledge soundness:

![image-20230606201530608](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230606201530608.png)

## IP Design



## The sum-check protocol

![image-20230607103604365](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230607103604365.png)

![image-20230607103703655](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230607103703655.png)

### An application: Counting Triangles:

![image-20230607105826354](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230607105826354.png)

## Polynomial IOP:

![image-20230607111212348](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230607111212348.png)

rewinding technique to proof knowledge soundness



# Lecture 5：Plonk SNARK

video: https://www.youtube.com/watch?v=A0oZVEXav24

![image-20230709161628117](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709161628117.png)



![image-20230624213044395](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230624213044395.png)

![image-20230709160640303](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709160640303.png)

![image-20230709160918118](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709160918118.png)



# Lecture6: Polynomial Commitments based on Pairing and Discrete Logarithm

video: https://www.youtube.com/watch?v=WyT5KkKBJUw

![image-20230709161758921](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709161758921.png)

![image-20230709161951015](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709161951015.png)

### Background

#### Group:

![image-20230709162211521](C:\Users\11654\AppData\Roaming\Typora\typora-user-images\image-20230709162211521.png)

#### Discrete logarithm:

![image-20230709162746407](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709162746407.png)

#### Diffie-Hellman assumption:

![image-20230709163102990](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709163102990.png)

#### Bilinear pairing:

![image-20230709163408154](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709163408154.png)

#### BLS signature:

![image-20230709163603781](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709163603781.png)

### KZG polynomial commitment

![image-20230709164026574](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709164026574.png)

![image-20230709164226804](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709164226804.png)

![image-20230709164403455](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709164403455.png)

![image-20230709164532035](C:\Users\11654\AppData\Roaming\Typora\typora-user-images\image-20230709164532035.png)

![image-20230709164721971](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709164721971.png)

![image-20230709164814936](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709164814936.png)

#### Soundness of KZG:

![image-20230709165027654](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709165027654.png)

![image-20230709165647154](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709165647154.png)

#### Knowledge soundness and KoE assumption:

![image-20230709170317840](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709170317840.png)

![image-20230709170705016](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709170705016.png)

#### Generic Group model(GGM)

![image-20230709170828888](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709170828888.png)

#### Properties of KZG

![image-20230709174118835](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709174118835.png)

#### Ceremony:

![image-20230709174346055](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709174346055.png)

#### Variants of KZG:

##### Multivariate poly-commit:

![image-20230709174944643](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709174944643.png)

##### Achieving zero-knowledge:

![image-20230709175337683](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230709175337683.png)

##### Batch opening: single polynomial:

![image-20230710165135417](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710165135417.png)

![image-20230710165332581](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710165332581.png)



### Bulletproofs and other scheme based on discrete-logarithm

#### Bullteproofs with transparent setup:

![image-20230710165940401](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710165940401.png)

![image-20230710170249249](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710170249249.png)

![image-20230710172001536](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710172001536.png)

![image-20230710172658127](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710172658127.png)

![image-20230710173048186](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710173048186.png)

![image-20230710173320247](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710173320247.png)

##### Other polynomial commitment:

###### Hyrax:

![image-20230710200314305](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200314305.png)

###### Dory:

![image-20230710200545826](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200545826.png)

###### Dark:

![image-20230710200635205](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200635205.png)

![image-20230710200648916](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200648916.png)



# Lecture7: Polynomial Commitments based on Error-correcting Codes

![image-20230710200849074](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200849074.png)

![image-20230710200951305](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710200951305.png)

## Background on error-correcting codes

### Error-correcting code

![image-20230710201503545](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710201503545.png)

![image-20230710201857466](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710201857466.png)

![image-20230710203129043](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710203129043.png)

### Linear code

![image-20230710203252119](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710203252119.png)

![image-20230710203934310](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710203934310.png)



## Polynomial Commitments based on Error-correcting Codes

![image-20230710204210788](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710204210788.png)

![image-20230710204345017](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710204345017.png)

![image-20230710204459464](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710204459464.png)

![image-20230710204609504](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710204609504.png)

![image-20230710211825328](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710211825328.png)

![image-20230710211857486](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710211857486.png)

![image-20230710212054791](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230710212054791.png)

![image-20230711101009700](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711101009700.png)

![image-20230711101308649](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711101308649.png)

![image-20230711101659308](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711101659308.png)

![image-20230711101829056](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711101829056.png)

![image-20230711101911919](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711101911919.png)

![image-20230711102704996](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711102704996.png)

![image-20230711102831829](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711102831829.png)

![image-20230711102911584](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711102911584.png)

![image-20230711103225774](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711103225774.png)

![image-20230711103647966](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711103647966.png)

![image-20230711104021772](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711104021772.png)



## Linear-time encodable code based on expanders

![image-20230711104442022](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711104442022.png)

![image-20230711105125991](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711105125991.png)

![image-20230711141150694](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711141150694.png)

![image-20230711141612937](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711141612937.png)

![image-20230711141824288](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711141824288.png)

![image-20230711141908172](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711141908172.png)

![image-20230711142039444](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711142039444.png)

![image-20230711142656245](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711142656245.png)



![image-20230711143111656](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711143111656.png)

![image-20230711143254755](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230711143254755.png)



# Lecture8: FRI-based Polynomial Commitments and Fiat-Shamir

![image-20230712171952736](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712171952736.png)

## The zoo for Polynomial IOPs and Polynomial commitment

![image-20230712202657268](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712202657268.png)

![image-20230712202622755](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712202622755.png)

## Some specimens from the zoo

![image-20230712203027090](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712203027090.png)

![image-20230712203042111](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712203042111.png)

![image-20230712203557729](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712203557729.png)

![image-20230712203729811](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712203729811.png)

![image-20230712203902059](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712203902059.png)

## FRI(Univariate) Polynomial Commitments

![image-20230712204313292](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712204313292.png)

![image-20230712204506760](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712204506760.png)

### Fix first problem:

![image-20230712204621422](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712204621422.png)

![image-20230712204637298](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712204637298.png)

![image-20230712204801866](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712204801866.png) 

![image-20230712205253456](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712205253456.png)

![image-20230712205308843](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712205308843.png)

![image-20230712210009440](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712210009440.png)

![image-20230712210220985](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712210220985.png)

![image-20230712210309780](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712210309780.png)

### Fix second problem:

![image-20230712210425141](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230712210425141.png)