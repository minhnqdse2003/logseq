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
  collapsed:: true
	- ```
	  import { create } from 'zustand'
	  
	  //It just merge the nested key with the original state but the child of it 
	  //Need to merge by using spread operator
	  const useCountStore = create((set) => ({
	    nested: { count: 0 },
	    inc: () =>
	      set((state) => ({
	        nested: { ...state.nested, count: state.nested.count + 1 },
	      })),
	  }))
	  
	  ```
- How to disable
	- ```
	  set((state) => newState, true)
	  ```