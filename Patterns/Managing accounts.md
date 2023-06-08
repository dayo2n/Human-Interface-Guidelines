# **[Managing accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts)**

```
When it doesn’t create an unnecessary barrier to your experience, 
an account can be a convenient way for people to access their content and track personal details.
경험에 불필요한 장애물을 만들지 않을 때,
계정은 사람들이 그들의 콘텐츠에 접근하고 개인정보를 추적하는 편리한 방법이 될 수 있다.
```

<img width=800 src="https://docs-assets.developer.apple.com/published/bc6ed656b5ef4483ce1c17d7e0042ce2/patterns-managing-accounts-intro@2x.png">

핵심 기능에 계정이 필요한 경우에만 계정을 생성하도록 요청하고, 그렇지 않은 경우에는 계정 없이 앱을 즐길 수 있도록 한다. 계정이 필요한 경우 사용자가 신뢰할 수 있는 일관된 로그인 환경과 여러 계정 및 인증 방법을 기억할 필요가 없는 편리함을 제공하기 위해 [Sign in with Apple](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple)을 사용해라.

## **[Best practices](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#Best-practices)**

**Explain the benefits of creating an account and how to sign up.   
계정 생성의 이점과 가입 방법을 설명하라.**    
앱에 계정이 필요한 경우, 요구사항의 이유와 이점에 대한 간략하고 친절한 설명을 작성한다. 로그인 화면에 이 메시지를 표시한다.   

**Delay sign-in for as long as possible.   
로그인을 가능한 오래 딜레이해라.**    
사람들은 유용한 일을 하기 전에 로그인해야 할 때 종종 앱을 포기한다. 이러한 상황을 방지하려면 사람들에게 앱이나 게임에 대해 로그인을 요청하기 전에 앱이 무엇을 하는지 이해할 수 있는 기회를 제공해라. 예를 들어, 쇼핑 앱은 원하는 만큼 검색할 수 있도록 하며, 구매할 준비가 되었을 때만 로그인을 요구한다.   

**If you don’t use Sign in with Apple in your iOS, iPadOS, or macOS app, prefer using a passkey.   
iOS, iPadOS 또는 macOS 앱에서 Apple 로그인을 사용하지 않는 경우에는 암호 키를 사용하는 것을 선호한다.**   
암호는 계정 생성 및 인증을 단순화하여 사용자가 암호를 만들거나 입력할 필요가 없다. 앱이 암호를 지원할 때 사람들은 새 계정을 만들거나 기존 계정에 로그인할 때 사용자 이름을 제공하기만 하면 된다. 개발자 지침은 [Supporting passkeys](https://developer.apple.com/documentation/authenticationservices/public-private_key_authentication/supporting_passkeys)을 참조하라. 암호를 계속 사용해야 하는 경우 [Password AutoFill](https://developer.apple.com/documentation/security/password_autofill)을 사용하여 암호 및 보안 코드 정보를 자동으로 생성하고 입력한다.   

**Always identify the authentication method you offer.   
항상 제공하는 인증 방법을 식별하라.**    
예를 들어, Face ID로 앱에 로그인하기 위한 버튼을 표시하는 경우, “Sign In”과 같은 일반 문구 대신 “Sign In with Face ID”와 같은 문구를 사용해 이름을 지정한다.   

**Refer only to authentication methods that are available in the current context.   
현재 상황에서 사용할 수 있는 인증방법만 참조하라.**    
예를 들어, Face ID를 제공하지 않는 기기에서 Face ID를 참조하지 않아야 한다. 기기의 기능을 확인하고 적절한 용어를 사용해야 한다. 개발자 지침은 [LABiometryType](https://developer.apple.com/documentation/localauthentication/labiometrytype)을 참조하라.   

**In general, avoid offering an app-specific setting for opting in to biometric authentication.   
일반적으로 생체 인증을 선택하기 위한 앱별 설정을 제공하지 마라.**   
사람들은 시스템 수준에서 생체 인증을 설정하기 때문에 앱 내 설정을 제시하는 것은 중복되며 혼란스럽게 할 수 있다.   

**Avoid using the term *passcode* to refer to account authentication.   
계정 인증을 나타낼 때는 암호 passcode라는 용어를 사용하지 마라.**    
사람들은 자신의 장치를 잠금 해제하거나 애플 서비스를 인증하기 위해 암호를 만든다. 만약 본인의 인터페이스에서 그 용어를 사용한다면, 사람들은 해당 앱에서 그들의 암호를 재사용하도록 요구한다고 생각할 수 있다.   

## **[Deleting accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#Deleting-accounts)**

앱 내에서 사람들의 계정 생성을 돕는 경우, 그들의 계정 삭제 또한 도와야 하며, 단순히 비활성화를 의미하는 것이 아니다. 아래 지침을 따르는 것 외에도 계정 삭제 및 잊혀질 권리와 관련된 해당 지역의 법적 요구사항을 이해하고 준수해야 한다.   

```
Important
법적 요구사항으로 인해 앱이 계정 또는 디지털 건강 기록 등의 정보를 유지하거나 
특정 계정 삭제 프로세스를 따라야 하는 경우, 
상황을 명확하게 설명하여 사람들이 유지해야 하는 정보 또는 계정과 
따라야 하는 프로세스를 이해할 수 있도록 해야한다.
```

**Provide a clear way to initiate account deletion within your app or game.   
앱 내에서 계정 삭제를 시작할 수 있는 명확한 방법을 제공하라.**    
앱 내에서 계정 삭제를 수행할 수 없는 경우 사용자가 수행할 수 있는 웹 페이지에 대한 직접적인 링크를 제공해야 한다. 해당 링크는 쉽게 검색할 수 있도록 한다. 예를 들어, 개인정보 보호 정책 또는 서비스 약관 페이지에 링크를 숨기지 않도록 한다.   

```
Developer note
사람들이 Sign in with Apple을 사용해 앱 내에 계정을 만든 경우,
사용자가 계정을 삭제할 때 관련 토큰을 취소한다.
Revoke tokens(https://developer.apple.com/documentation/sign_in_with_apple/revoke_tokens)를 참조하라
```

**Provide a consistent account-deletion experience whether people perform it within your app or game or on the website.   
사용자가 앱 또는 웹 어디서 수행하든 상관없이 일관된 계정 삭제 환경을 제공하라.**    
예를 들어, 한 버전의 삭제 흐름이 다른 버전보다 길거나 복잡해지지 않아야 한다.   

**Consider letting people schedule account deletion to occur in the future.   
사람들이 나중에 계정 삭제를 예약할 수 있도록 하라.**    
사람들은 그들의 계정을 삭제하기 전에 그들의 남은 서비스를 사용하거나 구독 자동 뉴스가 나올 때까지 기다릴 수 있는 기회를 감사하게 생각할 수 있다. 계정 삭제를 예약할 수 있는 방법을 제공하는 경우, 즉시 삭제할 수 있는 옵션도 제공해야 한다.   

**Tell people when account deletion will complete, and notify them when it’s finished.   
계정 삭제가 언제 완료되는지 사람들에게 알려주고, 완료되면 알려라.**    
계정을 완전히 삭제하는 데 시간이 걸릴 수 있기 때문에, 사람들이 무엇을 기대해야 하는지 알 수 있도록 삭제 프로세스의 상태에 대해 계속해서 알려주는 것이 중요하다.   

**If you support in-app purchases, help people understand how billing and cancellation work when they delete their account.   
앱 내 구매를 지원하는 경우, 사용자가 계정을 삭제할 때 청구 및 취소가 어떻게 작동하는지 이해할 수 있도록 도와라.**    
예를 들어, 다음과 같은 시나리오를 이해할 수 있도록 도와야 한다.   

- 자동 갱신형 구독에 대한 청구는 계정 삭제 여부와 관계없이 구독을 취소할 때까지 Apple을 통해 계속 된다.   
- 그들이 계정을 삭제한 후, 사람들은 그들의 구독을 취소하거나 환불을 요청해야 한다.   

사용자가 이러한 시나리오를 이해하는 데 도움이 될 뿐만 아니라, 구독을 취소하고 구매를 관리하는 방법을 설명하는 정보를 제공하라. 자세한 내용은 [Helping people manage their subscriptions](https://developer.apple.com/design/human-interface-guidelines/in-app-purchase#Helping-people-manage-their-subscriptions)과 [Providing help with in-app purchases](https://developer.apple.com/design/human-interface-guidelines/in-app-purchase#Providing-help-with-in-app-purchases)를 참조.   

```
Note
Even if people didn’t use your app to purchase the subscription, 
you still need to support account deletion.
사람들이 구독을 구입하기 위해 앱을 사용한 것이 아니더라도,
여전히 계정 삭제를 지원해야 한다.
```

## **[TV provider accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#TV-provider-accounts)**

많은 인기 TV 제공업체는 시스템 수준에서 사람들이 자신의 계정에 로그인할 수 있도록 하여 앱별로 인증할 필요가 없다. TV 공급자 앱에서 사용자 로그인이 필요한 경우, TV Provide Authentication을 사용하여 가장 효율적인 온보딩 경험을 제공해야 한다.   

**Avoid displaying a sign-out option when people are signed in at the system level.   
사용자가 시스템 수준에서 로그인할 때 로그아웃 옵션을 표시하지 않도록 한다.**    
만약 앱의 로그아웃 옵션을 포함해야 한다면, 사람들이 그들의 계정에서 로그아웃하기 위해 Settings > TV provider로 이동하도록 프롬프트를 표시해야 한다.   

**Never instruct people to sign out by adjusting privacy controls.   
개인정보 보호 제어를 조정해 로그아웃하도록 사람들에게 지시하지 마라.**    
TV provider가 Settings > Privacy에서 제어하는 것은 로그아웃 메커니즘이 아니다. 이러한 설정은 사용자가 TV provier 계정에 애개세스할 수 있는 앱을 관리하는 데 도움이 된다.   

## **[Platform considerations](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#Platform-considerations)**

*iOS, iPadOS, 또는 macOS에서 추가로 고려할 사항은 없다.*   

### **[tvOS](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#tvOS)**

대부분의 사람들은 키보드가 아닌 리모컨을 사용해 Apple TV와 상호작용하므로 필요한 최소한의 정보를 요청하라.   

**Prefer letting people use another device to sign up or authenticate.   
사람들이 가입하거나 인증하기 위해 다른 장치를 사용하도록 허용하는 것을 선호한다.**    
앱의 연결된 도메인을 구성하면 Apple TV가 다른 장치와 함께 작동하여 [Sign in with Apple](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple)을 포함한 로그인 credentials를 안전하게 제안할 수 있다. 개발자 지침은 [Configuring an associated domain](https://developer.apple.com/documentation/Xcode/configuring-an-associated-domain)를 참조.    

**When people are signed in to a shared account, avoid asking them to choose their profile every time they become the current user.   
사용자가 공유 계정에 로그인할 때 현재 사용자가 될 때마다 프로필을 선택하라는 요청을 피하라.**    
tvOS 16 이상에서는 앱이 모든 사용자와 credential을 공유하면서 각 개인의 프로필과 사용자 데이터를 별도로 저장할 수 있다. 이러한 유형의 공유를 지원하는 경우, 앱은 각 사용자에게 공유 계정에 개별적으로 로그인하도록 요청하지 않고 현재 사용자의 프로필을 자동으로 사용할 수 있다. 개발자 지침은[kSecUseUserIndependentKeychain](https://developer.apple.com/documentation/security/ksecuseuserindependentkeychain)과 [User Management Entitlement](https://developer.apple.com/documentation/bundleresources/entitlements/com_apple_developer_user-management)를 참조.   

**Minimize data entry.   
데이터 입력을 최소화하라.**    
적지 않은 정보를 수집해야 하는 경우, 다른 기기에서 웹 사이트를 방문하도록 요청하라. 이메일 주소가 필요한 경우, 최근에 입력한 주소 목록이 포함된 이메일 키보드 스크린을 표시한다.   

### **[watchOS](https://developer.apple.com/design/human-interface-guidelines/managing-accounts#watchOS)**

iCloud 동기화를 사용해 Keychain에 대한 액세스를 제공하여, 사용자가 사용자 이름과 비밀번호를 자동으로 채우고 앱 설정을 보존할 수 있다.


    
</br></br>
##### [Managing accounts | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/managing-accounts)
