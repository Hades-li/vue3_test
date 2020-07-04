<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <ul>
      <li>
<!--        <ren></ren>-->
      </li>
      <li>
        <test></test>
      </li>
    </ul>
  </div>
</template>

<script>
import Ren from "../components/Ren"
import Test from '../components/test'

export default {
  name: "Home",
  components: {
    // Ren,
    Test
  }
};
</script>
