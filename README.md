# 레이아웃 도면 인덱스

인테리어 상담용 현장 도면/레이아웃 뷰어 (정적 사이트, 빌드 없음).

- **뷰어**: `index.html` — 고객에게 보여주는 화면. `projects.json`을 읽어 렌더링.
- **관리자**: `admin.html` — 현장/이미지 데이터를 편집하고 GitHub에 직접 커밋.
- **데이터**: `projects.json` — 현장 목록, 도면안, 이미지 정보.
- **이미지**: `images/` — 업로드된 도면/렌더 이미지.

## 배포

GitHub Pages: Settings → Pages → Source: `main` / `(root)`.
1~2분 후 `https://<owner>.github.io/<repo>/` 에서 확인.

## 비밀번호

뷰어/관리자 공통 게이트 비밀번호는 `projects.json`의 `gate` 값 (기본 `9999`).
저장소가 public이면 이 비밀번호는 소스에 노출되므로 눈속임 수준입니다.

## 관리자 토큰

`admin.html`에서 편집하려면 이 저장소에 대한 GitHub fine-grained personal access token이 필요합니다.
- Repository access: 이 저장소만 선택
- Permissions → Contents: Read and write

`admin.html`은 자신이 올라간 GitHub Pages 주소(`<owner>.github.io/<repo>/`)에서 OWNER/REPO를 자동 감지합니다.
