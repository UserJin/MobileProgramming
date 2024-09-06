# MobileProgramming

## 1. :file_folder: 프로젝트 소개
> "모바일 프로그래밍"과목 팀프로젝트를 위해 개발한 가계부 관리 어플리케이션입니다.


![image1](https://github.com/user-attachments/assets/d13faddf-0a0e-4483-9922-ca7ce7ff44d0)
![image7](https://github.com/user-attachments/assets/8b327cdb-5af7-4fe5-9917-9635784391ee)


</br></br>

## 2. :calendar: 개발 기간 및 인원
* 전체 개발 기간: 2022-05-26 ~ 2022-06-10
* 개발 인원: 4명
* 담당 역할: Firebase Realtime Database를 통한 데이터 저장 및 문자메세지 자동 인식 기능
</br></br>

## 3. :house_with_garden: 개발 환경
* 개발 툴 - Android Studio Chipmunk | 2021.2.1 Patch 1
* 사용 언어 - Kotlin
* 대상 기기 - Android(Pixel 2 API 30)
* 데이터 베이스 - Firebase Realtime Database
</br></br>

## 4. :page_facing_up: 구현 사항 설명
*  데이터 구조
    * 크게 AutoAsscendingKey, Record, Budget으로 구분
    * AutoAsscendingKey은 Record에 사용되는 키를 의미하며, 기록 될 때마다 값을 증가시켜 중복키 문제를 예방함
    * Record는 지출(expenses)과 수입(income)으로 구분되며, 둘의 차이는 카테고리(rcategory)의 존재 유무
    * Budget은 각 월의 예산정보를 담는 데이터로 연월을 key로, 예산을 value로 갖는다.

* 화면 구조
    * 메인화면은 프래그먼트와 뷰페이저를 통해 예산, 기록, 챌린지 탭으로 구성됨
    * '예산'에서는 각 버튼을 통해 예산 설정, 지출 및 수입 기록 액티비티로 intent를 보내 이동
    * '기록'에서는 프래그먼트를 이용해 당월의 지출 및 수입 내역을 분리하여 원형차트와 리스트로 출력
    * '챌린지'에서는 캘린더를 표시하며, 각 날짜를 눌러 해당 날짜의 챌린지 달성 여부 및 지출 내역을 출력
</br></br>

## 5. :thought_balloon: 개선 사항 및 프로젝트 후기
* 포인트 적립 제도를 구현하여 사용자의 꾸준한 참여를 유도 가능
* 현재로서는 단순히 한명의 사용자만을 고려하여 구성되어 있으나, 이후 회원 제도를 도입한다면 각 회원의 정보를 담을 수 있는 데이터 구조를 설계해야 하고 이에 따라 기존 데이터 구조도 수정할 필요가 있음
