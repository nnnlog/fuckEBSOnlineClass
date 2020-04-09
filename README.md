# fuckEBSOnlineClass
EBS 온라인 클래스 진도율 주작치기

### 사용법
<img src="/images/photo_2020-04-10_00-20-36.jpg">
수강 완료하고 싶은 강의에 들어간다.<br><br>
F12 또는 Ctrl+Shift+I를 눌러서, 개발자 도구를 실행한다.<br>
Console 탭으로 이동한 후 아래 코드를 복붙한다.

```js
var postData = {};
postData.atnlcNo = $("#atnlcNo").val();
postData.lctreSn = $("#lctreSn").val();
postData.stepSn = $("#stepSn").val();
postData.lctreSeCode = $("#lctreSeCode").val();
postData.cntntsTyCode = $("#cntntsTyCode").val();
postData.revivTime = revivTime;
postData.lrnTime = revivTime;
$.post('/mypage/userlrn/lctreLrnSave.do', postData)
```
<img src="/images/photo_2020-04-10_00-20-37.jpg">
위처럼 아무런 오류 메세지가 없으면 된 것이다.