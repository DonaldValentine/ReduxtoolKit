# Redux Toolkit  

The official, batteries-included toolset for efficient Redux development.  
👉 Visit: [ReduxToolkit.com](https://reduxtoolkit.com/)  

---

## 🚀 Installation  

### Create a React Redux App  
The recommended way to start a new app with Redux Toolkit is by using our official templates:  

- **Vite + Redux + TypeScript**  
```bash
npx degit reduxjs/redux-templates/packages/vite-template-redux my-app

- **Next.js + Redux**  

These templates already include Redux Toolkit and React-Redux configured, with a small example project.  

### Existing Apps  
You can also install Redux Toolkit directly:  


---

## 📘 Documentation  

Full guides and API references are available on:  
- [Redux Toolkit Docs](https://reduxtoolkit.com/)  
- [Redux Core Docs](https://redux.js.org/)  

Learn everything from store setup to advanced features like RTK Query.  

---

## 🎯 Purpose  

Redux Toolkit was created to solve common concerns about Redux:  

- Store setup feels too complex  
- Too many extra packages are required  
- Too much boilerplate code  

Redux Toolkit simplifies this by providing good defaults, utility functions, and an optional data-fetching toolset (RTK Query).  

---

## 📦 What’s Included  

- `configureStore()` – Simplified store setup with good defaults  
- `createReducer()` – Cleaner reducer logic with **immer** support  
- `createAction()` – Auto-generates action creators  
- `createSlice()` – Combines reducer + actions into one slice  
- `combineSlices()` – Manage multiple slices easily  
- `createListenerMiddleware()` – Lightweight async side-effects  
- `createAsyncThunk()` – Handle async logic with pending/success/failure actions  
- `createEntityAdapter()` – Manage normalized data  
- `createSelector()` – Built-in selectors (re-exported from Reselect)  

---

## 🔍 RTK Query  

RTK Query is included inside Redux Toolkit as an optional add-on for **data fetching & caching**.  

### Key Features:  
- `createApi()` – Define API endpoints for your app  
- `fetchBaseQuery()` – Lightweight wrapper around `fetch`  
- React hooks auto-generated for your endpoints  
- Works seamlessly with Redux DevTools  

Example usage:  

```js
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react'

export const api = createApi({
  baseQuery: fetchBaseQuery({ baseUrl: '/api' }),
  endpoints: (builder) => ({
    getPosts: builder.query({ query: () => 'posts' }),
  }),
})

export const { useGetPostsQuery } = api
