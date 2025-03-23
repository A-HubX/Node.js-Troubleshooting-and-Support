Example:
# Install dependencies
npx create-next-app@latest nextjs-demo-app

cd nextjs-demo-app

# Modify pages/index.js for SSR

pages/index.js:
import React from 'react';

// SSR function to fetch data
export async function getServerSideProps() {
  const res = await fetch('https://api.example.com/data');
  const data = await res.json();
  return { props: { data } };
}

const Home = ({ data }) => (
  <div>
    <h1>Next.js SSR Example</h1>
    <pre>{JSON.stringify(data, null, 2)}</pre>
  </div>
);

export default Home;
