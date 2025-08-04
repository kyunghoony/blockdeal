# Blockdeal.kr MVP 더미 데이터 저장소

이 저장소는 Blockdeal.kr MVP 앱의 시각적 테스트를 위한 더미 데이터를 제공합니다.

---

## 🚀 사용 방법

1. **새로운 GitHub 저장소 생성:**  
   GitHub에서 `blockdeal-data`와 같은 이름으로 새로운 Public 저장소를 만듭니다.

2. **파일 업로드:**  
   이 저장소에 `listings.json`과 `bids.json` 파일을 업로드합니다.

3. **GitHub Pages 활성화:**
   - 저장소의 **Settings** 탭으로 이동합니다.
   - 왼쪽 메뉴에서 **Pages**를 선택합니다.
   - **Source**를 `Deploy from a branch`로 설정합니다.
   - **Branch**를 `main`(또는 기본 브랜치) 및 `/ (root)` 폴더로 설정하고 **Save**를 클릭합니다.

4. **URL 확인:**  
   잠시 후 페이지 상단에 녹색으로 "Your site is live at https://<YOUR_USERNAME>.github.io/<YOUR_REPOSITORY_NAME>/" 메시지가 표시됩니다. 이 URL을 복사합니다.

5. **데이터 URL 생성:**
   - **판매 매물 데이터 URL:**  
     `https://<YOUR_USERNAME>.github.io/<YOUR_REPOSITORY_NAME>/listings.json`
   - **구매 요청 데이터 URL:**  
     `https://<YOUR_USERNAME>.github.io/<YOUR_REPOSITORY_NAME>/bids.json`

6. **React 앱에 URL 적용:**
   - Blockdeal.kr MVP React 코드에서 `App` 컴포넌트를 찾습니다.
   - `useEffect` 훅 내부의 fetch URL을 위에서 생성한 각 데이터 URL로 교체합니다.

이제 앱은 Firestore가 아닌 GitHub에 호스팅된 JSON 파일에서 데이터를 가져와 안정적으로 화면을 표시합니다.
