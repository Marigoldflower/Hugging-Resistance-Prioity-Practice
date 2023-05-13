# Hugging-Resistance-Prioity-Practice

## Hugging, Resistance Priority 사용할 때 간단히 기억해야 할 2가지 

1. 우선 Content Hugging Priority와 Content Compression Resistance Priority가 생기려면 **"먼저 오토레이아웃을 설정해줘야 한다는 것을 기억해야 한다."** 오토레이아웃을 설정해준 후부터 Content Hugging Priority와 Content Compression Resistance Priority를 설정해줄 수 있다. 

2. Content Hugging Priority와 Content Compression Resistance Priority가 정확히 하는 일은 두 객체를 서로 비교하여 우선순위가 높고 낮음에 따라 변화를 주는 것이다. 즉, Content Hugging Priority와 Content Compression Resistance Priority를 적용하려면 **"반드시 객체가 2개 이상 존재해야 한다."**

--------------

* Content Hugging Priority와 Content Compression Resistance Priority를 살펴보니 Content Hugging Priority는 Horizontal과 Vertical의 크기가 각각 251로 설정이 되어있고 Content Compression Resistance Priority는 Horizontal과 Vertical의 크기가 각각 750으로 설정이 되어있다. 이게 무슨 뜻일까? 

--------------

## Content Hugging Priority 설명 

1. 하나하나 예를 들어서 설명해보겠다. A라는 객체와 B라는 객체가 있다고 가정해보자. 그리고 둘 다 "작은 크기의 객체"라고 가정하자. 우선 A라는 객체의 top, leading, trailing을 20으로 잡고, B라는 객체의 top, trailing을 20으로 잡겠다. 

2. 그러면 A가 View로부터 leading 영역이 20만큼 떨어져 있을 것이고,B가 A로부터 leading 영역이 20만큼 떨어져 있겠지? 이 상태라면 두 객체 모두 크기가 작으므로 "공간이 많이 남을 것 아닌가?" 이런 상태에서

> Content Hugging Priority: **"공간이 많이 남을 때"**, 우선순위가 낮은 쪽의 **"크기를 늘어나게 하는 것"**
> - A라는 객체를 클릭한 후 : 
> A의 Hugging Priority를 낮춰주면 우선순위가 더 높은 B가 크기를 유지하고 우선순위가 더 낮은 A의 크기가 늘어나게 된다.	


## Content Compression Resistance Priority 설명

1. 그렇다면 반대로 A라는 객체와 B라는 객체 "모두 크기가 엄청 크다고 가정해보자."
우선 A라는 객체의 top, leading, trailing을 20으로 잡고, B라는 객체의 top, trailing을 20으로 잡겠다. 

2. 그러면 A가 View로부터 leading 영역이 20만큼 떨어져 있을 것이고, B가 A로부터 leading 영역이 20만큼 떨어져 있을 것이다.
이 상태라면 두 객체 모두 크기가 너무 크므로 "공간이 많이 부족할 것 아닌가?" 이런 상태에서 

> Content Compression Resistance Priority: "공간이 많이 부족할 때", 우선순위가 낮은 쪽의 "크기를 줄이는 것"
> - A라는 객체를 클릭한 후 :
> A의 Compression Resistance Priority를 낮춰주면 우선순위가 더 높은 B가 크기를 유지하고 우선순위가 더 낮은 A의 크기가 줄어들게 된다.

