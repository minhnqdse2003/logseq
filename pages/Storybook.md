- ```
  npx storybook@latest init
  ```
- Added this line to use tailwind in ***`preview.ts`*** in `.storybook/.....`
  ```
  import type { Preview } from '@storybook/react'
  import 'tailwindcss/tailwind.css' # Add this line
  
  const preview: Preview = {
    parameters: {
      controls: {
        matchers: {
          color: /(background|color)$/i,
          date: /Date$/i,
        },
      },
    },
  }
  
  export default preview
  ```