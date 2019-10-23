---
layout: post
title: "Architecting on AWS 정리 1"
comments: true
description: "Quick review purpose"
keywords: "Cloud, AWS, Solutions Architect, Associate"
---

# AWS Basic Architecture

---
# Amazon S3
---

> S3는 Object level storage. 파일 한 개의 최대 용량 5TB, bucket 용량은 제한 없음.

+ 기본적으로 여러 시설과 각 시설의 여러 디바이스에 중복 저장됨. 웹 기반 AWS Management Console, API 및 SDK를 통한 프로그래밍 방식 또는 타사 솔루션(API/SDK를 사용)을 통해 액세스 할 수 있음.

+ Amazon S3의 event notification service를 이용하면, 사용자에게 특정 event 발생을 알려주거나 Lambda 스크립트와 같은 다른 프로세스를 trigger하는 데 사용할 수 있음.

+ Storage Class analyze를 이용하여 Storage access pattern을 파악하고 빈도가 낮은 데이터는 저렴한 비용의 서비스로 이전 가능.

## Amazon S3 use case 1

+ Static contents hosting
    + S3에 저장된 파일은 각 객체별로 unique HTTP URL에 연결되므로 S3에서 직접 전송할 수 있음.
    + 이를 응용하여 CloudFront의 origin으로 사용할 수도 있음.(Static Website Hosting)
    + 빠르게 성장하는 웹사이트에 효과적. 동영상 및 파일 즉각 제공.

+ Access Control
    + Amazon S3의 리소스는 default denied.
    + 리소스를 생성한 소유자만 액세스 권한을 부여 가능.

<a href="https://aws.amazon.com/blogs/aws/amazon-s3-block-public-access-another-layer-of-protection-for-your-accounts-and-buckets/">Amazon S3 Block Public Access – Another Layer of Protection for Your Accounts and Buckets</a>


## Amazon S3 use case 2

+ Static Website Hosting
    + Static HTML File, Image, 동영상, Client sied script service hosting 가능
    + High availability와 cost-effective를 동시에 만족 가능
    + Scalable!

+ S3 Versioning
    + Bucket option에서 활성화.
    + <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/Versioning.html">Versioning 참고</a>
    + MFA delete를 통해 실수 방지
    + SEC 17a-4, CTCC, FINRA 준수를 위한 <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lock.html">Object locking service</a> 제공

+ Cross Origin Resource Sharing
    + Amazon S3 resource에 대한 cross origin access 허용 가능
    + CORS 구성을 위해서는 특정 규칙을 포함하는 XML 문서를 생성함
        + bucket에 access하도록 허용할 origin
        + 각 origin에 대해 지원할 작업(HTTP method)
        + 작업별 정도 등
    + <a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html">CORS 참고</a>

## Amazon S3 use case 3

+ Data Store For Compute & Massive analysis 
    + Finantial trade data analysis
    + Click Stream analysis
    + media transcoding computing
+ horizontal Scale을 이용하여 동시 transaction 가능

## Amazon S3 use case 4

+ 내구성 및 확장성에 기반한 backup 및 archive tool로써 사용
+ Lifecycle policy를 적용하여 장기간 저장하는 데이터(자주 i/o가 생기지 않는)를 Glacier로 이전

## Amazon S3 Multipart Upload

## Amazon S3 Transfer Acceleration

## Amazon S3 Glacier

## Amazon S3 Storage Class

---
## Decision for AWS Region
---


