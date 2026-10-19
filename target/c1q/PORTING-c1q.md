# UN1CA — Galaxy Note 20 (Snapdragon, c1q) 포팅

> ⚠️ 실험용 · 실기기 부팅 검증 전 · 개인 사용 전용. 설치 전 EFS 백업 필수.

- 기반: UN1CA (ArtisanROM의 원본). 스냅드래곤 S20 FE(r8q) 빌드가 이미 검증된 시스템을 사용
- 칩 쪽 설정: UN1CA r8q (같은 SM8250) / 본체 쪽 설정: ArtisanROM c1s (Note 20 엑시노스)
- 커널: UN1CA kernel_samsung_sm8250 를 c1q 설정으로 빌드한 boot.img / dtbo.img (GitHub Release)
- 한국판 펌웨어 버전 조회가 비어 있을 때를 위해 `target/c1q/firmware_versions` 에 고정 버전을 둠

## GitHub 설정 (Settings → Secrets and variables → Actions)
- Secrets: `C1Q_FIRMWARE` = `SM-N981N/KOO/<IMEI>`  (KOO 는 알파벳 O)
- Variables: `C1Q_KERNEL_REPO` = `https://github.com/<아이디>/<저장소>/releases/download/c1q-kor`

## 빌드
Actions → Build Note 20 Snapdragon (c1q) → Run workflow (sim 1) → Artifacts 의 UN1CA-c1q
