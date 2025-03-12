# Project llan

large language model, vector databaes, prompt engineering 을 이용한 AI 플래너


### Tech Stack

- supabase service for `auth` `database (postgresql)`
- langgraph library for `prompt engineering`
- Llama3
- svelteKit framework for `web design`
- python3


### WHY

- 기존의 플래너의 하나하나 시간을 정하고, 날짜를 지정해 추가를 해야했던 번거로움을 해결하고 쉽게 일정을 추가하고 삭제, 조회하고자
- 이러한 프로젝트를 기획하게 되었습니다.
- 큰 리소스가 필요한 튜닝 대신 langgraph 라는 라이브러리를 통해 llm을 원하는대로 동작하는게 매우 매력적이여서 시작하게 되었습니다.





### **LOGIC**

<img width="198" alt="image" src="https://github.com/user-attachments/assets/e8c2c499-7a7b-477b-98d4-74bbb6b79ad7" />

<br>
<br>

먼저 postgresql 에서 vector plugin을 통해 쉽게 벡터 데이터 베이스를 이용할 수 있었습니다. 
유저를 구분하기 위해 id칼럼을 추가하였고 이를 통해 클라우드 시스템까지 함께 구현할수 있었습니다.

유저가 client side에서 api로 요청을 보내면 python에서는 Langgraph를 통해 적절한 요청을 수행 (플랜 조회, 삭제, 수정, 업데이트)을 수행합니다.
수행한 목록을 사용한 tool 리스트와 함께 반환함으로서 llm이 어떤 도구를 사용해 작업을 진행했는지 유저가 알수 있도록 하였습니다.





### 고찰.
영상 녹화시에는 몰랐는데 메시지 기록 전체를 계속 추가해버려서 같은 대화가 반복적으로 올라가는 현상이 있습니다. 참고해주세요..


### TODO

2025.03.12 플래너 기능 외에 여러 기능을 추가하여 서비스를 목표로 보다 확장 가능한 로직으로 서비스 제작중에 있습니다. 



https://github.com/user-attachments/assets/a3135af7-9417-4a50-a684-49e6b3de512b

