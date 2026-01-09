```jsx
import "./styles.css";
import { useState } from "react";

// Single BookToggle component
function BookToggle({ title }) {
  const [isRead, setIsRead] = useState(false); // private state per component

  return (
    <div>
      <button onClick={() => setIsRead((prev) => !prev)}>
        {title}: {isRead ? "Read" : "Not Read"}
      </button>
    </div>
  );
}

export default function App() {
  const books = [
    { id: 1, title: "Book A" },
    { id: 2, title: "Book2" },
    { id: 3, title: "Book3" },
  ];

  return (
    <div className="App">
      {books.map((book) => (
        <BookToggle key={book.id} title={book.title} />
      ))}
    </div>
  );
}
//<BookToggle title="Book A" />
//<BookToggle title="Book B" />
//<BookToggle title="Book C" />


```
