# 🎬 React MovieFlix

MovieFlix is a simple and fast React application built with **Vite**,
**Tailwind CSS**, and **TMDB API**.\
It allows users to **search movies**, view trending/popular movies, and
browse results in a clean UI.

## 🚀 Live Demo

https://cloud.shanto.net/

## 📦 Features

-   🔍 Instant movie search with debounce\
-   🎞 Popular movies on first load\
-   ⚡ Fast performance powered by Vite\
-   🎨 Modern UI with Tailwind CSS\
-   🔄 Loading state handling\
-   ❌ Error handling for failed API calls\
-   📱 Fully responsive layout

## 🛠️ Tech Stack

-   React 18\
-   Vite\
-   Tailwind CSS\
-   TMDB API\
-   Custom Debounce Hook / use-debounce

## 📂 Project Structure

    src/
    │── component/
    │   ├── Search.jsx
    │   ├── Spinner.jsx
    │   └── MovieCard.jsx
    │
    │── App.jsx
    └── main.jsx

## 🔧 Installation & Setup

### 1️⃣ Clone the repository

``` bash
git clone https://github.com/shanto-w3dev/React-MovieFlix.git
cd React-MovieFlix
```

### 2️⃣ Install dependencies

``` bash
npm install
```

### 3️⃣ Replace the `.env.example` file by creating a `.env.local` file and add your credentials

    VITE_TMDB_API_KEY=[Your TMDB API Key]
    VITE_APPWRITE_PROJECT_ID =[Your Appwrite ID]
    VITE_APPWRITE_DATABASE_ID= [Your Appwrite Database ID]
    VITE_APPWRITE_TABLE_COLLECTION_ID=[Your Appwrite Table ID]

### 4️⃣ Start the development server

``` bash
npm run dev
```

## 🧩 Debouncing

``` js
import { useDebounce } from "use-debounce";
const [debouncedSearch] = useDebounce(searchTerm, 500);
```

Or custom hook:

``` js
export default function useDebounce(value, delay = 500) {
  const [debouncedValue, setDebouncedValue] = useState(value);
  useEffect(() => {
    const timer = setTimeout(() => setDebouncedValue(value), delay);
    return () => clearTimeout(timer);
  }, [value, delay]);
  return debouncedValue;
}
```

## 🧪 Scripts

``` bash
npm run dev
npm run build
npm run preview
```

## 🚀 Deployment

Vercel or Netlify recommended.\
Set env: `VITE_TMDB_API_KEY`

## 🤝 Contribution

1.  Fork\
2.  Branch\
3.  Commit\
4.  PR

## 📄 License

For personal and learning use.
