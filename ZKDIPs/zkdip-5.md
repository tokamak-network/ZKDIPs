---
zkdip: 5
title: circuit note input spec
author: Kevin Jeong (@inditow)
discussions-to: https://github.com/Onther-Tech/ZKDIPs/issues/4
status: Draft
type: Standards Track
category : Circuit
created: 2019-8-26
requires (*optional): 
replaces (*optional): 
---
## Simple Summary
Note Input spec definition

## Abstract
- note.owner : 256 byte
- note.value : 256 byte
- note.type : 128 byte
- note.viewKey : 256 byte
- note.salt : 128 byte

## Motivation
노트 인풋 스펙이 정리되지 않아서 업무에 혼란이 있음

## Specification
note.owner : 254 bit
note.value : 254 bit
note.type : 128 bit
note.viewKey : 254 bit
note.salt : 128 bit

## Rationale


## Backwards Compatibility


## Test Cases

## Implementation

https://github.com/Onther-Tech/zk-dex/blob/master/circuits/transferNote/transferNote.code#L5-L10
## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
