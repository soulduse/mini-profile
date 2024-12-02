# 프로그래밍좀비 프로필 페이지

이 저장소는 [programmingzombie.com](https://programmingzombie.com)의 소스 코드를 포함하고 있습니다. 300개 이상의 앱을 개발하여 퇴사를 이룬 개발자의 프로필과 콘텐츠를 소개하는 원페이지 웹사이트입니다.

## 주요 기능

- 반응형 디자인으로 모든 디바이스에서 최적화된 경험 제공
- 프로필 정보, 소셜 미디어 링크, 제품 소개 섹션 포함
- 블로그 포스트와 인터뷰 등 주요 콘텐츠 링크 프리뷰 제공
- GitHub 컨트리뷰션 그래프 통합
- Google Analytics를 통한 사용자 행동 추적

## 기술 스택

- HTML5
- CSS3 (Tailwind CSS)
- Google Analytics
- Pretendard 웹폰트

## AWS 배포 과정

이 웹사이트는 다음과 같은 AWS 서비스들을 활용하여 배포되었습니다:

1. **도메인 구매 (Route 53)**
   - AWS Route 53을 통해 programmingzombie.com 도메인 구매 및 관리

2. **정적 웹 호스팅 (S3)**
   - Amazon S3 버킷 생성
   - 정적 웹사이트 호스팅 기능 활성화
   - HTML 파일 및 관련 리소스 업로드

3. **CDN 설정 (CloudFront)**
   - CloudFront 배포 생성 및 S3 버킷 연결
   - SSL/TLS 인증서 설정으로 HTTPS 지원
   - 글로벌 엣지 로케이션을 통한 빠른 컨텐츠 전송

4. **도메인 연결 (Route 53 + CloudFront)**
   - Route 53에서 CloudFront 배포와 도메인 연결
   - DNS 레코드 설정으로 도메인 연결 완료

## 개발 노트
이 프로젝트는 Claude AI의 도움을 받아 2시간 만에 개발부터 배포까지 완료되었습니다. 웹 개발 경험이 없는 상태에서도 AI의 도움으로 전문적인 웹사이트를 구축할 수 있었던 좋은 사례입니다.

## UI 디자인 영감
[성구님 사이트](https://www.seonggoo.com/)
