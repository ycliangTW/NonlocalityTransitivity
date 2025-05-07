# Nonlocality Transitivity

Matlab data relevant to the work reported in the preprint ["Nonlocality of Quantum States can be Transitive"](https://arxiv.org/abs/2412.10505)

In the Matlab data file [NLTransitivityFromHaarRandomThreeQutrit.mat](https://github.com/ycliangTW/NonlocalityTransitivity/blob/main/NLTransitivityFromHaarRandomThreeQutrit.mat), one finds 500 state vectors for three-qutrit pure states generated from Haar-random unitaries stored as the columns of the variable PsiNLT. The marginals of all these vectors are examples of reduced states exhibiting so-called nonlocality transitivity of quantum states.

More precisely, from the j-th of these vectors, PsiNLT(:,j), the partial traces of the corresponding projector give three two-qutrit reduced density matrices, rhoAB{j}, rhoBC{j}, and rhoAC{j}. It can be verified that all these reduced states are nonlocal by noting that they violate either the CHSH-Bell inequality or the [I3322-Bell inequality](https://arxiv.org/abs/quant-ph/0306129).

In the 500 x 3 variable visM2, one finds the best [white-noise visibility](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.85.052113) found for each of these reduced states when optimizing their CHSH-Bell inequality violation using the algorithm presented [here](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.75.042103). A CHSH-Bell inequality violation is found if and only if the corresponding entry is less than 1. Otherwise, the entry is set to the default value of 100. For example, visM2(j,1) gives the best white-noise visibility found for rhoAB{j}.

Similarly, in the 500 x 3 variable visM3, one finds the best white-noise visibility found for each of these reduced states when optimizing their I3322-Bell inequality violation. An I3322-Bell inequality violation is found if and only if the corresponding entry is less than 1. Otherwise, the entry is set to the default value of 100.

Finally, in the 500 x 1 variable MinF, one finds the minimum fidelity (with respect to each vector in PsiNLT) of the global state compatible with the respective rhoAB and rhoBC marginals. All these entries deviate from 1 by less than 1e-6, indicating that (within numerical precision of the optimization), the global state is uniquely determined by these reduced states.

