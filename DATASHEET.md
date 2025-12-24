## Dataset Datasheet

### Motivation  
This dataset was created to support the evaluation of **black-box optimisation methods** under realistic conditions, including noisy outputs, limited query budgets, increasing dimensionality, and local optima. 
It is designed to study scaling behaviour, diminishing returns, and emergent optimisation dynamics in sequential decision-making problems such as hyperparameter tuning, experimental design, and surrogate-based optimisation.

### Composition  
The dataset contains **eight independent optimisation functions**, each mapping multi-dimensional inputs (2D–8D) to scalar outputs. 
Inputs and outputs are stored as NumPy arrays with fixed shapes per function. 
The dataset grows incrementally over time, with higher-numbered functions exhibiting greater dimensionality and complexity.

### Collection Process  
Data are generated via an **interactive query interface**, where inputs are selected sequentially rather than sampled exhaustively. 
Queries are issued on a **weekly basis**, reflecting adaptive optimisation strategies that balance exploration and exploitation.

### Preprocessing and Uses  
No preprocessing or feature transformations are applied beyond basic formatting. 
The dataset is intended for benchmarking optimisation algorithms, analysing robustness and convergence, and studying emergent behaviour. 
It is not suitable for supervised learning or real-world decision deployment.

### Distribution and Maintenance  
The dataset is maintained by the author and updated as new queries are generated. 
It is distributed for research and educational use, with no guarantee of completeness or stationarity.
