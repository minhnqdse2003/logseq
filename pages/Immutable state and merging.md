- No need to use spread operator to set an immutable state
	- ```
	  // No need
	  set((state) => ({ ...state, count: state.count + 1 }))
	  
	  //Instead
	  set((state) => ({ count: state.count + 1 }))
	  ```
- **Notices**: