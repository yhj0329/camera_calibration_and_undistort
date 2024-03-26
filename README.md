# camera_calibration_and_undistort
OpenCV를 이용해서 카메라의 영상을 Calibration하고 카메라 렌즈 왜곡을 보정하는 프로그램이다.

## camera_calibration.py
카메라의 영상을 Calibration 하는 기능이다.

#### 기능
카메라는 우리가 실제로 보는 3차원 세상을 2차원 이미지로 변환한다.  
이때 3차원의 점들이 이미지 상에서 어디에 맺히는지 기하학적으로 생각하면,  
실제 이미지는 사용된 렌즈, 렌즈와 이미지 센서와의 거리, 렌즈와 이미지 센서가 이루는 각 등  
카메라 내부의 기구적인 부분에 의해서 크게 영향을 받는 것을 알 수 있다.  
그러므로, 3차원 점들이 영상에 투영된 위치를 구하거나, 역으로 영상 좌표로부터 3차원 공간좌표를 복원할 때에는  
내부 요인을 제거해야하만 정확한 계산이 가능하다.  
이러한 내부의 매개변수(Parameter) 값을 구하는 과정을 Camera Calibration이라고 합니다.

#### 조작키
- SPACE BAR : 정지하고 꼭짓점을 보여준다
- ENTER after pause : calibration 할 이미지 선택
- ESC : 종료

#### 결과
![camera_calibration](https://github.com/yhj0329/camera_calibration_and_undistort/assets/102153681/4102c0e7-8dce-4f4e-bc24-86c278d947d0)

## distortion_correction.py
카메라의 렌즈 왜곡을 보정하는 기능이다.

#### 기능
Calibration 으로 알아낸 매개변수를 사용해 initUndistortRectifyMap로 Maping Table을 만들고 remap을 통해 카메라 렌즈의 왜곡을 보정한다.

#### 조작키
- TAB : Rectified / Original 모드 변경
- SPACE BAR : 정지
- ESC : 종료

#### 결과
https://github.com/yhj0329/camera_calibration_and_undistort/assets/102153681/2e32f764-f03b-4f22-8321-927013118da8

