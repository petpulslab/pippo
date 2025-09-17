# Curacle 팝업 설정

이 폴더는 Curacle 협업 프로모션 팝업을 GitHub를 통해 원격으로 관리하기 위한 설정 파일들을 포함합니다.

## 파일 구조

```
docs/curacle/
├── popup-config.json           # 팝업 설정 JSON 파일
├── simple_result_popup.png     # 검사 결과 화면 팝업 이미지
├── launch_popup_event.png      # 홈 화면 런치 이벤트 팝업 이미지
└── README.md                   # 이 파일
```

## popup-config.json 설정

```json
{
  "simple_result_popup": {
    "popup_enabled": true,
    "popup_image_url": "https://raw.githubusercontent.com/petpulslab/pippo/refs/heads/main/curacle/simple_result_popup.png",
    "popup_blog_url": "https://blog.naver.com/curacle_cp01",
    "popup_form_url": "https://form.naver.com/response/jDn2ROD-U9PcHSV5UDZDvA"
  },
  "home_screen_popup": {
    "popup_enabled": true,
    "popup_image_url": "https://raw.githubusercontent.com/petpulslab/pippo/refs/heads/main/curacle/launch_popup_event.png",
    "popup_link_url": "https://smartstore.naver.com/petpulslab/products/10124282845"
  }
}
```

## 팝업 종류별 설정

### 1. 검사 결과 화면 팝업 (`simple_result_popup`)
- **표시 위치**: 소변 검사 결과 화면 (`simple_result.dart`)
- **표시 조건**: 한국어 + (디버그 모드 OR 중요 검사항목 이상)
- **설정 항목**:
  - `popup_enabled`: 팝업 활성화 여부
  - `popup_image_url`: 팝업 이미지 URL
  - `popup_blog_url`: 상단 5/6 영역 클릭 시 이동할 블로그 URL
  - `popup_form_url`: 하단 1/6 영역 클릭 시 이동할 폼 URL

### 2. 홈 화면 런치 이벤트 팝업 (`home_screen_popup`)
- **표시 위치**: 홈 화면 (`home_screen.dart`)
- **표시 조건**: 한국어 + (디버그 모드 OR 오늘 처음 접속)
- **설정 항목**:
  - `popup_enabled`: 팝업 활성화 여부
  - `popup_image_url`: 팝업 이미지 URL
  - `popup_link_url`: 이미지 클릭 시 이동할 상품 페이지 URL

### 설정 변경 방법

#### 검사 결과 팝업 관리
1. **팝업 활성화/비활성화**: `simple_result_popup.popup_enabled` 값 변경
2. **이미지 변경**: `simple_result_popup.popup_image_url` 수정
3. **블로그 링크 변경**: `simple_result_popup.popup_blog_url` 수정
4. **폼 링크 변경**: `simple_result_popup.popup_form_url` 수정

#### 홈 화면 팝업 관리
1. **팝업 활성화/비활성화**: `home_screen_popup.popup_enabled` 값 변경
2. **이미지 변경**: `home_screen_popup.popup_image_url` 수정
3. **상품 링크 변경**: `home_screen_popup.popup_link_url` 수정

### 사용 방법

1. GitHub에 이 폴더를 업로드
2. 앱에서 GitHub Raw URL을 통해 설정값 불러오기
3. 설정 변경시 GitHub에서 파일만 수정하면 앱에 즉시 반영

### GitHub Raw URL 예시

```
https://raw.githubusercontent.com/username/repository/main/docs/curacle/popup-config.json
```

## 주의사항

- JSON 파일 형식을 정확히 지켜주세요
- 이미지는 `.png`, `.jpg`, `.jpeg` 형식을 권장합니다
- URL은 `https://`로 시작하는 완전한 URL을 사용해주세요
