# UlarBox: Organize Your Digital Life

## 1. 프로젝트 개요
- **목적**: 개인의 디지털 삶을 체계적으로 관리하기 위한 홈페이지 (UlarBox 랜딩 페이지)
- **기술 스택**:
  - **Frontend**: HTML5, Vuetify 3 (CDN), Google Fonts
  - **Hosting**: GitHub Pages
  - **Domain**: [www.ular.io](https://www.ular.io)
- **배포 브랜치**: `main`

## 2. 주요 관리 스크립트 (CLI)

### 2.1. 배포 상태 확인
```bash
# GitHub Pages 설정 및 배포 URL 확인
gh api repos/:owner/:repo/pages

# 최신 배포 워크플로우 실행 상태 확인
gh run list --workflow "pages-build-deployment" --limit 5
```

### 2.2. 로컬 테스트
```bash
# 로컬 서버 실행 (Python 3 활용)
python3 -m http.server 8000
```

### 2.3. 변경 사항 배포
```bash
# 변경 사항 반영 및 푸시 (GitHub Actions 자동 배포 트리거)
git add .
git commit -m "update: [변경 내용 요약]"
git push origin main
```

### 2.4. 이슈 및 릴리스 관리
```bash
# 현재 활성화된 이슈 확인
gh issue list

# 새로운 릴리스 태그 생성 및 배포
gh release create v1.0.0 --title "Initial Launch" --notes "Official website launch"
```

## 3. 주의 사항
- `CNAME` 파일 수정 시 도메인 연결이 끊길 수 있으므로 주의할 것.
- 외부 라이브러리는 현재 CDN 방식을 사용 중임.
