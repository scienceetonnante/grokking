# Grokking with a simple embedding + feedfoward network on modular addition

Grokking is a new phenomenon in deep learning where some models exhibit a (very) late generalisation phase, after an initial phase of very strong over-fitting.

In the original publication, it has been demonstrated with modular arithmetic and a transformer architecture.

<img width="1310" alt="grokking_openai" src="https://github.com/scienceetonnante/grokking/assets/15683540/d516f2a9-f805-4c61-887d-911baffab2bf">

POWER, Alethea, BURDA, Yuri, EDWARDS, Harri, et al. Grokking: Generalization beyond overfitting on small algorithmic datasets. arXiv preprint arXiv:2201.02177, 2022.

In this notebook, I show how to reproduce the grokking phenomenon in a minimalistic setting : modular addition and a model involving only linear embedding followed by a feedfoward (one hidden layer).

![architecture](https://github.com/scienceetonnante/grokking/assets/15683540/5c49927b-5588-4dd8-a9b9-c514db91affb)

![accuracy_zoom](https://github.com/scienceetonnante/grokking/assets/15683540/932d4881-5dbd-4c7e-a22f-ed712622370e)

![loss_zoom](https://github.com/scienceetonnante/grokking/assets/15683540/d02a2fa0-450f-4b32-a4a6-e5455f651344)


In particular, principal component analysis on the embedding layer weights shows how the model learnt to organize the embedding of the tokens in a circular way, similar to what happens with a clock.

![pca_annotated](https://github.com/scienceetonnante/grokking/assets/15683540/1d9110a1-808f-4581-ba9c-074509f8001c)


Other relevant publications :

NANDA, Neel, CHAN, Lawrence, LIBERUM, Tom, et al. Progress measures for grokking via mechanistic interpretability. arXiv preprint arXiv:2301.05217, 2023.

LIU, Ziming, KITOUNI, Ouail, NOLTE, Niklas S., et al. Towards understanding grokking: An effective theory of representation learning. Advances in Neural Information Processing Systems, 2022, vol. 35, p. 34651-34663.

Liu, Z., Michaud, E. J., & Tegmark, M. (2022). Omnigrok: Grokking beyond algorithmic data. arXiv preprint arXiv:2210.01117.

ZHONG, Ziqian, LIU, Ziming, TEGMARK, Max, et al. The Clock and the Pizza: Two Stories in Mechanistic Explanation of Neural Networks. arXiv preprint arXiv:2306.17844, 2023.
