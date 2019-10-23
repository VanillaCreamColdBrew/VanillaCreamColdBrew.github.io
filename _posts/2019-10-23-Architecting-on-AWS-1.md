---
layout: post
title: "Architecting on AWS 정리 1"
comments: true
description: "Quick review purpose"
keywords: "Cloud, AWS, Solutions Architect, Associate"
---

# AWS Global Infrastructures

## What is Cloud?

> Cloud Computing
Computing resource를 대여해서 사용하는 것.
Internet에 연결되어 있다면 언제든지 사용가능.
'Pay as you go'기 때문에 전략을 바꿀때 민첩성에 힘을 실어줌.

### 6 benefits from cloud computing

1. CapEX --> VarEX
2. 규모의 경제
3. 용량 추정 불필요
4. Agility & Fast
5. 중요한 문제(Business)에 집중
6. Go global in minuites

## AWS Well-Architected Framework

> _AWS의 설계 원칙 목표_ 는 보안, 안정성, 비용 최적화, 성능 효율성 그리고 운영 우수성으로 나뉜다.

+ **보안**

    정보를 보호하고 손해를 최소화하는 목표.
    Architecture level에서 자격 증명 기반, traceability activation, 모든 layer에 security rule 적용, security best practice 자동화, 전송 및 저장 시 데이터 암호화 등의 basic security guide line 적용. 이를 통해 보안 강화.

+ **안정성**

    기존 환경에서는 안정성을 보장하기가 어려움. 단일 장애 지점, 자동화 미비, 탄력성 부족에서 문제가 발생합니다. 안정성 핵심 요소의 아이디어를 적용하면 이러한 문제를 다수 방지할 수 있습니다. HA Architecture, fault tolerance and overall duplication 을 통해서 안정성 취할 수 있음

+ **Cost Optimization**

    Production의 수명 내내 정교화되고 개선되어야 함. 현재 Architecture를 지속적으로 관리하고 더욱 최적화하는 것은 중요.

+ **Operation Outstanding**

    Deploy - Update - Operating Chain을 활성화. AWS 상의 모든 workload는 code화 가능. 거버넌스를 어떻게 가져가는지에 따라 효율성 극대화 가능.

+ **Performance Efficiency**

    효율적인 리소스를 선택하고 수요 변화에 따라 효율성을 유지가능. Market Place의 vendor가 제공하는 solution을 빠르게 적용해볼 수 있다. 복잡성과 지식은 전문가에게 넘기고 비즈니스에 집중할 수 있음.
===
# AWS's Global Infrastructure intro.

### AWS Data Center

 > All Data Center of AWS is connected online. 전 세계 여러 region에 cluster 형태로 구축됨. 

### AWS Availablility Zone

> 각 AZ는 하나 이상의 DC로 구성. 일부 AZ는 최대 6개의 DC로 구성되기도 함. AZ에 DC가 포함되는 관계.

### AWS Region

> 하나의 Region은 두 개 이상의 AZ로 이루어짐. AWS Region은 여러 ISP, 그리고 public internet에 비해 비용이 더 저렴하고, inter-region network latency가 일관적인 Private Global Backbone network에 연결됨.

### AWS Edge Location

> Point of Presence(PoP)를 Global하게 서비스하고 있음. Route 53, CloudFront 서비스에 주로 사용. 

