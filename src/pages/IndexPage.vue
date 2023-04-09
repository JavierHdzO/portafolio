<template>
  <q-page class="row items-center justify-evenly bg-grey-10">
<div class="container">
  <div class="top">
    <div class="square">
      <div class="square">
        <div class="square">
          <div class="square">
            <div class="square"><div class="square">
            </div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="bottom">
    <div class="square">
      <div class="square">
        <div class="square">
          <div class="square">
            <div class="square"><div class="square">
            </div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="left">
    <div class="square">
      <div class="square">
        <div class="square">
          <div class="square">
            <div class="square"><div class="square">
            </div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="right">
    <div class="square">
      <div class="square">
        <div class="square">
          <div class="square">
            <div class="square"><div class="square">
            </div></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
  </q-page>
</template>

<style>
.container {
  position: absolute;
  top: 45%;
  left: 48%;
}

.square {
  width: 8px;
  height: 30px;
  background: #0097a7;
  border-radius: 10px;
  display: block;
  /*margin:10px;*/
  -webkit-animation: turn 2.5s ease infinite;
  animation: turn 2.5s ease infinite;
  -webkit-box-shadow: #0097a7 0px 1px 15px 0px;
          box-shadow: #0097a7 0px 1px 15px 0px;
}

.top {
  position: absolute;
  left: 40%;
  top: 50%;
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
      transform: rotate(90deg);
}

.bottom {
  position: absolute;
  left: 40%;
  top: 50%;
  -webkit-transform: rotate(-90deg);
  -ms-transform: rotate(-90deg);
      transform: rotate(-90deg);
}

.left {
  position: absolute;
  left: 40%;
  top: 50%;
}

.right {
  position: absolute;
  left: 40%;
  top: 50%;
  -webkit-transform: rotate(-180deg);
  -ms-transform: rotate(-180deg);
      transform: rotate(-180deg);
}

@-webkit-keyframes turn {
  0% {
    -webkit-transform: translateX(0) translateY(0) rotate(0);
            transform: translateX(0) translateY(0) rotate(0);
  }

  50% {
    -webkit-transform: translateX(400%) translateY(100%) rotate(90deg);
            transform: translateX(400%) translateY(100%) rotate(90deg);
  }

  100% {
    -webkit-transform: translateX(0) translateY(0) rotate(0);
            transform: translateX(0) translateY(0) rotate(0);
  }
}

@keyframes turn {
  0% {
    -webkit-transform: translateX(0) translateY(0) rotate(0);
            transform: translateX(0) translateY(0) rotate(0);
  }

  70% {
    -webkit-transform: translateX(400%) translateY(100%) rotate(90deg);
            transform: translateX(400%) translateY(100%) rotate(90deg);
  }

  100% {
    -webkit-transform: translateX(0) translateY(0) rotate(0);
            transform: translateX(0) translateY(0) rotate(0);
  }
}
</style>

<script setup lang="ts">
import { Todo, Meta } from 'components/models';
import { ref } from 'vue';

const meta = ref<Meta>({
  totalCount: 1200
});
</script>
