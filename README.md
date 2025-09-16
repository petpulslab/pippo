# Curacle 팝업 설정

이 폴더는 Curacle 협업 프로모션 팝업을 GitHub를 통해 원격으로 관리하기 위한 설정 파일들을 포함합니다.

## 파일 구조

```
docs/curacle/
├── popup-config.json    # 팝업 설정 JSON 파일
├── images/             # 팝업 이미지 저장 폴더
│   └── curacle_popup.png
└── README.md           # 이 파일
```

## popup-config.json 설정

```json
{
  "popup_enabled": true,                    // 팝업 활성화 여부
  "popup_image_url": "이미지 URL",          // 팝업에 표시할 이미지 URL
  "popup_destination_url": "이동할 URL"     // 팝업 클릭시 이동할 URL
}
```

### 설정 변경 방법

1. **팝업 활성화/비활성화**: `popup_enabled` 값을 `true` 또는 `false`로 변경
2. **이미지 변경**: `images/` 폴더에 새 이미지 업로드 후 `popup_image_url` 수정
3. **링크 변경**: `popup_destination_url` 값 수정

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