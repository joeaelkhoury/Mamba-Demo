# Mamba Demo
# Next Steps and some insights for Fine-Tuning and Evaluating the Mamba Model

## 1. Adjust Learning Rate
- Initial learning rate of 0.0005 was ineffective.
- Reducing the learning rate to 0.00005 improved outcomes.

## 2. Evaluate the Mamba Model
- Evaluation is challenging due to subjective metrics.
- Utilize benchmarks like [EleutherAI's lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness), Chatbot Arena, and artificial intelligence referee at [Chatbot Arena Leaderboard](https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard).

## 3. Benchmarking and Skepticism
- Used Mamba author's benchmarks as a starting point.
- Skepticism around benchmark numbers without prior Mamba experience.

## 4. Learning Rate Reconsideration
- Original learning rate of 0.0005 potentially too high.
- Lack of clarity on Mamba's pre-training learning rate.

## 5. Further Fine-Tuning Experiments
- Experimented with even lower learning rates (3x10e-5 and 2x10e-5).
- Tested different training rounds and datasets, including the OA dataset and [HuggingFaceH4/ultrachat_200k](https://huggingface.co/datasets/ultrachat_200k).

## 6. Comparison with TinyLlama
- Noted significant speed advantage of Mamba over TinyLlama.
- Mamba's lower VRAM usage and faster token generation rate.

## 7. Long Context Capability of Mamba
- Tested Mamba's ability to handle long prompts (up to 10k tokens).
- Mamba struggles with very long texts (136K tokens), but performs better with shorter ones (1.54K tokens).
- Example: Triathlon article [triathlon features](https://www.tri247.com/triathlon-features/interviews/lionel-sanders-championship-preview).

## 8. Limitations in Generating High-Quality Content
- Mamba's pre-training limited to 2048 tokens might hinder its ability to summarize large texts.
- Suggestion to fine-tune smaller Mamba models for potential improvement.

## 9. Summary
- Mamba excels in speed and token handling capacity.
- Fine-tuning Mamba is currently complex, with anticipation for future improvements.
- TinyLlama generates better text, likely due to more extensive pre-training data.
