# picollama 🦙

### A complete LLama 3 implementation for local training

picollama is a miniature but complete implementation of the LLAMA architecture, as well as pre- and post-training protocols, designed to be small enough for training on a personal computer overnight. It's a resource for those who want to learn the end-to-end process of crafting and training a state-of-the-art large language model but don't have infinite resources. We use the complete Llama 3 architecture as described in the official "The Llama 3 Herd of Models" paper (arxiv:2407.21783), but train the smallest 40M parameter version that can be done overnight on a personal computer.

🚀 Features
	•	Compact Design: Fully implements the LLAMA architecture but scaled down for personal computers.
	•	Locally Trainable: Small enough to train a meaningful model in on a personal computer overnight.
	•	Educational Focus: A folder of Jupyter notebooks explaining the step by step process, with also complete stand-alone code to compare to a final result.
	•	Pre- and post-training: Alignment processes like SFT, DPO, and RLHF included.
	•	Pytorch is used throughout, but a Jax implementation is also provided for those who prefer that.

🧠 Prerequisites

We will follow a very similar educational approach as Andrej Karpathy in his Micrograd/Makemore/GPT YouTube videos. We are extending that material to Llama and post-training which contain a few more advanced concepts than he covers. If you have the background to follow his videos - which you are encouraged to watch - you should be fine.

🛠️ Installation
	1.	Clone the repository:

```
git clone https://github.com/jsmidt/picollama.git
cd picollama
```


2.	Install the dependencies:

```
pip install -r requirements.txt
```


3.	You’re ready to roll!

📚 Usage

Training

To train picollama:

    python train.py --data_path <your_dataset_path> --epochs <num_epochs>

Example:

    python train.py --data_path data/sample_texts.txt --epochs 10

Generating Text

After training, you can use picollama to generate text:

    python generate.py --model_path <path_to_trained_model> --prompt "Once upon a time..."

Configuring Hyperparameters

Modify the config.yaml file to tweak parameters like model size, number of layers, or token embedding size.

📁 Directory Structure
	•	src/: Core model and utility implementations.
	•	data/: Placeholder for datasets.
	•	configs/: Configuration files for training and model parameters.
	•	outputs/: Where trained models and logs are saved.

🔬 How It Works

picollama follows the LLAMA architecture closely, with features like:
	•	Multi-head Self-Attention
	•	Feedforward Neural Networks
	•	Layer Normalization

For a detailed explanation, check out the docs.

🧑‍💻 Contributing

Contributions are welcome! If you find bugs, have feature requests, or want to help improve picollama:
	1.	Fork the repository.
	2.	Create a new branch.
	3.	Submit a pull request.

Check out our Contributing Guidelines for more details.

🤝 Acknowledgments
	•	Inspired by the LLAMA architecture from Meta.
	•	Thanks to the open-source ML community for inspiration and tools.

📝 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute as long as you provide attribution.

🌟 Support

If you find picollama helpful, please give the repository a star ⭐! Your support helps make this project better.

Let me know if you want additional sections or tweaks!
