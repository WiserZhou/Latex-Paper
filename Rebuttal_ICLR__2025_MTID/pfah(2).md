<!-- Thanks for the revision, most of my comments are addressed. However, I am not convinced by the 'logic' of the Latent Space Temporal Logical Interpolation module, Yes, I agree actions have temporal and causal relations. But the module is logical, it means that one can deploy programs (e.g. consists of binary operations like AND, OR and so on) to infer actions. Clearly Latent Space Temporal Logical Interpolation module can't do this. I wouldn't link anything to logic, it only creates confusion. Moreover, causal relation is also not the Latent Space Temporal Logical Interpolation module learns. It requires a model to learn invariant representations which satisfy identifiability, such as causal representation learning methods. I will not link the Temporal Logical Interpolation module to causality either.

Overall, I appreciate the additional ablation studies. I still have the concern that the proposed method MTID does not consistently outperform SOTA on all metrics on all datasets (SR when T=6 on crosstalk, SR when T=3 on coin). But I will increase my score. -->


We sincerely appreciate the reviewer's recognition of our work and the increased score. 

Regarding the Latent Space Temporal Interpolation module, we have decided to remove the 'logical' word from the paper to avoid confusion. It also should be noted that the module is not designed for concrete but implicit logical and casual inference.

For the comparison with state-of-the-art methods, we would like to address several points:

- First, regarding the comparison with SCHEMA[1], their use of Large Language Models (LLMs) introduces external knowledge not present in the original dataset, making it an unfair comparison.

- Second, for COIN with T=3, our analysis in Table 9 (line 843) demonstrates that increasing model size alone can improve performance. This finding suggests that for larger datasets, it is essential to develop a memory mechanism to store relevant information, rather than focusing solely on temporal relationships. We will explore this direction in our future research.

- Finally, our analysis in Table 15 (line 1012) shows that for T=6 compared to T=5, there is a larger gap between real and interpolated features. This suggests our current interpolation strategy may be insufficient for longer sequences, as features lack diversity to capture actions fully. We will explore improving interpolated feature quality in future work.

[1] Niu, Y., Guo, W., Chen, L., Lin, X., & Chang, S. F. (2024). SCHEMA: State CHangEs MAtter for Procedure Planning in Instructional Videos. arXiv preprint arXiv:2403.01599.