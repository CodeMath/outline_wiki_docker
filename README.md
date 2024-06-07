# outline self-hosting via docker
> `outline` 위키 페이지를 docker로 구동하기


## [outline](https://www.getoutline.com/) 은 notion 과 같은 서비스 입니다.

### 1. 마크다운 및 다양한 기능
> 기본적으로 마크다운 형식과 더불어 Figma, Google(시트, 독스, 폼), Youtube, 인스타그램 등 다양한 URL을 미리볼 수 있어 편리합니다.

* 사용하기 쉽게 템플릿화 하여 문서를 정리할 수 있습니다.
* Slack 계정을 통해 인증된 사용자만 볼 수 있습니다.
* 공동 작업이 가능합니다.
* 마크다운, JSON, Notion, Confluence 등에서 데이터를 불러올 수 있습니다.
* Slack 웹훅을 통해 실시간 업데이트 현황을 추적할 수 있습니다.
* 해당 문서에 댓글을 달 수 있습니다.


### 2. 예시 파일 업로드
`docker-compse.yml`
```
outline
redis
postgres
```
위 3개 이미지를 사용하나, 실 프로덕션 상에서는 안정성 및 백업을 위해 `AWS RDS`로 전환합니다. 

환경변수 파일을 설정하기 위해, `docker.env`을 설정해줘야합니다.

자세한 환경변수 설정은 [링크](https://github.com/outline/outline/blob/main/.env.sample) 를 통해 확인하면 됩니다.

### 3. 도커 실행
```
docker compose up -d
```
