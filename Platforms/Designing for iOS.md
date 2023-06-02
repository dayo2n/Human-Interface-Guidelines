# Platforms

## Designing for iOS

```
📱 People depend on their iPhone to help them stay connected, play games, view media, 
   accomplsh tasks, and track personal data in any location and while on the go.
```

iOS 앱이나 게임 디자인에 들어갈 때, iOS 경험을 구분하는 다음과 같은 기본적인 기기의 특성과 패턴을 이해하는 것부터 시작하라. 이런 특징과 패턴을 사용해 디자인을 결정하는 것이 아이폰 사용자가 좋아하는 앱을 제공하는 데 도움이 된다.

**Display.** 아이폰은 **중간 사이즈**의 **고해상도** 디스플레이를 가진다.

**Ergonomics.** 사람들은 일반적으로 아이폰을 한 손 또는 두손으로 들고, 필요에 따라 가로와 세로 방향을 바꾼다. 사람들이 기기와 상호 작용하는 동안, 그들의 시야거리는 30에서 60cm도 되지 않는 경향이 있다.

**Inputs.** Multi-Touch [gestures](https://developer.apple.com/design/human-interface-guidelines/touchscreen-gestures), [onscreen keyboards](https://developer.apple.com/design/human-interface-guidelines/onscreen-keyboards), 그리고 [voice](https://developer.apple.com/design/human-interface-guidelines/siri) control를 통해 이동 중에도 작업을 수행하고 의미있는 작업을 완수할 수 있다. 게다가 사람들은 종종 앱이 자신의 개인정보를 사용하고 기기의 자이로스코프, 가속도계에서 입력하기를 원하며, 공간 상호 작용에도 참여하기를 원하기도 한다.

**App interactions.** 때때로 사람들은 이벤트 확인나 소셜 미디어 업데이트, 데이터 추적 또는 메시지 전송에 1-2분씩 소요한다. 다른 때에는 웹 브라우징, 게임 또는 미디어를 즐기는데 한시간 이상의 시간을 쓰기도 한다. 사람들은 전형적으로 동시에 여러 앱을 열기도 하고, 그 앱들 사이에 자주 전환할 수 있음에 감사함을 느낀다.

**System features.**  iOS는 친밀하고 일관된 방식과 사람들이 시스템과, 앱과 상호작용할 수 있도록 도와주는 여러가지 기능을 제공한다. 

- [*Widgets*](https://developer.apple.com/design/human-interface-guidelines/widgets)
- [*Home Screen quick actions*](https://developer.apple.com/design/human-interface-guidelines/home-screen-quick-actions)
- [*Spotlight*](https://developer.apple.com/design/human-interface-guidelines/searching)
- [*Shortcuts*](https://developer.apple.com/design/human-interface-guidelines/siri#Shortcuts-and-suggestions)
- [*Activity views*](https://developer.apple.com/design/human-interface-guidelines/activity-views)

### Best practices

훌륭한 아이폰 경험은 사람들이 가장 가치있게 여기는 플랫폼과 기기 기능을 통합한다. 디자인이 iOS에서 편안함을 느낄 수 있도록, 다음과 같은 특징과 기능을 통합하는 방법의 우선순위를 정하라.

- 최소한의 작용으로 보조적인 디테일과 액션을 찾을 수 있게 하면서 화면 컨트롤의 수를 제한하여, **기본적인 작업과 내용에 집중**할 수 있도록 지원하기
- 기기의 orientation(화면 방향), 다크모드, 다이나믹 타입과 같은 모양 변경을 원활하게 적용해, 사용자에게 가장 적합한 구성을 선택하기
- 사용자들이 주로 기기를 잡는 방식을 수용하는 인터랙션을 지원하기
    
    예를 들어, 기기 디스플레이의 중간 또는 아래쪽에 배치되어 있는 컨트롤에 도달하는 것이 더 쉽고 편리한 경향이 있으므로, 목록의 행에서 이전 화면으로 이동하거나 작업을 시작할 수 있도록 하는 것이 특히 중요하다.
- 사용자의 허가를 받아 플랫폼 기능을 통해 사용가능한 정보를 사용자에게 데이터입력을 요청하지 않고 통합하여 사용자 경험을 향상시키기
    
    예를 들어, 결제를 수락하거나, 생체 인증을 통해 보안을 제공하거나 위치 사용 기능을 제공할 수 있다.

    
</br></br>
##### [Designing for iOS | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/designing-for-ios)
