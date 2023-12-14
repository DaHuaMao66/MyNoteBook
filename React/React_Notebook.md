# React Notebook✅

## State Management

#### When to create state❓

#### What type of it are necessary❓

#### Where to place them ❓

![Alt Answers](image.png)

### Global State VS. Local State 🤔

|        LOCAL STATE         |            GLOBAL STATE             |
| :------------------------: | :---------------------------------: |
| one or few components uzit |        many components uzit         |
|  defined inside component  | shared for all component in the app |

#### Inverse Data Flow 🤔

In react,the data flow direction is always **_one-way_**⬇  
which means the data will not be passed from children  
**components** to parent **components**.
The "Lifting Up State" can solove that scene.  
**_Move the state to parent component and pass the [state,setState]  
as props._**

#### State Derived 🤔

Sometime we don't have to create State variable  
just simplily derive state from exsit state.

**_Example_**✅: we derive num state & totalPrice state  
from cart state
![Alt text](image-1.png)  
**Every single we update state cause the component re-render.💔**

## Children Props 🤔

children Props can make our components  
be re-usable.
Imagine that you want to show some different  
description on **_Button Components_**,and  
now you can pass **component** as a prop to Component you want to render,this **component** will be received by reserve variable 'children'.
For Example😀:

![Alt text](image-5.png)

## Component Categories Logically 🤔

#### Stateless Components

No State.  
Can receive props and simplly present receive data or content.  
Usually small and reusable.

#### Stateful Components

Have state.  
Can still be reusable.

#### Sructureal Components

"Pages","layouts"......  
Result of composition.
Can be Huge and non-reusable

![Alt text](image-4.png)

#### Props Drilling 🤔

Sometimes,the component nested so much  
In order to pass Prop to the Target Component  
we must keep passing the props over and  
over again which is noisying.😫

#### How to fix Props Drilling 😀

The Answer is **_Children Props_**

![Alt text](image-6.png)

# How actually things work intenally inside React✅

#### Components && Instances && Elements

![Alt text](image-9.png)
![Alt text](image-8.png)
![Alt text](image-10.png)
![Alt text](image-11.png)

##### Summary 😋

Actually,React does not directly manipulate  
**_DOM_**,but it will create some **_elements_** by  
calling React Functions. And this kind of elements are bascially comprise with some  
instances of **_ReactComponent_** which is function  
we defined in component related file,those  
components will return **_JSX_** when we use it.

### Tip: Component != JSX but invole it

Components encapsulate the behavior and  
structure of UI.They can be function or classes that return **_JSX_**,defining how the **_UI_** looks like based on the component's logic and props.

## ------------------------------------

### Componrnt(Instances) Lifecycle🤔

Before we learn about the hook **_useEffect_**  
section **which** we should konw something  
about lifecycle of a component.

![Alt text](image-7.png)

### How Rendering Work🤔

#### OverView

![Alt text](image-12.png)
![Alt text](image-13.png)
![Alt text](image-14.png)

### Rendering Phase ✅

![Alt text](image-17.png)

##### The Mechanics Of State In React

![Alt text](image-16.png)

##### Virtual Dom

![Alt text](image-15.png)

##### Recociliation By Recociler:Fiber

![Alt text](image-18.png)
![Alt text](image-19.png)
![Alt text](image-20.png)
![Alt text](image-21.png)

### Commit Phase ✅

![Alt text](image-22.png)
![Alt text](image-23.png)

### Summary Process Of Rendering

![Alt text](image-24.png)

### Effects And Data Fetching ✅
