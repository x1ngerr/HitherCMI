Hither-CMI

Numerous studies show that circular RNA (circRNA) functions as a sponge for microRNA (miRNA), significantly regulating gene expression by interacting with miRNA, which in turn affects the progression of human diseases. Traditional experimental approaches for investigating circRNA-miRNA interactions (CMI) are time-consuming and expensive, making computational methods a valuable alternative. Hence, we propose a computational model for predicting CMI, leveraging hybrid multimodal network and higher-order neighborhood information (Hither-CMI). Specifically, Hither-CMI employs Multiple Kernel Learning (MKL) to integrate sequence, structure, and expression similarity networks of circRNA and miRNA, resulting in a hybrid multimodal network. Next, an enhanced Graph Convolutional Network (GCN) is utilized to combine the circRNA-miRNA hybrid multimodal network with the CMI association network, producing a hybrid higher-order embedding representation. Finally, the XGBoost classifier is applied for training and prediction. The Hither-CMI model achieved a predicted AUC value of 0.9134. In case studies, 25 out of the top 30 predicted CMI were confirmed by recent literature. These extensive experimental results further validate the effectiveness of Hither-CMI in predicting potential CMI, making it a promising pre-screening tool for further biological research.

Directory Structure

    project/
    │
    ├── main.py                    # Main entry point for running the program
    ├── config.py                  # Configuration file for setting hyperparameters and arguments
    ├── models/
    │   ├── __init__.py            # Marks the directory as a Python package
    │   ├── gcn_layers.py          # Defines GCN-related layers (e.g., convolution layers)
    │   └── hithercmi.py             # Defines the Hither-CMI model
    │
    ├── utils/
    │   ├── __init__.py            # Marks the directory as a Python package
    │   ├── data_processing.py     # Handles data loading, preparation, and processing
    │   ├── file_operations.py     # Manages file storage and retrieval
    │   ├── graph_operations.py    # Defines graph-related operations
    │   └── evaluation.py          # Evaluation and training methods for the model
    │
    └── result/                    # Directory to store output results
    

Running the Main Program

To run the program, simply execute the main.py file. This will initiate the full process of data loading, feature extraction, model training, and evaluation.

    python main.py

Requirements

Ensure that the following Python packages are installed:

    pip install numpy keras scikit-learn joblib tqdm matplotlib

Contributing

Contributions are welcome! If you find a bug or have a suggestion, please open an issue or submit a pull request.
