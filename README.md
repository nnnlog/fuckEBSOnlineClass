# Vulnerability of EBSOnlineClass
EBS 온라인 클래스 취약점

```js
let wait = async(ms) => new Promise(r => setTimeout(() => r(), ms));
let run = async() => {
    for (let i = Math.ceil(revivTime / 120); i > 0; i--) {
        var postData = {};
        postData.atnlcNo = $("#atnlcNo").val();
        postData.lctreSn = $("#lctreSn").val();
        postData.stepSn = $("#stepSn").val();
        postData.lctreSeCode = $("#lctreSeCode").val();
        postData.cntntsTyCode = $("#cntntsTyCode").val();
        postData.revivTime = $("#revivTime").val();
        i === 1 && (postData.endButtonYn = "Y");
        postData.lrnTime = 120;
        $.post('/mypage/userlrn/lctreLrnSave.do', postData);
        await wait(50);
    }
};
run();


```

### 분석
https://blog.naver.com/sorisem4106/221920190523

### 분석 (현재 작동안함, 이전 코드)
[https://blog.naver.com/sorisem4106/221900009549](https://blog.naver.com/sorisem4106/221900009549)
