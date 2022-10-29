## DAVINZ: Data Valution using Deep Neural Networks at Initialization
### Authors/ Team: Bryan Kian Hsiang Low
### Conference/ Journal: ICML
### Year: 2022

**Motivation:**

**Score Funciton**: $\nu(S)=-k\sqrt{\hat{y}^{\top}\Theta_{0}^{-1}\hat{y}/m_{s}}-d_{\mathcal{H}}(T, S)$

*In-domain:*

Generalization error can be interpreted as a complexity measure of dataset $S$

$-k\sqrt{\hat{y}^{\top}\Theta_{0}^{-1}\hat{y}/m_{s}}$

In which, $\hat{y}\triangleq y-f(x, \theta_0)$

$k=2\rho$

*Biased MMD(out-of-domain):*

 Generalization error measured by the domain discrepancy will become zero when $S$ approaches $T$. When $T$ is a preferred dataset of data consumers, this result aligns with the desirable awareness of data preference in data valuation

$\mathcal{H}:$ any funciton space

$\mathcal{D}_T:$ target domain

$\mathcal{D}_S:$ source domain

$$
d_{\mathcal{H}}(\mathcal{D}_T, \mathcal{D}_S) \triangleq \sup_{h\in\mathcal{H}}|\mathbb{E}_{x_{'}\sim \mathcal{D}_T}[h(x^{'})]-\mathbb{E}_{x\sim\mathcal{D}_{S}}[h(x)]|
$$

$$
d_{\mathcal{H}}(T, S) \triangleq \sup_{h\in\mathcal{H}}|\frac{1}{m_{T}}\sum_{i=1}^{m_{T}}h(x_i^{'})-\frac{1}{m_{S}}\sum_{i=1}^{m_S}h(x_{i})|
$$

**Properties**

*Awareness of Data Quantity:* higher score to the dataset with more data samples

*Stability to Noise:* similar scores to the original dataset and its counterpart with a small-sale noise

*Robustness to Model:* similar scoresto a dataset even when distinct DNN models are used undercertain conditions


