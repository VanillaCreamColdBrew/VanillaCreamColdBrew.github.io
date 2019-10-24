---
layout: post
title: "Architecting on AWS 정리 3"
comments: true
description: "Quick review purpose"
keywords: "Cloud, AWS, Solutions Architect, Associate"
---

# AWS EC2(Elastic Compute Cloud)

* * *

## 1. EC2's Features

* * *

-   Web Hosting
-   Database
-   Authentication
-   A to Z from using Server computer

* * *

### + Virtual Machine과 Physical Server

* * *

-   Virtual Machine을 on-demand 방식으로 이용가능.
-   Physical Server를 구매하지 않아도 Workload 테스트가 가능.
-   비용상 이점(짧은 이용시간 고려)

* * *

## 2. Amazon Machine Image(AMI)

* * *

-   AMI는 Cloud의 Virtual Machine인 Instance를 시작하는 데 필요한 정보를 제공.
-   Instance 시작 시, source AMI 지정
-   AMI에 저장되는 정보
    -   Root volume용 template. Root volume은 일반적으로 OS 및 해당 OS에 설치된 모든 구성 요소를 포함.
    -   AMI를 사용하여 Instance를 시작할 수 있는 AWS 계정 제어 시작 권한
    -   Block device mapping
-   AMI 얻는 source
-   Amazon 제공
-   Marketplace's Catalog
-   자체 생성(Donut Machine or Golden Instance)
-   Community AMI(기엄/production 환경 사용 권장 X)

* * *

-   AMI's Features
    -   반복성 : 동일한 AMI에서 시작된 Instance는 서로 똑같은 복제본이기 때문에 클러스터 구축이나 컴퓨팅 환경 재생성이 훨씬 쉽다.
    -   재사용성 : AMI는 EC2 Instance의 전체 구성 및 Contents를 packaging하므로 효율적이고 정확하게 Instance를 계속 다시 사용할 수 있음.
    -   복구성 : AMI는 장애가 발생한 시스템을 동일한 AMI에서 생성된 새 Instance로 교체하는 데 이상적입니다.
    -   AWS Marketplace Solution : 특정 Vendor의 solution은 marketplace의 AMI에 제공되고 있을 수 있다.
    -   Backup : AMI는 전체 EC2 Instance 구성을 Backup하는 방법을 제공하여, 장애 발생 시 대체 Instance를 시작하는 데 사용할 수 있다.

* * *

> Userdata를 이용하여 EC2 Instance 시작

-   EC2 인스턴스를 생성할 때, user data를 Instance에 전달할 수 있는 옵션이 있는데, 이를 이욯하여 instance 시작 완료를 자동화 할 수 있습니다. Shell script나 Cloud-init 명령으로 구현 가능.
-   Instance Metadata Retrieving
    -   <http://169.254.169.254/latest/meta-data>
    -   상단의 URI를 통해서 ami-id, ami-launch-index, hostname등 상세한 metadata를 얻을 수 있다.

* * *
