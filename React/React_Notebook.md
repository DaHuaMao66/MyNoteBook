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
