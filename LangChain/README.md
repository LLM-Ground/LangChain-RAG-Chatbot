# LangChain이란

### 정의
LLM(거대 언어 모델)을 단순 Q & A를 넘어서 실제 서비스/어플리케이션에 통합할 수 있게 해주는 오픈소스 프레임워크

### 출시 시기
2022년 후반

### LangChain이 필요한 이유
> 외부 데이터와의 연결
> LangChain은 다음과 같은 다양한 데이터와 유기적으로 연결 가능
> GPT 모델만으론 불가능한 작업을 LangChain으로 가능하게 한다.

* 외부 데이터 소스나 도구
* API
* 문서
* 데이터베이스
* 사용자 입력 등

ex> 사내에서 파이썬 개발 역량이 있는 직원을 알려줘
-> GPT는 알 수 없음. 그러나 사내 DB또는 문서를 검색해서 답변가능

### 주요 기능
* RAG: 정보를 검색하고 보충하여 생성
* 에이전트 시스템: 여러 도구를 활용해 스스로 판단하고 작업 수행
* 체인 구성: 여러 단계를 연결하여 복잡한 흐름 구현 가능

### 활용 예시
* 실시간 챗봇
* 문서기반 질의 응답 시스템
* 검색 기반 요약 도구
* 내부 지식 기반 검색 서비스 등

### OpenAI API Key 발급
https://openai.com/ko-KR/index/openai-api/
회원가입 및 로그인

1. start building

2. create organization
<img width="487" height="684" alt="스크린샷 2025-08-05 오후 6 16 14" src="https://github.com/user-attachments/assets/9d4e0f6f-09c8-4381-adb3-bd7a726e7eea" />

3. api key 발급
```py
from openai import OpenAI

client = OpenAI(
  api_key={key}
)

response = client.responses.create(
  model="gpt-4o-mini",
  input="write a haiku about ai",
  store=True,
)

print(response.output_text);

```

4. credit 결제
* API를 써서 gpt와 통신을 하기위해서는 대화를 할 때마다 비용발생
* 데이터를 많이보내고 많은 데이터를 응답 받을수록 비용은 적게 발생
* 5달러면 충분
