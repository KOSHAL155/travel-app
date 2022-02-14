<template>
<Layout>
    <div class="imgs">
        <img src="../assets/brazil.jpg"/>
    
<div class="all" >
<div class="field">
  <label class="label">Username/Email</label>
  <div class="control has-icons-left has-icons-right">
    <input class="input is-success" type="text" placeholder="Enter Username/Email" value="">
    <span class="icon is-small is-left">
      <i class="fas fa-user"></i>
    </span>
    <span class="icon is-small is-right">
      <i class="fas fa-check"></i>
    </span>
  </div>

</div>

<div class="field">
  <label class="label">Password</label>
  <div class="control has-icons-left has-icons-right">
    <input class="input is-danger" type="password" placeholder="Password input" value="">
    <span class="icon is-small is-left">
      <i class="fas fa-envelope"></i>
    </span>
    <span class="icon is-small is-right">
      <i class="fas fa-exclamation-triangle"></i>
    </span>
  </div>

</div>

<div class="field is-grouped">
  <div class="control">
    <button class="button is-link">Login</button>
  </div>
  <div class="control">
    <button class="button is-link is-light">Cancel</button>
  </div>
</div>
</div>
    </div>
</Layout>
</template>
<style scoped>

.all{
display:grid;
  justify-content: right;
  padding-right: 600px;
  margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
  
  }
  .imgs{
      display: flex;
      justify-content: space-between;
       padding-left: 300px;
      
  }

</style>