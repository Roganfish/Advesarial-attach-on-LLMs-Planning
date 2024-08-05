# Summary Literature Reivew (Attack on LLMs Planning)





## Prompt Planning
### Pythonic code Prompt Planning (Few shot)
<span style="color: blue;"> Code as Policies: Language Model Programs for Embodied Control (IEEE, 2023)<span>

**Main point:**<br>
This paper describes the use of LLMs to transform natural language into policy code that the system can compile and run directly. Secondly, it improves the reasoning ability and accuracy of the code generation model by proposing a method to hierarchically generate functions. Thirdly, a benchmark for evaluating language models in the context of robotic code generation is provided.Fourthly, it is shown that CaP improves metrics of generalisation, following the law that larger models perform better.

**Methods:**<br>
LMPs are few-shot prompted with examples to generate different subprograms that may process object detection results, build trajectories, or sequence control primitives. LMPs can be generated hierarchically by composing known functions (e.g., get_obj_names() using perception modules) or invoking other LMPs to define undefined functions.

Combining control flows, LMP composition, and hierarchical function generation.

1. ![alt text](image.png) <br>


2. ![alt text](image-1.png)<br>


3. ![alt text](image-2.png)
![alt text](image-3.png)<br>


**Pros:**<br>

1. The policy code and API parameters can be adapted to new natural language instructions;<br>
2. Can generalize to new objects and environments by bootstrapping off of open-vocabulary perception systems and/or saliency models.<br>
3. Don't need any additional data collection or model training.<br>
4. supporting instructions with non-English languages or emojis.<br>
5. The generated code strategy is directly compilable and executable

**Cons:**<br>

1. The Perception API has limited descriptive capabilities, e.g., it cannot describe the smoothness of a trajectory, the shape of a path.<br>
2. The available control primitives are limited.<br>
3. Inadequate ability to understand complex instructions<br>
4. Cannot perform 3D construction tasks.<br>
5. Assuming all instructions are feasible.<br>

