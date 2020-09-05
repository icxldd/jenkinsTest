# Jenkins Docker (Docker in Docker, docker-compose)

## how to use
### Preparations
docker-compose 를 이용하기 위해서 다운 받아야 된다. 
```
curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)"
```
컨테이너 안에서 다운 받으면 너무 느리기 때문에 미리 다운받은 후 mount, link 시키도록 하자.

### Build
```
docker-compose build --no-cache --pull
```
- --no-cache : 빌드 내용을 캐싱 하지 않겠다는 것이다.
- --pull : 이미지 밀어 넣어버리기

### Run
```
docker-compose run -d
```
- -d : `--detach` 의 약자로 백그라운드로 실행하겠다는 의미이다.

### TEST
```
localhost:8200
```
port 번호는 `.env` 파일을 통해 변경할 수 있다.

### Shutdown
```
docker-compose down
```