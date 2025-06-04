<h2>Discrete Diffusion Modeling by Estimating the Ratios of the Data Distribution (Aaron Lou, Chenlin Meng, Stefano Ermon)</h2>
<p>
Given a set of categories ${1, \ldots, N}$, let a random process X represent its evolution with time. At time $t$, let $p_t\in \mathbb{R}^N$ be the marginal distribution. The discrete diffusion equation governing its evolution is written as:
</p>
\begin{equation}
  \frac{dp_t}{dt} = Q_tP_t
\end{equation}


\begin{equation}
\theta^* = \underset{\theta}{\arg\min} \sum_{i=1}^N \sigma_i^2 \mathbb{E}_{p_{DATA}(x)} \mathbb{E}_{p_{\sigma_i}(\tilde{x} | x)} [\|s_\theta(\tilde{x}, \sigma_i) - \nabla_{\tilde{x}} \log p_{\sigma_i}(\tilde{x} | x)\|_2^2] \tag{1}\label{smld-theta}
\end{equation}
