- Optimize meta data
  logseq.order-list-type:: number
- ```
  import Head from 'next/head'
  
  export default function Page() {
    return (
      <Head>
        <title>Page Title</title>
        <meta name="description" content="Page Description" />
        <link rel="canonical" href="https://example.com/page" />
      </Head>
    )
  }
  ```