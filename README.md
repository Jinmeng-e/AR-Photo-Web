# AR-Photo-Web

## **필요한 것**

### 1. **개발 준비**
	1. 도메인 주소
		- 웹을 게시 및 QR CODE 로 제작하기 위한 웹 주소.
	2. 호스팅
		- 예상 접속 인원이 산정된 서버 임대 필요.
			- 필요한 서버 비용 산정 필요.
	3. 디자인
		- 전체 용량 15MB 이하로 유지하는 것을 권장.
			- [15MB 최적화된 3D모델 예시](https://sketchfab.com/models/3b29167b2eb44797826f8de646400756/embed)
			- 용량이 더 커질 경우 통신 상태에 따라 10초 이상의 지연 발생, 테스트 필요.
		- 그래픽~사람 간의 뎁스 테스트 필요
		- 인식하는 이미지를 사람이 가렸을 때의 인식률 해결
		- 사람이 앞에 섰을 때 이미지가 사람을 가리지 않도록 수정.
	4. 모바일 환경에 맞춰 사이트 수정 및 배포.
	5. 운영 및 개발간 돌발상황 예측
		- 무료 플랫폼을 사용했을 때 생길 수 있는 문제와 대응 가능성 판단.
		- 운영 간 생길 수 있는 문제 파악과 요금 및 사이트 이전여부 판단 및 대응.
### 2. **외부 제안 시**
	1. 예상 접속 인원 산정.
		- 인원수에 맞는 가격 책정 필요.
	2. 디자인(3D 모델)시의 한계 전달.
		- 지정한 3D 모델에 따라 화질 저하 발생.
		- 3D 모델(그래픽) - 사람 간의 뎁스 문제.
	3. 사용자의 크롬 브라우저 사용 권장 전달.
		- 다른 브라우저의 경우 정상 작동이 되지 않을 수 있음.

---
## **AR 사이트 호스팅 비교**
	**1. Netlify**
		**개요**: Netlify는 개발자가 웹 프로젝트를 배포하고 호스팅하는 데 널리 사용되는 플랫폼입니다. 최신 프레임워크와 JAMStack 아키텍처를 지원합니다.
		**특징**:
			- 맞춤 도메인(무료 SSL 인증서)
			- 지속적 배포(GitHub, GitLab, Bitbucket에서)
			- 서버리스 기능 및 API 통합
			- 더 빠른 로드 시간을 위한 에지 호스팅(AR 경험에 중요)
		**장점**:
			- 정적 웹사이트에 대한 설정이 쉽고 경량 AR 페이지에 적합
			- 커밋할 때마다 변경 사항을 자동 배포합니다.
			- 향상된 글로벌 접근성을 위해 CDN이 내장되어 있어 빠릅니다.
			- 한도가 넉넉한 무료 요금제(100GB 대역폭/월)
		**단점**:
			- 무료 플랜에서는 빌드 시간과 대역폭이 제한되어 있습니다.
			- 서버리스 기능 등 일부 고급 기능은 유료입니다.
		**가격**:
			- 무료 등급: 월 100GB 대역폭, 월 300분 빌드 시간 및 사용자 지정 도메인이 포함됩니다.
			- 유료 플랜(Pro): 사용자당 월 $19, 빌드 시간이 월 1000분으로 증가하고 대역폭이 400GB로 늘어납니다.
			- 추가 비용: $20/100GB 추가 대역폭.
		**최적의 용도**: 중소 규모 AR 프로젝트, 정적 AR 웹 앱의 빠른 배포.
	**2. Vercel**
		**개요**: Vercel은 Next.js와의 통합 및 기타 프레임워크 지원으로 잘 알려진 성능 중심 호스팅 플랫폼입니다.
		**특징**:
			- 빠른 로드 시간을 위한 글로벌 CDN
			- 에지 캐싱 및 서버리스 배포
			- 개발자를 위한 실시간 협업 배포
			- 자동 HTTPS 및 맞춤 도메인
		**장점**:
			- 빠른 CDN을 통한 즉각적인 글로벌 배포(AR에 적합)
			- Next.js, React 및 Vue.js와 같은 프레임워크와 원활하게 작동합니다.
			- 이미지 및 자산 최적화를 통한 고성능
		**단점**:
			- 무료 플랜의 대역폭 제한
			- 서버리스 및 더 큰 대역폭과 같은 고급 기능에는 유료 요금제가 필요합니다.
		**가격**:
			- 무료 등급: 무료 사용자 정의 도메인, 무제한 빌드, 100GB 대역폭 및 1000번의 서버리스 기능 실행.
			- 유료 플랜(Pro): 사용자당 월 20달러, 1TB 대역폭 및 1백만 개의 서버리스 기능 실행이 포함됩니다.
			- 엔터프라이즈 플랜: 맞춤형 가격으로 더 많은 대역폭과 기능 실행을 제공합니다.
		**최적의 용도**: 속도와 확장성에 중점을 두고 React 및 Next.js와 같은 프레임워크로 구축된 AR 경험입니다.
	**3. GitHub 페이지**
		**개요**: GitHub 페이지는 GitHub 리포지토리에 직접 통합된 정적 사이트 호스팅 서비스로, 오픈 소스 프로젝트에 적합한 옵션입니다.
		**특징**:
			- GitHub 저장소 통합을 통한 무료 호스팅
			- 간단한 정적 사이트 호스팅
			- 맞춤 도메인 지원(HTTPS 사용)
		**장점**:
			- 완전 무료, 대역폭 제한 없음
			- 모든 정적 사이트 생성기(예: Jekyll, Hugo)와 함께 사용하기 쉽습니다.
			- 데모 WebAR 프로젝트 호스팅에 적합
		**단점**:
			- 정적 전용 호스팅(동적 콘텐츠 또는 서버측 스크립팅 없음)
			- 무료로 사용할 수 있는 공개 저장소로 제한됩니다.
			- 다른 옵션에 비해 성능이 최적화되지 않았습니다.
		**최적의 용도**: 서버 측 기능이 필요하지 않은 소규모 오픈 소스 AR 프로젝트.
	**4. Firebase 호스팅(Google 제공)**
		**개요**: Firebase 호스팅은 Firebase 플랫폼의 일부로 웹 앱을 위한 안전하고 빠른 호스팅 서비스를 제공합니다.
		**특징**:
			- 맞춤 도메인 및 SSL 포함
			- 빠른 자산 전달을 위한 글로벌 CDN
			- 서버리스 기능(Cloud Functions)
			- Firebase 데이터베이스, 인증, 분석과의 직접 통합
		**장점**:
			- Firebase 서비스(데이터베이스, 인증 등)와 통합
			- 실시간 데이터가 필요한 AR 경험(예: 다중 사용자 AR)에 이상적입니다.
			- 강력한 CDN으로 빠르고 확장 가능
			- 한도가 넉넉한 무료 등급
		**단점**:
			- 비정적 웹사이트의 경우 더 복잡한 설정
			- 트래픽 양이 매우 많으면 가격이 높아질 수 있습니다.
		**최적의 용도**: 실시간 백엔드 통합과 동적 콘텐츠가 필요한 AR 애플리케이션.
	**5. CloudFront(AWS)가 포함된 Amazon S3**
		**개요**: CloudFront(AWS CDN)와 결합된 Amazon S3는 정적 콘텐츠와 동적 콘텐츠를 모두 호스팅하기 위한 강력한 옵션입니다.
		**특징**:
			- 확장성이 뛰어난 스토리지
			- 글로벌 콘텐츠 배포를 위한 CloudFront CDN
			- AWS 서비스(Lambda, 서버리스 기능 등)와의 통합
			- 맞춤 도메인 및 SSL
		**장점**:
			- 고성능 및 확장성
			- 호스팅 및 CDN 구성에 대한 세밀한 제어
			- 소규모 및 대규모 프로젝트 모두에 비용 효율적입니다(종량제)
		**단점**:
			- Netlify/Vercel에 비해 설정이 더 복잡함
			- 초보자에게 친숙하지 않습니다. AWS 관리 지식이 필요합니다
		**최적의 용도**: 높은 확장성과 백엔드 서비스 통합이 필요한 엔터프라이즈급 AR 경험 또는 프로젝트.
	**6. Heroku**
		**개요**: Heroku는 동적 애플리케이션의 배포 및 관리를 단순화하는 클라우드 플랫폼입니다.
		**특징**:
			- 여러 언어 지원(Node.js, Ruby, Python 등)
			- 맞춤 도메인 및 SSL 지원
			- 데이터베이스, 캐싱 등을 위한 추가 기능
		**장점**:
			- 동적 웹 앱 및 AR 경험을 위한 손쉬운 배포
			- 데이터베이스, 캐싱 및 타사 서비스를 위한 내장 통합
		**단점**:
			- 순수 정적 사이트에는 적합하지 않습니다(Netlify 또는 Vercel과 비교).
			- 무료 등급은 활동이 없으면 잠자기 상태가 될 수 있으므로 초기 로드 시간이 길어질 수 있습니다.
		**최적의 용도**: 사용자 계정이나 실시간 기능 등 백엔드가 필요한 동적 AR 애플리케이션.
	**7. Cloudflare 페이지**
		**개요**: Cloudflare Pages는 Cloudflare의 글로벌 에지 네트워크와 통합되어 성능과 속도를 최적화하는 무료 호스팅 서비스입니다.
		**특징**:
			- 글로벌 CDN 및 엣지 캐싱
			- 자동 SSL을 사용하는 맞춤 도메인
			- 서버리스 기능 지원
		**장점**:
			- 무료, 대역폭 제한 없음
			- Cloudflare의 에지 네트워크 덕분에 매우 빠릅니다.
			- 보다 동적인 콘텐츠를 위해 서버리스 작업자와의 통합을 지원합니다.
		**단점**:
			- 복잡한 프로젝트의 경우 서버측 기능이 제한됨
			- AWS 또는 Firebase에 비해 백엔드 통합 수가 적습니다.
		**최적의 용도**: 성능과 보안에 중점을 두고 빠르게 로딩되는 AR 사이트.
### **Summary Table**

| Platform             | Free Tier                                    | Paid Plans / Pricing                             | Performance (CDN)   | Best For                                         |
| -------------------- | -------------------------------------------- | ------------------------------------------------ | ------------------- | ------------------------------------------------ |
| **Netlify**          | 100GB bandwidth, 300 build minutes           | Pro: $19/month/user, $20/100GB extra bandwidth   | Fast (built-in CDN) | Static AR pages with quick setup                 |
| **Vercel**           | 100GB bandwidth, 1000 serverless executions  | Pro: $20/month/user, 1TB bandwidth               | Fast (global CDN)   | Framework-based AR experiences (Next.js, React)  |
| **GitHub Pages**     | Free for public repos                        | Pro GitHub account: $4/month                     | Limited             | Small, static AR projects, open-source hosting   |
| **Firebase**         | 1GB storage, 10GB/month data transfer        | Pay-as-you-go: $0.026/GB storage, $0.15/GB data  | Fast (global CDN)   | Dynamic AR apps with real-time data needs        |
| **AWS (S3 + CF)**    | 5GB storage, 50GB transfer (first 12 months) | S3: $0.023/GB, CF: $0.085/GB (first 10TB)        | High (CloudFront)   | Large-scale AR projects needing backend services |
| **Heroku**           | 550 dyno hours, 512MB RAM                    | Hobby: $7/month/dyno, Production: from $25/month | Moderate            | Dynamic AR apps with backend functionality       |
| **Cloudflare Pages** | Unlimited bandwidth, 500 build minutes       | Pro: $20/month                                   | Fast (edge CDN)     | Performance-oriented static AR sites             |
### **사용 사례 기반 권장사항**

	**소규모 정적 AR 프로젝트의 경우:**
		- Netlify 또는 Vercel을 사용하면 빠른 설정과 탁월한 성능을 얻을 수 있습니다.
		- GitHub 페이지 오픈 소스 프로젝트인 경우 속도에 대한 우려가 적습니다.
	
	**동적 또는 실시간 AR 경험의 경우:**
		- Firebase 호스팅 또는 AR 프로젝트에 동적 콘텐츠(예: 사용자 상호작용, 데이터베이스)가 포함된 경우 Heroku.
		- AWS(S3 + CloudFront) 높은 확장성과 백엔드 서비스가 모두 필요한 엔터프라이즈 수준의 대규모 AR 프로젝트용.
	
	**엔터프라이즈/성능 중심 AR 프로젝트의 경우:**
		- AWS(S3 + CloudFront) 또는 Cloudflare Pages를 통해 제어, 보안 및 글로벌 도달 범위를 극대화할 수 있습니다.


---
## **유료 플랫폼 비교**

	**1. 8th Wall**
	
		- **Overview:** 8th Wall은 마커리스 AR, 이미지 추적, 월드 효과와 같은 고급 기능을 제공하는 선도적인 WebAR 개발 플랫폼입니다. 고품질의 대규모 WebAR 프로젝트에 널리 사용됩니다.
		- **Key Features:**
			- 마커리스 AR, 이미지 및 얼굴 추적
			- 물리적 공간에 물체를 배치하기 위한 SLAM(World Tracking)
			- 클라우드 기반 호스팅 및 게시
			- 앱 없이 iOS와 Android 모두에서 작동
		- **Pricing:**
			- **Starter Plan:** 스타터 플랜: 프로젝트당 월 $99. 이 계획에는 워터마크가 있는 플랫폼에 대한 전체 액세스가 포함됩니다.
			- **Pro Plan:** 프로젝트당 월 $495. 워터마크를 제거하고 더 많은 맞춤형 브랜딩 기능과 고급 지원을 포함합니다.
			- **Enterprise Plan:** 대규모 조직을 위한 맞춤형 가격 책정 및 무제한 프로젝트, 프리미엄 지원, 분석과 같은 고급 기능.
		- **Best For:** 세계 추적 및 고급 AR 기능을 갖춘 고품질의 복잡한 WebAR 경험입니다.
	
	**2. Zappar (Zappar WebAR)**
	
		- **Overview:** Zappar는 개발자를 위한 ZapWorks Studio 및 Universal AR SDK와 같은 사용하기 쉬운 도구와 함께 WebAR을 제공하는 확립된 AR 플랫폼입니다.
		- **Key Features:**
			- 이미지 및 얼굴 추적
			- 빠른 AR 생성을 위한 ZapWorks Studio
			- AR을 맞춤형 프레임워크(Three.js, A-Frame, Unity)에 통합하기 위한 범용 AR SDK
			- 분석 및 맞춤형 브랜딩 옵션
		- **Pricing:**
			- **ZapWorks Starter:** $59/월(1개의 프로젝트 및 기본 기능으로 제한됨).
			- **ZapWorks Pro:** $175/월, 여러 프로젝트, 맞춤형 브랜딩 및 분석이 포함됩니다.
			- **Enterprise Plan:** 무제한 프로젝트, 프리미엄 지원 및 화이트 라벨 솔루션이 포함된 맞춤형 가격입니다.
		- **Best For:** 프로젝트 구축을 위한 이미지 추적 및 사용하기 쉬운 도구를 갖춘 보다 저렴한 WebAR 플랫폼을 찾는 팀 및 개발자.
	
	**3. Blippar**
	
		- **Overview:** Blippar는 대화형 브랜드 기반 경험에 중점을 둔 WebAR 솔루션을 제공합니다. 여기에는 강력한 AR 생성 도구와 광범위한 파트너 네트워크가 포함됩니다.
		- **Key Features:**
			- 마커 기반 및 마커리스 AR
			- WebAR 포털 및 Blippbuilder(코드 없는 AR 생성 도구)
			- 고급 이미지 및 표면 추적
			- 전자상거래 및 소셜 미디어 플랫폼과의 통합
		- **Pricing:**
			- **Blippar Pro:** Blippbuilder를 사용하는 제작자의 경우 월 $50입니다(제한된 기능 포함).
			- **Blippar Enterprise:** 사용량에 따른 맞춤형 가격 책정, 화이트 라벨 솔루션, 전체 API 액세스 및 AR 캠페인에 대한 제한 없음을 제공합니다.
		- **Best For:** 특히 마케팅 및 전자 상거래를 위한 풍부한 대화형 AR 경험을 만들고자 하는 브랜드입니다.
	
	**4. ARize (ARize Web Studio)**
	
		- **Overview:** ARize는 코딩 없이 대화형 AR을 만들려는 제작자와 기업을 대상으로 보다 저렴한 WebAR 플랫폼을 제공합니다. 주요 초점은 제품 시각화 및 마케팅에 있습니다.
		- **Key Features:**
			- 마커리스 AR, 이미지 추적
			- 제품 시각화 도구(3D 개체 배치)
			- 사용자 정의 가능한 UI 및 브랜딩
			- 간단한 드래그 앤 드롭 인터페이스
		- **Pricing:**
			- **Business Plan:** 월 $25부터 시작하며 최대 10개의 AR 경험과 3D 모델이 포함됩니다.
			- **Enterprise Plan:** 맞춤형 가격으로 더 많은 AR 경험, 더 나은 분석, API 액세스를 제공합니다.
		- **Best For:** 기술적 복잡성 없이 제품 AR 경험을 위한 저렴하고 간단한 솔루션을 원하는 중소기업 및 제작자.
	
	**5. echoAR**
	
		- **Overview:** echoAR은 클라우드 기반 AR 스토리지 및 스트리밍에 중점을 두어 3D 자산을 WebAR 경험에 쉽게 저장, 관리 및 전달할 수 있도록 해줍니다.
		- **Key Features:**
			- 3D 콘텐츠를 위한 클라우드 스토리지 및 스트리밍
			- 다양한 3D 형식 지원(GLB, FBX, OBJ 등)
			- 크로스 플랫폼 지원(iOS, Android, 웹)
			- AR 콘텐츠 실시간 업데이트
		- **Pricing:**
			- **Free Tier:** 제한된 클라우드 스토리지와 도구에 대한 기본 액세스가 포함됩니다.
			- **Starter Plan:** $79/월, 추가 저장 공간 및 사용량이 포함됩니다.
			- **Business Plan:** 대규모 AR 프로젝트 및 엔터프라이즈급 기능의 경우 월 $249입니다.
			- **Enterprise Plan:** 대규모 AR 배포를 위한 맞춤형 가격입니다.
		- **Best For:** 실시간 3D 콘텐츠 업데이트를 갖춘 WebAR용 확장 가능한 클라우드 솔루션이 필요한 개발자 및 기업.
	**6. Lightship by Niantic (Niantic Lightship ARDK)**
	
		- **Overview:** Lightship은 Niantic의 AR 플랫폼으로, 모바일 앱과 WebAR 모두에서 공유 AR 경험을 구축하기 위한 도구를 제공합니다. 멀티플레이어 경험을 포함한 대규모 AR 애플리케이션용으로 설계되었습니다.
		- **Key Features:**
			- 멀티플레이어 AR(공유 세계 경험)
			- 실제 객체 인식을 위한 의미론적 분할
			- 마커리스 AR 및 실제 매핑
			- 맞춤형 AR 개발을 위한 광범위한 SDK 지원
		- **Pricing:**
			- **Free Tier:** ARDK 도구 및 개발 기능에 대한 기본 액세스입니다.
			- **Enterprise Plan:** 프리미엄 지원 및 대규모 배포가 포함된 상업용 맞춤형 가격입니다.
		- **Best For:** 특히 게임이나 소셜 상호작용을 위한 대규모 멀티플레이어 WebAR 또는 앱 기반 AR 경험을 구축하는 개발자.

---

### **Summary Table (with Pricing)**

| Platform      | Key Features             | Pricing                          | Best For                |
| ------------- | ------------------------ | -------------------------------- | ----------------------- |
| **8th Wall**  | 마커리스 AR, SLAM, 이미지 추적    | 스타터: $99/월/프로젝트, 프로: $495/월/프로젝트 | 고품질 WebAR, 고급 기능        |
| **Zappar**    | 이미지, 얼굴 추적, 간편한 도구       | 스타터: $59/월, 프로: $175/월           | 기본 기능을 갖춘 저렴한 WebAR     |
| **Blippar**   | 마커 기반 및 마커리스 AR          | Pro: $50/월, Enterprise: 맞춤형 가격   | 브랜드 중심 WebAR, 인터랙티브 마케팅 |
| **ARize**     | 마커리스 AR, 제품 시각화          | 비즈니스: $25/월, 엔터프라이즈: 맞춤형 가격      | 제품 시각화를 위한 저렴한 WebAR    |
| **echoAR**    | 클라우드 기반 3D 콘텐츠 저장 및 스트리밍 | 스타터: $79/월, 비즈니스: $249/월         | WebAR용 확장 가능한 클라우드 솔루션  |
| **Lightship** | 멀티플레이어 AR, 실제 매핑         | 프리 티어, 엔터프라이즈: 맞춤형 가격            |~ 대규모 AR, 멀티플레이 경험        |

---

### 사용 사례 및 예산에 따른 권장 사항

1. 중소규모 WebAR 프로젝트의 경우:**
	
	- **Zappar** 는 월 $59부터 시작하는 소규모 WebAR 프로젝트를 진행하는 기업이나 개발자에게 이상적인 저렴한 솔루션을 제공합니다.
	- **ARize**는 월 $25의 저렴한 시작 가격으로 제품 시각화 및 마케팅을 위한 훌륭한 옵션입니다.
2. 고급 WebAR 경험의 경우:**
	
	- **8th Wall**은 SLAM 및 마커 없는 추적과 같은 고급 AR 기능을 위한 최고의 선택이지만 가격은 더 높습니다(월 99~495달러).
	- **Blippar**는 월 $50부터 시작하는 전문 도구와 맞춤 설정을 통해 브랜드 중심의 대화형 AR 경험을 제공합니다.
3. **For Large-Scale or Multiplayer AR Projects:**
	
	- **Niantic Lightship**은 공유 AR 또는 멀티플레이어 환경을 작업하는 개발자에게 적합하며 무료 등급 및 맞춤형 기업 가격이 제공됩니다.
	- **echoAR**은 월 $79부터 시작하는 대규모 3D 자산 라이브러리를 위한 확장 가능한 클라우드 스토리지가 필요한 사용자에게 이상적입니다.


---
## **DEVELOPMENT**

모바일 WebAR 개발에서는 성능, 사용자 경험 및 장치 간 호환성에 중점을 두는 것이 중요합니다. 다음은 기본 AR 경험을 위한 샘플 스크립트와 함께 모바일 WebAR에 맞춰 수정된 개발 프로세스입니다.

**모바일 WebAR 개발 프로세스 개정**
**1. 모바일 AR 경험 정의**
	**사용 사례**: 모바일 경험에 필요한 AR 요소를 고려하세요. 사용자가 작은 화면에서 AR 장면과 어떻게 상호작용할지 생각해 보세요(예: 개체 탭하기, 회전하기, 끌기).
	**환경**: 사용자는 마커 기반 AR(QR 코드와 같은 물리적 마커 사용)을 경험하게 됩니까, 아니면 마커 없는 AR(평면에 물체 배치)을 경험하게 됩니까?
**2. 모바일에 최적화된 WebAR 프레임워크 선택**
- AR.js: 마커 기반 AR을 위한 가볍고 모바일 친화적입니다. 대부분의 최신 브라우저에서 작동합니다.
- 8th Wall: 강력하고 기능이 풍부하며 고급 모바일 기능을 갖춘 마커리스 AR에 적합합니다.
- A-Frame: 모바일을 지원하며 빠른 프로토타이핑 및 맞춤형 WebAR 장면을 위해 AR.js와 잘 작동합니다.
- MindAR: 모바일 AR 경험을 위한 성능 중심의 소규모 라이브러리입니다.
**3. 모바일에 최적화된 자산 준비**
- 3D 모델: 모바일에서 빠른 로딩에 최적화된 .glb 또는 .gltf 형식으로 모델이 가벼운지 확인하세요.
- 텍스처 및 애니메이션: 텍스처를 압축하고 애니메이션을 단순화하여 저전력 모바일 장치에서 원활하게 렌더링되도록 합니다.
- 폴리 수 감소: 보다 원활한 상호 작용과 빠른 성능을 위해 다각형 수를 최소화합니다.
**4. 모바일 중심 개발 환경 구축**
- 모바일 우선 반응형 디자인을 사용하여 AR 요소가 다양한 화면 크기에 걸쳐 올바르게 확장되고 표시되도록 합니다.
- 레이아웃이 모바일 화면에 잘 적응되도록 뷰포트 메타 태그를 추가합니다.

<meta name="viewport" content="width=device-width, initial-scale=1.0">
**5. 모바일 AR 경험 개발**
- 카메라 액세스: 카메라 권한을 요청하고 AR 장면에서 권한이 거부된 경우를 처리하는지 확인하세요.
- 터치 상호 작용: 직관적인 터치 상호 작용을 추가합니다(예: 탭하여 개체 배치, 핀치하여 확대/축소, 스와이프하여 회전).
- 성능 최적화: 모델 크기를 줄이고 모바일 친화적인 압축 기술을 활용하여 로드 시간을 최적화합니다.
**예제 코드(모바일용 A-Frame + AR.js)**
	이 기본 예에서는 AR.js 및 A-Frame을 사용하여 모바일에서 마커 기반 WebAR 환경을 만듭니다.

<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
<script src="https://cdn.rawgit.com/jeromeetienne/AR.js/1.7.2/aframe/build/aframe-ar.min.js"></script>
<title>Mobile WebAR</title>
</head>
<body>
<a-scene embedded arjs="sourceType: webcam;">
  <!-- Define a marker to anchor the AR content -->
  <a-marker preset="hiro">
	<!-- 3D model to display in AR -->
	<a-entity 
	  gltf-model="url(path/to/your-model.glb)" 
	  scale="0.5 0.5 0.5" 
	  position="0 0 0" 
	  rotation="0 0 0"
	  animation="property: rotation; to: 0 360 0; loop: true; dur: 10000">
	</a-entity>
  </a-marker>
  
  <!-- Add a basic light source -->
  <a-light type="directional" position="0 4 4"></a-light>
  
  <!-- Camera and scene setup -->
  <a-entity camera></a-entity>
</a-scene>
</body></html>
	코드의 주요 특징:
		- 모바일 최적화: 코드는 모바일 브라우저에서 원활하게 작동하는 AR.js를 활용합니다. 모바일 친화적인 크기 조정을 위해 'viewport' 메타 태그를 사용합니다.
		- 마커 기반 AR: 마커가 정의되어('hiro') 모바일 장치에서 AR 콘텐츠를 더 쉽게 인식하고 렌더링할 수 있습니다.
		- 간단한 3D 모델: '.glb' 모델이 마커에 배치되며 간단한 회전 애니메이션을 사용하여 상호작용성을 추가합니다.
		- 경량: 이 예제는 단순성과 경량 라이브러리 사용으로 인해 모바일 장치에 적합합니다.
1. 모바일 장치 테스트
	- 여러 기기에서 테스트: iOS(Safari) 및 Android(Chrome) 기기 모두에서 환경이 원활하게 실행되는 지 확인하세요.
	- 양한 화면 크기에 맞게 최적화: AR 개체의 크기가 올바르게 조정되고 다양한 모바일 장치에서 상호 작용이 유지되는지 확인하세요.
	- 권한 확인: 사용자가 액세스를 거부하는 시나리오를 포함하여 사이트에서 카메라 권한을 처리하는 방법을 테스트합니다.
2. 모바일에서 배포 및 액세스
	- 호스팅: 모바일 네트워크에서 빠른 로딩을 위해 글로벌 CDN을 갖춘 모바일에 최적화된 호스팅 플랫폼(예: Netlify 또는 Vercel)을 선택하세요.
	- QR 코드 액세스: 사용자는 모바일 기기에서 AR 경험에 액세스하게 되므로 빠른 액세스를 위해 QR 코드를 제공하세요. qr-code-generator.com과 같은 서비스는 귀하의 URL에 대한 코드를 생성할 수 있습니다.
3. 모바일 성능 모니터링 및 최적화
	- 분석: 모바일 분석을 통합하여 다양한 장치에서의 로드 시간, 사용자 상호 작용 및 성능을 추적합니다.
	- 반복: 실제 테스트를 기반으로 특히 성능 및 터치 상호 작용을 개선합니다.
