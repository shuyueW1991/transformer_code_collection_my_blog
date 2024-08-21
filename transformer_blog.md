# Build a transformer from scratch: why and how

Due its 'pattern' different from its previous counterparts in the world of deep learning, the architecture of transformer gains its popularity in many tasks.
Therefore, many deep learning amateurs become fanatic to this architecture, and to its build-up from scratch thereof.

In many similar blogs, the `scratch` refers to pytorch. That is to say, we don't build a transformer from 0-1 binary, and we don't build a transformer from python toolkits --- we build a transformer from torch, and more specifically, the `nn.Module` packages and other torch utilities.
There are some phases in building a transformer that has convenient combo of layers. For example, the Encoder part has its official issue in transformers package. There are some bloggers using those directly in their architecture.
Alongside with those meticulous works, a much more popluar way of deploying transformer is to read the model card of an existing huggingface repository, calling the API's via `from_pretrained`, `tokenizer`, etc, thus customizing pipelines.
This blog that you are reading belongs to the first class of blogs.

The most typical method of realizing a transformer is to write class for each part of architecture.
Good news is that many codes are shared in many code repositories that you find in GitHub, for example, the indent and empty lines in attention class is almost the same! which makes things very strange that the most difficult part of the code becomes one of the easiest to understand.
As matter of fact, more time and effort and dedicated to the I/O of data.
This repo will be focused on the big picture of transforem in measure of class, and build one step-by-step.
During description, some comments would be made along the codes, which is important for understanding.
A code realization in parallel can be found in xxxxx. Please move your ass there, thanks.





