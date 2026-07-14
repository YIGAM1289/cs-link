# cs-link — 이감 고객센터 페이지

카카오톡 CS 상담 연결 + 택배 배송조회 페이지.

- 고객용 페이지: https://yigam1289.github.io/cs-link/
- 관리 페이지: https://yigam1289.github.io/cs-link/admin.html

## 구조

| 파일 | 역할 |
|---|---|
| `index.html` | 고객용 페이지. 상담방 목록을 `agents.json`에서 불러와 근무중인 방으로 무작위 분배 |
| `agents.json` | 상담방 목록 원본 (이름 · 오픈채팅 링크 · 근무/휴무) |
| `admin.html` | 관리 페이지. 상담방 추가/삭제, 휴무 처리 후 저장하면 `agents.json`에 자동 커밋 |

## 상담방 관리 방법

1. 관리 페이지(admin.html) 접속
2. 최초 1회: GitHub Fine-grained 토큰 발급(cs-link 저장소, Contents: Read and write) 후 등록 — 자세한 방법은 관리 페이지 안내 참고
3. 상담방 추가(＋) / 삭제(🗑) / 휴무 토글(✅근무중 ↔ 🌙휴무) 후 "저장하고 반영하기"
4. 실제 페이지 반영까지 1~2분 소요

토큰은 사용하는 브라우저의 localStorage에만 저장되며 저장소에는 올라가지 않습니다.
