- No need to use spread operator to set an immutable state
	- ```
	  // No need
	  set((state) => ({ ...state, count: state.count + 1 }))
	  
	  //Instead
	  //Reason: As set api also auto merge the new key value with the original one
	  //So spread operator to clone a new state is not neccessary
	  set((state) => ({ count: state.count + 1 }))
	  ```
- **Notices**: set api also support for deep level 1 which mean it's only supported ["state","count"] but not supported ["state","nested","count"]
	- ```
	  ```