## Acknowledgements

We would like to thank (to do: include list of people).

This article was prepared using the [Distill](https://distill.pub) [template](https://github.com/distillpub/template).

The experiments in this work were performed on both a P100 GPU and a multi-core CPU Linux virtual machine provided by [Google Cloud Platform](https://cloud.google.com/).

Any errors here are our own and do not reflect opinions of our proofreaders and colleagues. If you see mistakes or want to suggest changes, feel free to contribute feedback by participating in the discussion [forum](https://github.com/weightagnostic/weightagnostic.github.io/issues) for this article.

<h3 id="citation">Citation</h3>

For attribution in academic contexts, please cite this work as

<pre class="citation short">Adam Gaier and David Ha, "Weight Agnostic Neural Networks", 2019.</pre>

BibTeX citation

<pre class="citation long">@article{wann2019,
  author = {Adam Gaier and David Ha},
  title  = {Weight Agnostic Neural Networks},
  eprint = {arXiv:1906.XXXXX},
  url    = {https://weightagnostic.github.io},
  note   = "\url{https://weightagnostic.github.io}",
  year   = {2019}
}</pre>

## Open Source Code

<!--The instructions to reproduce the experiments in this work is available [here](https://github.com/somewhere/).-->

The instructions to reproduce the experiments in this work will be released soon! (we promise ;-)

## Reuse

Diagrams and text are licensed under Creative Commons Attribution [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) with the [source available on GitHub](https://github.com/designrl/designrl.github.io), unless noted otherwise. The figures that have been reused from other sources don’t fall under this license and can be recognized by the citations in their caption.

## Supplementary Materials

For further discussion about the implementation details of the experiments, and results for multiple independent runs of the search algorithms, please refer to the Supplementary Materials section in the [pdf](https://arxiv.org/) version of this article.

## Performce Profiles

### Average Performance (100 trial) versus Weight for Champion Networks

<div style="text-align: center;">
<img src="assets/png/champ_swingup_profile.png" style="display: block; margin: auto; width: 60%;"/>
<figcaption style="text-align: center;">
CartpoleSwingUp
</figcaption>
<br/>
<img src="assets/png/champ_biped_profile.png" style="display: block; margin: auto; width: 60%;"/>
<figcaption style="text-align: center;">
BipedalWalker-v2
</figcaption>
<br/>
<img src="assets/png/champ_carracing_profile.png" style="display: block; margin: auto; width: 60%;"/>
<figcaption style="text-align: center;">
CarRacing-v0
</figcaption>
</div>

## Additional Bipedal Walker Results

### Increasing search space

<div style="text-align: center;">
<img src="assets/png/biped_net_outConns.png" style="display: block; margin: auto; width: 100%;"/>
<figcaption style="text-align: left;">If we allow connection between outputs (a small modification to the search space), we discovered a simple and elegant WANN for the Bipedal Walker task.</figcaption>
</div>

<div style="text-align: center;">
<video class="b-lazy" data-src="assets/mp4/trial_outConns_-1.0.mp4" type="video/mp4" autoplay muted playsinline loop style="display: block; margin: auto; width: 100%;" ></video>
<figcaption style="text-align: left;">Rollout of policy using above network, weight set to -1.0. Gait is simpler compared to the network in the main text, possibly due to network's simplicity.</figcaption>
</div>

### Bloopers

<div style="text-align: center;">
<video class="b-lazy" data-src="assets/mp4/trial_biped_failures.mp4" type="video/mp4" autoplay muted playsinline loop style="display: block; margin: auto; width: 100%;" ></video>
<figcaption style="text-align: left;">Failure cases at bad weight values.</figcaption>
</div>

<div style="text-align: center;">
<video class="b-lazy" data-src="assets/mp4/trial_balancer.mp4" type="video/mp4" autoplay muted playsinline loop style="display: block; margin: auto; width: 100%;" ></video>
<figcaption style="text-align: left;">But even at some bad weights (here, weight set to +1.14), our agent performs non trivial actions like balancing.</figcaption>
</div>