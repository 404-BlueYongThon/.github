# 로고 가이드

## 📁 로고 파일 위치

```
.github/
└── assets/
    ├── logo.png           # 404 Found 로고 (300x100px)
    ├── logo-square.png    # 정사각형 로고 (512x512px)
    ├── banner.png         # 배너 이미지 (1200x300px)
    └── social-card.png    # SNS 공유 이미지 (1200x630px)
```

---

## 🎨 로고 디자인 가이드

### 컨셉: "404 Not Found → 404 Found"

**핵심 메시지:**
- 404 에러 (찾을 수 없음)
- 응급 환자를 위한 병원을 찾음
- AI가 해결

**색상 팔레트:**
- Primary: `#4A90E2` (Blue - 신뢰, 의료)
- Secondary: `#FF6B6B` (Red - 응급, 긴급)
- Accent: `#00D9FF` (Cyan - AI, 기술)
- Dark: `#2C3E50` (Text)
- Light: `#ECF0F1` (Background)

**타이포그래피:**
- Font Family: Inter, Pretendard (한글)
- 404: Bold, 크게
- Found: Medium, 색상 강조

---

## 🛠️ 로고 제작 방법

### Option 1: Figma (추천)
1. Figma 무료 계정 생성
2. 템플릿 파일 열기: [링크 추가 예정]
3. 색상/텍스트 수정
4. Export as PNG (2x, 3x)

### Option 2: Canva
1. Canva 무료 계정 생성
2. "Logo" 템플릿 선택
3. 위 색상 팔레트 사용
4. "404 Found" 텍스트 + 의료/AI 아이콘
5. 다운로드 (PNG, 투명 배경)

### Option 3: AI 생성 (빠름!)
```bash
# DALL-E / Midjourney Prompt
"404 Found logo, modern tech style, blue and red colors, 
medical emergency theme, AI technology, minimalist design, 
clean typography, professional"
```

---

## 📏 로고 규격

### 1. logo.png (300x100px)
- Organization profile용
- 가로형 로고
- 투명 배경 PNG

### 2. logo-square.png (512x512px)
- Repository 아바타용
- 정사각형
- 투명 배경 PNG

### 3. banner.png (1200x300px)
- GitHub banner용
- 배경 + 로고 + 슬로건
- "응급 환자를 위한 병원을, AI가 찾아드립니다"

### 4. social-card.png (1200x630px)
- SNS 공유 이미지 (Open Graph)
- 배경 + 로고 + 주요 통계
- 각 Repository Settings에 업로드

---

## 🚀 로고 업로드 방법

### 1. .github 레포에 업로드
```bash
cd .github
mkdir -p assets
cp logo.png assets/
cp logo-square.png assets/
cp banner.png assets/
cp social-card.png assets/
git add assets/
git commit -m "feat: Add logo and brand assets"
git push
```

### 2. Organization 프로필 이미지 설정
```
GitHub → Org Settings → Profile → Picture
→ logo-square.png 업로드
```

### 3. Repository Social Preview 설정
```
각 Repository → Settings → General → Social Preview
→ social-card.png 업로드
```

---

## 🎯 빠른 시작 (지금 당장!)

**시간 없으면 Placeholder 사용:**

### 현재 사용 중인 Placeholder:
```
https://via.placeholder.com/300x100/4A90E2/FFFFFF?text=404+Found
```

**나중에 실제 로고로 교체:**
1. 위 URL을 실제 로고 경로로 변경
2. `profile/README.md` 수정
3. Push

---

## 📝 체크리스트

- [ ] logo.png 제작 (300x100px)
- [ ] logo-square.png 제작 (512x512px)
- [ ] banner.png 제작 (1200x300px)
- [ ] social-card.png 제작 (1200x630px)
- [ ] .github/assets/에 업로드
- [ ] Organization 프로필 이미지 설정
- [ ] BE Repository Social Preview 설정
- [ ] FE Repository Social Preview 설정
- [ ] profile/README.md 이미지 경로 수정

---

## 💡 디자인 팁

**로고에 포함하면 좋은 요소:**
- 십자가 / 병원 아이콘
- 전화 / 통화 아이콘
- AI / 뇌 / 회로 아이콘
- 404 숫자 (크게, 눈에 띄게)
- "Found" 텍스트 (색상 강조)

**피해야 할 것:**
- 너무 복잡한 디자인 (단순하게!)
- 작은 크기에서 안 보이는 디테일
- 3개 이상의 색상 (2-3개 권장)
- 읽기 어려운 폰트

---

**급하면 일단 Placeholder로 시작하고, 나중에 교체해도 OK!** 🔥
