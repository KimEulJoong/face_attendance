# face_attendance

## 아키텍처 및 다이어그램
  <img src = "./images/시스템 아키텍쳐.png"><img>

## 사용 시나리오
  <img src = "./images/사용 시나리오.png"><img>


## 구현 기능 및 알고리즘 : 3가지 기능으로 시스템 동작
- 얼굴 인식 (RetinaFace) : 얼굴의 위치 5가지 (양 눈의 중심점, 코 끝, 두 입꼬리)
- 특징 추출 (FaceNet) : 128차원 임베딩 벡터를 직접적으로 학습
  - triplet loss 함수 사용 (첫번째와 두번째 임베딩 벡터 사이 거리는 가깝게, 첫번째와 세번째 임베딩 벡터 사이 거리는 멀게 학습)
  - deep convolution network (합성공 신경망 CNN)
  <img src = "./images/FaceNet.png"><img>
 
## 작동 방식
1. 로그인 (Secure hash Algorithm)
2. 강의 추가 (이름 학번 추가 > DB Course 테이블에 교수id추가 > Coures_student 테이블에 학생 id, 강의 id 추가 > attendance_check 테이블에 강의 id, 학생id 추가하여 15주에 해당하는 출석 여부 생성)
3. 강의 목록
4. 출석표 (출력)
5. 출석확인
