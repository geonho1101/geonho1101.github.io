# geonho1101.github.io · K‑Magpie

1인 인디 게임 개발자 **K‑Magpie**(geonho1101)의 깃허브 페이지 저장소입니다.
이 저장소는 간단한 랜딩 페이지와 \*\*AdMob `app-ads.txt`\*\*를 호스팅합니다.

---

## 🔗 Live

* 사이트: **[https://geonho1101.github.io](https://geonho1101.github.io)**
* app-ads.txt: **[https://geonho1101.github.io/app-ads.txt](https://geonho1101.github.io/app-ads.txt)**

> `index.html`에는 `/app-ads.txt` 존재 여부를 자동으로 체크해 배지로 표시하는 스크립트가 포함되어 있습니다.

---

## 🚀 Quickstart

1. 저장소 이름을 **`geonho1101.github.io`** 로 생성 (Public).
2. 루트(최상위)에 아래 파일을 커밋:

   * `index.html` (랜딩 페이지)
   * `app-ads.txt` (AdMob 인증 파일)
3. **Settings → Pages**

   * Source: `Deploy from a branch`
   * Branch: `main` / `/ (root)` 선택 → Save
4. 몇 초 후 `https://geonho1101.github.io` 에서 확인.

---

## 📁 Repository Structure

```
/ (root)
├─ index.html        # 랜딩 페이지 (Games/About/Contact)
├─ app-ads.txt       # AdMob 인증 파일 (루트 필수)
└─ assets/           # (선택) 이미지 등 정적 리소스
```

---

## 📣 Edit Points (필수 교체)

* `index.html`

  * Games 섹션의 **Google Play** 링크 `href` 값
  * 썸네일: `assets/` 폴더에 이미지 추가 후 `<img>` 태그로 교체 가능
  * Contact 섹션: 이메일/깃허브 링크 확인
* `app-ads.txt`

  * 본인 **Publisher ID**가 맞는지 확인 (아래 참고)

---

## 🧾 AdMob `app-ads.txt`

* 위치: **루트 경로**(반드시 `/app-ads.txt`)
* 한 줄 구조: `<도메인>, <게시자ID>, <관계>, <인증기관ID>`
* 본 저장소에서 사용할 내용(예시 아님, 본인 ID):

```txt
google.com, pub-3632022254909828, DIRECT, f08c47fec0942fa0
```

### 필드 설명

* `google.com` : 광고 시스템 도메인 (AdMob/AdSense = Google)
* `pub-3632022254909828` : **게시자 ID(Publisher ID)**
* `DIRECT` : 직접 소유 계정이면 `DIRECT` (대행사면 `RESELLER`)
* `f08c47fec0942fa0` : Google 인증 기관 ID (고정값)

> 반영은 AdMob에서 **최대 24\~48시간 지연**될 수 있습니다. AdMob → *app-ads.txt 상태 확인*으로 재검사할 수 있습니다.

---

## 🛠️ Troubleshooting

* `https://.../app-ads.txt` 가 404 → 파일이 **루트**에 있는지, 확장자가 `.txt` 인지 확인.
* GitHub Pages 캐시로 변경이 늦게 보일 때 → 강력 새로고침(CTRL/CMD+Shift+R) 또는 파일 내용에 사소한 변경 후 재커밋.
* `index.html`의 상태 배지가 "경고"일 때 → `/app-ads.txt` 접근 가능 여부와 내용(google.com / pub-) 포함 여부 점검.

---

## 📬 Contact

* Email: **[lewlew123rnrmf@gmail.com](mailto:lewlew123rnrmf@gmail.com)**
* GitHub: **[https://github.com/geonho1101](https://github.com/geonho1101)**

---

## Notes

* 현재는 공용 도메인(`github.io`)을 사용합니다. 추후 커스텀 도메인을 연결하려면 **Settings → Pages → Custom domain**에서 CNAME 설정을 통해 연결할 수 있습니다.
* 각 게임별 개인정보처리방침은 해당 게임의 스토어 페이지에 링크하는 **개별 문서**로 운영하는 것을 권장합니다.(본 저장소에는 공통 Privacy 링크를 제거했습니다.)
