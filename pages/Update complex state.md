- normal way
  collapsed:: true
	- ```
	    normalInc: () =>
	      set((state) => ({
	        deep: {
	          ...state.deep,
	          nested: {
	            ...state.deep.nested,
	            obj: {
	              ...state.deep.nested.obj,
	              count: state.deep.nested.obj.count + 1
	            }
	          }
	        }
	      })),
	  ```
- Immer
  collapsed:: true
	- ```
	    immerInc: () =>
	      set(produce((state: State) => { ++state.deep.nested.obj.count })),
	  ```
- optics-ts
	- ```
	    opticsInc: () =>
	      set(O.modify(O.optic<State>().path("deep.nested.obj.count"))((c) => c + 1)),
	  ```
	- ###
	- Best for **strongly-typed, complex nested state management**.
	-
- ramda
  collapsed:: true
	- ```
	    ramdaInc: () =>
	      set(R.modifyPath(["deep", "nested", "obj", "count"], (c) => c + 1)),
	  ```