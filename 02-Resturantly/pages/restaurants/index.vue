<template>
  <div>
    <Html :lang="30 <= 50 ? 'en-GB' : 'en-US'" >
      <Head>
        <Title>TOP-50</Title>
        <Meta 
          name="description"
          content="My awesome Nuxt3 web app"
        />
        <Link 
          rel="preload"
          href="https://www.iconpacks.net/icons/2/free-sad-face-icon-2691-thumb.png"
          as="script"
        />
      </Head>
    </Html>
    <NuxtLayout name="custom">
      <div class="container">
        <RestaurantTable />
      </div>
    </NuxtLayout>
  </div>
</template>