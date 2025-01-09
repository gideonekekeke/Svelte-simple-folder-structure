<script>
	import MainLayout from "./layouts/MainLayout.svelte";
	import Home from "./pages/Home.svelte";
  import About from "./pages/About.svelte";
  import Contact from "./pages/Contact.svelte";
	import DashboardLayout from "./layouts/DashboardLayout.svelte";

  const currentPath = window.location.pathname
  const user = true
  
  
</script>

<main>
 
 
 {#if !user} 
 <MainLayout>
   <div>
     <!-- Your Svelte app goes here -->
    {#if currentPath === '/'}
    <Home  />
      {:else if currentPath === '/about'}
      <About  />
        {:else if currentPath === '/contact'}
        <Contact  />
         {:else}
    <h1>404 - Page Not Found</h1>
  {/if}
   </div>
 </MainLayout>
 
 {:else}
 <DashboardLayout >
  <div>this is the dashboard</div>
 </DashboardLayout>
 {/if}
 
</main>
















