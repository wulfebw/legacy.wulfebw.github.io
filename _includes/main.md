
# Bio

I am a Computer Science Master's student at Stanford studying artificial intelligence. I'm interested in Reinforcement Learning, and particularly the question of how artifical agents can autonomously learn increasingly complex behavior. My research focuses on this topic, which is central to hierarchical reinforcement learning (HRL). I'm more generally interested in deep reinforcement learning and multiagent coordination, and am currently researching these topics as part of the <a href="http://web.stanford.edu/group/sisl/cgi-bin/wordpress/people/" class="md-link">Stanford Intelligent System Lab</a>. 

For undergrad I studied Computer Science at Vanderbilt University, where I performed research related to autonomous UAVs with my advisor <a href="http://engineering.vanderbilt.edu/bio/julie-adams" class="md-link">Julie Adams</a> as part of the <a href="http://eecs.vanderbilt.edu/research/hmtl/wp/" class="md-link">Human-Machine Teaming Lab</a>. I also did an independent study advised by <a href="http://engineering.vanderbilt.edu/bio/eugene-vorobeychik" class="md-link">Eugene Vorobeychik</a> dealing with social interaction analysis, which is how I originally became interested in machine learning.

---

# Research

### Deep Reinforcement Learning for Collision Avoidance
We learn UAV collision avoidance policies directly from a simulator with a Deep Q-Network (DQN). This approach not only solves for policies more quickly than value iteration, but also arrives at safer and more efficient solutions by learning a direct mapping from the state space instead of discretizing it. 

<div id="content-wrapper">
    <div id="content">
        <img class="small-img" src="{{ site.github.url }}/media/policy_-180.gif" />
        <img class="small-img" src="{{ site.github.url }}/media/value_-180.gif" />
    </div>
</div>

---

### Multi-agent Action Coordination
How can UAVs with different collision avoidance strategies coordinate manuevers so as to minimize collisions? This research presents an approach that enforces reasonable requirements on the behavior of UAVs, and as a result dramatically improves safety in dangerous encounters. The method is essentially to ensure that UAV manuevers align with the directions of those advised by an optimal joint solution. 

<div>
<a href="https://github.com/sisl/HorizontalCoordUAVs" class="md-link">code</a>
</div>

<div id="content-wrapper">
    <div id="content">
            <img class="med-img" src="{{ site.github.url }}/media/joint_actions.png" />
    </div>
</div>

---

### Playig Atari with Hierarchical Reinforcement Learning 
How can artifical agents autonomously learn increasingly complex behavior? The <a href="http://people.idsia.ch/~juergen/subgoals.html" class="md-link">traditional</a> <a href="https://people.cs.umass.edu/~mahadeva/papers/hrl.pdf" class="md-link">approach</a> to solving this problem is to identify subgoals, and then to learn options (i.e., skills) useful for acheiving those subgoals. In this research, we instead take a bottom-up approach to HRL, wherein the sequential, primitive actions of an agent are modeled as the result of latent variables, which may themselves be used as options (similar in concept to the approach taken <a href="http://www.ausy.tu-darmstadt.de/uploads/Site/EditPublication/Daniel2016JMLR.pdf" class="md-link">here</a>). This research makes an intial step in this direction, using hierarchical recurrent neural networks within a <a href="https://arxiv.org/abs/1507.06527" class="md-link">Recurrent Q-Network</a>.

<div>
<a href="https://github.com/wulfebw/hierarchical_rl" class="md-link">code_1</a>
<a href="{{ site.github.url }}/assets/CS239_Final_Paper.pdf" class="md-link">pdf_1</a>
<a href="https://github.com/wulfebw/playing_atari" class="md-link">code_2</a>
<a href="{{ site.github.url }}/assets/CS221_Final_Paper.pdf" class="md-link">pdf_2</a>
</div>

<div id="content-wrapper">
    <div id="content">
        <div>
            <img class="small-img" src="{{ site.github.url }}/media/hsRQN.jpg" />
            <img class="small-img" src="{{ site.github.url }}/media/sRQN.jpg" />
        </div>
    </div>
</div>

---

### Language Modeling with Recurrent Generative Adversarial Networks
<a href="https://arxiv.org/abs/1406.2661" class="md-link">GANs</a> have had a lot of success in generating images; can they be applied with similar effect to natural language? Since natural language is discrete, we formulate this task as a reinforcement learning problem, and use REINFORCE to train a recurrent generative network to maximize rewards produced by a discriminating network. We found this approach did not scale well to the vocab sizes used in realistic datasets (> 60,000 words), but believe improved training methods (e.g., <a href="https://arxiv.org/abs/1502.05477" class="md-link">TRPO</a>) and curriculum learning (e.g., <a href="https://arxiv.org/abs/1511.06732" class="md-link">MIXER</a>) might overcome these issues.

<div>
<a href="https://github.com/wulfebw/adversarial_rl" class="md-link">code</a>
<a href="{{ site.github.url }}/assets/CS224d_Final_Paper.pdf" class="md-link">pdf</a>
</div>

<div id="content-wrapper">
    <div id="content">
        <div>
            <img class="small-img" src="{{ site.github.url }}/media/sine.gif" />
            <img class="small-img" src="{{ site.github.url }}/media/circle.gif" />
        </div>
    </div>
</div>


---

### Geolocalization of Street View Images
Given an random, street-level image of a city from around the world, could you identify where the picture was taken? In this project, we collected a dataset of 100,000 images from ten cities, and trained a convolutional neural network to predict the city from the image. We found that the network successfully identifies the city with ~75% accuracy. Research tackling this project at a much larger scale was published concurrently (<a href="https://arxiv.org/abs/1602.05314" class="md-link">PlaNet</a>).

<div>
<a href="https://github.com/wulfebw/LittlePlaNet-Models" class="md-link">code</a>
<a href="{{ site.github.url }}/assets/CS231n_Final_Paper.pdf" class="md-link">pdf</a>
</div>

<div id="content-wrapper">
    <div id="content">
        <div>
            <img class="small-img" src="{{ site.github.url }}/media/tsne.png" />
            <img class="small-img" src="{{ site.github.url }}/media/inclusion.png" />
        </div>
    </div>
</div>

---

### Predicting Social Interaction Outcomes
In this project, I analyzed a set of ~2,000 pairwise social encounters. Using the audio, visual, and network features from those interactions, I was able to predict their outcomes with about 85% accuracy. While I am more focused on reinforcement learning now, I still think this topic is interesting, and in particular believe that enabling computers to intelligently interact with people (e.g., in healthcare or educational settings) would be widely beneficial.

<div>
<a href="https://github.com/wulfebw/Independent_Study" class="md-link">code</a>
<a href="{{ site.github.url }}/assets/IS_Final_Paper.pdf" class="md-link">pdf</a>
</div>

---

### 3D Map Generation with Autnomous UAVs
Our goal in this project was to develop a method for collecting imagery of archeological sites using autonomous UAVs, which could then be used to generate 3D mappings of those sites. We lived in a highland village in Peru for two months while we attempted to collect imagery using the UAVs. The cover image for this website is a photo I took of the archeological site where we spent the summer. 

<div>
<a href="https://github.com/wulfebw/Independent_Study" class="md-link">code</a>
<a href="{{ site.github.url }}/assets/IS_Final_Paper.pdf" class="md-link">pdf</a>
</div>

---
