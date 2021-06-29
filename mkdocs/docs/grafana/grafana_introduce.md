### 인스턴스 생성

### Grafana 초기 설정

### Plug-in 설치

- worldping : (전세계에서 Ping 응답 속도 확인)
- Image-renderer : (Slack 알람 시, 이미지 포함)
- worldmap-panel : 월드맵 상에서 데이터를 점으로 표현. Elasticsearch, GeoHash Data를 사용 할 수 있음
- alexanderzobnin-zabbix-app : zabbix 연동을 위한 plugin

```
sudo grafana-cli plugins install raintank-worldping-app

sudo grafana-cli plugins install grafana-image-renderer

sudo grafana-cli plugins install grafana-worldmap-panel

sudo grafana-cli plugins install alexanderzobnin-zabbix-app
```


- 플러그인 설치 리스트 확인
```
grafana-cli plugins ls
sudo service grafana-server restart
```

![image-20200520112732620](../img/grafana/grafana-01.png)



### WorldPing 설정

![grafana-01-1](../img/grafana/grafana-01-1.png)


![image-20200520164255470](../img/grafana/grafana-02.png)


Plug-In 중 worldPing 선택



![image-20200520164255470](../img/grafana/grafana-02.png)



![image-20200520164339690](../img/grafana/grafana-03.png)

End Point 입력
![image-20200520164339690](../img/grafana/grafana-03-1.png)




![image-20200520164536737](../img/grafana/grafana-04.png)





![image-20200520164619489](../img/grafana/grafana-05.png)



![image-20200520164750423](../img/grafana/grafana-06.png)





