<template>
  <div class="container">
   
    <Header />
    <div class="container-agroup">
      <Card typeCard="Basic" valueCard="22.99" />
      <CardHome typeCard="Professional" valueCard="32.00" />
      <Card typeCard="Master" valueCard="30.00" />
    </div>
  </div>
</template>

<style>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.container-agroup {
  display: flex;
}

</style>
