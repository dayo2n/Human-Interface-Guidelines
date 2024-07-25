
# **Collections**

```swift
A collection manages an ordered set of content and presents it in a customizable and highly visual layout.
컬렉션은 정렬된 컨텐츠 셋을 관리하고, 시각적으로 뛰어나며 커스텀 가능한 레이아웃을 제공한다.
```

<img width="800"  src="https://github.com/user-attachments/assets/4cb0ead8-a753-4b4d-a7f6-186eca99e032">   

일반적으로 컬렉션은 이미지 기반 콘텐츠를 보여주는 데 사용한다.


## **[Best practices](https://developer.apple.com/design/human-interface-guidelines/collections#Best-practices)**

**Use the standard row or grid layout whenever possible.    
가능한 표준 행 또는 그리드 레이아웃을 사용하라.**  
이는 사람들이 기대하는 간단하고 효과적인 형태이다. 사람들을 혼란스럽게 하거나 불필요한 주의를 끌 수 있는 지정 레이아웃을 만드는 것은 피해야 한다.

**Consider using a table instead of a collection for text.   
텍스트에 대해서는 컬렉션 대신 테이블을 사용할 것을 고려하라.**   
스크롤 가능한 목록에 표시되는 것이 텍스트 정보를 보고 소화하는 데에 일반적으로 더 간단하고 효율적이다. 

**Make it easy to choose an item.   
아이템을 선택하기 쉽게 만들어라.**   
컬렉션에서 아이템을 찾는 것이 너무 어렵다면 사람들이 좌절하기 쉬워 원하는 콘텐츠에 도달하기 전에 관심을 잃을 것이다. 이미지 주변에 적절한 패딩을 사용해 focus나 hover 효과를 쉽게 볼 수 있도록 하고 콘텐츠가 겹치지 않게 한다.

**Add custom interactions when necessary.   
필요시 커스텀 인터랙션을 추가하라.**   
레이블을 짧게 유지하려면 불필요한 단어를 생략하라. 예를 들어, 메일은 Flagged나 Drafts와 같은 보다 간결한 용어를 사용하여 각 우편함의 제목에서 Messages라는 단어를 생략한다. 

**Consider using animations to provide feedback when people insert, delete, or reorder items.   
사람들이 아이템을 삽입, 삭제 또는 재정렬할 때 피드백을 제공하기 위한 애니메이션 사용을 고려하라.**   
컬렉션은 이러한 작업에 대한 표준 애니메이션을 제공하며 커스텀도 사용할 수 있다.

## **[Platform considerations](https://developer.apple.com/design/human-interface-guidelines/collections#Platform-considerations)**

*No additional considerations for macOS, tvOS or visionOS. Not supported in watchOS.*   
*macOS, tvOS, visionOS에서 추가적으로 고려할 사항은 없으며, watchOS에서는 지원되지 않는다.*   

### **[iOS, iPadOS](https://developer.apple.com/design/human-interface-guidelines/collections#iOS-iPadOS)**

**Use caution when making dynamic layout changes.   
동적 레이아웃 변경에는 주의하라.**    
컬렉션의 레이아웃은 동적으로 변경될 수 있다. 모든 변경 사항이 의미있고 추적이 쉬운지 확인해야 한다. 가능하다면, 명시적 액션에 대한 응답이 아닌 한, 사람들이 보고 상호작용하는 동안에는 레이아웃을 변경하지 않아야 한다.


</br></br>
##### [Collections | Apple Developer Documentation](https://developer.apple.com/design/human-interface-guidelines/collections)
