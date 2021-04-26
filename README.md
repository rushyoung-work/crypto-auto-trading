# 가상화폐 자동투자 프로그램  
업비트 API 와 pyupbit 라이브러리를 사용하여 가상화폐 자동거래를 해 주는 프로그램입니다.  

## 파일구성  
+ backtesting.py : 백테스팅 코드  
+ cryptoAutoTrade_v0 : 이평선 돌파전략 코드  
+ cryptoAutoTrade_v1 : 변동성 돌파 전략 코드  

## 구동
1. 업비트에 고객센터에서 API 를 발급받은 후 access key, secret key 저장한다.
2. crypto-auto 폴더 안에 auth.py 파일을 하나 만들고 access = "본인의 access key 값" secret = "본인의 secret key 값" 을 넣고 저장한다. 이 값은 cryptoAutoTrade 코드에서 import 하여 사용된다.
3. backtesting, cryptoAutoTrade 파일 내부 변수를 원하는 변수로 바꾸어준다. coin : 투자할 가상화폐의 ticker, fees : 수수료, day_count : 백테스팅 시 불러올 데이터의 수
4. 필요한 모듈 다운로드
    + pip3 install pyupbit
    + pip3 install openpyxl
    + ...
5. 실행

## 백그라운드 실행
+ 한국 기준으로 서버시간 설정 : sudo ln -sf /usr/share/zoneinfo/Asia/Seoul /etc/localtime  
+ 백그라운드 실행 : nohup python3 bitcoinAutoTrade.py > output.log &  
+ 프로세스 확인 : ps -ef | grep .py  
+ 프로세스 종료 : kill -9 PID  (PID 는 ps 명령의 출력값에서 해당 프로세스의 맨 앞의 숫자)  

## 개발 과정 포스팅
+ 업비트 API : https://poalim.tistory.com/27  
+ 알고리즘 및 백테스팅 : https://poalim.tistory.com/29
