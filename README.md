# 🕶️ CTF 프로젝트: Pixel Gallery

![CTFmain](CTF_PixelGallery_main.gif)

> 실제 웹 해킹 시나리오 기반의 워게임 플랫폼  
> Team EN 제작 · 정보보안 교육 및 실습용 프로젝트

---

## 🎯 프로젝트 개요

<p float="left">
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2001.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2002.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2003.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2004.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2005.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2006.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2007.png" width="200" />
  <img src="https://github.com/whathekim/CTF_PixelGallery/blob/main/walkthrough%2008.png" width="200" />
</p>

**Pixel Gallery**는 다양한 웹 취약점을 학습할 수 있도록 구성된 **CTF(해킹 문제 풀이)** 기반 워게임 프로젝트입니다.  
WordPress, FTP, SSH 등 실제 웹 환경과 유사하게 구축하였으며, 시나리오 기반으로 문제를 해결하며 **실전 대응 능력**을 향상시킬 수 있습니다.

이 프로젝트는 다음과 같은 목적을 지닙니다:
- 정보보안 실습 및 교육
- CTF 훈련 및 모의 해킹 연습
- 실전 침해 대응 능력 강화

---

## 🧰 주요 시나리오 및 기술 요소

- 🔍 **웹소스 분석 및 힌트 추출**  
  HTML 주석, base64, QR 코드, brainfuck 등 다양한 기법으로 인코딩된 힌트 분석

- 🖼️ **스테가노그래피 활용**  
  이미지 속 메시지를 `stegseek`으로 추출하여 추가 정보 확보

- 🗂️ **디렉토리 브루트포싱 및 WordPress 구조 분석**  
  `gobuster`를 통해 `wp-content` 및 주요 경로 탐색

- 🧩 **워드리스트 기반 파일 추적**  
  숨겨진 `.txt` 파일을 탐색하며 정답에 접근

- 🎮 **웹 기반 미니게임 내 힌트 분석**  
  점프 게임을 통한 힌트(HEX 등) 획득 및 경로 유추

- 🔑 **SSH 계정 크래킹 및 접속**  
  `hydra`를 활용한 로그인 정보 크래킹

- 🧾 **SQL Injection 시나리오 구성**  
  `' OR 1=1 --` 등 입력을 통한 인증 우회

- 📤 **FTP 익명 로그인 및 웹쉘 업로드**  
  `webshell.php` 업로드 후 RCE 시나리오 진행

- 🚪 **포트 스캐닝 및 knock 시퀀스 활용**  
  `knock.sh`로 비공개 포트 개방

- 🧬 **웹쉘을 통한 경로 탐색 및 플래그 획득**  
  시스템 내 파일 탐색을 통한 정보 수집

- ⚙️ **루트 권한 상승 트리거 설계**  
  특정 포트 연결 시 루트 권한 실행 조건 설정

---

## 🧑‍💻 팀 구성 및 역할

| 이름       | GitHub ID                                      | 담당 역할                                                             |
|------------|------------------------------------------------|------------------------------------------------------------------------|
| 조범근     | [whathekim](https://github.com/whathekim) | 취약 웹사이트 제작, hydra 기반 공격 환경 구성, 전체 시나리오 설계 및 워크스루 문서 작성                           |
| 김정현     | [JeongHyeon96](https://github.com/JeongHyeon96)       | WordPress, FTP, SQLi, 웹쉘 취약점 환경 구성 |
| 김병욱     | [byungwook99](https://github.com/byungwook99)   | SSH 환경 설계 및 권한 상승 트리거 구성                                |

---

## 💽 가상머신 다운로드

워크게임 환경 테스트용 OVA 가상머신은 아래 링크에서 확인 가능합니다.  
👉 [PixelGallery_VM.ova 다운로드](https://drive.google.com/file/d/1_gizfkVfZi1t7p3K2RI9asCyjgrrKsUH/view)

---

## 🚀 실행 가이드

1. Oracle VM VirtualBox 실행  
2. `PixelGallery_VM.ova` 가져오기  
3. 네트워크 설정: **호스트 전용 어댑터**  
4. 가상머신 부팅 후 `nmap`으로 포트 및 서비스 스캐닝

---

## 📝 워크스루 문서

문제별 상세 풀이가 포함된 워크스루 문서는 아래 링크에서 확인할 수 있습니다.
👉 [Walkthrough 보기 및 다운로드 (pdf 파일)](https://github.com/whathekim/CTF_PixelGallery/blob/main/EN_CTF%20walkthrough.pdf)



