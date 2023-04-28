# CodeGen LGM (Large Graph Model)

CodeGen LGM is a graph-based code generation system.

Traditional code-gen LLMs train on code as text. 

_This_ system is designed to explore whether training on graph structures, using 2023 graph-based attention and other graph-tuned neural network techniques, can outperform SOTA benchmarks achieved by traditional code gen LLMs.

The self-attention mechanism in the Transformer model does is designed and does learn global code structure (that's the whole point of it), so there is a reasonable question as to what you might gain by instead training on graphs.

The hypothesis this repo will aim to test is whether the graph nature of the data enhances training efficiency by providing this global structure data to the learning system up front. And from there, whether higher order data topology information can be used to create a final system that produces higher quality code, or larger 'context window' outputs, than are achieved with traditional code-gen LLM architectures.