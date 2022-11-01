# 이미지에서 균열 추출하기.

## 케글 대회
   Surface Crack Detection [바로가기](https://www.kaggle.com/datasets/arunrk7/surface-crack-detection)

* 참고코드
1. 한국어 설명, 코드가 짧음. 정확도만을 판단하는데 의미를 두고 먼저 분석할 것임.
[바로가기](https://www.kaggle.com/code/song3song/smc-detection-of-surface-crack-feat-cnn)

<2022. 10. 15 돌려몸. 일반적인 코딩을 조금 이해함.>

2. 한국어 설명. 이해하는데 큰 도움 될 것임
[바로가기](https://www.kaggle.com/code/formeforu/team-4-cnn-for-concrete-crack-image)

<2022. 10. 16 돌려보기 시작> 

3. 한국어 설명, 학습할 이미지처리에 대해 자세한 설명이 있음.
[바로가기](https://www.kaggle.com/code/formeforu/smarcle-w3-concrete-crack-image)

4. 모델을 저장하는 방법이 기술되어 있다. 꺼내쓰기까지는 구현하지 않음.
[바로가기](https://www.kaggle.com/code/jiyajiwon/surface-crack-detection-using-cnn#Model-1:-Inception-V3)

5. 모델을 저장하고 그것을 평가하는 방법까지 구현.
[바로가기](https://www.kaggle.com/code/kutaykutlu/99-9-acc-resnet50-inceptionv3-vgg16)&nbsp; 
<br>

* 작업사항
1. 내가 가진 이미지에서 "균열" "균열아님" 폴더에 이미지를 500개씩 넣는다.

 --> 작업중, 균열이 있는 이미지는 넘쳐나는데, 균열이 없는 이미지는 찾기 어려웠다.(2022.10.16)
 
 --> 앞으로 작업시 한 구조물에서 손상이 없는 사진을 찍어야 한다. 
 
 --> 사진을 찍을때 주의점을 선생님께 여쭙는다. -(화소가 같아야 하는지. 거리가 같아야 하는지. 등)<br>
   답 : 10/18 : 화소가 같아야 한다. 이미지의 화소를 같게 할 수 있는 파이썬 코딩을 찾아야 한다. 나의 이미지는 4:3 이고, 학습한 이미지는 1:1이다. 비율도 수정해야 한다.
 
2. 카메라로 찍은 사진을 분석한다.

 --> 내 사진을 불러와서 비교하는 코딩을 모른다.(2022.10.17)--> 선생님께 질문해서 코딩을 얻어온다.
 
3. 분석한 색의 백터 이미지를 얻을 수 있는 코딩을 얻는다.
<br>

* 찾아서 구현해야 할 사항
1. 내가 가진 한 장의 이미지를 분석해서 균열인지 아닌지 만드는 코드 <br>
2. 이미지를 같은 코드로 줄여주는 코드(파이썬) <br>
 2.1. 내가 가진 이미지 500장 추려낼 것. <br>
 2.2. 집어넣을 이미지 선택, 균열인지 아닌지 판단할 것.<br>
   20221019 비슷한 코딩 발견[바로가기](https://hyjykelly.tistory.com/m/20)<br>
   20221028 다중 이미지 분석 [바로가기](https://zeuskwon-ds.tistory.com/49)
   20221028 이미지 크기 확인 [바로가기](https://ponyozzang.tistory.com/596)
<br>

* 날짜별 진행상황<br>
10/17~18 : 케글에서 내 컴퓨터의 램이 부족하여 마지막 문장이 돌아가지 않는다. 램을 구입했고, 장착하는 대로 새로 작성하자.
[바로가기](https://www.kaggle.com/code/kimhyunoh/20221017/edit)<br>
10/19 : 램을 장착하여 02. 를 돌렸으나 램이 부족하여 멈추었다. "ACCELERATOR"를 'GPU' 에서 'NONE'으로 바꿔 돌려보고 있다. 속도는 느리지만 돌아는 가고 있다.
        RAM과 CPU가 거의 풀로 올로가 있어서 중간에 멈출 가능성이 클 것 같다.<br>
        내일 날이 밝아 코딩을 시작한다면, 주피터 노트북의 힘을 빌려 돌려봐야 할 것 같고, 판다스에서도 돌려서 웹상에 올려보는 것도 재미있겠다.<br>
<br>
오늘<br>
1. 500장씩 선별하여 가장 빠르게 돌아간 모델로 돌림.<br>
2. 돌린 녀석을 밖으로 빼내는 것을 해봄<br>
3. 이미지를 멀쩡한거 1장, 균열간거 1장을 만듦<br>
4. 블로그에 있는 판별한 코딩을 가져와서 판별까지 해봄

