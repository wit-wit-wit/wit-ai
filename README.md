## < 학습 및 inference를 모두 진행할 시 >
1. https://pytorch.org/get-started/locally/ 에서 pytorch 설치 (2.3.0 cpu 버전)     ==> pip install torch==2.3.0 torchvision==0.18.0
2. requirements 설치                                                              ==> pip install -r requirements.txt

## < Inference만 진행할 시 >
1. https://pytorch.org/get-started/locally/ 에서 pytorch 설치 (2.3.0 cpu 버전)     ==> pip install torch==2.3.0 torchvision==0.18.0
2. inference_only_requirements 설치                                               ==> pip install -r inference_only_requirements.txt

# 사용
- image_search.py 의 함수 image_search를 호출하면 유사도가 높은 장소 top-k개를 return
- 함수 image_search 매개변수 설명
  - base64_string: base64 형식의 이미지
  - keyword: keyword 정보 (해당하는 것은 1, 아닌것은 0으로 표시) ex)[0, 1, 0, 1, 1, ..., 1]
  - top_k: 얻고자하는 유사도가 높은 장소 갯수, top_k=10이면 유사도가 높은 순으로 1~10위의 장소를 선택함.
