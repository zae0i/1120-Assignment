# 1120-Assignment
Grant 4가지 인증 방식이 적용되는 사례 각각 1개 이상(총 4개) 찾기

1. Authorization Code Grant(권한 부여 승인 코드 방식)<br/>
   •사용처: Google, Facebook, Twitter 로그인을 통한 SSO(Single Sign-On)<br/>
   •이유:<br/>
   a) 높은 보안성: Google OAuth 로그인은 사용자의 Google 계정 ID와 비밀번호를 클라이언트 애플리케이션에 노출하지 않는다. 이를 통해 보안 리스크가 줄일 수 있다.<br/>
   b) 확장성과 환경 지원: Google OAuth는 클라이언트 애플리케이션이 인증 서버와 통신할 수 있는 모든 환경에서 사용 가능하도록 설계되었기 때문에 동일한 인증 방식을 여러 디바이스 및 플랫폼에서 일관되게 사용할 수 있다.<br/>
   
2. Implicit Grant(암묵적 승인 방식)<br/>
   •사용처:  Angular, React, Vue.js와 같은 프론트엔드 SPA에서 사용자 인증<br/>
   •이유:<br/>
   a) 서버 없는 구조: SPA는 자체적으로 서버를 가지지 않으므로, 인증 서버와 직접 통신할 수 있는 방식이 필요하다. Implicit Grant는 클라이언트와 인증 서버 간의 직접 통신을 허용하여 서버 없는 환경에 적합하다.<br/>
   b) 빠른 액세스 토큰 발급: SPA는 사용자 경험(UX)이 중요한 애플리케이션으로, 로그인 후 API 호출까지의 지연 시간을 최소화해야 한다. 승인 코드 방식은 추가 네트워크 요청(토큰 교환)이 필요해 SPA의 빠른 동작 요구에 부담이 된다.<br/>

3. Resource Owner Password Credentials Grant(자원 소유자 자격증명 승인 방식)<br/>
   •사용처: 사내에서만 사용되는 포털 시스템, 인트라넷 앱.<br/>
   •이유:<br/>
   a)내부 애플리케이션 특화: 사내 네트워크는 외부 접근이 제한되며, 트래픽은 내부 방화벽 및 보안 정책으로 보호된다. Resource Owner Password Credentials Grant는 인증 요청 및 자격 증명 전송이 폐쇄된 네트워크 환경 내에서 이루어지므로 보안 리스크가 낮다.또한 기업은 자체 보안 솔루션으로 추가적인 보호 조치를 제공할 수 있다.<br/>
4. Client Credentials Grant (클라이언트 자격증명 승인 방식)<br/>
   •사용처: Stripe, PayPal 등 결제 서비스 API<br/>
   •이유:<br/>
   a) 사용자 없이 동작하는 자동화 작업: 결제 서비스 API는 백엔드에서 자동화된 작업(ex. 주기적으로 결제 내역 확인, 구독 상태 확인, 자동 환불 요청)을 처리하는 데 자주 사용된다. Client Credentials Grant (클라이언트 자격증명 승인 방식)는 서버 간 통신만 필요하고, 사용자 인증(예: 비밀번호, 리다이렉트 등)을 요구하지 않으므로 효율적이다.
