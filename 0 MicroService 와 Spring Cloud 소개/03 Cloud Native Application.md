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
  
변경된 시스템을 무조건 반영하기보다는 기존 시스템을 같이 운영하면서      
사용자들에게 발생할 수 있는 이질감이라든가 문제점들을 최소화 하는 것을 의미한다.    

**카나리 배포와 블루 그린배포**    
* 카나리 배포 
    * 95% 이전 버전   
    * 5% 새 버전      
* 블루 그린 배포 
    * 이전 버전에서 새버전으로 전환 

# DevOps
> Development + Operations  
 
개발 조직과 운영 조직의 통합을 의미한다.         
이러한 통합으로 고객의 요구사항을 빠르게 반영하고 만족도 높은 결과물을 제시하는 것에 목적        
    
기존의 엔터프라이즈 애플리케이션은 고객의 요구사항에 맞게 도메인을 분석하고        
시스템을 설계, 애플리케이션 구현과 테스트 마지막으로 배포 과정을 거쳐 시스템 개발을 완료한다.    
개발 기간이 긴데, 개발 기간이 길어진다는 것은 변경사항이나 요구사항에 대처하기 어렵다는 문제가 발생할 수 있다.     

![Devops-strategy-devops-toolchain](https://user-images.githubusercontent.com/50267433/137627757-4e7095b3-2c39-4570-885e-f0e94decfb8a.png)

devops를 잘 설정하여 위와 같은 방식들을 지속적으로 진행하고 관리하면서      
보다 유연한 시스템 개발 프로세스를 가져가는 것이 목적이다.     

# Container 가상화  

컨테이너 가상화 기술은 기존의 하드웨어 가상화, 서버 가상화 기술에 비해 적은 리소스를 사용하여  가상화 서비스 구축 가능   

![가상화의_발전_과정](https://user-images.githubusercontent.com/50267433/137627852-dbf74a82-7304-40d6-a51f-4c77261c4e04.png)



1. **전통적인 배포 시대**   
초기 조직은 애플리케이션을 물리 서버에서 실행     
한 물리 서버에서 여러 애플리케이션의 리소스 한계를 정의할 방법이 없었기에, 리소스 할당의 문제 발생    
물리 서버 하나에서 여러 애플리케이션을 실행하면, 리소스를 과다 사용하는 인스턴스가 다른 애플리케이션의 성능 저하 유발   
서로 다른 여러 물리 서버에서 각 애플리케이션을 실행하는 것은 리소스가 충분히 활용되지 않으며, 유지 비용 과다    
   
2. **가상화된 배포 시대**       
단일 물리 서버의 CPU에서 여러 가상 시스템 (VM)을 실행        
VM간에 애플리케이션을 격리하고 애플리케이션의 정보를      
다른 애플리케이션에서 자유롭게 액세스 할 수 없으므로, 일정 수준의 보안성을 제공  
리소스를 보다 효율적으로 활용할 수 있으며,     
쉽게 애플리케이션을 추가하거나 업데이트할 수 있고 하드웨어 비용을 절감할 수 있어 더 나은 확장성 제공    
가상화를 통해 일련의 물리 리소스를 폐기 가능한(disposable) 가상 머신으로 구성된 클러스터로 구성 가능   
각 가상 머신은 가상화된 하드웨어 상에서 자체 운영체제를 포함한 모든 구성 요소를 실행하는 하나의 완전한 머신   
     
3. **컨테이너 개발 시대**        
컨테이너는 VM과 유사하지만 격리 속성을 완화하여 애플리케이션 간에 운영체제(OS)를 공유하므로 각각의 컨테이너는 보다 가벼움    

컨테이너 가상화 기술은 운영 체제 위에 컨테이너 가상화를 위한 SW를 작동하고        
컨테이너 가상화에서는 공통적인 라이브러리나 리소스에 대해서는 공유하면서 사용한다.       
대신, 각자 필요한 부분에 대해서만 독립적인 영역에서 실행한다.(더 적은 리소스 사용)   
가볍고 빠르다! 



