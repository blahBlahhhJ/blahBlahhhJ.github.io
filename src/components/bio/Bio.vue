<template>
  <div class="bio-container">
    <Paragraph title="Biography" class="biography">
      <p>
        Jason was born in Ottawa, Canada, and moved to
        <a href="https://en.wikipedia.org/wiki/Shenzhen">Shenzhen</a>, China 
        at the age of 3. He spent his next 15 wonderful years there, all the way 
        from kindergarten to high school.
      </p>
      <p>
        For college, Jason came to America to study Computer Science as an undergraduate at 
        <a href="https://eecs.berkeley.edu">UC Berkeley</a> Class of 2022. 
        During his 3.5 years of undergraduate career, Jason worked as an 
        undergraduate student instructor for 2 years, and he was the head TA for a 
        600-student AI course <a href="https://inst.eecs.berkeley.edu/~cs188/">CS 188</a>. 
        Besides teaching, Jason was an AI researcher in 
        <a href="https://bair.berkeley.edu">Berkeley Artificial Intelligence Reserach Lab 
          (BAIR)</a> supervised by Professor Sergey Levine. 
        Jason graduated from UC Berkeley with full 4.0 GPA and won the 
        <a href="https://www2.eecs.berkeley.edu/Students/Awards/21/">Mark D. Weiser Excellence 
        in Computing Scholarship Award</a> as well as the 
        <a href="https://lsadvising.berkeley.edu/policies/deans-listhonors">Highest Distinction 
        in General Scholarship</a> (summa cum laude).
      </p>
      <p>
        For work, Jason interned at <a href="https://www.nvidia.com/en-us/">NVIDIA</a> 
        twice for nearly a year as a Deep Learning Algorithm Engineer. He helped develop 
        many AI models and tools for both NVIDIA's customers and internal use.
      </p>
      <p>
        Jason is now pursuing an MSCS degree at 
        <a href="https://cs.stanford.edu">Stanford University</a> where he will focus on AI. 
        He hopes to get exposed to more cutting-edge AI technology and research in order to 
        be more successful in his future career. Jason is a research assitant in Stanford's
        <a href="https://crfm.stanford.edu">Center for Research on Foundation Models (CRFM)</a> 
        supervised by Professor Percy Liang. 
      </p>
    </Paragraph>
    <hr />
    <Paragraph title="Interest" class="interest">
      <p>
        Jason is very interested in Deep Learning. He enjoys doing "weird" 
        projects whenever he has interesting ideas (see <a href="#">project</a> section). 
        Jason loves music - not just listening but also playing and producing music. 
        He can play piano and fingerstyle guitar, and he sometimes create his own music.
      </p>
    </Paragraph>
    <Paragraph title="Skills" class="skills">
      <p>
        For Machine Learning, Jason is very fluent in writing Python code, and familiar 
        with using popular DL platforms like <a href="https://pytorch.org">PyTorch</a> 
        to build and train models as well as exporting models to other formats like 
        <a href="https://github.com/NVIDIA/TensorRT">TensorRT</a> to maximize inference performance for deployment. He also 
        had experience writing lower level customized kernels using 
        <a href="https://openai.com/research/triton">OpenAI Triton</a> to achieve best 
        performance for specific workflows.
      </p>
      <p>
        For Software Engineering, Jason could use Python, Java, C/C++ depending on
        the actual task.
      </p>
      <p>
        For Web Development, Jason had full stack developing experience using
        <a href="https://www.djangoproject.com">Django</a> &
        <a href="https://reactjs.org">React.js</a>. He could also build websites
        using <a href="https://vuejs.org">Vue.js</a> (as that's how this website
        is built).
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