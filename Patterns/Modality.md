# Modality

```
Modality is a design technique that presents content in a separate, 
focused mode that prevents interaction with the parent view and requires an explicit action to dismiss.
모달리티는 상위 뷰와 상호 작용을 방지하고,
명시적인 작업이 필요한 별도의 집중 모드로 콘텐츠를 표시하는 디자인 기법이다.
```

<img width=800 src="https://docs-assets.developer.apple.com/published/9efb35fd7fafa01ce3447dc6f13ae2d8/patterns-modality-intro@2x.png">

콘텐츠를 모달로 표시하는 것은:

- 사용자가 중요한 정보를 수신하고, 필요한 경우 조치를 취하도록 보장
- 최근 작업을 확인하거나 수정할 수 있는 옵션 제공
- 사용자가 이전 컨텍스트를 놓치지 않고 범위가 좁은 개별 작업을 수행할 수 있도록 지원
- 사용자에게 몰입감 있는 경험을 제공하거나 복잡한 작업에 집중할 수 있도록 지원

플랫폼에 따라 다양한 구성 요소를 사용하여 이러한 유형의 모달 경험을 제공할 수 있다. 예를 들어, 모든 플랫폼은 앱과 관련된 중요한 정보를 전달하는 모달 뷰인 알림을 표시할 수 있다. 또한 각 플랫폼은 activity views, sheets 및 confirmation dialogs 또는 action sheets와 같은 상황별 옵션을 표시하기 위한 다양한 유형의 모달 뷰를 정의할 수 있다. 사람들이 다른 작업을 수행할 수 있도록 돕기 위해 iOS, iPadOS 및 macOS 앱은 sheets 또는 popovers를 사용하는 경향이 있지만, macOS 및 iPadOS 앱도 별도의 창을 사용할 수 있다.   

미디어 보기와 같은 일시적인 몰입형 경험을 제공하거나 콘텐츠 편집과 같은 고유하고 다단계 작업에 집중할 수 있도록 앱은 full-screen 모달 경험을 제공할 수 있다. 이와 대조적으로, 앱은 비모달 유형의 full-screen 경험을 제공할 수도 있다. 지침은 [Going full screen](https://developer.apple.com/design/human-interface-guidelines/going-full-screen)을 참조하라.

### **[Best practices](https://developer.apple.com/design/human-interface-guidelines/modality#Best-practices)**

**Present content modally only when there’s a clear benefit.   
명확한 이점이 있을 때만 콘텐츠를 모달로 표시하라.**   
모달 경험은 사람들을 현재 상황에서 벗어나게 하고 무시할 조치가 필요하므로, 사람들이 집중하거나 콘텐츠나 기기에 영향을 미치는 선택을 하는 데 도움이 될 때만 모달리티를 사용하는 것이 좋다.   

**Aim to keep modal tasks simple, short, and narrowly focused.   
모달 작업은 단순하고 짧고 좁게 집중하는 것을 목표로 하라.**    
모달 태스크가 너무 복잡할 경우, 사람들은 모달 보기에 들어갈 때 일시 중단한 작업에 대한 추적을 잃을 수 있으며, 특히 모달 뷰가 그들의 이전 컨텍스트를 흐리게 할 경우에는 더욱 그러하다.   

**Take care to avoid creating a modal experience that feels like an app within your app.   
앱 내에서 앱처럼 느껴지는 모달 경험을 만들지 않도록 주의하라.**    
특히 모달 작업 내에 뷰 계층을 표시해버리면 사람들이 자신의 단계를 다시 추적하는 방법을 잊을 수 있다. 모달 작업에 하위 보기가 포함되어야 하는 경우, 계층을 통과하는 단일 경로를 제공하고, 사용자가 모달 뷰를 무시하는 버튼으로 착각할 수 있는 버튼을 포함하지 않아야 한다.   

**Consider using a full-screen modal style for immersive content or a complex task.   
몰입형 콘텐츠 또는 복잡한 작업에는 full-screen 모달 스타일을 사용해라.**   
디스플레이나 윈도우를 채우는 모달 체험은 방해를 최소화하므로 비디오, 사진 또는 카메라 뷰를 표시하거나 문서를 마크업하거나 사진 편집 등의 다단계 작업을 지원할 수 있다.   

**Always give people an obvious way to dismiss a modal view.   
항상 사람들에게 모달 뷰를 무시할 수 있는 명백한 방법을 제공하라.**    
일반적으로 사람들이 이미 알고 있는 플랫폼 규약을 따르는 것이 효과적이다. 예를 들어, iOS, iPadOS 및 watch의 경우, 일반적으로 사람들은 네비게이션 바에서 버튼을 찾거나 아래로 스와이프하기를 기대한다. macOS와 tvOS 앱에서 사람들은 메인 콘텐츠 뷰에서 버튼을 찾기를 기대한다.   

**When necessary, help people avoid data loss by getting confirmation before closing a modal view.   
필요한 경우, 모달 뷰를 닫기 전에 확인을 받아 사용자가 데이터 손실을 방지할 수 있도록 지원하라.**   
사람들이 dismiss 제스처를 사용하든 버튼은 사용하든, 보기를 닫으면 사용자가 생성한 콘텐츠가 손실될 수 있다면 상황을 설명하고 해결 방법을 제공해야 한다. 예를 들어 iOS에서 저장 옵션이 포함된 작업 sheet를 표시할 수 있다.   

**Make it easy to identify a modal view’s task.   
모달 뷰의 작업을 쉽게 식별할 수 있다.**    
사람들이 모달 뷰가 열릴 때, 그들은 이전 컨텍스트로부터 전환하고 바로 돌아가지 않을 수 있다. 모달 뷰의 작업 이름을 지정하는 타이틀이나, 작업을 설명하거나 지침을 제공하는 추가 텍스트를 제공하면 다른 사용자가 앱에서 자신의 위치를 유지하도록 도울 수 있다.   

**Avoid presenting a modal view on top of another modal view.   
다른 모달 뷰 위에 모달 뷰를 표시하지 않도록 한다.**    
동시에 화면에 나타나는 여러 모달 뷰는 사람들이 이전 컨텍스트를 두 개 이상 기억해야 하기 때문에 혼란스러울 수 있다. 중요한 정보를 전달하기 위해 경고가 다른 모든 콘텐츠 위에 나타날 수 있지만, 동시에 화면에 두 개 이상의 경고가 표시되는 것은 매우 혼란스러운 일이다.   

<img width=900 src="https://github.com/dayo2n/Human-Interface-Guidelines/assets/57654681/7c3a1b02-a654-4e9f-bd5a-714359d68d82">

그러나 애플 뮤직의 계정 > 계정 설정은 모달 뷰 위에 모달 뷰를 표시하고 있다....예외일까?


</br></br>
##### [Modality | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/modality)
