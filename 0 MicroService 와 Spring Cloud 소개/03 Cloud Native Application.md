Cloud Native Application
==========================

Cloud Native Application는, Cloud Native Architecture에 의해 설계되고 구현되는 애플리케이션을 의미한다.    
아키텍처의 특징을 가지고 다음과 같은 구현을 나타낸다.   

1. 마이크로 서비스 
2. CI/CD
3. DevOps
4. Containers  

# CI/CD 
## 지속적인 통합
* 하나의 애플리케이션을 여러 팀이나 여러 개발자들에 의해서 개발하고 있는 경우에    
  결과물을 통합하기 위한 형상관리, 통함된 코드를 빌드하고 테스트 하는 과정 자체를 의미함     
* Jenkins, Team CI, Travis CI 

## 지속적인 배포 
* Continuous Delivery   
* Continuous Deployment
* Pipe Line 

지속적인 전달과 배포      
깃과 같은 소스 저장소에 업로드된 코드를 가지고 와서       
패키지화된 형태 결과물을 실행 환경에 어떻게 배포하는지에 따라서 달라진다.   

패키지화된 작업을 수작업으로 진행 필요 -> Continuous Delivery     
운영자나 관리자 없이 완전 자동화 작업 -> Continuous Deployment      
      
배포하는 과정에서 무작정 기존 코드를 버리고 다시 배포하는 것은 아니다.     
가장 중요한 것은 시스템의 정상적인 운영이고, 시스템의 다운 타임을 최소화하는 것이다.    
