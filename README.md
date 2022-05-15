# ESMusic (EunSeop Music)

EcmaScript 와 ESModule 을 좋아하는 ES의 음악 작업히스토리 저장 공간.

## 장비

가상악기를 사용하는 순간 악기 그 자체의 스피커의 성능은 의미가 없다. 건반이 클래식악기의 타건감을 그대로 재현했느냐 그것만 따지면 됨. 비싼 악기를 살 돈으로 오디오 인터페이스를 사고 좋은 스피커를 사면 훨씬 저렴하면서 즐겁게 음악을 즐길 수 있음.

- 악기: Roland FP10. 스피커의 원가를 절감한 대신 건반의 타건감을 최상으로 끌어올렸다. 롤랜드사 윗급 고가의 악기와 건반액션 종류가 동일하다. 가상악기를 사용하는 입장에서 정말 행운의 악기인듯..
- 오디오 인터페이스: [Focusrite Scarlett 2i2](https://focusrite.com/ko/usb-audio-interface/scarlett/scarlett-2i2). 가성비가 좋은 제품으로 전문가도 사이드로 사용하는 제품이라고 함. 원래는 솔로 제품을 사려고 했으나 스테레오 관련 이슈가 나중에 발생할 수도 있고 혹시나 내가 작곡을 하게될 수도 있어서 안정적인 제품을 선택함.
- 오인페 케이블: [Focusrite의 공식사이트](https://support.focusrite.com/hc/en-gb/articles/360007885360-Scarlett-3rd-Gen-USB-C-to-USB-C-connectivity-)를 참고하여 검증된 [ANKER usb c to c 케이블](https://smartstore.naver.com/anker/products/6031900318?NaPm=ct%3Dl35f6f0b%7Cci%3Dcheckout%7Ctr%3Dppc%7Ctrx%3D%7Chk%3Dd8e93c15367f842d9015b45d018b69f05090159e) 사용. 맥북 유저라 동봉된 c to a 케이블을 쓸 수가 없었다..
- 미디케이블: MIDI란, 노트 정보만을 송출하는 아주 단순한 데이터이기 때문에 성능을 따질 필요가 없다. 따라서 적당히 길고 고급소재이다 싶은 제품 고르면 됨. [구입 링크](https://inflow.pay.naver.com/rd?no=510819782&tr=ppc&pType=P&retUrl=https%3A%2F%2Fsmartstore.naver.com%2Fmain%2Fproducts%2F5882371174&vcode=uRdNG%2BTyddsKf%2Bh1MSzXj%2BmF0g3tI732njFSPgWUWcSpFxsxHa1RcRwHVJhfAV0ov7ilUSoYDzaPwlp%2Fa%2BrUNodS%2F3K%2Fh5GXH%2FESJhKbE%2BYHsReNIibwb5Ms85Xf2PKd)
- 헤드셋: 소니 1000xm3 노이즈캔슬링 헤드셋 사용. 모니터링 헤드폰을 살까 지름신이 잠깐 왔지만, 지금 가지고 있는거 그대로 사용하기로.. 상대음감이라 어차피 제대로 듣지도 못하는데 그정도의 전문성은 아직 필요 없다.
- 헤드셋 케이블: 기본 동봉 케이블 + 3.3 to 6.5 변환젠더 혹은 Mogami 케이블 사용 예정. 두개를 각각 비교해봐서 어떤것이 음질이 더 좋은지 결정해보자..

## 연결법

악기에서 유선 MIDI 로 맥북에 연결하는건 레이턴시가 없다. 하지만 맥북으로부터 외부 현실세계로 음악을 송출하는건 레이턴시가 발생할 수 있다. 그 이유는 미디를 바탕으로 그것에 가상악기 사운드를 입히는 작업이 매우 무거운 반면 맥북의 사운드카드의 성능이 좋지 않기 때문. 그래서 오인페를 맥북에 연결해서 오인페를 통해 현실세계로 음을 송출하도록 해야한다.

1. 악기의 MIDI를 맥북에 전송해야 한다. 악기와 맥북 사이에 MIDI 케이블을 연결한다.  "난 그냥 녹음만 하고 끝날건데?" 하면 여기까지만 하면 된다. 문제는 그 좋은 가상악기 소리를 녹음만 하지 말고 실시간으로 나도 듣고 싶다는것. 녹음 안하고 그냥 연주만 할 수도 있으니까. 그래서 오인페가 필요한 것이다.
2. 오인페와 맥북 사이에 케이블을 연결한다. 이 때 주의할 것은, 허브 없이 다이렉트로 연결해야 한다. 위에서 언급한 공식사이트에서도 허브를 통한 연결은 퍼포먼스를 보장할 수 없다고 한다.
3. 헤드셋을 오인페에 연결하면 끝

## 사용 프로그램

- DAW(Digital Audio Workstation): GarageBand, Logic Pro. 미디에 가상악기 씌우는 작업만 할거라 사용하기 간단한 거라지밴드를 쓰려고 했는데.. 기본 가상악기가 스타인웨이밖에 없다. 당분간은 로직 프로를 써서 당분간은 뵈젠도르퍼나 야마하 등의 기본 사운드를 충분히 즐기고 좀 더 즐기고 싶으면 가상악기를 그때 사도록
- 영상편집 프로그램: iMovie, Final Cut Pro. 단순 사운드 입히는 작업인데 파이널컷은 너무 오버스펙.. 당분간은 iMovie로 작업하기
