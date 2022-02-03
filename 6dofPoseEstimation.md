# [6-dof pose estimation] 3D pose estimation! 종류 구별하기 가이드라인 만들기

```
본 글은 여러 논문의 Related work를 추려서 정리하고 분류하는 것을 목표로 하였습니다. 개인적인 생각과 직역, 오역이 있을 수 있으니 오류가 난 부분이 있다면 댓글 부탁드립니다. 참고시 출처 기입 부탁드립니다.
```
## 6 dof pose estimation이란?
- 물체의 공간상의 정보를 표현하는 것을 말한다 6 dof (degrees of freedom) 물체의 자유도를 뜻하고 , 물체가 어떤 기준 좌표계 ( 카메라, 로봇, 가상현실 좌표계) 등으로 부터 어디에 어떻게 위치해 있는가를 추정하는 것이다.

## Method 들을 구별해보자 각 논문의 Related work를 통하여
### PoseCNN
- Templete-based : 강체가 구성되어 있고, 이미지 위에서 강체를 찾는 방식 각 위치에서 similarity score를 계산하여 객체의 자세를 추정하는 방식이다. texture-less object detecting 시 유용하지만, 잘려지거나 가려진 객체를 추정하는 것에 오류가 많다. ( 이미지에서 template matching 과 유사한 방식이라 이해했다. 여기서 texture less란? 3차원 객체의 표면 정보를 뜻하며 UV map과 같은 것으로 표현한 것인데 이게 less 된 object detecting이란 말은 3차원 물체의 texture정보를 사용하지 않는다는 의미이다.)
- Feature-based : 관심영역 혹은 전 픽셀에서 local feature를 추출하여 3d model과 matching 하는 방식이다. occulsion(가려진)을 다루는 것이 가능하지만 물체에 충분한 texture 정보가 필요하다
- PoseCNN은 두 강점을 결합하였다.

### PVnet
- Holistic method
- Keypoint-based method
- Dense methods
- PVnet 은 Keypoint-based + Dense

### DPOD
- Deep learning 6D pose detector
- Deep learning 6D pose refiners

### EfficientPose(2020) 
- Direct estimation of the 6D pose
- 2D Detection and PnP
- 2D Object detection(?) 이건 그냥 여기서 사용되어져서 추가 한듯 싶다 
- 

### SO-Pose(2021)
- 전통적인 basic structure of baseline methods 2D-3D point Matching 기법에서 Self-occlusion information을 더한 것이다.


### GRD-net(CVPR2021)
