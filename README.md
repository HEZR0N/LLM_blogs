# Analysis: An Embodied Generalist Agent in 3D World
_By Hezron Perez, Computer Science graduate student at UTSA, May 10, 2024_


![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/67386294-a0de-4cbd-828f-5933db993678)      
_LEO, an embodied multi-modal generalist agent capable of grounding, reasoning, chatting, planning, and acting in the 3D world. LEO is trained in a two-stage scheme: (i) 3D vision-language (VL) alignment and (ii) 3D vision-language-action (VLA) instruction tuning._

## Intro
Some researchers believe that the current work in AI will eventually result in the creation of a single generalist model that is able to handle any problem that comes its way. In this blog, we will discuss the ideas, experiments, and results that came of the creation of LEO, an embodied multimodal generalist agent that represents one more step towards that amazingly well-rounded generalist model. 
## Related Work
### Generalist agents
### Multi-modal instruction tuning
### Grounded 3D scene understanding
## Models and Tokenization
![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/148abe01-271d-4df4-bff8-50e4ddd361c1)      

## Datasets
![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/4a1da4c0-a9a7-4dcb-bd83-036a699c98b2)       

![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/8dec55bc-043d-4ac0-a968-19e61126b20c)       

## Experiments and Results
 - The instruction tuning of LEO conforms to the scaling law
 - Scaling up LLM
 - Alignment leads to consistent improvements.
## Closing Thoughts
LEO is an excellent demonstration of our current ability to cobble together multiple models trained on several different datasets of various modalities into a single model, but in trying to do everything, it still falls behind some models that are designed to complete a single type of tasks. In other words, LEO is also a good demonstration of our current limitations. The designers of LEO have not yet explored any ideas/features to accommodate LEO’s skill deficits in certain tasks (i.e. novel scenes), though they have proposed the following for future work:
 - More Data: Enhancing the 3D VL understanding capability by leveraging larger-scale VL data from richer 3D domains
 - Better translate Vision into Action: Continually bridging the gap between 3D VL and embodied action, as our experiments reveal the efficacy of their joint learning
 - Possibly use RLHF: Investigating the issues of safety and alignment in the context of embodied generalist

## References
Author(s). (2024). An Embodied Generalist Agent in 3D World. arXiv, 2311.12871. Retrieved from https://arxiv.org/2311.12871
