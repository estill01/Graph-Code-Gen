# CodeGen LGM (Large Graph Model)

CodeGen LGM is a graph-based code generation system.

Traditional code-gen LLMs train on code as text. 

_This_ system is designed to explore whether training on graph structures, using 2023 graph-based attention and other graph-tuned neural network techniques, can outperform SOTA benchmarks achieved by traditional code gen LLMs.

The self-attention mechanism in the Transformer model is designed to, and does, learn global code structure (that's the whole point of it), so there is a reasonable question as to what you might gain by instead training on graph representations of code, e.g. ASTs or ASTs augmented with control and data flow diagram, and other, data.

The hypothesis this repo aims to explore is whether the graph nature of the data enhances training efficiency by providing this global structure data to the learning system up front. Instead of spending our training time discovering this structure, if we just give it to the learning system, we can presumably reduce the amount of time we need to train, or refocus our training on learning other characteristics of code useful for generating higher quality code, or larger system implementations.