# Analysis: An Embodied Generalist Agent in 3D World
_By Hezron Perez, Computer Science graduate student at UTSA, May 10, 2024_


![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/67386294-a0de-4cbd-828f-5933db993678)      
_LEO, an embodied multi-modal generalist agent capable of grounding, reasoning, chatting, planning, and acting in the 3D world. LEO is trained in a two-stage scheme: (i) 3D vision-language (VL) alignment and (ii) 3D vision-language-action (VLA) instruction tuning._

## Intro
Some researchers believe that the current work in AI will eventually result in the creation of a single generalist model that is able to handle any problem that comes its way. In this blog, we will discuss the ideas, experiments, and results that came of the creation of LEO, an embodied multimodal generalist agent that represents one more step towards that amazingly well-rounded generalist model, which in this case, can perform tasks such as 3D captioning, question answering, embodied reasoning, navigation, and manipulation.
## Related Work
### Generalist agents
Jacks of all trades, masters of none! ChatGPT has knowledge on a wide range of topics, but it isn’t a specialist in any single domain. It has a limited ability to abstract to tackle novel problems into general ones, which is more apparent when provided with a few examples in the prompt so it can do few-shot learning. LEO needs a similar capability in the 3D world, maintaining knowledge of its state relative to its environment. 
### Multi-modal instruction tuning
Currently, instruction-tuned LVLMs (Large Vision-Language Models) can take instruction via text as input as well as images, both from which the model is able to encode to a common (abstract) representation. However, these images are 2D, and while there are models that can handle 3D input, they only go as far as interpreting the input/instructions and are not trained to interact with the environment. 
### Grounded 3D scene understanding
The agent LEO needs to understand its relationship to its environment and define that relationship in natural language. In other words, LEO needs to ground the 3D world with natural language. However, compared to 2D data, the amount of 3D data that exists is extremely limited, and so little exploration has been to utilize LLMs to ground the 3D scene. Some works use a combination of 2D images to simulate 3D data and other works use actual 3D point cloud data. LEO uses a combination of 2D and 3D data. 
### 3D data prompting from LLMs
Current works curate 3D instruction-following data either manually with bounding boxes and dense captions or LVLMs. In contrast, LEO uses scene-graph-based prompting and refinement methods to prompt and correct the data.
## Models and Tokenization
![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/148abe01-271d-4df4-bff8-50e4ddd361c1)      

## Datasets
![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/4a1da4c0-a9a7-4dcb-bd83-036a699c98b2)       

![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/8dec55bc-043d-4ac0-a968-19e61126b20c)       

## Experiments and Results
![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/b66487a0-2744-47ef-9e20-9ede83cd219b)    

![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/a78a1c7e-23be-4e59-ba9b-42b876a92f84)      

![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/b8fc10a8-70a5-4916-8e37-5ecc28f6a740)     



![image](https://github.com/HEZR0N/LLM_blogs/assets/99786488/9e8d59b1-169a-412b-94ff-120ac5f3d23c)     

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
