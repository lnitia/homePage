<template>
  <div class="card">
    <div class="cardin">
      <div class="text">
        <h2 class="heading"><slot name="heading"></slot></h2>
        <div class="intro"><slot name="intro"></slot></div>
      </div>
      <div class="img"><slot name="img"></slot></div>
    </div>
  </div>
</template>

<style scoped>
.card {
  position:relative;
  box-shadow:0 1px 4px rgba(0, 0, 0, 0.3), 0 0 20px rgba(0, 0, 0, 0.1) inset;
  width: 98%;
  margin-left:1%;
  margin-bottom: 30px;
  border:2px dashed #F7EEEE;
  border-radius:5px;
  background-color: #f5f5f5;

  &:before, &:after{
    position:absolute;
    content:"";
    top:14px;bottom:14px;left:0;right:0;
    box-shadow:0 0 15px 3px #122e5b;
    border: radius 0px;
    z-index:-1;
  }
  .cardin {
    padding: 15px 20px;
    display: flex;
    align-items:flex-start;
    justify-content: space-between;
    .heading {
      display: flex;
      justify-content: center;
    }
    .intro {
      padding: 0 10px;
    }
  }
}
</style>