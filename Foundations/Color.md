# Foundations

## Color

```swift
🎨 Judicious use of color can enhance communication, evoke your brand, provide visual continuity, 
  communicate status and feedback, and help people understand information.
  현명한 색상 사용은 의사소통을 향상시키고, 브랜드를 환기시키며, 시각적 연속성을 제공하고, 
  상태와 피드백을 전달하고, 사람들이 정보를 이해하는 데 도움을 줄 수 있다.
```

이 시스템은 다양한 배경과 외관 모드(dark, light mode)에 어울리는 색상을 정의하고, 생동감 효과와 접근성 설정에 자동으로 적응할 수 있다. 사람들은 시스템 컬러에 익숙하며, 그것들을 사용하는 것은 기기에서 편안한 경험을 할 수 있는 편리한 방법이다.

또한 커스텀 컬러를 사용해 본인 앱의 시각적 경험을 향상시키고 유니크한 개성을 표현할 수도 있다. 다음 지침은 시스템 정의 색상을 사용하든 커스텀 색상을 사용하든 상관없이, 사용자가 원하는 방식으로 색상을 지정하는 데 도움이 된다.

### Best Practices

**Use color sparingly in nongame apps.**
**비게임 앱에서는 색상을 적게 사용하라.**
게임이 아닌 앱에서 색상의 과도한 사용은 의사소통을 덜 명확하게 만들고 주의를 산만하게 한다. 중요한 정보에 집중시키거나 인터페이스의 부분 간의 관계를 표시하기 위해 색상을 사용하는 것을 선호한다.

**Avoid using the same color to mean different things.**
**같은 색을 다른 의미로 사용하는 것을 피하라.**
인터페이스 전체에서 색상을 일관되게 사용하는 것은, 특히 상태나 상호 작용과 같은 정보를 전달하는 데에 도움이 된다. 예를 들어, 앱은 텍스트를 눌러 그 내용을 더 볼 수 있음을 나타낼 때 파란색을 사용한다. 앱이 색상에 의존하지 않는 시각적 표시기(visual indicator; 화살표←→ 또는 쉐브론〈 〉 아이콘)를 사용해 대화형 텍스트에 파란색이 아닌 다른 색상을 사용해 대화형 텍스트를 전달하는 경우에도 혼란이 발생한다.

**Make sure your app’s colors work well in both light and dark appearance modes.**
**앱이 밝은 모드 / 어두운 모드에서 모두 색상이 잘 보이는지 확인해라.**
항상 순수한 검은 색 배경을 사용하는 watchOS를 제외하고, 플랫폼은 기본 light appearance에 대한 dark alternative를 제공한다. 다크 모드는 모든 화면, 뷰, 메뉴 및 컨트롤에 더 어두운 색상 팔레트를 사용하며, (foreground와 background 색상을 동적으로 혼합하는 미묘한 효과인) 진동을 증가시켜 어두운 background에서 foreground의 콘텐츠를 돋보이게 할 수 있다. 시스템 컬러는 두 가지 appearnce를 모두 자동으로 지원합니다; 커스텀 컬러를 사용하고 싶다면, 밝은 색상과 어두운 색상을 모두 제공해야 합니다. 자세한 내용은 [Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode)를 참고하세요.

**Test your app’s color scheme under a variety of lighting conditions.**
**다양한 조명 조건에서 앱의 색 구성을 테스트해라.**
햇빛이 좋은 날이나 어두운 조명에서 앱을 실행할 때 색상이 다르게 보일 수 있다. 대부분의 유스케이스에서 최적의 viewing 경험을 제공하도록 색상을 조정해야 한다.

**Test your app on devices with different displays.**
**디스플레이가 다른 기기에서 테스트해라.**
예를 들어, (특정 iPhone, iPad 및 Mac 모델에서 사용 가능한) True Tone 디스플레이는 주변 조도 센서를 사용해 현재 환경의 조명 조건에 맞게 디스플레이의 [white point](https://en.wikipedia.org/wiki/White_point)를 자동으로 조정한다. 주로 독서, 사진, 비디오 및 게임에 초점을 맞춘 앱은 white point 적응 스타일을 지정함(개발자 지침은 [UIWhitePointAdaptivityStyle](https://developer.apple.com/documentation/bundleresources/information_property_list/uiwhitepointadaptivitystyle) 참조)으로써 이 효과를 강화하거나 약화시킬 수 있다. 
여러 브랜드의 HD 및 4K TV에서도 tvOS의 앱을 테스트한다. 또한 `시스템 설정 > 디스플레이`에서 프로필을 선택하여 Mac에서 P3 및 표준 RGB(sRGB)와 같은 다른 색상 프로필을 사용하여 앱 모양을 테스트할 수 있다. 자세한 내용은 [Color management](https://developer.apple.com/design/human-interface-guidelines/color#Color-management)를 참고하세요.

**Consider how artwork and translucency affect nearby colors.**
**artwork와 투명도가 주변 색에 어떤 영향을 미치는지 고려해라.**
예술 작품의 변화는 때때로 시각적 연속성을 유지하고 인터페이스 요소들이 너무 압도적이거나 잡아먹히지 않게 하기 위해 주변 색상 변경을 요구한다. 예를 들어 지도는, 맵 모드일 때는 밝은 색 스킴을 표시하지만, 위성 모드일 때는 어두 운 색 스킴으로 전환된다. 색상은 toolbar와 같은 반투명 요소 뒤에 놓거나 적용될 때 다르게 나타날 수 있다.

**If your app lets people choose colors, prefer system-provided color controls where available.**
**앱에서 사람들에게 색상을 선택할 수 있게 하는 경우, 시스템이 제공하는 색상 컨트롤을 선호한다.**
내장된 컬러 픽커를 사용하면 일관된 사용자 경험을 제공할 뿐만 아니라, 모든 앱에서 접근할 수 있는 색상 집합을 저장할 수 있다. 개발자 지침은 [NSColorPanel](https://developer.apple.com/documentation/appkit/nscolorpanel)(macOS), [UIColorWell](https://developer.apple.com/documentation/uikit/uicolorwell) 및 [UIColorPickerViewController](https://developer.apple.com/documentation/uikit/uicolorpickerviewcontroller) (iOS, iPadOS, 및 Mac Catalyst)를 참조하세요.

### Inclusive color

**Avoid relying solely on color to differentiate between objects, indicate interactivity, or communicate essential information.**
**개체를 구별하거나 상호작용을 나타낼 때, 중요한 정보를 전달하는 데에 색상에만 의존하지 마라.**
정보를 전달하기 위해 색상을 사용할 때, **색맹이나 다른 시각 장애**를 가진 사람들이 이해할 수 있도록 동일한 정보를 대체 방법을 제공해야 한다. 예를 들어, 레이블 또는 글리프 모양(글자의 모양)을 사용하여 개체 또는 상태를 식별할 수 있다.

**Avoid using colors that make it hard to perceive content in your app.**
**앱에서 컨텐츠를 인식하기 어렵게 만드는 색을 사용하지 마라.**
예를 들어, 대비가 부족하면 아이콘과 텍스트를 배경과 혼합되어 내용을 읽기 어렵게 하고, 색맹인 사람들은 일부 색 조합을 구별하지 못할 수 있다. 자세한 내용은 [Color and effects](https://developer.apple.com/design/human-interface-guidelines/accessibility#Color-and-effects)를 참조하세요.

**Consider how the colors you use might be perceived in other countries and cultures.** 
**내가 사용하는 색이 다른 나라와 문화에서 어떻게 인식되는지 생각해봐라.**
예를 들어, 빨간색은 어떤 문화권에서는 위험을 알리지만, 다른 문화권에서는 긍정적인 의미를 가진다. 앱의 색상이 의도한 메시지를 보내는지 확인하세요.

### System Colors

**Avoid hard-coding system color values in your app.**
**앱 내 시스템 컬러 값을 하드코딩하지 않도록 하자.**
문서화된 색상 값은 앱 디자인 프로세스 중 참조할 수 있는 값이다. 실제 색상 값은 다양한 환경 변수에 따라 릴리즈마다 변동될 수 있다. [Color](https://developer.apple.com/documentation/SwiftUI/Color)와 같은 API를 사용하여 시스템 색상을 적용하자.
iOS와 macOS는 표준 UI 컴포넌트의 컬러 스킴과 일치하는 *dynamic system colors* 세트가 정의되어 있고, 자동으로 라이트, 다크모드에 적용된다.
각각의 동적 컬러는 모양이나 색상 값이 아닌, **목적**에 따라 의미를 담아 정의된다. 예를 들어, 어떤 컬러는 서로 다른 계층 수준의 뷰 배경을 의미하고, 또 어떤 컬러는 레이블, 링크 및 구분점과 같은 foreground 콘텐츠를 나타낸다.

**Avoid replicating dynamic system colors.**
**동적 시스템 컬러를 복제하지 마라.**
일부는 패턴일 수 있는 동적 시스템 컬러는 환경 변수에 따라 릴리즈마다 변동될 수 있다.

**Avoid redefining the semantic meanings of dynamic system colors.**
**동적 시스템 컬러에 담긴 의미를 재정의하지 마라.**
일관된 경험을 보장하고 훗날 macOS의 외관이 달라지더라도 좋은 인터페이스를 위해, 의도한 대로 동적 시스템 컬러를 사용하세요.

### Color management

*color space*는 RGB나 CMYK같은 *color model*의 컬러들을 말한다. 일반적인 *color space*은 sRGB와 디스플레이 P3이다.

<img width="246" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/38f2c96d-2d6e-4f57-8a7e-1675f0ff0375">

*color profile*은, 예를 들어 색상들을 숫자 표현에 매핑하는 수학 공식이나 데이터 표를 사용해 *color space*를 설명한다. 이미지는 기기가 이미지의 색상을 올바르게 해석해 디스플레이에 재현할 수 있도록 *************color profile*************을 포함한다.

**Apply color profiles to your images.**
**color profile을 이미지에 적용하라.**
color profile은 서로 다른 여러 디바이스들에서 앱의 색상이 의도한대로 보이는데 도움이 된다. sRGB color profile은 대부분의 디스플레이에서 정확한 색깔을 생성한다.

**Use wide color to enhance the visual experience on compatible displays.
와이드 컬러를 사용해 호환가능한 디스플레이에서 시각적 경험을 향상하라.
와이드 컬러는** sRGB보다 더 풍부하고 포화도가 높은 P3 color space를 지원한다. 그 결과, 와이드 컬러를 사용하는 사진과 비디오가 더욱 실물과 유사하며, 와이드 컬러를 사용하는 시각 데이터와 상태 표시기가 더욱 의미를 가질 수 있다. 필요한 경우, 픽셀당(채널당) 16비트의 디스플레이 P3 color profile을 사용하고 PNG 형식으로 이미지를 내보낸다. 와이드 컬러 이미지를 디자인하고 P3 컬러를 선택하려면 와이드 컬러 디스플레이를 사용해야 한다.

**Provide color space–specific image and color variations if necessary.
필요한 경우 color space별 이미지 및 색 변형을 제공하라.**
일반적으로sRGB 디스플레이에서 P3 색상과 이미지는 잘 나타나지만, 때때로 매우 유사한 두 P3 색상을 구분하는 것이 어렵다. P3 색상을 사용하는 그라데이션은 때때로 잘린 것처럼 보이기도 한다. 이러한 이슈를 방지하고, 와이드 컬러와 sRGB 디스플레이 모두에서 시각적 충실도를 보장하기 위해 Xcode 프로젝트의 asset catalog를 사용해 각 color space에 대해 서로 다른 버전의 이미지와 색상을 제공할 수 있다.

To learn more, see [How to start designing assets in Display P3](https://developer.apple.com/news/?id=5cda5ipr).

## **[Platform considerations](https://developer.apple.com/design/human-interface-guidelines/color#Platform-considerations)**

### **[iOS, iPadOS](https://developer.apple.com/design/human-interface-guidelines/color#iOS-iPadOS)**

iOS는 system과 grouped라는 두 가지 다이나믹 백그라운드 컬러를 정의하며, 각 배경색에는 정보 계층을 전달하는 데 도움이 되는 primary, secondary, teritiary variants가 포함된다. 일반적으로 **grouped** 배경색([systemGroupedBackground](https://developer.apple.com/documentation/uikit/uicolor/3173145-systemgroupedbackground), [secondarySystemGroupedBackground](https://developer.apple.com/documentation/uikit/uicolor/3173138-secondarysystemgroupedbackground), and [tertiarySystemGroupedBackground](https://developer.apple.com/documentation/uikit/uicolor/3173155-tertiarysystemgroupedbackground))을 사용하고, 그렇지 않은 경우 **system** 배경색([systemBackground](https://developer.apple.com/documentation/uikit/uicolor/3173140-systembackground), [secondarySystemBackground](https://developer.apple.com/documentation/uikit/uicolor/3173137-secondarysystembackground), and [tertiarySystemBackground](https://developer.apple.com/documentation/uikit/uicolor/3173154-tertiarysystembackground))을 사용한다.

일반적으로 두 배경색 세트 모두 variants를 사용해 다음과 같은 방식으로 계층을 나타낸다.

- 전체 보기(overall view)에 대해 **Primary**
- 전체 보기 내에서 내용 || 요소를 그룹화하기 위한 **Secondary**
- 보조 요소 내의 내용 || 요소를 그룹화하기 위한 **Tertiary**

foreground 콘텐츠에 대해 iOS는 다음과 같은 다이나믹 컬러를 정의하고 있다.

| Color | Use for… | UIKit API |
| --- | --- | --- |
| Label | A text label that contains primary content. | https://developer.apple.com/documentation/uikit/uicolor/3173131-label |
| Secondary label | A text label that contains secondary content. | https://developer.apple.com/documentation/uikit/uicolor/3173136-secondarylabel |
| Tertiary label | A text label that contains tertiary content. | https://developer.apple.com/documentation/uikit/uicolor/3173153-tertiarylabel |
| Quaternary label | A text label that contains quaternary content. | https://developer.apple.com/documentation/uikit/uicolor/3173135-quaternarylabel |
| Placeholder text | Placeholder text in controls or text views. | https://developer.apple.com/documentation/uikit/uicolor/3173134-placeholdertext |
| Separator | A separator that allows some underlying content to be visible. | https://developer.apple.com/documentation/uikit/uicolor/3173139-separator |
| Opaque separator | A separator that doesn’t allow any underlying content to be visible. | https://developer.apple.com/documentation/uikit/uicolor/3173133-opaqueseparator |
| Link | Text that functions as a link. | https://developer.apple.com/documentation/uikit/uicolor/3173132-link |

### **[macOS](https://developer.apple.com/design/human-interface-guidelines/color#macOS)**

macOS에 대해 다음과 같은 다이나믹 시스템 컬러가 정의되어 있다. 표준 Color 패널의 Developer palette에서도 볼 수 있다.

| Color | Use for… | AppKit API |
| --- | --- | --- |
| Alternate selected control text color | The text on a selected surface in a list or table. | https://developer.apple.com/documentation/appkit/nscolor/1527413-alternateselectedcontroltextcolo |
| Alternating content background colors | The backgrounds of alternating rows or columns in a list, table, or collection view. | https://developer.apple.com/documentation/appkit/nscolor/2998825-alternatingcontentbackgroundcolo |
| Control accent | The accent color people select in System Settings. | https://developer.apple.com/documentation/appkit/nscolor/3000782-controlaccentcolor |
| Control background color | The background of a large interface element, such as a browser or table. | https://developer.apple.com/documentation/appkit/nscolor/1531948-controlbackgroundcolor |
| Control color | The surface of a control. | https://developer.apple.com/documentation/appkit/nscolor/1524856-controlcolor |
| Control text color | The text of a control that is available. | https://developer.apple.com/documentation/appkit/nscolor/1535230-controltextcolor |
| Current control tint | The system-defined control tint. | https://developer.apple.com/documentation/appkit/nscolor/1526377-currentcontroltint |
| Unavailable control text color | The text of a control that’s unavailable. | https://developer.apple.com/documentation/appkit/nscolor/1530573-disabledcontroltextcolor |
| Find highlight color | The color of a find indicator. | https://developer.apple.com/documentation/appkit/nscolor/2998827-findhighlightcolor |
| Grid color | The gridlines of an interface element, such as a table. | https://developer.apple.com/documentation/appkit/nscolor/1527240-gridcolor |
| Header text color | The text of a header cell in a table. | https://developer.apple.com/documentation/appkit/nscolor/1531237-headertextcolor |
| Highlight color | The virtual light source onscreen. | https://developer.apple.com/documentation/appkit/nscolor/1527697-highlightcolor |
| Keyboard focus indicator color | The ring that appears around the currently focused control when using the keyboard for interface navigation. | https://developer.apple.com/documentation/appkit/nscolor/1532031-keyboardfocusindicatorcolor |
| Label color | The text of a label containing primary content. | https://developer.apple.com/documentation/appkit/nscolor/1534657-labelcolor |
| Link color | A link to other content. | https://developer.apple.com/documentation/appkit/nscolor/2998828-linkcolor |
| Placeholder text color | A placeholder string in a control or text view. | https://developer.apple.com/documentation/appkit/nscolor/2998829-placeholdertextcolor |
| Quaternary label color | The text of a label of lesser importance than a tertiary label, such as watermark text. | https://developer.apple.com/documentation/appkit/nscolor/1534635-quaternarylabelcolor |
| Scrubber textured background color | The background of a scrubber in the Touch Bar. For guidance, see https://developer.apple.com/design/human-interface-guidelines/touch-bar. | https://developer.apple.com/documentation/appkit/nscolor/2646931-scrubbertexturedbackgroundcolor |
| Secondary label color | The text of a label of lesser importance than a primary label, such as a label used to represent a subheading or additional information. | https://developer.apple.com/documentation/appkit/nscolor/1533254-secondarylabelcolor |
| Selected content background color | The background for selected content in a key window or view. | https://developer.apple.com/documentation/appkit/nscolor/2998830-selectedcontentbackgroundcolor |
| Selected control color | The surface of a selected control. | https://developer.apple.com/documentation/appkit/nscolor/1526796-selectedcontrolcolor |
| Selected control text color | The text of a selected control. | https://developer.apple.com/documentation/appkit/nscolor/1535591-selectedcontroltextcolor |
| Selected menu item text color | The text of a selected menu. | https://developer.apple.com/documentation/appkit/nscolor/1526658-selectedmenuitemtextcolor |
| Selected text background color | The background of selected text. | https://developer.apple.com/documentation/appkit/nscolor/1528136-selectedtextbackgroundcolor |
| Selected text color | The color for selected text. | https://developer.apple.com/documentation/appkit/nscolor/1528605-selectedtextcolor |
| Separator color | A separator between different sections of content. | https://developer.apple.com/documentation/appkit/nscolor/2998831-separatorcolor |
| Shadow color | The virtual shadow cast by a raised object onscreen. | https://developer.apple.com/documentation/appkit/nscolor/1525121-shadowcolor |
| Tertiary label color | The text of a label of lesser importance than a secondary label. | https://developer.apple.com/documentation/appkit/nscolor/1532376-tertiarylabelcolor |
| Text background color | The background color behind text. | https://developer.apple.com/documentation/appkit/nscolor/1535446-textbackgroundcolor |
| Text color | The text in a document. | https://developer.apple.com/documentation/appkit/nscolor/1527025-textcolor |
| Under page background color | The background behind a document’s content. | https://developer.apple.com/documentation/appkit/nscolor/1534707-underpagebackgroundcolor |
| Unemphasized selected content background color | The selected content in a non-key window or view. | https://developer.apple.com/documentation/appkit/nscolor/2998832-unemphasizedselectedcontentbackg |
| Unemphasized selected text background color | A background for selected text in a non-key window or view. | https://developer.apple.com/documentation/appkit/nscolor/2998833-unemphasizedselectedtextbackgrou |
| Unemphasized selected text color | Selected text in a non-key window or view. | https://developer.apple.com/documentation/appkit/nscolor/2998834-unemphasizedselectedtextcolor |
| Window background color | The background of a window. | https://developer.apple.com/documentation/appkit/nscolor/1528630-windowbackgroundcolor |
| Window frame text color | The text in the window’s title bar area. | https://developer.apple.com/documentation/appkit/nscolor/1524257-windowframetextcolor |

### **[App accent colors](https://developer.apple.com/design/human-interface-guidelines/color#App-accent-colors)**

macOS 11부터 accent color를 지정해 앱의 버튼, 셀렉션 하이라이팅과 사이드바를 커스텀할 수 있다. 시스템은 General > Accent color 설정이 multicolor라면 내가 지정한 accent color로 적용한다.

<img width="246" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/c4474d27-5ec7-4bb4-8c5d-23116fba31c5">
<img width="246" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/f46e798d-0d4c-4b89-abae-bdee1b7070d5">

유저들이 accent color를 multi color가 아닌 다른 값으로 설정하면, 시스템은 선택된 색상을 앱 전체의 관련 항목에 적용하여 accent color를 대체한다. 지정한 고정색상을 사용하는 사이드바 아이콘은 예외이다. 고정 색상의 사이드바 아이콘은 어떤 의미를 전달하기 위해 특정 색상을 사용하기 때문에 유저가 accent color 값을 변경할 때 시스템이 해당 색상은 재정의하지 않는다. 자세한 내용은 [Sidebars](https://developer.apple.com/design/human-interface-guidelines/sidebars)를 참조하세요.

<img width="246" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/e120742c-d084-4b83-bdb6-138741c89255">

iCloud 아이콘은 다른 글리프가 주황색을 사용하더라도 파란색으로 유지된다.

### **[tvOS](https://developer.apple.com/design/human-interface-guidelines/color#tvOS)**

**Consider choosing a limited color palette that coordinates with your app logo.** 
**앱 로고와 일치하는 제한된 색상 팔레트를 선택하는 것을 고려해라.**
색상의 미묘한 사용은 내용을 미루면서 브랜드를 표현하는 데 도움이 될 수 있다.

**Avoid using only color to indicate focus.
focus을 나타내기 위해 색상만 사용하는 것은 피해라.**
요소가 focus될 때 상호 작용을 나타내는 주요한 방법은 미묘한 스케일링과 반응 애니메이션이다.

### **[watchOS](https://developer.apple.com/design/human-interface-guidelines/color#watchOS)**

**Use pure black for your app’s background color.
앱의 배경색은 순수 블랙을 사용해라.**
#000000의 hex 코드를 가지는 순수 블랙(Pure black)은 애플 워치의 베젤과 완벽하게 결합되어 엣지없는 화면과 같은 착각을 줄 수 있다.

<img width="246" alt="image5" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/07cbc40e-3e4e-4e51-a52b-df342a0462ea">

<img width="200" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/313972ad-3ed8-44bf-9234-d3b551d2b406">

**Recognize that people might prefer graphic complications to use tinted mode instead of full color.
사람들이 풀컬러 대신 tinted mode를 사용하기 위해 그래픽의 복합성을 선호할 수 있음을 인지해라.**
이 시스템은 그래픽 복합성의 이미지, 게이지 및 텍스트에서 워치 착용자가 색상을 기반으로 한 단일 컬러를 사용할 수 있다. 자세한 내용은 [Complications](https://developer.apple.com/design/human-interface-guidelines/complications)를 참조하세요.


</br></br>
##### [Color | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/color)
