<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App',
  created() {
    let urlFromRequest = new URL(window.location.href);

    console.log(urlFromRequest);
    // console.log(urlFromRequest.search);      
    let propParams = new URLSearchParams(urlFromRequest.search);

    // console.log(document.referrer);


    console.log(propParams);

    let keyForSaveAuthTokenInLocal = propParams.getAll("state")[0];

    console.log(keyForSaveAuthTokenInLocal);



    window["cafe24aimedisonkeywordappshopid"] = keyForSaveAuthTokenInLocal;




  }
}
</script>
