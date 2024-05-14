# helm chart
```
helm create custom-chart # 차트 생성
helm lint custom-chart # 차트 검사
helm template custom-chart # 차트 미리보기
helm install release-name custom-chart --debug --dryrun # 가상 설치
```

## 문법
- {{ .Values }}  
  values.yaml에서 정의된 변수  
- {{ .Charts }}  
  Charts.yaml에서 정의된 변수  
- {{ .Release }}  
  배포할 때에 할당한 정보 사용  
- {{ include "service.fullname" . }}  
  _helpers.tpl에서 정의된 변수  
- {{- with .Values.port }}  
    {{- toYaml .Values.resources }}  
  {{- end }}  
  with은 스코프 정의, toYaml은 변수를 yaml 형식으로 변경  
