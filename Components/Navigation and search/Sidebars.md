
# **Sidebars**

```swift
A sidebar can help people navigate your app or game, 
providing quick access to top-level collections of content.
사이드바는 사용자가 앱을 탐색할 수 있도록 도와주며, 
최상위 수준의 콘텐츠 모음에 빠르게 액세스할 수 있도록 지원한다.
```

<img width="800" alt="스크린샷 2023-06-07 오후 11 12 47" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/7a9e24a5-be27-476b-b3c8-22bd8dc53db0">   


sidebar라는 용어는 [split view](https://developer.apple.com/design/human-interface-guidelines/split-views)의 기본 창에 거의 항상 표시되는 최상위 앱 영역 및 컬렉션 목록을 나타낸다. 사용자가 사이드바에서 항목을 선택하면 스플릿 뷰는 항목의 세부 정보를 보조 창에 표시하거나 항목에 목록이 포함된 경우 보조 창에 목록을 표시하고 세 번째 창에 세부 정보를 표시합니다. 예를 들어 iOS, iPadOS 및 macOS의 메일은 사이드바 스타일과 동작을 사용해 계정 및 우편함 목록을 표시한다. 일반적으로 메시지 목록은 보조 창에 표시되고 메시지 내용은 세 번째 창에 표시된다.

<img width="800" alt="스크린샷 2023-06-07 오후 11 12 47" src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/eae0fa43-93e8-4814-825c-f200e458767a">


사이드바 레이아웃은 특히 사이드바와 함께 제공되는 창을 화면에 동시에 표시하려는 경우 수평 공간이 많이 소요될 수 있다. 콤팩트한 환경에서는 [tab bar](https://developer.apple.com/design/human-interface-guidelines/tab-bars)와 같은 대체 구성 요소를 고려할 수 있다.

```plain text
Developer note
When you use SwiftUI to construct a sidebar interface, 
you automatically get platform-appropriate appearance and behavior.
For developer guidance, see NavigationSplitView.
If you don’t use SwiftUI, you can instead use UISplitViewController or NSSplitViewController.

SwiftUI를 사용하는 경우,
사이드바 인터페이스를 구성하는 UI는 플랫폼에 적합한 모양과 동작을 자동으로 제공한다.
개발자 지침은 NavigationSplitView를 참고하라.
스유를 사용하지 않으면 대신 UISplitViewController 또는 NSSplitViewController를 사용할 수 있다.

ref.
NavigationSplitView | https://developer.apple.com/documentation/SwiftUI/NavigationSplitView
UISplitViewController | https://developer.apple.com/documentation/uikit/uisplitviewcontroller
NSSplitViewController | https://developer.apple.com/documentation/appkit/nssplitviewcontroller
```

## **[Best practices](https://developer.apple.com/design/human-interface-guidelines/sidebars#Best-practices)**

**Use a sidebar to help people quickly navigate to key areas of your app or top-level collections of content, like folders and playlists.   
사이드바를 사용하면 유저가 앱의 주요 영역이나 폴더 및 재생 목록과 같은 최상위 콘텐츠 컬렉션으로 빠르게 이동할 수 있다.**  
사이드바는 사용자가 여러 피어 정보 카테고리 또는 모드에 동시에 액세스할 수 있도록 정보 계층을 평평하게 만드는 데 도움이 된다.

**When possible, let people customize the contents of a sidebar.   
가능한 경우 사용자가 사이드바의 내용을 커스텀할 수 있다.**   
사이드바를 사용하면 사용자가 앱의 주요 영역으로 이동할 수 있으므로 사용자가 어떤 영역이 가장 중요하고 어떤 순서로 나타나는지 결정할 수 있을 때 잘 작동한다.   

**Consider letting people hide the sidebar.   
사람들이 사이드바를 숨길 수 있도록 해라.**     
사람들은 때때로 사이드바를 숨겨 콘텐츠 세부사항에 대한 공간을 늘리고 싶어한다. 가능한 경우, 사람들이 이미 알고 있는 플랫폼별 상호 작용을 사용해 사이드바를 숨기거나 표시할 수 있다. 예를 들어, iPadOS에서 사람들은 내장된 가장자리 스와이프 제스처를 사용할 수 있을 것으로 예상한다. macOS에서 show/hide 버튼을 포함하거나 사이드바 표시 및 숨기기 명령을 앱의 메뉴에 추가할 수 있다. 사이드바가 찾을 수 있는 상태로 유지되도록, 디폴트로 사이드바를 숨기지 마라.   

**In general, show no more than two levels of hierarchy in a sidebar.   
일반적으로 사이드바에 계층 수준을 두 층 이하로 표시한다.**   
데이터 계층이 두 층보다 깊은 경우 사이드바 항목과 상세 보기 사이에 내용 목록이 포함된 스플릿 뷰 인터페이스를 사용하는 것이 좋다.   

**If you need to include two levels of hierarchy in a sidebar, use succinct, descriptive labels to title each group.   
사이드바에 두 단계의 계층 구조를 포함해야 하는 경우, 간결하고 설명적인 레이블을 사용하여 각 그룹의 제목을 지정한다.**   
레이블을 짧게 유지하려면 불필요한 단어를 생략하라. 예를 들어, 메일은 Flagged나 Drafts와 같은 보다 간결한 용어를 사용하여 각 우편함의 제목에서 Messages라는 단어를 생략한다.   

## **[Platform considerations](https://developer.apple.com/design/human-interface-guidelines/sidebars#Platform-considerations)**

*No additional considerations for tvOS. Not supported in watchOS.*   
tvOS에서 추가적으로 고려할 사항은 없으며, watchOS에서는 지원되지 않는다.   

### **[iOS, iPadOS](https://developer.apple.com/design/human-interface-guidelines/sidebars#iOS-iPadOS)**

**In an iOS app, consider using a tab bar instead of a sidebar.   
iOS 앱에서 사이드바 대신 탭바를 사용해라.**    
사이드바 인터페이스는 수평 공간이 많이 필요할 수 있으므로 iPhone에서 특히 세로 방향으로 너무 붐빌 수 있다. 이와 반대로 탭바는 각 섹션 내에서 현재 탐색 상태를 유지하면서 사용자가 앱의 최상위 섹션 간에 빠르게 전환할 수 있도록 지원한다.   

**In an iPadOS app, consider using a sidebar instead of a tab bar.   
iPadOS 앱에서 탭바 대신 사이드바를 사용해라.**   
사이드바는 많은 항목을 표시할 수 있기 때문에 아이패드 앱을 보다 효율적으로 탐색할 수 있다. 또한 사용자가 사이드바의 항목을 커스텀하고 더 많은 콘텐츠 공간을 만들기 위해 항목을 숨기도록 할 수 있다.   

**If necessary, apply the correct appearance to a sidebar.   
필요한 경우 사이드바에 올바른 모양을 적용해라.**    
사이드바를 SwiftUI를 사용하지 않고 만드는 경우, 컬렉션 뷰 리스트 레이아웃의 사이드바 모양을 사용할 수 있다. 개발자 지침은 [UICollectionLayoutListConfiguration.Appearance](https://developer.apple.com/documentation/uikit/uicollectionlayoutlistconfiguration/appearance)를 참조.   

### **[macOS](https://developer.apple.com/design/human-interface-guidelines/sidebars#macOS)**

macO에서 source list라고도 하는 사이드바는 창의 전체 높이까지 확장되며, 선택한 항목 하이라이트 표시에 둥근 모서리 모양을 사용한다.   

사이드바의 행 높이, 텍스트 및 글리프 크기는 전체 크기에 따라 달라진다. 크기를 프로그래밍 방식으로 설정할 수 있지만 일반 설정에서 다른 사이드바 아이콘 크기를 선택해 변경할 수도 있다. 아래 표는 macOS에서 사이드바에 대한 기본 메트릭(측정값)을 보여준다.   

| Sidebar size | Sidebar component | Default metrics |
| --- | --- | --- |
| Small | Row height | 24 pt |
| SF Symbol scale | Medium * |  |
| Icon size | 16x16 px @1x |  |
| Text size (style) | 11 pt (Subhead) |  |
| Medium | Row height | 28 pt |
| SF symbol scale | Medium |  |
| Icon size | 20x20 px @1x |  |
| Text size (style) | 13 pt (Body) |  |
| Large | Row height | 32 pt |
| SF Symbol scale | Medium |  |
| Icon size | 24x24 px @1x |  |
| Text size (style) | 15 pt (Title 3) |  |
| All | Horizontal spacing between cells | 17 pt |
| Vertical spacing between cells | 0 pt |  |

*In some cases, a small sidebar uses small-scale SF Symbols by default.   
경우에 따라 작은 사이드바는 기본적으로 작은 크기의 SF 심볼을 사용한다.*   

**Consider using familiar symbols to represent items in the sidebar.   
친숙한 심볼을 사용해 사이드바의 항목을 표시해라.**    
SF symbols는 앱의 항목을 표시하는 데 사용할 수 있는 광범위한 커스텀 가능한 기호를 제공한다. 비트맵 이미지를 사용해 사이드바에 대한 사용자 지정 인터페이스 아이콘을 만들어야 하는 경우 @1x 및 @2x 해상도와 위의 표에 표시된 small, medium, and large 크기로 이미지를 만든다.   

**Avoid stylizing your app by specifying a fixed color for all sidebar icons.   
모든 사이드바 아이콘에 고정 색상을 지정하여 앱 스타일을 변경하지 마라.**    
기본적으로 사이드바 아이콘은 현재 액센트 색상을 사용하며, 사용하는 모든 앱에서 사용자가 선택한 액센트 색상을 볼 수 있다. 고정 색상을 아이콘의 의미를 명확히 하는 데 도움이 될 수 있지만, 대부분의 사이드바 아이콘이 사용자가 선택한 색상이 표시되도록 할 수 있다.   

**If necessary, apply the correct background appearance to a sidebar.   
필요한 경우, 올바른 배경 모양을 사이드바에 적용한다.**    
스유를 사용하지 않는 경우 macOS 앱에서 사이드바를 만들려면 창에 사이드바가 두 개 이상 포함되어 있거나, 패널이나 설정 창에서 사이드바를 사용할 때 불투명한 배경을 지정해야 할 수 있다. 다른 모든 유스케이스에서는 사이드바에 반투명 배경을 사용해라.   

**Consider automatically hiding and revealing a sidebar when its container window resizes.   
컨테이너 창 크기가 조정될 때 사이드바를 자동으로 숨기거나 표시해라.**    
예를 들어, 메일 뷰어 창의 크기를 줄이면 사이드바가 자동으로 축소되어 메시지 내용에 더 많은 공간이 생길 수 있다.   

**In an editable sidebar, avoid placing edit buttons at the bottom edge of the view.   
편집 가능한 사이드바에서 편집 버튼을 뷰의 맨 아래 가장자리에 배치하지 마라.**   
항목에 대한 정보를 추가, 제거, 조작 또는 가져오는 버튼을 제공하는 것을 생각해보자. 뷰의 맨 아래 가장자리가 화면 밖에 있을 때 사이드바 맨 아래에 있는 버튼을 숨길 수 있다. 사용자가 새 사이드바 그룹을 추가할 수 있도록 하려면 그룹 레이블의 뒤에 있는 [disclosure triangle](https://developer.apple.com/design/human-interface-guidelines/disclosure-controls#Disclosure-triangles) 옆에 추가 (+) 버튼을 포함한다. 컨텍스트 메뉴 또는 메뉴 바 메뉴에서 제거 remove와 같은 다른 작업을 제공한다. 예를 들어 컨텍스트 메뉴에서 새 메일박스 명령을 제공하는 것 외에도 메일은 메일박스 메뉴에서 이 명령을 제공한다.   
