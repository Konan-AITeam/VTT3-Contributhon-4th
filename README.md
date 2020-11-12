# VTT3-Contributhon-4th

VTT 3세부에서 수행하는 주 업무인 Metadata 생성에 대한 주제로 컨트리뷰톤 개최

- 대회 주제 : 효율적인 Metadata JSON 구조 설계
- 대회 일시 : 2020년 11월 09일 09:00 ~ 2020년 11월 13일 14:00
- 참가 방법 : 주어진 예시 Metadata JSON 파일을 제안하는 Metadata JSON 구조로 변환 후, Github의 [repository](https://github.com/Konan-AITeam/VTT3-Contributhon-4th)에 `Pull requests` 또는 `Push`

- 시상식 및 결과 발표
  - 일시 : 2020년 11월 13일 14:00
  - 장소 : [Zoom](https://zoom.us/j/95285782221?pwd=VVNtTXVlU094UkhlR1VZR0I3eURBdz09) 또는 강남역 모임플러스 강의실3

## 컨트리뷰톤 진행 내용

- 제출 경로
  - `submit` 폴더에 `'소속'_'이름'_'버전'.json` 으로 업로드 (ex: ./submit/코난_강은철_v.1.0.json)

- 설계 범위
  - 4가지 종류의 JSON 구조를 최소 1개 이상의 JSON 구조를 재설계

- 예시 Metadata JSON 설명 - 주요 Key 설명
  - visual_results : 시각 정보
  ``` json
    "st": "00:02:41.454", # 발화 시작 시간
    "et": "00:02:42.994", # 발화 종료 시간
    "speaker": "Dokyung", # 발화자
    "utter": "Okay, cut." # 발화 내용
  ```
  - script : 자막 정보
  ``` json
    "st": "00:02:41.454", # 발화 시작 시간
    "et": "00:02:42.994", # 발화 종료 시간
    "speaker": "Dokyung", # 발화자
    "utter": "Okay, cut." # 발화 내용
  ```
  - sound_results : 소리 정보
  ``` json
    "start_time": "00:00:00.347", # 소리 시작 시간
    "end_time": "00:00:30.83", # 소리 종료 시간
    "sound_type": "background_music" # 소리 종류
  ```
  - qa_results : QnA 및 묘사
  ``` json
    "videoType": "scene", # 비디오 종류(scene, shot)
    "description": "Haeyoung1 is walking. Haeyoung1 is crying sadly. Haeyoung1 is wearing a coat.", # 묘사
    "qid": 9135, # id
    "qa_level": 3, # QnA 난이도
    "q_level_mem": 3,
    "q_level_logic": 3,
    "que": "How does Haeyoung1 feel?", # 질문
    "true_ans": "Haeyoung1 is so sad.", # 정답
    "false_ans": [
      "Haeyoung1 feels so happy.", # 오답 1
      "Haeyoung1 looks so satisfied.", # 오답 2
      "Haeyoung1 is so excited.", # 오답 3
      "Haeyoung1 feels so thrilled." # 오답 4
    ]
  ```
