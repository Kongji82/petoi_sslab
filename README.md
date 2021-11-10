# Petoi Document

[https://bittle.petoi.com/](https://bittle.petoi.com/)

[https://github.com/PetoiCamp/OpenCat](https://github.com/PetoiCamp/OpenCat)

# 1. Github에서 소스 코드 clone 받기

[https://github.com/Kongji82/petoi_sslab](https://github.com/Kongji82/petoi_sslab)

# 2. 라이브러리 세팅

[https://github.com/jrowberg/i2cdevlib](https://github.com/jrowberg/i2cdevlib) 에서 파일을 다운로드 받아야 합니다.

![KakaoTalk_Photo_2021-11-04-15-13-15](https://user-images.githubusercontent.com/62738554/141056556-8ef37528-65a6-4db1-9e06-276998cc2329.png)

[https://bittle.petoi.com/4-configuration](https://bittle.petoi.com/4-configuration) 에서 4.2절 참고

# 3. NyBoard 드라이버 세팅

포트가 안 잡히는 경우가 있습니다. 그런 상황에서는 NyBoard 드라이버 세팅이 필요합니다.

<img width="862" alt="스크린샷 2021-11-04 오후 3 21 52" src="https://user-images.githubusercontent.com/62738554/141056718-9c9a1bfe-57d3-48c3-9e09-247c717c200d.png">
[https://bittle.petoi.com/4-configuration](https://bittle.petoi.com/4-configuration) 4.2.5절 참고

# 4. 실행

실행을 할 때에는 어댑터 연결 후 **OpenCat.ino** 파일을 업로드 하면 됩니다.

# 5. 동작 반복 횟수 수정

커스텀 동작은 InstinctBittle.h 파일에 주석이 포함되어 있습니다.

해당 동작을 반복시키기 위해서는 두번째 열 수정을 하면 반복 횟수를 수정할 수 있습니다.

<img width="871" alt="스크린샷 2021-11-04 오후 3 44 15" src="https://user-images.githubusercontent.com/62738554/141056928-a34af320-5a35-4d3f-b8d9-bc7ba5b93fe5.png">



→ **0번 프레임부터 8번 프레임까지 100번 반복**을 정의합니다.

[https://bittle.petoi.com/8-teach-bittle-new-skills](https://bittle.petoi.com/8-teach-bittle-new-skills) 8.2.2 참고

배열 수정하였으면, **WriteInstinct.ino** 를 실행하여 메모리에 업로드 해줘야 합니다.

WriteInstinct.ino 파일을 업로드하고, Serial Monitor를 통해 값을 입력합니다. 

**Line ending 없음**으로 설정함에 유의해야 합니다.

![KakaoTalk_Photo_2021-11-04-15-56-48](https://user-images.githubusercontent.com/62738554/141057060-6836419f-4442-48d0-b32a-c337081deced.png)
![KakaoTalk_Photo_2021-11-04-15-57-06](https://user-images.githubusercontent.com/62738554/141057062-d36ecdc4-dc2e-4745-8538-cb05d7b9fe7a.png)
![KakaoTalk_Photo_2021-11-04-15-57-28](https://user-images.githubusercontent.com/62738554/141057064-361db79b-a6d2-4e7f-9db7-4a0cb1b4e2a3.png)
![KakaoTalk_Photo_2021-11-04-15-57-52](https://user-images.githubusercontent.com/62738554/141057066-8b424437-1aff-4afc-8064-02e46651bb23.png)



위와 같은 결과가 나오면 완료된 것 입니다.

# 6. 리모콘 동작 매핑

리모콘에는 다음과 같이 동작들이 연결되어 있습니다.

ch- → rest (납작 엎드려 있기)

ch+ → gyro (자이로 센서 on/off)

➖ → 일시정지

EQ → calibrate

0번 → 걷기

1번 → 빨리 걷기

2번 → **배변**

3번 → **구토**

4번 → **다리 절뚝거리기**

5번 → **배깔고 눕고 일어나기**

6번 → **배뇨**

7번 → **음수**

8번 → 죽은 척 하기

9번 → **기침**

# 7. 기타 고려사항

### 처음 Petoi 작동 시키기

배터리의 파란색 버튼을 3초 정도 누르면 전자음과 함께 작동이 시작합니다.

### 배터리 부족 현상

전자음이 지속적으로 발생할 경우는 배터리가 부족한 상황이기 때문에 충전이 필요합니다.

다만, 충전중에는 Petoi가 동작하지 않습니다.
