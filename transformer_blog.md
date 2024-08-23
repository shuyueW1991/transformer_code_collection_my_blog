# Build a transformer from scratch: why and how

The transformer architecture, renowned for its innovative approach to sequence modeling, has quickly gained popularity in various deep learning tasks. 
Its departure from traditional recurrent neural network (RNN) structures has opened up new possibilities and improved performance.
The allure of building a transformer from scratch has captivated many aspiring deep learning practitioners. 


While some might envision starting from absolute zero, the reality often involves leveraging powerful frameworks like PyTorch. 
In many similar blogs, the `scratch` refers to PyTorch. 
That is to say, we don't build a transformer from 0-1 binary, and we don't build a transformer from python toolkits --- we build a transformer from torch.
Specifically, the `nn.Module` class and other PyTorch utilities provide a solid foundation for constructing transformer components.


There are some phases in building a transformer that has convenient combo of layers, thanks to the transformer's modular design allows for flexible customization. 
While some enthusiasts delve into the intricacies of constructing individual layers like the encoder, others prefer to take advantage of pre-trained models available through platforms like Hugging Face.
For example, the Encoder part has its official issue in transformers package. 
There are some bloggers using those directly in their architecture.
Alongside with those meticulous works, a much more popular way of deploying transformer is to read the model card of an existing huggingface repository, calling the API's via `from_pretrained`, `tokenizer`, etc, thus customizing pipelines.
Au contraire, it is very hard to really code things like a transformer from total blank.
This is because the mainstream code is dependent upon existing wheels.
The wheels are different in utilities and conditions, but they have to be familiar with before you use them to serve you. 
The level of granularity a developer desires in controlling the transformer's execution is a key consideration. 
I believe that the potential variations of transformer code are finite, as the number of classes, blocks, and code optimizations is limited. This makes it generally feasible to trace and understand the behavior of a transformer implementation within specific code segments.


This blog that you are reading belongs to the first class of blogs: it is focused on the fundamental building blocks of a transformer architecture, guiding you through the process of creating each component as a self-contained class. 
The most typical method of realizing a transformer is to write class for each part of architecture (or `blocks` in form of classes).
You'll discover that many code repositories share common patterns and structures, making the implementation of key components surprisingly straightforward. 
Good news is that many codes are shared in many code repositories that you find in GitHub, for example, the indent and empty lines in attention class is almost the same! 
--- which makes things very strange that the most difficult part of the code becomes one of the easiest to understand.



Beyond the core architecture, a significant portion of your efforts will be dedicated to data preparation and I/O tasks. 
This blog will provide a comprehensive overview of the entire process, from data loading to model training and evaluation. 
This repo will be focused on the big picture of transforem in measure of class, and build one step-by-step.
During description, some comments would be made along the codes, which is important for understanding.
A code realization in parallel can be found in [transformer_code.ipynb](https://github.com/shuyueW1991/transformer_code_collection_my_blog/blob/main/transformer_code.ipynb). 
Please go over there, thanks.


A deep understanding of the underlying components, or 'building blocks,' is crucial for mastering any complex system. In the realm of technology, this principle applies particularly to the transformer architecture. By thoroughly understanding the intricacies of each component, you can gain a competitive edge and innovate effectively.
This approach, prevalent in the early 21st century, has become a cornerstone of modern knowledge creation. By combining a deep understanding of fundamentals with a focus on innovation and practical application, individuals can excel in their fields and contribute to groundbreaking advancements.



