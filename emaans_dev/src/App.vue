<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'AnimatedBox',
  setup() {
    const box = ref<HTMLDivElement | null>(null);

    const animateBox = () => {
      if (box.value) {
        box.value.classList.toggle('animate');
      }
    };

    return { box, animateBox };
  },
});
</script>

<template>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <div>
    <div ref="box" class="box">Animate Me!</div>
    <button @click="animateBox">Animate</button>
</div>

  <div class="biome">
    <div class="macrobiome">
      <!-- <p>1w</p> -->
    </div>
    <div class="macrobiome">
      <!-- <p>2w</p> -->
      <div class="macrobiome">
        <div>
          <h1>Emaan Haseem</h1>
        </div>

        <div class="microbiome">
          <h3>...So you're here for my resume...</h3>
          <p>can i offer you some green eggs and ham instead?</p>
          <p>no, you said? well that's a shame - how else shall i get this bread?</p>
        </div>

        <div class="microbiome">
          <h3>Well that's fine I guess</h3>
          <p>I'll deal I suppose</p>
          <p>Or... shall I offer you something...</p>
        </div>

        <div class="microbiome">
          <h2>More:</h2>
        </div>

        <div class="microbiome">
          <h2>...Clean!</h2>
        </div>

        <div class="microbiome">
          <h2>~Sleek</h2>
        </div>

        <div class="microbiome">
          <h2>Composed !!!</h2>
        </div>

        <div>
          <iframe
            src="https://pdflink.to/cd3162c8/embed/"
            style="width: 60vw; height: 70vw"
          ></iframe>
        </div>
      </div>
    </div>
    <div class="macrobiome">
      <!-- <p>3w</p> -->
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Funnel+Display:wght@300..800&display=swap');

/* body {
  background-image: url(emaans_dev/src/assets/rustams_first_course.webp);
} */

/* .flex-container {
  background-image: url(emaans_dev/src/assets/rustams_first_course.webp);
} */

h1 {
  font-family: 'Funnel Display', sans-serif;
  color: rgb(119, 47, 39);
  text-align: center;
  font-weight: 600;
  background-color: rgb(162, 182, 168);
  height: 5vh;
}

iframe {
  border: none;
  height: 100%;
  width: 100%;
  max-width: 100%;
}

/* h1 {
  font-family: 'Funnel Display', sans-serif;
  color: brown;
  font-size: 128px;
  width: 100vw;
} */

.box {
  width: 100px;
  height: 100px;
  background: blue;
  transition: transform 0.5s ease;
}
.box.animate {
  transform: translateX(200px);
}
</style>
