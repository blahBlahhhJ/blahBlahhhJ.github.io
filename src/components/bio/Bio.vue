<template>
  <div class="bio-container">
    <Paragraph title="Biography" class="biography">
      <p>
        I was born in Ottawa, Canada, and moved to
        <a href="https://en.wikipedia.org/wiki/Shenzhen">Shenzhen</a>, China
        when I was 3 years old (before I could properly remember things). At a
        technology event near my home, I learned about programming for the first
        time, and started building robots in 2010. I graduated from Shenzhen
        Middle School in 2019 and was lucky enough to be admitted to
        <a href="https://eecs.berkeley.edu">UC Berkeley</a> Class of 2023 as a
        Computer Science student. As a (rising) junior student now, I'm an
        Undergraduate Student Instrctor at this amazing course
        <a href="https://inst.eecs.berkeley.edu/~cs188/">CS 188</a>
        (Introduction to Artificial Intelligence). I'm also proud to work as a
        Reader & Tutor for <a href="https://cs170.org">CS 170</a> (Efficient
        Algorithms and Intractable Problems) in my sophomore year.
      </p>
    </Paragraph>
    <hr />
    <Paragraph title="Interest" class="interest">
      <p>
        I'm very interested in Deep Learning, especially Deep Reinforcement
        Learning - it's very fascinating to see an agent learn to improve its
        performance just by itself. I enjoy doing "weird" projects whenever I
        have interesting ideas (see <a href="#">project</a> section). I also
        play fingerstyle guitar and sometimes produce music (if I really have
        the time to do so). Not sure if I'll still be making videos, but I'll
        take that as one of my interests as well :(
      </p>
    </Paragraph>
    <Paragraph title="Skills" class="skills">
      <p>
        For Machine Learning, I'm fluent in writing Python code, and using DL
        frameworks such as <a href="https://pytorch.org">PyTorch</a> and
        <a href="https://www.tensorflow.org">TensorFlow</a>. <br />
        For Software Engineering, I could use Python, Java, C/C++ depending on
        the actual task. <br />
        For Web Development, I had full stack developing experience using
        <a href="https://www.djangoproject.com">Django</a> &
        <a href="https://reactjs.org">React.js</a>. I could also build websites
        using <a href="https://vuejs.org">Vue.js</a> (as that's how this website
        is built with).
      </p>
    </Paragraph>
    <hr />
  </div>
</template>

<script>
import Paragraph from "./Paragraph.vue";

export default {
  name: "Bio",
  components: { Paragraph },
};
</script>

<style scoped>
.bio-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  column-gap: 1rem;
  row-gap: 1.2rem;
}

.biography,
hr {
  grid-column: 1 / span 2;
}

p {
  font-weight: 500;
  margin-top: 1rem;
  margin-bottom: 0;
}

hr {
  border: 1px solid #ccc;
  width: 100%;
}
</style>