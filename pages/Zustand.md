- Update complex state:
	- Normal way
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
	- optics-ts
		-
	- Ramda:
-