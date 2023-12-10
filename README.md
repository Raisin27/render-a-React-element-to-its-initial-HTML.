# render-a-React-element-to-its-initial-HTML.
render a React element to its initial HTML.
...
import ReactDOMServer from "react-dom/server";

export default function App() {
  useEffect(() => {
    const msg = document.createElement("div");
    msg.innerHTML = ReactDOMServer.renderToString(
      <Link to="/">
        <div>
          <h3>Title</h3>
          <p> some message...</p>
        </div>
      </Link>
    );

    document.body.appendChild(msg);
  }, []);

  return null;
}
