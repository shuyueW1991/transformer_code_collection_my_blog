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


It is very hard to really code things like a transformer from total blank.
This is because the mainstream code is dependent upon existing wheels.
The wheels are differnt in utilities and conditions, but they have to be familar with before you use them to serve you. 
In this way, a transformer is quite similar to another under fingertips of many coders, which is a natural phenomenon.
The only major difference lies in how *fine* a coder want to have his/her control in the transformer running process.
Therefore, i believe that the versions of transformer code can be enumerated within countable numbers, because the class numbers are limited, the blocks are limited, and the  shortened code is always easy to trace within some certain block.
I think, if people (i, in particular) are familiar with the detailed version of each block(in East Asian culture, to 'Bei4', wink), then you can master the area.
The experience can also be extended to other areas, for those who wants to be innovational in creative ideas and professional in product delivery.
This is the modern fashion of knowledge manufacturing in early half of 21th century.


