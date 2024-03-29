<template>
  <div class="project-list-container">
    <h2>Projects</h2>
    <Project
      image="FaceControl.jpg"
      date="Dec 2023"
      title="Face Control"
      repo="https://github.com/blahBlahhhJ/FaceControl"
      site="https://drive.google.com/file/d/1gzjCfk4g5xG8soqMQbqwqMBgeDMUrJ8j/view?usp=sharing"
    >
      <p>
        A research project about controllable face generation.
        <br /><br />
        Users can generate whatever face they want by specifying facial landmarks and text prompt.
        <br /><br />
        Related Technology: PyTorch, Stable Diffusion, Controlnet
      </p>
    </Project>
    <Project
      image="CLIP.jpg"
      date="July 2023"
      title="CLIP Demo"
      site="https://catalog.ngc.nvidia.com/orgs/nvidia/teams/ai-foundation/models/clip"
    >
      <p>
        A demo to show <a href="https://arxiv.org/abs/2103.00020">CLIP's</a> 
        ability to align image and text representations.
        <br /><br />
        This project is done during my internship@NVIDIA DL Algo, and it is one of the 
        first demos released in NVIDIA's AI Foundation models. 
        <br /><br />
        Users can extract the most relevant image of any input text.
        <br /><br />
        Related Technology: PyTorch, Multimodal, TensorRT, Deployment
      </p>
    </Project>
    <Project
      image="BaggingBot.gif"
      date="Dec 2022"
      title="Bagging Bot"
      repo="https://github.com/blahBlahhhJ/BaggingBot"
      site="https://sites.google.com/berkeley.edu/baggingbot/home"
    >
      <p>
        A robotics project that uses computer vision to automatically put blocks
        into a bag, and then lifts the bag - like a shopping bot.
        <br /><br />
        Related Technology: Robotics, ROS, OpenCV
      </p>
    </Project>
    <Project
      image="TerrainRendering.gif"
      date="May 2022"
      title="Terrain Rendering Shader"
      repo="https://www.shadertoy.com/view/flBcR3"
    >
      <p>
        A shader project that procedually generates an infinite terrain with
        grass, clouds, and realistic lightings.
        <br /><br />
        Related Technology: GLSL, shader
      </p>
    </Project>
    <Project
      image="ProjectProcgen.gif"
      date="May 2021"
      title="Project Procgen"
      repo="https://github.com/blahBlahhhJ/ProjectProcgen"
      site="https://docs.google.com/document/d/1cYYbDuHn-3CFncGhJIIKFL-SFDjk2jx6JFnyj-vrjsI/edit?usp=sharing"
    >
      <p>
        A research project about improving RL generalizability and sample
        efficiency.
        <br /><br />
        Proposed several new variants of
        <a href="https://arxiv.org/abs/2010.10814">Mixture Regularization</a>
        which significantly boosted the agent's performance by a large margin
        comparing to a baseline
        <a href="https://arxiv.org/abs/1707.06347">PPO</a> model. <br /><br />
        (*Fruitbot Demo - positive reward for fruit, negative reward for other
        foods)<br /><br />
        Related Technology: PyTorch, Deep RL, PPO
      </p>
    </Project>
    <Project
      image="LightningBolts.png"
      date="April 2021"
      title="PyTorch Lightning Bolts - Open Source Contribution"
      repo="https://github.com/PyTorchLightning/lightning-bolts"
      site="https://lightning-bolts.readthedocs.io/en/latest/"
    >
      <p>
        A deep learning toolbox that contains a ton of SOTA models built on
        PyTorch for research and production.
        <br /><br />
        Contribute to Reinforcement Learning section by implementing
        <a href="https://github.com/PyTorchLightning/lightning-bolts/pull/598"
          >A2C</a
        >
        and
        <a href="https://github.com/PyTorchLightning/lightning-bolts/pull/627"
          >SAC</a
        >. <br /><br />
        Related Technology: PyTorch, PyTorch Lightning, Deep RL, Actor Critic
      </p>
    </Project>
    <Project
      image="StressBusterAR.gif"
      date="May 2020"
      title="Stress Buster AR"
      repo="https://github.com/blahBlahhhJ/stress-buster-ar"
    >
      <p>
        A fun little iOS app featuring Augmented Reality and Deep Learning. It
        achieves real time foot detection using Semantic Segmentation for users
        to destroy virtual objects.
        <br /><br />
        Won the Most Technical Project Award in UC Berkeley's
        <a href="https://iosdev.berkeley.edu">iOS Dev DeCal</a> in Spring 2020.
        <br /><br />
        Related Technology: PyTorch, Swift, CoreML, ARKit
      </p>
    </Project>
    <Project
      image="CropYourFace.gif"
      date="March 2020"
      title="Crop Your Face"
      repo="https://github.com/blahBlahhhJ/CropYourFace"
    >
      <p>
        A weird demo featuring real time face and palm detection. It recognizes
        the pistol gesture and shoots the face in the given direction.
        <br /><br />
        Related Technology: TensorFlow, OpenCV
      </p>
    </Project>
  </div>
</template>

<script>
import Project from "./Project.vue";

export default {
  name: "ProjectList",
  components: {
    Project,
  },
};
</script>

<style scoped>
.project-list-container {
  margin-top: 3rem;
  text-align: left;
}

p {
  margin: 0;
}
</style>