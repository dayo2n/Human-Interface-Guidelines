**June 21, 2023**

Consolidated guidance into new page and updated for visionOS.

# Privacy

## Privacy is paramount: it’s critical to be transparent about the privacy-related data and resources you require and essential to protect the data people allow you to access.
개인 정보 보호는 무엇보다 중요하다. 개인 정보 관련 데이터와 리소스에 대해 투명하게 파악하고 사람들이 액세스할 수 있도록 허용하는 데이터를 보호하는 데 필수적인 요소다.

![Untitled](https://docs-assets.developer.apple.com/published/c955797c748120da148d31af58117804/foundations-privacy-intro~dark@2x.png)

People use their devices in very personal ways and they expect apps to help them preserve their privacy. 

사람들은 디바이스를 매우 개인적인 용도로 사용하고, 앱이 사생활을 보호하는 데 도움이 되기를 바란다. 

When you submit a new or updated app, you must provide details about your privacy practices and the privacy-relevant data you collect so the App Store can display the information on your product page. (You can manage this information at any time in [App Store Connect](https://help.apple.com/app-store-connect/#/dev1b4647c5b).) People use the privacy details on your product page to make an informed decision before they download your app. To learn more, see [App privacy details on the App Store](https://developer.apple.com/app-store/app-privacy-details/).

새 앱 또는 업데이트된 앱을 제출할 때는 개인 정보 보호 관행 및 수집한 개인 정보 관련 데이터에 대한 세부 정보를 제공해야 앱 스토어에서 제품 페이지에 정보를 표시할 수 있다. ([App Store Connect](https://help.apple.com/app-store-connect/#/dev1b4647c5b)에서 언제든지 이 정보를 관리할 수 있다.) 사람들은 앱을 다운로드하기 전에 제품 페이지의 개인 정보 조항을 보고, 그에 입각한 결정은 내린다. 자세한 내용은  [App privacy details on the App Store](https://developer.apple.com/app-store/app-privacy-details/)를 참조.

![An app’s App Store product page helps people understand the app’s privacy practices before they download it.
앱의 앱스토어 프로덕트 페이지는 사람들이 앱을 다운로드하기 전에 앱의 개인 정보 보호 조항을 이해하는 데 도움이 된다.](https://docs-assets.developer.apple.com/published/0a39f679c227c371d63b8968fd825922/privacy-practices~dark@2x.png)

An app’s App Store product page helps people understand the app’s privacy practices before they download it.

앱의 앱스토어 프로덕트 페이지는 사람들이 앱을 다운로드하기 전에 앱의 개인 정보 보호 조항을 이해하는 데 도움이 된다.

## **[Best practices](https://developer.apple.com/design/human-interface-guidelines/privacy#Best-practices)**

**Request access only to data that you actually need.** Asking for more data than a feature needs — or asking for data before a person shows interest in the feature — can make it hard for people to trust your app. Give people precise control over their data by making your permission requests as specific as possible.

**실제로 필요한 데이터에 대해서만 액세스를 요청한다.** 기능에 필요한 것보다 더 많은 데이터를 요청하거나 사용자가 해당 기능에 관심을 보이기 전에 데이터를 요청하면 사용자가 앱을 신뢰하기 어려워질 수 있다. 사용자의 권한 요청을 가능한 한 구체적으로 지정하여 사용자가 자신의 데이터를 정확하게 제어할 수 있어야 한다.

**Be transparent about how your app collects and uses people’s data.** People are less likely to be comfortable sharing data with your app if they don’t understand exactly how you plan to use it. Always respect people’s choices to use system features like Hide My Email and Mail Privacy Protection, and be sure you understand your obligations with regard to app tracking. To learn more about Apple privacy features, see [Privacy](https://www.apple.com/privacy/); for developer guidance, see [User privacy and data use](https://developer.apple.com/app-store/user-privacy-and-data-use/).

**앱이 사람들의 데이터를 수집하고 사용하는 방법에 대해 투명성을 유지하라.** 사용자가 앱을 사용하는 방법을 정확히 이해하지 못하면 사용자가 앱과 데이터를 공유하는 데 불편함을 느낄 가능성이 높다. 내 전자 메일 숨기기 및 메일 개인 정보 보호와 같은 시스템 기능을 사용하는 사용자의 선택을 항상 존중하고 앱 추적과 관련된 의무를 이해해야 한다. Apple 개인 정보 기능에 대한 자세한 내용은 [Privacy](https://www.apple.com/privacy/)를 참조. 개발자 지침은 [User privacy and data use](https://developer.apple.com/app-store/user-privacy-and-data-use/)를 참조.

**Process data on the device where possible.** In iOS, for example, you can take advantage of the Apple Neural Engine and custom CreateML models to process the data right on the device, helping you avoid lengthy and potentially risky round trips to a remote server.

**가능한 경우 디바이스에서 데이터를 처리한다.** 예를 들어 iOS에서는 Apple Neural Engine 및 커스텀 CreateML 모델을 사용하여 장치에서 데이터를 바로 처리할 수 있으므로 원격 서버로의 장시간 왕복을 방지할 수 있다.

**Adopt system-defined privacy protections and follow security best practices.** For example, in iOS 15 and later, you can rely on CloudKit to provide encryption and key management for additional data types, like strings, numbers, and dates.

**시스템 정의 개인 정보 보호를 채택하고 보안 모범 사례를 따르라.** 예를 들어 iOS 15 이상에서는 CloudKit를 사용하여 문자열, 숫자 및 날짜와 같은 추가 데이터 유형에 대한 암호화 및 키 관리를 제공할 수 있다.

## **[Requesting permission](https://developer.apple.com/design/human-interface-guidelines/privacy#Requesting-permission)**

Here are several examples of the things you must request permission to access:
다음으로 액세스 권한을 요청해야 하는 몇 가지 예가 있다: 

- Personal data, including location, health, financial, contact, and other personally identifying information
위치, 상태, 재무, 연락처 및 기타 개인 식별 정보를 포함한 개인 데이터
- User-generated content like emails, messages, calendar data, contacts, gameplay information, Apple Music activity, HomeKit data, and audio, video, and photo content
이메일, 메시지, 캘린더 데이터, 연락처, 게임 정보, Apple Music 활동, HomeKit 데이터 및 오디오, 비디오 및 사진 콘텐츠와 같은 사용자 생성 콘텐츠
- Protected resources like Bluetooth peripherals, home automation features, Wi-Fi connections, and local networks
블루투스 주변 장치, 홈 자동화 기능, Wi-Fi 연결 및 로컬 네트워크와 같은 보호된 리소스
- Device capabilities like camera and microphone
카메라와 마이크와 같은 장치 기능
- The device’s advertising identifier, which supports app tracking
앱 추적을 지원하는 장치의 광고 식별자

The system provides a standard alert that lets people view each request you make. You supply copy that describes why your app needs access, and the system displays your description in the alert. People can also view the description — and update their choice — in Settings > Privacy.

시스템은 개발자가 요청한 각 요청을 볼 수 있는 표준 알림을 제공한다. 앱에 액세스해야 하는 이유를 설명하는 복사본을 제공하면 시스템이 알림으로 설명을 표시한다. 또한 사용자는 설정 > 개인 정보 보호에서 설명을 보고 선택한 내용을 업데이트할 수 있다.

**Request permission only when your app clearly needs access to the data or resource.** It’s natural for people to be suspicious of a request for personal information or access to a device capability, especially if there’s no obvious need for it. Ideally, wait to request permission until people actually use an app feature that requires access. For example, you can use the [location button](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#Location-button) to give people a way to share their location after they indicate interest in a feature that needs that information.

**앱에서 데이터 또는 리소스에 대한 액세스가 확실히 필요한 경우에만 권한을 요청하라.** 사람들이 개인 정보나 장치 기능에 대한 액세스 요청을 의심하는 것은 당연하며, 특히 장치 기능에 대한 명확한 필요성이 없는 경우에는 더욱 그렇다. 사람들이 실제로 액세스가 필요한 앱 기능을 사용할 때까지 권한을 요청하는 것이 이상적이다. 예를 들어 [location button](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#Location-button)를 사용하여 사용자가 해당 정보가 필요한 기능에 관심이 있음을 표시한 후 위치를 공유할 수 있다.

**Avoid requesting permission at launch unless the data or resource is required for your app to function.** People are less likely to be bothered by a launch-time request when it’s obvious why you’re making it. For example, people understand that a navigation app needs access to their location before they can benefit from it. Similarly, before people can play a visionOS game that lets them bounce virtual objects off walls in their surroundings, they need to permit the game to access information about their surroundings.

**앱이 작동하는 데 데이터 또는 리소스가 필요하지 않은 경우 시작 시 권한을 요청하지 마라.** 사람들은 이유가 분명할 때 launch-time 요청에 대해 덜 신경 쓸 것이다. 예를 들어, 사람들은 내비게이션 앱이 위치에 대한 액세스가 필요하다는 이유가 분명하므로 앱 실행시 접근을 요청하는 것을 이해한다. 비슷하게, 사람들이 가상의 물체를 그들의 주변의 벽에서 튕겨낼 수 있게 하는 비전OS 게임을 플레이하기 전에, 게임이 그들의 주변에 대한 정보에 접근하도록 허용해야 한다.

**Write copy that clearly describes how your app uses the ability, data, or resource you’re requesting.** The standard alert displays your copy (called a *purpose string* or *usage description string*) after your app name and before the buttons people use to grant or deny their permission. Aim for a brief, complete sentence that’s straightforward, specific, and easy to understand. Use sentence case, avoid passive voice, and include a period at the end. For developer guidance, see [Requesting access to protected resources](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources) and [App Tracking Transparency](https://developer.apple.com/documentation/apptrackingtransparency).

**요청하는 기능, 데이터 또는 리소스를 앱이 어떻게 사용하는지 명확하게 설명하는 문서를 작성하라.** 표준 알림은 앱 이름 뒤와 사용자가 권한을 부여하거나 거부하는 데 사용하는 버튼 앞에 복사본(*purpose string* 또는 *usage description*이라고 함)을 표시한다. 간단하고 구체적이며 이해하기 쉬운 짧고 완전한 문장을 목표로 해야 한다. 문장은 대소문자를 사용하고, 수동적인 음성을 피하고, 끝에 마침표를 포함해야 한다. 개발자 지침은 [Requesting access to protected resources](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources)와 [App Tracking Transparency](https://developer.apple.com/documentation/apptrackingtransparency)를 참조.

Here are several examples of the standard system alert:

표준 시스템 알림의 몇가지 예이다.

![위치 허용](https://docs-assets.developer.apple.com/published/42ed20b73b1fef384afdbc6fb1eafd03/permission-request-1~dark@2x.png)![사진 접근 허용](https://docs-assets.developer.apple.com/published/4f643f17b17a90115ffe0f2755ea2932/permission-request-2~dark@2x.png)![연락처 접근 허용](https://docs-assets.developer.apple.com/published/8d608eb39fc931d84759415617357618/permission-request-3~dark@2x.png)


## ****[Pre-alert screens, windows, or views](https://developer.apple.com/design/human-interface-guidelines/privacy#Pre-alert-screens-windows-or-views)****

Ideally, the current context helps people understand why you’re requesting their permission. If it’s essential to provide additional details, you can display a custom screen before the system alert appears. The following guidelines apply to custom screens that display before system alerts that request permission to access protected data and resources, including camera, microphone, location, contact, calendar, and tracking.

이상적으로 현재 상황은 사용자가 사용자의 권한을 요청하는 이유를 이해하는 데 도움이 된다. 추가 세부 정보를 제공해야 하는 경우 시스템 경고가 나타나기 전에 사용자 지정 화면을 표시할 수 있다. 다음 지침은 카메라, 마이크, 위치, 연락처, 일정 및 추적을 포함하여 보호된 데이터 및 리소스에 대한 액세스 권한을 요청하는 시스템 경고 전에 표시되는 사용자 지정 화면에 적용된다.

**Include only one button and make it clear that it opens the system alert.** People can feel manipulated when a custom screen also includes a button that doesn’t open the alert because the experience diverts them from making their choice. Another type of manipulation is using a term like “Allow” to title the custom screen’s button. If the screen’s button seems similar in meaning and visual weight to the allow button in the alert, people can be more likely to choose the alert’s allow button without meaning to. Use a term like “Continue” or “Next” to title your custom screen’s single button, clarifying that its action is to open the system alert.

**버튼을 하나만 포함하고, 그것만이 시스템 알림을 나타내는지 확인하라.** 사용자 지정 화면에 알림을 열지 않는 버튼이 포함되어 있을 때 사람들은 조작된 느낌을 받을 수 있다. 왜냐하면 경험이 그들의 선택을 방해하기 때문이다. 다른 유형의 조작은 "허용"과 같은 용어를 사용하여 사용자 지정 화면의 버튼제목을 지정하는 것이다. 화면의 버튼이 알림의 허용 버튼과 의미 및 시각적 가중치가 유사한 것처럼 보이는 경우 사람들은 의미 없이 알림의 허용 버튼을 선택할 가능성이 더 높아질 수 있다. "계속" 또는 "다음"과 같은 용어를 사용하여 사용자 지정 화면의 단일 버튼에 제목을 지정한다. 이 버튼의 작업은 시스템 경고를 나타내는 것이다.

![](https://docs-assets.developer.apple.com/published/fc7f233de9ee89f9dbdb48c175225a59/custom-messaging-correct-1@2x.png)

![](https://docs-assets.developer.apple.com/published/237274110e00048cc265d0f0042dd0c8/custom-messaging-correct-2@2x.png)

![](https://docs-assets.developer.apple.com/published/88662da92338267bb64cd2275c84e484/checkmark@2x.png)

**Don’t include additional actions in your custom screen.** For example, don’t provide a way for people to leave the screen without viewing the system alert — like offering an option to close or cancel.

**사용자 지정 화면에 추가 작업을 포함하지 마라.** 예를 들어, 닫기 또는 취소 옵션을 제공하는 것과 같이 사람들이 시스템 경고를 보지 않고 화면을 떠날 수 있는 방법을 제공하지 마라.

![](https://docs-assets.developer.apple.com/published/6ff09ed38ef7b3823347bc240c48b347/custom-messaging-incorrect-5@2x.png)

![](https://docs-assets.developer.apple.com/published/6910c5e5f213833465fb3d06c6e9689a/custom-messaging-incorrect-6@2x.png)

![](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)

## **[Tracking requests](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#Tracking-requests)**

App tracking is a sensitive issue. In some cases, it might make sense to display a custom screen that describes the benefits of tracking. If you want to perform app tracking as soon as people launch your app, you must display the system-provided alert before you collect any tracking data.

앱 추적은 민감한 문제이다. 경우에 따라 추적의 이점을 설명하는 사용자 지정 화면을 표시하는 것이 합리적일 수 있다. 사람들이 앱을 실행하는 즉시 앱 추적을 수행하려면 추적 데이터를 수집하기 전에 시스템에서 제공한 경고를 표시해야 한다.

**Never precede the system-provided alert with a custom screen that could confuse or mislead people.** People sometimes tap quickly to dismiss alerts without reading them. A custom messaging screen that takes advantage of such behaviors to influence choices will lead to rejection by App Store review.

**사용자를 혼동하거나 오도할 수 있는 사용자 지정 화면으로 시스템 alert를 선행하지 마라.** 사람들은 때때로 경고를 읽지 않고 무시하기 위해 빠르게 탭한다. 이러한 행동을 이용하여 선택에 영향을 미치는 사용자 지정 메시징 화면은 앱스토어 검토에서 거부로 이어질 수 있다.

There are several prohibited custom-screen designs that will cause rejection. Some examples are offering incentives, displaying a screen that looks like a request, displaying an image of the alert, and annotating the screen behind the alert (as shown below). For guidance, see [App Store Review Guidelines: 5.1.1 (iv)](https://developer.apple.com/app-store/review/guidelines/#data-collection-and-storage).

거부를 유발하는 몇 가지 금지된 사용자 지정 화면 디자인이 있다. 몇 가지 예로는 인센티브 제공, 요청처럼 보이는 화면 표시, 경고 이미지 표시, 경고 뒤의 화면 주석 달기 등이 있다 (아래 그림 참조). 자세한 내용은 [App Store Review Guidelines: 5.1.1 (iv)](https://developer.apple.com/app-store/review/guidelines/#data-collection-and-storage)을 참조.

![[Incentive](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)](https://docs-assets.developer.apple.com/published/cd97429e2555ad384979258c510fcf30/custom-messaging-incorrect-1@2x.png)

[Incentive](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)

![](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)

Don’t offer incentives for granting the request. You can’t offer people compensation for granting their permission, and you can’t withhold functionality or content or make your app unusable until people allow you to track them.

요청을 승인하는 것에 대한 인센티브를 제공하지 마라. 사람들에게 그들의 권한을 부여한 것에 대한 보상을 제공할 수 없으며, 사람들이 추적하는 것을 허락할 때까지 기능 또는 콘텐츠를 보류하거나 앱을 사용할 수 없게 만들 수 없다.

![[Alert image](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)](https://docs-assets.developer.apple.com/published/754adf94fd632793b649b54acaac0ecd/custom-messaging-incorrect-2@2x.png)

[Alert image](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)

![](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)

Don’t show an image of the standard alert and modify it in any way.

표준 알림을 이미지로 표시하거나 수정하지 마라.

![[Imitation request](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)](https://docs-assets.developer.apple.com/published/fbdd26e0fda5fc902bec91b4b9717cd0/custom-messaging-incorrect-3~dark@2x.png)

[Imitation request](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)

![](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)

Don’t display a custom screen that mirrors the functionality of the system alert. In particular, don’t create a button title that uses “Allow” or similar terms, because people don’t allow anything in a pre-alert screen.

시스템 알림의 기능을 나타내는 사용자 지정 화면을 표시하지 마라. 특히, 사람들은 사전 경고 화면에서 아무것도 허용하지 않으므로 "허용" 또는 유사한 용어를 사용하는 버튼 제목을 만들지 마라.

![[Alert annotation](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)](https://docs-assets.developer.apple.com/published/713a338451a9b96788b0490cf1b75435/custom-messaging-incorrect-4~dark@2x.png)

[Alert annotation](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#)

![](https://docs-assets.developer.apple.com/published/209f6f0fc8ad99d9bf59e12d82d06584/crossout@2x.png)

Don’t draw a visual cue that draws people’s attention to the system alert’s Allow button.

시스템 알림의 허용 버튼에 사람들의 주의를 끄는 시각적인 신호를 그리지 마라.

## **[Location button](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#Location-button)**

Beginning in iOS 15, iPadOS 15, and watchOS 8, Core Location provides a button so people can grant your app temporary authorization to access their location at the moment a task needs it. A location button’s appearance can vary to match your app’s UI and it always communicates the action of location sharing in a way that’s instantly recognizable.

iOS 15, iPad OS 15 및 watchOS 8이 들어오면서, Core Location은 사람들이 작업이 필요한 순간에 자신의 위치에 액세스할 수 있는 임시 권한을 앱에 부여할 수 있도록 버튼을 제공한다. 위치 버튼의 모양은 앱의 UI에 따라 달라질 수 있으며 항상 위치 공유의 동작을 즉시 인식할 수 있는 방식으로 전달한다.

![](https://docs-assets.developer.apple.com/published/2d4e44adec80170cec96d3446617e700/location-button@2x.png)

The first time people open your app and tap a location button, the system displays a standard alert. The alert helps people understand how using the button limits your app’s access to their location, and reminds them of the location indicator that appears when sharing starts.

사람들이 처음으로 앱을 열고 위치 버튼을 누르면 시스템은 표준 알림를 표시한다. 이 알림은 사용자가 버튼을 사용하여 앱의 위치 액세스를 제한하는 방법을 이해하는 데 도움이 되며 공유가 시작될 때 나타나는 위치 표시기를 알려준다.

![Untitled](https://docs-assets.developer.apple.com/published/053f55e79f0f1d08c2c118c4ab64f56f/location-button-alert~dark@2x.png)

After people confirm their understanding of the button’s action, simply tapping the location button gives your app one-time permission to access their location. Although each one-time authorization expires when people stop using your app, they don’t need to reconfirm their understanding of the button’s behavior.

사람들이 버튼의 동작에 대한 이해를 확인한 후, 위치 버튼을 누르기만 하면 앱이 자신의 위치에 액세스할 수 있는 **일회성** 권한을 부여한다. 비록 사람들이 앱을 사용하는 것을 중단할 때 각각의 일회성 승인이 만료되지만, 버튼의 동작에 대한 그들의 이해를 재확인할 필요가 없다.

```
💡 Note
If your app has no authorization status, 
tapping the location button has the same effect 
as when a person chooses Allow Once in the standard alert. 
If people previously chose While Using the App, 
tapping the location button doesn’t change your app’s status. 
For developer guidance, see LocationButton (SwiftUI) and CLLocationButton (Swift).
앱에 권한 부여 상태가 없는 경우 
위치 버튼을 누르면 표준 알림에서 한 번 허용을 선택한 경우와 동일한 효과가 있다. 
이전에 앱을 사용하는 동안을 선택한 경우 위치 버튼을 눌러도 앱의 상태가 변경되지 않는다. 
개발자 지침은 LocationButton (SwiftUI) 및 CLLocationButton(Swift)을 참조.

LocationButton: https://developer.apple.com/documentation/corelocationui/locationbutton
CLLocationButton: https://developer.apple.com/documentation/corelocationui/cllocationbutton
```

**Consider using the location button to give people a lightweight way to share their location for specific app features.** For example, your app might help people attach their location to a message or post, find a store, or identify a building, plant, or animal they’ve encountered in their location. If you know that people often grant your app *Allow Once* permission, consider using the location button to help them benefit from sharing their location without having to repeatedly interact with the alert.

**위치 버튼을 사용하여 특정 앱 기능에 대한 위치를 사람들이 쉽게 공유할 수 있는 방법을 제공하라.** 예를 들어, 앱은 사람들이 자신의 위치를 메시지나 게시물에 첨부하거나, 상점을 찾거나, 해당 위치에 있는 건물, 식물 또는 동물을 식별하는 데 도움을 줄 수 있다. 사람들이 앱에 한 번 허용 권한을 부여하는 경우가 많다는 것을 알고 있다면 위치 버튼을 사용하여 알림과 반복적으로 상호 작용하지 않고 위치를 공유함으로써 이점을 얻을 수 있다.

**Consider customizing the location button to harmonize with your UI.** Specifically, you can:

**위치 버튼을 사용자 정의하여 UI와 조화를 이루어라.** 구체적으로 다음을 수행할 수 있다:

- Choose the system-provided title that works best with your feature, such as “Current Location” or “Share My Current Location.”
"현재 위치" 또는 "내 현재 위치 공유"와 같이 기능에 가장 적합한 시스템에서 제공한 제목을 선택
- Choose the filled or outlined location glyph.
채우기 또는 윤곽선이 있는 위치 글리프를 선택
- Select a background color and a color for the title and glyph.
제목과 글리프의 배경색과 색상을 선택
- Adjust the button’s corner radius.
버튼의 모서리 반지름을 조정

To help people recognize and trust location buttons, you can’t customize the button’s other visual attributes. The system also ensures a location button remains legible by warning you about problems like low-contrast color combinations or too much translucency. In addition to fixing such problems, you’re responsible for making sure the text fits in the button — for example, button text needs to fit without truncation at all accessibility text sizes and when translated into other languages.

사용자가 위치 버튼을 인식하고 신뢰할 수 있도록 버튼의 다른 시각적 속성을 사용자 지정할 수 없다. 또한 이 시스템은 저대비 색상 조합 또는 과도한 투명도와 같은 문제에 대해 경고함으로써 위치 버튼을 읽을 수 있도록 한다. 사용자는 이러한 문제를 해결하는 것 외에도 버튼 텍스트가 버튼에 맞는지 확인해야 합니다. 예를 들어, 버튼 텍스트는 모든 내게 필요한 텍스트 크기와 다른 언어로 번역될 때 잘리지 않고 적합해야 한다.

```
💡 Important
If the system identifies consistent problems with your customized location button, 
it won’t give your app access to the device location when people tap it. 
Although such a button can perform other app-specific actions, 
people may lose trust in your app if your location button doesn’t work as they expect.
시스템이 사용자 지정 위치 버튼과 관련된 일관된 문제를 확인하게 되는 경우, 
사람들이 탭을 하더라도 앱에서 장치 위치에 액세스할 수 없게 된다. 
이러한 버튼은 다른 앱별 작업을 수행할 수 있지만, 
위치 버튼이 예상대로 작동하지 않으면 사람들은 앱에 대한 신뢰를 잃을 수 있다.

```

## **[Protecting data](https://developer.apple.com/design/human-interface-guidelines/privacy#Protecting-data)**

Protecting people’s information is paramount. Give people confidence in your app’s security and help preserve their privacy by taking advantage of system-provided security technologies when you need to store information locally, authorize people for specific operations, and transport information across a network.

사람들의 정보를 보호하는 것이 가장 중요하다. 로컬로 정보를 저장하고, 특정 작업에 대한 권한을 부여하고, 네트워크를 통해 정보를 전송해야 할 때 시스템에서 제공하는 보안 기술을 활용하여 사용자에게 앱의 보안에 대한 확신을 주고 개인 정보를 보호할 수 있다.

Here are some high-level guidelines.
여기 몇 가지 고수준의 가이드라인이 있다.

**Avoid relying solely on passwords for authentication.** Take advantage of other technologies like Touch ID, which lets people authenticate with a fingerprint. For developer guidance, see [Local Authentication](https://developer.apple.com/documentation/localauthentication).
**인증을 위해 패스워드에만 의존하지 마라**. 사람들이 지문으로 인증할 수 있는 터치 ID와 같은 다른 기술을 활용하라. 개발자 지침은 [Local Authentication](https://developer.apple.com/documentation/localauthentication)을 참조.

**Store sensitive information in a keychain.** A keychain provides a secure, predictable user experience when handling someone’s private information. For developer guidance, see [Keychain Services](https://developer.apple.com/documentation/security/keychain_services).
**중요한 정보를 키 체인에 저장하라.** 키체인은 누군가의 개인 정보를 다룰 때 안전하고 예측 가능한 사용자 경험을 제공한다. 개발자 지침은 [Keychain Services](https://developer.apple.com/documentation/security/keychain_services)를 참조.

**Never store passwords or other secure content in plain-text files.** Even if you restrict access using file permissions, sensitive information is much safer in an encrypted keychain.
**암호 또는 기타 보안 콘텐츠를 일반 텍스트 파일에 저장하지 마라.** 파일 권한을 사용하여 액세스를 제한하더라도 중요한 정보는 암호화된 키 체인에서 훨씬 안전하다.

**Avoid inventing custom authentication schemes.** If your app requires authentication, prefer system-provided features like [Sign in with Apple](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple) or [Password AutoFill](https://developer.apple.com/documentation/security/password_autofill). For guidance, see [Managing accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts).
커스텀 **인증 체계를 만들지 마라.** 앱에 인증이 필요한 경우, [Sign in with Apple](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple) 또는 [Password AutoFill](https://developer.apple.com/documentation/security/password_autofill)과 같은 시스템에서 제공하는 기능을 사용하라. 자세한 내용은 [Managing accounts](https://developer.apple.com/design/human-interface-guidelines/managing-accounts)를 참조.

## **[Platform considerations](https://developer.apple.com/design/human-interface-guidelines/privacy#Platform-considerations)**

*No additional considerations for iOS, iPadOS, tvOS, or watchOS.*

### **[macOS](https://developer.apple.com/design/human-interface-guidelines/accessing-private-data#macOS)**

**Sign your app with a valid Developer ID.** If you choose to distribute your app outside the store, signing your app with Developer ID identifies you as an Apple developer and confirms that your app is safe to use. For developer guidance, see [Xcode Help](https://developer.apple.com/go/?id=ios-app-distribution-guide).

**올바른 개발자 ID로 앱에 서명하라.** 앱을 스토어 외부에 배포하기로 선택한 경우 개발자 ID로 앱에 서명하면 사용자가 Apple 개발자임을 확인하고 앱을 안전하게 사용할 수 있음을 확인할 수 있다. 개발자 지침은 [Xcode Help](https://developer.apple.com/go/?id=ios-app-distribution-guide)을 참조.

**Protect people’s data with app sandboxing.** Sandboxing provides your app with access to system resources and user data while protecting it from malware. All apps submitted to the Mac App Store require sandboxing. For developer guidance, see [Configuring the macOS App Sandbox](https://developer.apple.com/documentation/Xcode/configuring-the-macos-app-sandbox).

**앱 샌드박스를 통해 사용자의 데이터를 보호하라.** 샌드박스는 악성 프로그램으로부터 보호하면서 시스템 리소스 및 사용자 데이터에 대한 액세스를 앱에 제공한다. 맥 앱스토어에 제출된 모든 앱은 샌드박스가 필요하다. 개발자 지침은 [Configuring the macOS App Sandbox](https://developer.apple.com/documentation/Xcode/configuring-the-macos-app-sandbox)를 참조.

**Avoid making assumptions about who is signed in.** Because of fast user switching, multiple people may be active on the same system.

**로그인한 사용자에 대한 가정을 하지 마라.** 빠른 사용자 전환으로 인해 동일한 시스템에서 여러 명이 활성화될 수 있다.

### ****[visionOS](https://developer.apple.com/design/human-interface-guidelines/privacy#visionOS)****

By default, visionOS uses ARKit algorithms to handle features like persistence, world mapping, segmentation, matting, and environment lighting. These algorithms are always running, allowing apps and games to automatically benefit from ARKit while in the Shared Space.

기본적으로 비전OS는 ARKit 알고리즘을 사용하여 지속성, 월드 매핑, 세그멘테이션, 매트 및 환경 조명과 같은 기능을 처리한다. 이러한 알고리즘은 항상 실행되므로 공유 공간에 있는 동안 앱과 게임이 자동으로 ARKit의 이점을 누릴 수 있다.

ARKit doesn’t send data to apps in the Shared Space; to access ARKit APIs, your app must open a Full Space. Additionally, features like Plane Estimation, Scene Reconstruction, Image Anchoring, and Hand Tracking require people’s permission to access any information. For developer guidance, see [Setting up access to ARKit data](https://developer.apple.com/documentation/visionOS/setting-up-access-to-arkit-data).

ARKit는 공유 공간에 있는 앱으로 데이터를 전송하지 않는다. ARKit API에 액세스하려면 앱에서 전체 공간을 열어야 한다. 또한 평면 추정, 장면 재구성, 이미지 고정 및 손 추적과 같은 기능을 사용하려면 사용자가 모든 정보에 액세스할 수 있는 권한이 필요하다. 개발자 지침은 [Setting up access to ARKit data](https://developer.apple.com/documentation/visionOS/setting-up-access-to-arkit-data)을 참조.

In visionOS, user input is private by design. The system automatically displays hover effects when people bring focus to components that you create using SwiftUI or RealityKit, giving people the visual feedback they need without exposing the direction of their gaze before they tap. For guidance, see [Focus and selection](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection) and [Gestures > visionOS](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS).

비전 OS에서 사용자 입력은 설계상 비공개이다. 사용자가 SwiftUI 또는 RealityKit를 사용하여 만든 구성 요소에 포커스를 가져오면 시스템이 자동으로 호버 효과를 표시함으로 사람들이 탭하기 전에 시선의 방향을 노출시키지 않고 필요한 시각적 피드백을 제공한다. 자세한 내용은  [Focus and selection](https://developer.apple.com/design/human-interface-guidelines/focus-and-selection)과 [Gestures > visionOS](https://developer.apple.com/design/human-interface-guidelines/gestures#visionOS)을 참조.

Developer access to device cameras works differently in visionOS than it does in other platforms. Specifically, the back camera provides blank input and is only available as a compatibility convenience; the front camera provides input for [Spatial Personas](https://developer.apple.com/design/human-interface-guidelines/shareplay#visionOS), but only after people grant their permission. If the iOS or iPadOS app you’re bringing to visionOS includes a feature that needs camera access, remove it or replace it with an option for people to import content instead. For developer guidance, see [Checking whether your existing app is compatible with visionOS](https://developer.apple.com/documentation/visionOS/checking-whether-your-app-is-compatible-with-visionos).

장치 카메라에 대한 개발자 액세스가 다른 플랫폼에 비해 visionOS에서는 다르게 작동한다. 특히, 후면 카메라는 공백(blank) 입력을 제공하며 호환성 편의를 위해서만 사용할 수 있다. 전면 카메라는 [Spatial Personas](https://developer.apple.com/design/human-interface-guidelines/shareplay#visionOS)에 대한 입력을 제공하지만, 사람들이 허락한 후에만 사용할 수 있다. 비전OS을 실행할 iOS 또는 iPadOS 앱에는 카메라 액세스가 필요한 기능이 포함되며, 이 기능을 제거하거나 사람들이 콘텐츠를 대신 가져올 수 있는 옵션으로 대체한다. 개발자 지침은 [Checking whether your existing app is compatible with visionOS](https://developer.apple.com/documentation/visionOS/checking-whether-your-app-is-compatible-with-visionos)을 참조.

</br></br>
##### [Privacy | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/privacy)
