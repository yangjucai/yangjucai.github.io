---
layout: post
title: Cryptography
categories: [Cryptography]
description: It is the note of cryptography course by Dan Boneh.
keywords: cryptography
---
# Cryptography(By Dan Boneh)

# lecture1: introduction

### introduce to cryptography

![image-20230715213745833](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715213745833.png)

![image-20230715213919022](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715213919022.png) 

###### Secure multi-party computation:

![image-20230715215423902](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715215423902.png)

![image-20230715215452739](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715215452739.png)

###### Outsourcing computation:

![image-20230715215641415](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715215641415.png)

###### Zero knowledge:

![image-20230715215823862](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715215823862.png)

#### Three steps in cryptography:

![image-20230715220155064](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715220155064.png)

### history of symmetric cipher:

##### Symmetric ciphers:

![image-20230715220518758](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715220518758.png)

###### 1 Substitution cipher:

![image-20230715220649320](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715220649320.png)

e.g. Caesar Cipher:

![image-20230715220750313](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715220750313.png)

how to break:

![image-20230715221245373](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715221245373.png)

###### 2 Vigener cipher:

![image-20230715221422148](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715221422148.png)

how to break:

- know the key length:

  ![image-20230715221632397](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715221632397.png)

- not know the key length:

  assume key = 1,2,3, ..., n

###### 3 Rotor Machines:

![image-20230715221918488](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715221918488.png)

![image-20230715222059923](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715222059923.png)

###### 4 Data Encryption Standard:

![image-20230715222300215](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715222300215.png)

### Discrete Probability:

Probability distribution：

![image-20230715222840442](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715222840442.png)

Events：

![image-20230715223159848](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715223159848.png)

The union bound:

![image-20230715223415810](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715223415810.png)

Random Variables:

![image-20230715223752050](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715223752050.png)

The uniform random variable:

![image-20230715224021218](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715224021218.png)

Randomized algorithms:

![image-20230715224350155](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715224350155.png)

Independence:

![image-20230715224907694](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715224907694.png)

An important property of XOR:

![image-20230715225503721](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715225503721.png)

The birthday paradox:

![image-20230715225646181](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230715225646181.png)

$$1.2\times\sqrt {365} \approx 24$$

##### Cipher definition:

![image-20230716091441330](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716091441330.png)

![image-20230716091521495](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716091521495.png)

# Lecture2: Stream Ciphers

### 1 The One Time Pad:

![image-20230716091911880](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716091911880.png)

![image-20230716091947346](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716091947346.png)

###### Information Theoretic Security:(Shannon 1949) (Perfect secrecy)

![image-20230716092331448](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716092331448.png)

 ![image-20230716093338539](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716093338539.png)

#### Stream Ciphers:

![image-20230716095513738](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716095513738.png)

![image-20230716095624976](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716095624976.png)

###### PRG must be unpredicable:

![image-20230716100229954](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716100229954.png)

![image-20230716095950107](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716095950107.png)

![image-20230716100301456](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716100301456.png)

###### Negligible and Non-negligible:

![image-20230716100947608](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716100947608.png)

e.g. 

![image-20230716101101759](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716101101759.png)

##### Attack on OTP and stream cipher

###### Attack1: two time pad(used twice):

![image-20230716101525579](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716101525579.png)

![image-20230716104903038](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716104903038.png)

###### Attack2: no integrity(OTP is malleable)

![image-20230716105325937](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716105325937.png)

### 2 RC4:

![image-20230716105846040](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716105846040.png)

### 3 CSS:

![image-20230716110055696](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716110055696.png)

![image-20230716110843248](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716110843248.png)

### 4 eStream:

![image-20230716111045820](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716111045820.png)

![image-20230716111551127](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716111551127.png)

![image-20230716111657780](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716111657780.png)

### PRG Security Def.

![image-20230716112111343](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716112111343.png)

###### Statistical tests:

![image-20230716112409443](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716112409443.png)

![image-20230716112610963](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716112610963.png)

###### Advantage:

![image-20230716114202728](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716114202728.png)

e.g. 

![image-20230716114445225](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716114445225.png)

###### Secure PRGs: crypto def.

![image-20230716114730360](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716114730360.png)

unpredictable:

![image-20230716114936340](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716114936340.png)

![image-20230716115412254](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716115412254.png)

![image-20230716115551858](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716115551858.png)

###### Computationally indistinguishable:

![image-20230716120421893](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716120421893.png)

### Sematic security:

![image-20230716161033394](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716161033394.png)

![image-20230716161057781](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716161057781.png)

![image-20230716161106093](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716161106093.png)

e.g.

![image-20230716161423620](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716161423620.png)

e.g.

![image-20230716161839093](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716161839093.png)

##### Stream ciphers are semantically secure:

![image-20230716162148393](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716162148393.png)

![image-20230716162435001](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716162435001.png)

![image-20230716162520913](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716162520913.png)

![image-20230716162553370](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716162553370.png)

![image-20230716162752119](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716162752119.png)

![image-20230716163154132](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716163154132.png)

# Lecture3: Block ciphers

### introduction to block ciphers:

![image-20230716174719285](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716174719285.png)

![image-20230716174906587](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716174906587.png)

![image-20230716174935068](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716174935068.png)

### PRF：

![image-20230716175306246](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716175306246.png)

### PRP：

![image-20230716175323457](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716175323457.png)

![image-20230716175444591](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716175444591.png)

### Secure PRFs:

![image-20230716175739626](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716175739626.png)

![image-20230716175945475](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716175945475.png)

![image-20230717165043126](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717165043126.png)

### Secure PRP:

![image-20230717165151704](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717165151704.png)

### PRF => PRG

![image-20230716180411587](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230716180411587.png)

### DES(The data encryption standard)

![image-20230717143132359](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717143132359.png)

###### Feistel Network:

![image-20230717143350232](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717143350232.png)

![image-20230717143515519](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717143515519.png)

![image-20230717143644756](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717143644756.png)

![image-20230717143909063](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717143909063.png)

![image-20230717144109588](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717144109588.png)

![image-20230717144356474](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717144356474.png)

![image-20230717145012332](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717145012332.png)

#### Security of DES:

##### Exhaustive Search for block cipher key:

![image-20230717152335842](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717152335842.png)

![image-20230717152601976](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717152601976.png)

###### DES challenge:

![image-20230717152829674](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717152829674.png)

![image-20230717152906937](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717152906937.png)

###### Strengthening DES against ex. search:

![image-20230717153102728](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717153102728.png)

![image-20230717153954979](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717153954979.png)

##### More attack:

###### 1 side channel attacks:

![image-20230717160014176](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717160014176.png)

###### 2 Fault attack:

![image-20230717160157286](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717160157286.png)

(make sure correctness before output ciphertext)

###### 3 Linear and differential attacks:

![image-20230717160505913](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717160505913.png)

![image-20230717160749053](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717160749053.png)

###### 4 Quantum attacks:

![image-20230717161127798](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717161127798.png)

![image-20230717161302496](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717161302496.png)

### AES:

#### Substitution-Permutation network:

![image-20230717161702451](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717161702451.png)

![image-20230717161835492](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717161835492.png)

![image-20230717161948230](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717161948230.png)

![image-20230717162022119](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717162022119.png)

![image-20230717162128224](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717162128224.png)

![image-20230717162254290](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717162254290.png)

![image-20230717162648821](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717162648821.png)

##### Attacks to AES:

![image-20230717163236348](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717163236348.png)

### more block ciphers:

###### PRF from PRG:

![image-20230717163844204](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717163844204.png)

![image-20230717164340824](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717164340824.png)

###### PRP from PRF:

![image-20230717164455375](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717164455375.png)



# Lecture4: using block ciphers

### PRF Switching Lemma:

![image-20230717165722835](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717165722835.png)

## One-time key

### Incorrect use of a PRP:

![image-20230717170255550](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717170255550.png)

![image-20230717170337498](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717170337498.png)

![image-20230717170544297](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717170544297.png)

## Many-time key:

### Semantic Security for many-time key:

![image-20230717171142187](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717171142187.png)

![image-20230717171507446](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717171507446.png)

### Ciphers insecure under CPA:

![image-20230717171831246](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717171831246.png)

![image-20230717171937728](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717171937728.png)

#### solution1: randomized encryption:

![image-20230717172109605](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717172109605.png)

#### solution2: Nonce-based Encryption:

![image-20230717172513150](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717172513150.png)

![image-20230717172832267](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717172832267.png) 

![image-20230717173220817](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230717173220817.png)

### Modes of operation:

#### Cipher block chain(CBC):

![image-20230718093933366](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718093933366.png)

![image-20230718094023906](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718094023906.png)

![image-20230718094251883](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718094251883.png)

![image-20230718094743353](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718094743353.png)

##### CBC': nonce-based CBC

![image-20230718102911736](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718102911736.png)

##### CBC technicality: padding:

![image-20230718103324015](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718103324015.png)

#### Randize counter mode: 

![image-20230718105201872](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718105201872.png)



##### nonce ctr-mode:

![image-20230718105337591](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718105337591.png)

![image-20230718105447691](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718105447691.png)

![image-20230718105729838](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718105729838.png)

![image-20230718105856621](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718105856621.png)

# Lecture5: Message integrity:

### MACs(Message Authentication Code):

![image-20230718110427021](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718110427021.png)

#### Security:

![image-20230718110850459](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718110850459.png)

![image-20230718111428450](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718111428450.png)

#### Mac based on PRFs:

![image-20230718112647930](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718112647930.png)

##### Security:

![image-20230718112753515](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718112753515.png)

![image-20230718113052236](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718113052236.png)

![image-20230718130121407](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718130121407.png)

#### CBC-MAC(ECBC, CMAC):

![image-20230718130611268](C:\Users\11654\AppData\Roaming\Typora\typora-user-images\image-20230718130611268.png)

##### Security:

![image-20230718134609926](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718134609926.png)

#### NMAC(Nested MAC):

![image-20230718130825318](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718130825318.png)

##### Security:

![image-20230718135036035](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718135036035.png)

![image-20230718135747172](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718135747172.png)

#### MAC Padding:

##### CMAC(NIST standard):

![image-20230718142333577](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718142333577.png)

#### A parallel MAC(PMAC):

![image-20230718142705247](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718142705247.png)

##### Security:

![image-20230718142812488](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718142812488.png)

#### One-time MAC:

![image-20230718201211830](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718201211830.png)

#### Carter-Wegman MAC(Many-time MAC):

![image-20230718201420986](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718201420986.png)

#### HMAC:

##### Collision resistance:

![image-20230718202309847](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718202309847.png)

![image-20230718202519141](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718202519141.png)

![image-20230718202614774](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718202614774.png)

##### Attack for Collision resistance:

###### Generic attack:

![image-20230718203203466](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718203203466.png)

###### The birthday paradox:

![image-20230718203817600](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718203817600.png)

##### The Merkle-Damgard iterated construction:

![image-20230718204816154](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718204816154.png)

(if no space for PB, add another block)

###### collision resistance:

![image-20230718205706258](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718205706258.png)

###### compression function from a block cipher:

![image-20230718205957950](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718205957950.png)

![image-20230718210244959](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718210244959.png)

##### HMAC construction:

![image-20230718211149007](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718211149007.png)

![image-20230718211352315](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718211352315.png)

![image-20230718211317110](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718211317110.png)

![image-20230718211634388](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718211634388.png)

##### Timing attack on MAC verification:

![image-20230718211840001](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718211840001.png)

![image-20230718212100656](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718212100656.png)

![image-20230718212404269](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718212404269.png)

![image-20230718212605388](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230718212605388.png)

# Lecture6: Authenticated Encryption:

### Sample tampering attacks:

#### reading someone else's data:

![image-20230720095045279](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720095045279.png)

![image-20230720094945532](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720094945532.png)

#### attack using network access:

![image-20230720095413747](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720095413747.png)

## Definition of authenticated encryption:

#### goals:

![image-20230720101501948](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720101501948.png)

![image-20230720101543414](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720101543414.png)

#### ciphertext integrity:

![image-20230720101739215](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720101739215.png)

#### authenticated encryption:

![image-20230720101828314](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720101828314.png)

#### implication:

##### authenticity:

![image-20230720102407605](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720102407605.png)

##### against chosen ciphertext attack:

###### example of ciphertext attack:

![image-20230720102616439](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720102616439.png)

###### chosen ciphertext security:

![image-20230720102713053](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720102713053.png)

![image-20230720102924382](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720102924382.png)

![image-20230720102944475](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720102944475.png)

![image-20230720103148561](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720103148561.png)

###### authenticated encryption => CCA:

![image-20230720103250281](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720103250281.png)

![image-20230720103557865](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720103557865.png)

![image-20230720103645295](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720103645295.png)

 

### Construct from ciphers and MACs:

#### Combing MAC and ENC(CCA):

![image-20230720104533904](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720104533904.png)

![image-20230720104813544](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720104813544.png)

![image-20230720104936395](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720104936395.png)

##### Standards:

![image-20230720105347054](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720105347054.png)

#### OCB： direct construction from a PRP:

![image-20230720110531056](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720110531056.png)

##### Performance:

![image-20230720110738708](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720110738708.png)

### Case study:

#### TLS:

![image-20230720111114525](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720111114525.png)

![image-20230720111505766](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720111505766.png)

![image-20230720132645239](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720132645239.png)

##### Bugs in older versions:

![image-20230720133016246](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720133016246.png)

### Attacks:

#### Padding attack:

![image-20230720133935371](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720133935371.png)

![image-20230720134647239](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720134647239.png)

##### solution:

![image-20230720134730744](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720134730744.png)

#### Attacking non-atomic decryption:

![image-20230720135232130](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720135232130.png)

![image-20230720135524414](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720135524414.png)

![image-20230720135631321](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230720135631321.png)

# leture7: Odds and ends

## Key derivation:

### one key to many key:

#### source key is uniform:

![image-20230724131042899](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724131042899.png)

#### source key is not uniform:

![image-20230724131305064](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724131305064.png)

![image-20230724131634434](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724131634434.png)

e.g.,

![image-20230724131741404](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724131741404.png)

![image-20230724132207202](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724132207202.png)

## Deterministic encryption:

![image-20230724135334094](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724135334094.png)

![image-20230724135459771](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724135459771.png)

![image-20230724135714855](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724135714855.png)

![image-20230724135957096](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724135957096.png)

![image-20230724140057303](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724140057303.png)

![image-20230724140749425](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724140749425.png)

![image-20230724141143186](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724141143186.png)

### Constructions:

#### Synthetic IV (SIV):

![image-20230724141848881](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724141848881.png)

![image-20230724142046679](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724142046679.png)

![image-20230724142353162](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724142353162.png)

#### Just use PRP:

![image-20230724142929409](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724142929409.png)

![image-20230724143250259](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724143250259.png)

![image-20230724143343903](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724143343903.png)

![image-20230724143640911](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724143640911.png)

## Tweakable encryption:

![image-20230724154926402](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724154926402.png)

![image-20230724155239965](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724155239965.png)

![image-20230724155552119](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724155552119.png)

![image-20230724155750430](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724155750430.png)

#### trivial construction:

![image-20230724160107081](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724160107081.png)

#### XTS constraction:

![image-20230724160506332](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724160506332.png)

![image-20230724160810901](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724160810901.png)

## Format preserving encryption:

![image-20230724161344566](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724161344566.png)

![image-20230724161956191](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724161956191.png)

![image-20230724162222180](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724162222180.png)

![image-20230724162355627](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724162355627.png)



# lecture8: Key exchange

### Key management:

![image-20230724172109958](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724172109958.png)

![image-20230724172219176](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724172219176.png)

![image-20230724185810540](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724185810540.png)

### key exchange without online TTP:

#### Merkel puzzles:

![image-20230724190707815](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724190707815.png)

![image-20230724190951772](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724190951772.png)

![image-20230724191228909](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724191228909.png)

### Diffie-Helloman protocol:

![image-20230724192101766](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724192101766.png)

![image-20230724192222079](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724192222079.png)

![image-20230724193112602](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724193112602.png)

![image-20230724194003029](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724194003029.png)

### Public-key encryption:

![image-20230724201732674](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724201732674.png)

![image-20230724201842893](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724201842893.png)

![image-20230724202059706](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724202059706.png)

![image-20230724202637122](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724202637122.png)



# Lecture9: Number Theory:

### Notation:

![image-20230724203233733](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724203233733.png)

![image-20230724204630831](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724204630831.png)

![image-20230724205734251](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724205734251.png)

![image-20230724210138582](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724210138582.png)



### GCD:

![image-20230724203638532](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724203638532.png)

### Modular inversion:

![image-20230724203830174](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724203830174.png)

 

![image-20230724204138382](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724204138382.png)

###   Fermat's theorem:

![image-20230724205123101](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724205123101.png)

![image-20230724205430722](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724205430722.png)

### Euler's generalization of Fermat:

![image-20230724210636366](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724210636366.png)

### Modular e'th roots:

![image-20230724210758641](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724210758641.png)

![image-20230724210928622](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724210928622.png)

![image-20230724211413158](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724211413158.png)

### Quadratic residue:

![image-20230724211714010](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724211714010.png)

![image-20230724212031798](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724212031798.png)

![image-20230724212426557](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724212426557.png)

![image-20230724212518435](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724212518435.png)

![image-20230724212811803](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724212811803.png)

### Representing bignums:

![image-20230724212946662](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724212946662.png)

#### Arithmetic:

![image-20230724213310288](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724213310288.png)

#### Exponentiation:

![image-20230724213657075](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724213657075.png)

![image-20230724214214566](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230724214214566.png)

### Intractable problems:

#### discrete logarithm:

![image-20230725100238606](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725100238606.png)

![image-20230725100658833](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725100658833.png)

![image-20230725101358880](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725101358880.png)

![image-20230725101708324](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725101708324.png)

# Lecture10: Public Key Encryption（RSA-based）

![image-20230725102421072](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725102421072.png)

![image-20230725102544285](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725102544285.png)

![image-20230725103335255](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725103335255.png)

![image-20230725103553658](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725103553658.png)

![image-20230725103825201](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725103825201.png)

## Construction:

### Trapdoor functions(TDF):

![image-20230725104144323](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725104144323.png)

![image-20230725104402369](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725104402369.png)

### public-key encryption from TDFs

![image-20230725104736463](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725104736463.png)

#### Incorrect use:

![image-20230725105117146](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725105117146.png)

### RSA trapdoor function:

![image-20230725111223544](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725111223544.png)

#### RSA assumption:

![image-20230725111518502](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725111518502.png)

#### RSA public-key encryption:

![image-20230725111836564](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725111836564.png)

#### Textbook RSA is insecure:

![image-20230725111955734](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725111955734.png)

![image-20230725143147858](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725143147858.png)

#### PKCS1:

![image-20230725143801270](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725143801270.png)

![image-20230725144228780](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725144228780.png)

![image-20230725145250508](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725145250508.png)

![image-20230725145825485](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725145825485.png)

![image-20230725150219449](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725150219449.png)

#### Is RSA a one-way permutation?

![image-20230725151256826](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725151256826.png)

![image-20230725151632075](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725151632075.png)

![image-20230725152535566](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725152535566.png)

#### RSA in practice:

![image-20230725153747968](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725153747968.png)

![image-20230725154018091](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725154018091.png)

![image-20230725154515090](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725154515090.png)



# Lecture11: Public Key Encryption（Diffie-Hellman-based）

![image-20230725194259532](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725194259532.png)

## ElGamal:

 ![image-20230725194921121](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725194921121.png)

![image-20230725195059372](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725195059372.png)

 

![image-20230725195401182](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725195401182.png)

### Security:

![image-20230725195850125](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725195850125.png)

![image-20230725200134703](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725200134703.png)

![image-20230725200811804](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725200811804.png)

![image-20230725201032565](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725201032565.png)

![image-20230725201119749](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725201119749.png)

## Variants of ElGamal:

![image-20230725201500525](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725201500525.png)

### Twin ElGamal:

  ![image-20230725201806948](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725201806948.png)

## A Unifying Theme:

### One-way function:

![image-20230725202704511](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725202704511.png)

![image-20230725203158877](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725203158877.png)

![image-20230725203344325](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725203344325.png)

![image-20230725203536945](https://cdn.jsdelivr.net/gh/yangjucai/picgo@main/image-20230725203536945.png)