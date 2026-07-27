# legal

위유즈 서비스의 정책·지원 페이지. GitHub Pages(main 루트)로 공개됩니다.

```
https://daco2020.github.io/legal/<프로젝트>/privacy.html
```

## 구조

| 경로 | 무엇 |
| --- | --- |
| `style.css` | 모든 프로젝트가 공유하는 스타일. 여기만 고치면 전부 바뀝니다 |
| `<프로젝트>/privacy.html` | 개인정보 처리방침 |
| `<프로젝트>/support.html` | 고객 지원 (App Store Connect의 Support URL) |

## 갱신

원본 마크다운은 각 프로젝트 저장소에 있고, 여기에는 **빌드된 HTML만** 올립니다.
Abilit의 경우 원본은 `Abilit/docs/legal/privacy-ko.md` 입니다.

```bash
cp ~/dev/Abilit/docs/legal/site/*.html abilit/ && git add -A && git commit -m "abilit: 방침 갱신" && git push
cp ~/dev/noname-2/docs/legal/site/*.html yarr/ && git add -A && git commit -m "yarr: 방침 갱신" && git push
```

Yarr의 원본은 `noname-2/docs/legal/{privacy-en,privacy-ko,support}.md` 이고, 앱의 링크 상수는 `Sources/App/AppLinks.swift` 입니다.

## 주의

이 URL은 **App Store 심사 필수 항목**입니다. 404가 나면 앱이 스토어에서 내려갑니다.
경로를 바꾸면 앱의 `AbilitShared/AppLinks.swift`도 같이 고쳐야 합니다.
