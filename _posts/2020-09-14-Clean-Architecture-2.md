---
layout: post
title: "Clean Architecture 2"
categories: develop
---

## SOLID

- SRP(Single Responsibility Principle)
- OCP(Open-Closed Principle)
- LSP(Liskov Substitution Principle)
- ISP(Interface Segregation Principle)
- DIP(Dependency Inversion Principle)

### SRP
> 하나의 `모듈`은 하나의, 오직 하나의 `액터`에 대해서만 책임져야 한다.

- 액터가 다르면 기능을 분리 해야 한다. 
- 기능 중복제거를 하거나, 병합하는 과정에서 원하지 않는 수정이 발생 할 수 있다. 
- SRP는 메서드와 클래스의 수준이다. (저수준의 메서드를 말하는게 아님)

### OCP
> 소프트웨어 `개체의 행위는 확장` 할 수 있어야 하지만, 이때 `산출물을 변경해서는 안 된다.` 

- SRP로 기능 분리, 분리한 기능을 컴포넌트의 계층구조로 조직화 한다. 
- 고수준과 저수준들의 레벨을 정리하고 저수준으로 부터 고수준을 보호한다. 
- 확장(변경)하기 쉽고, 변경사항의 범위를 최소화 한다.     
