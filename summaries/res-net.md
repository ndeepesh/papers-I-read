Residual Networks Notes
1. Vanishing Gradients problem addressed by ReLU’s and Batch Normalization
2. Incomes another problem (Degradation Problem) - As the network depth increases, accuracy gets saturated and eventually starts degrading(This is not overfitting and train error degrades)
3. Construct deeper networks with Identity Mappings
4. To counter degradation problem, residual representations are introduced. Our stacked layers will learn this residual representation(or mapping) rather than original mapping(Theories in Image recognition and graphics strenthen this claim that optimization is better and faster when converted to residual representation)
5. Some Intuitions - Can resolve Gradient Diminishing problem since there is some part of the network not in influence of activation functions.
6. More Intuitions - More information flow through the network, so the further stacked layers need not learn the whole function but only the errors induced in previous stacked layer(error = actual function - previous output)
7. More Intuitions - Quantitavely mention that degradation problem is not due to diminishing gradients since they use BN and manually verify norms in forward and backward passes. So this has to be a problem with learning where convergence is not possible(not studied here) with deep layers
8. When adding identity, there may be cases where dimensions don’t match. To match those 3 techniques introduced
    1. Zero padding to match dimensions
    2. Projections for remaining dimensions and identity for rest
    3. Projections for all
