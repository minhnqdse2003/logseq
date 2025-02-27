- Optimize meta data
  logseq.order-list-type:: number
  collapsed:: true
	- ```
	  import Head from 'next/head'
	  - //Page route
	  export default function Page() {
	  return (
	    <Head>
	      <title>Page Title</title>
	      <meta name="description" content="Page Description" />
	      <link rel="canonical" href="https://example.com/page" />
	    </Head>
	  )
	  }
	  - //App route
	  export const metadata = {
	  title: 'Page Title',
	  description: 'Page Description',
	  }
	  ```
- URL Structure and Routing
  logseq.order-list-type:: number
- logseq.order-list-type:: number