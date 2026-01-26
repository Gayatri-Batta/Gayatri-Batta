# Hi there, I'm Gayatri! 👋

### MS in AI Candidate @ Stony Brook University | Machine Learning Researcher

I am an AI researcher and engineer bridging the gap between **theoretical ML** and **scalable production systems**. Currently, I am focused on **Multi-Agent Systems**, **LLMs**, and **Clinical Time-Series Forecasting**.

Previously, I worked as a **Cloud & Data Engineer**, where I built scalable **ML inference pipelines** on AWS and automated infrastructure operations using Ansible.

---

### Technical Skills

* **Languages:** Python, C++, SQL, Bash, LaTeX
* **Machine Learning:** PyTorch, SciPy, Pandas, NumPy, Time-Series Forecasting
* **Generative AI:** AutoGen, LangChain, Hugging Face, RAG, LoRA/QLoRA
* **Cloud & DevOps:** AWS, Docker, Kubernetes, CI/CD (GitHub Actions)

---

### Research: Clinical Time-Series Forecasting

I am researching **continuous-time machine learning models** to improve post-operative care for thyroidectomy patients.

* **The Clinical Context:** The critical challenge in this recovery is monitoring **calcium levels**. During surgery, accidental damage to the parathyroid glands can disrupt calcium regulation, causing patients to suffer from **hypocalcemia** (critically low calcium) or **hypercalcemia** (excessively high calcium). These imbalances can lead to life-threatening situations, such as seizures and cardiac failure.
  * **The Shift:** Current hospital protocols are purely **reactive**, keeping patients hospitalized for days just to observe trends. My work shifts this to a **predictive and proactive** approach, allowing doctors to intervene before a patient reaches a critical state.

* **The Data Challenge:** In a real-world clinical setting, this data is **discrete and irregular**. Lab tests and supplement doses do not happen on a fixed schedule; gaps can range from 1 hour to 10 hours.
    * **The Risk of Interpolation:** Architectures like **LSTMs and RNNs** require fixed time steps (e.g., data every hour). To use them, data interpolation is required. But in a high-stakes medical setting, making decisions based on synthetic, guessed data is fundamentally risky.
    * **The "Black Box" Problem:** Standard neural networks operate as **Black Boxes**. They generate predictions without explaining the underlying reasoning. They are also often **overconfident**, outputting a single number without any measure of uncertainty. Doctors cannot trust a model that doesn't know when it might be wrong.

* **My Solution:** I developed a hybrid framework using **HiPPO-LegS** memory combined with a **Gaussian Process**.
    * **Handling Time:** The HiPPO module treats patient history as a continuous function rather than a sequence of dots. It projects the irregular data onto a basis of **orthogonal Legendre polynomials**, creating a compressed memory vector that captures both long-term trends and recent fluctuations. This allows the model to update based on the *exact* elapsed time ($\Delta t$) without interpolation.
    * **Handling Uncertainty:** Instead of a raw number, the **Gaussian Process** outputs a probability distribution. This provides clinicians with a **confidence interval**, explicitly showing when the model is uncertain due to sparse data, enabling safer, more informed interventions.


### Connect with Me
* [LinkedIn](https://www.linkedin.com/in/gayatri-batta)
* [Email](mailto:gayatribatta20@gmail.com)

