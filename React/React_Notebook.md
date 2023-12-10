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

#### Inverse Data Flow

In react,the data flow direction is always **_one-way_**⬇  
which means the data will not be passed from children  
**components** to parent **components**.

```javascript
export default function App() {
  const [items, setItems] = useState([]);

  function handleAddItems(item) {
    setItems((items) => [...items, item]);
    console.log(items);
  }

  return (
    <div className="app">
      <Form onAddItems={handleAddItems} />
    </div>
  );
}

function Form({ onAddItems }) {
  const [description, setDescription] = useState("");
  const [quantity, setQuantity] = useState(1);

  function handleSubmit(e) {
    e.preventDefault();

    if (!description) return;
    const newItem = { description, quantity, packed: false, id: Date.now() };
    console.log(newItem, "NewItem OBJ has been created!!");

    onAddItems(newItem);

    setDescription("");
    setQuantity(1);
  }

  return (
    <form className="add-form" onSubmit={handleSubmit}>
      <h3>What do you need fot your trip 😋?</h3>
      <select value={quantity} onChange={(e) => setQuantity(+e.target.value)}>
        {Array.from({ length: 20 }, (_, i) => i + 1).map((num) => (
          <option value={num} key={num}>
            {num}
          </option>
        ))}
      </select>
      <input
        type="text"
        placeholder="Item..."
        value={description}
        onChange={(e) => setDescription(e.target.value)}
      ></input>
      <button>ADD</button>
    </form>
  );
}
```
