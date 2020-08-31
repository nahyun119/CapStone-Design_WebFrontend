# 2020-1 Capstone Design 방구석 수집가 WEB
![image](https://user-images.githubusercontent.com/52439497/91727985-6e5b5300-ebdd-11ea-85a6-fd182a2924ef.png)

AI 학습을 위한 데이터 수집 및 가공 플랫폼인 방구석 수집가의 web frontend 코드입니다.       
방구석 수집가를 web 환경에서 작업을 의뢰하거나 작업을 진행할 때 필요한 소스코드입니다.       
의뢰자는 방구석 수집가를 통해 쉽게 데이터 수집 및 가공을 복잡한 절차 없이 의뢰할 수 있으며, 플랫폼에서 자동으로 이루어지는 교차검증을 통해 기존의 데이터 수집 및 가공 플랫폼보다 더 고품질의 데이터를 제공받을 수 있습니다.       
교차 검증은 작업자가 분류 작업을 진행하면서 검증 작업이라는 것을 인지하지 않고 이루어집니다.       
또한 교차 검증은 한 문제 세트 당 5명의 작업자(검수자)가 참여하고, 작업자의 등급은 상 상 중 중 하 로 구성됩니다.      
다양한 등급의 작업자가 참여하기 때문에 하 등급의 작업자가 오답을 해도 상 또는 중 등급의 작업자가 작업을 하여 올바르게 검수한다면 자동으로 하 등급의 작업 결과를 올바른 답으로 분류할 수 있습니다.         

작업자는 방구석 수집가를 통해 의뢰자가 의뢰한 수집 및 라벨링 작업을 진행할 수 있습니다.      
방구석 수집가는 안드로이드 기반의 휴대폰을 이용하여 이미지 수집 또는 음성 수집, 텍스트 수집 등 작업을 시간과 장소에 구애받지 않고 진행할 수 있습니다.    
또한 방구석 수집가는 앱 뿐만 아니라 웹으로도 제공을 하기 때문에 작업자는 자신이 편리한 환경에서 작업을 진행할 수 있습니다.     
수집 작업은 이미지 수집, 음성 수집, 텍스트 수집이 존재합니다.     
라벨링 작업은 이미지, 음성, 텍스트를 주어진 라벨에 맞게 분류하는 분류 작업과 이미지에 주어진 라벨에 맞는 사물 혹은 인물을 바운딩 박스를 그리는 이미지 바운딩 박스 작업이 존재합니다.      
    
## 방구석 수집가 구성도
### 방구석 수집가 SW 구성
![image](https://user-images.githubusercontent.com/52439497/91727886-479d1c80-ebdd-11ea-9a83-cf14135b34cd.png)

### 방구석 수집가 SW 컴포넌트 구성
![image](https://user-images.githubusercontent.com/52439497/91727876-42d86880-ebdd-11ea-8ac4-a39c7983bee3.png)


## 방구석 수집가 화면 

#### 1. 홈 화면
![image](https://user-images.githubusercontent.com/52439497/91726407-23404080-ebdb-11ea-8239-1c83a2b36a19.png)

#### 2. 로그인 화면
![image](https://user-images.githubusercontent.com/52439497/91726486-4834b380-ebdb-11ea-9c08-d836a78a4fd4.png)


#### 3. 회원가입 화면
![image](https://user-images.githubusercontent.com/52439497/91726501-4ec32b00-ebdb-11ea-800e-8674f5f6c36d.png)


#### 4. 오픈 뱅킹 계좌 등록 화면
오픈 뱅킹 api를 이용하여 계좌 등록을 구현하였다.      
![image](https://user-images.githubusercontent.com/52439497/91726518-584c9300-ebdb-11ea-9620-d882b39ecfb2.png)


#### 5. 마이페이지 & 개인 정보 수정 화면
![image](https://user-images.githubusercontent.com/52439497/91726533-63072800-ebdb-11ea-8284-18026bf91470.png)
![image](https://user-images.githubusercontent.com/52439497/91726543-68647280-ebdb-11ea-9b95-f9be0c99abf9.png)

#### 6. 수집 작업 의뢰
![image](https://user-images.githubusercontent.com/52439497/91726571-731f0780-ebdb-11ea-8457-5980ef9ed29f.png)

#### 7. 라벨링 작업 의뢰
![image](https://user-images.githubusercontent.com/52439497/91726588-7ca86f80-ebdb-11ea-97ca-86692678cb54.png)

#### 8. 작업 검색
![image](https://user-images.githubusercontent.com/52439497/91726623-8a5df500-ebdb-11ea-9692-6db17b2a89aa.png)

#### 9. 작업 시작(개인정보이용동의)
![image](https://user-images.githubusercontent.com/52439497/91726656-947ff380-ebdb-11ea-86e5-b29b3a365d74.png)

#### 10. 이미지 수집 작업
![image](https://user-images.githubusercontent.com/52439497/91726679-9b0e6b00-ebdb-11ea-8360-203bde00f40c.png)

#### 11. 텍스트 수집 작업 
![image](https://user-images.githubusercontent.com/52439497/91726714-a497d300-ebdb-11ea-832f-37ab48e60135.png)

#### 12. 음성 수집 작업
![image](https://user-images.githubusercontent.com/52439497/91726735-acf00e00-ebdb-11ea-824c-2b3be55aebda.png)

#### 13. 분류 작업
한 문제 세트 당 5개의 문제가 주어진다.        
1문제는 작업자의 작업 능력을 판단하기 위해 검증 완료된 정확도 100%의 사용자 검증 문제가 주어진다.        
2문제는 의뢰자가 의뢰한 분류 작업 프로젝트에서 문제가 주어진다.       
해당 문제는 작업 완료 후 또 다른 작업자들에게 교차 검증 문제로 주어진다.      
또 다른 2문제는 다른 작업자들의 수집 작업 결과로 교차 검증이 이루어져야 하는 문제가 주어진다.             
여기서 교차검증이 이루어지며 상 등급 2명, 중 등급 2명, 하 등급 1명이 동일한 문제 세트에 대해 작업한다.          
각 등급의 작업자들이 작업을 모두 완료하면 교차검증이 완료 상태가 되고 데이터 검증 작업이 완료되어 데이터 라벨이 결정된다.      
이 때 작업자는 자신이 교차검증에 참여하고 있다는 사실을 모르기 때문에 데이터 편향 문제를 보다 완화시킬 수 있다.        
![image](https://user-images.githubusercontent.com/52439497/91726757-b8dbd000-ebdb-11ea-963d-624c81fb8c60.png)

#### 14. 이미지 바운딩 박스 작업
한 문제 세트 당 5개의 문제가 주어진다.      
이미지 위에 주어진 라벨에 해당하는 사물 또는 인물을 마우스로 박스를 치면 된다.       
canvas 위에 해당 이미지를 불러온 후에 canvas의 stroke method를 통해 바운딩 박스를 그린다.     
바운딩 박스는 canvas 위에 마우스가 눌린 지점을 시작점으로 하고, 마우스가 놓인 지점을 끝점으로 하여 시작점과 끝점의 x,y 좌표를 이용하여 시작 위치와 width, height를 구한다.    
이 때 canvas는 고정된 크기로 800 * 600 이고, 이미지를 불러올 때 canvas의 비율과 이미지 비율을 고려해서 불러온다.    

![image](https://user-images.githubusercontent.com/52439497/91726858-de68d980-ebdb-11ea-8ea2-28fee182a51c.png)

#### 15. 완료한 작업 목록
![image](https://user-images.githubusercontent.com/52439497/91726840-d9a42580-ebdb-11ea-9f77-e8ff7ac9b5c7.png)

#### 16. 의뢰한 작업 목록
![image](https://user-images.githubusercontent.com/52439497/91726900-eb85c880-ebdb-11ea-8122-66415c092f79.png)

#### 17. 의뢰한 작업 결과
![image](https://user-images.githubusercontent.com/52439497/91726953-f93b4e00-ebdb-11ea-99de-99f96d83d82d.png)
![image](https://user-images.githubusercontent.com/52439497/91727142-330c5480-ebdc-11ea-9850-4c4ee4c277fc.png)
![image](https://user-images.githubusercontent.com/52439497/91726971-fe989880-ebdb-11ea-9b06-13c42acdcff7.png)

#### 18. 결과물 다운로드
![image](https://user-images.githubusercontent.com/52439497/91727046-1708b300-ebdc-11ea-8f7c-83ef625da988.png)








## 프로젝트 setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
yarn serve
```

### Compiles and minifies for production
```
yarn build
```
### 실행 후 에러 수정
실행 시 음성 파일을 재생을 위한 오픈소스 라이브러리인 WaveSurfer.js에서 발생하는 에러를 수정해야합니다.         
npm install 이후 생성된 node_modules/wavesurfer.js/src/plugin/timeline.js를 프로젝트 최상단에 있는 timeline.js로 변경하면 됩니다.                 

### 오픈 소스 
[Configuration Reference](https://cli.vuejs.org/config/).      
[WaveSurfer.js](https://wavesurfer-js.org/).        
[Vue Audio Recorder](https://github.com/grishkovelli/vue-audio-recorder).          
[Canvas](https://developer.mozilla.org/ko/docs/Web/HTML/Canvas).         
[Draw on Canvas](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Drawing_graphics).         
[Sha256](https://nodei.co/npm/js-sha256/).          
[Vue phone number Input](https://www.npmjs.com/package/vue-phone-number-input).           
