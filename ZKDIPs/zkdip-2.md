---
zkdip: 2
title: zk address
author: Kevin Jeong (@ggs134 )
discussions-to: https://github.com/Onther-Tech/ZKDIPs/issues/2
status: Accepted
type: Standards Track
category : Protocol
created: 2019-8-24
requires (*optional): 
replaces (*optional): 
---

## Simple Summary
<!--"If you can't explain it simply, you don't understand it well enough." Provide a simplified and layman-accessible explanation of the EIP.-->
- zk address format = "zk"+base58(sha256(pubkey.x+pubkey.y)[12:])
- A zk-address is an identifier of 42 or 64  characters long that represents a possible destination for a zk-note asset payment.

## Abstract
[Slide](https://docs.google.com/presentation/d/18lSXlUvGRS7OjCsCM3ZTFUJ9-YYwVEq5ck72sqt6YFs/edit?usp=sharing)

## Motivation
In zk-dex, single ethereum account can have many zk-dex accounts (note.owner). But, zk-dex should use different account type from ethereum, because it's limitation of variables in jubjub algorithm. 

## Specification

### derivation
- ```zk Address format  = "zk"+base58encode(sha256(hex(pubkey.x) + hex(pubkey.y))[12:])```
- ```Note Address(Note Hash) = sha256( circuit-input-format + value + type + viewKey + salt)```

```+``` means appending string
ex) "1abd" + "bda" = "1abdbda"

### other format
- pubkey(point x, y) : {x : field value, y: field value} 
- pubkey hexstring : hex(x) + hex(y)
- digested pubkey : sha256(pubkey hexstring)
- zk address : digested pubkey[12:] (20 byte)
- zk address format : "zk"+base58encode(zk address)

### public key cryptography algorithm (sk -> pk)
- JubJub : https://github.com/Onther-Tech/Babyjubjub-keygen

### examples

- sk(Integer) : ``` "137215550892293264522532280805192033568" ```
- pubkey(point x, y) : 
```
{
  x : "3221685307190689865347586017200458153912689357176235248982582720407412477386", 
  y : "5146970447429328755369555831351493575582722874440366554208606834938898586669"
}
```
- pubkey hexstring : 
```
"71f68c591f2badb615a1e28bcc8e8afc04cad56989be57b4e0ec30ad6c90dcab61150068fd22e9fd7934e1aecc490c53c945a116967ae411d42d929fd89c2d"
```
- zk address : ``` "70f1d6ef6a6db055aa4aaad57f0a46e692c58935" ```
- base58encoded zk address : ``` "2aGHYonwumtLAG7SNKjharksCP3r" ```
- zk address format : ``` "zk2aGHYonwumtLAG7SNKjharksCP3r" ```

## Rationale

## Backwards Compatibility
It is not backward competible.

## Test Cases
<!--Test cases for an implementation are mandatory for EIPs that are affecting consensus changes. Other EIPs can choose to include links to test cases if applicable.-->

## Implementation
zkdex-utils : https://github.com/Onther-Tech/zkdex-utils

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
