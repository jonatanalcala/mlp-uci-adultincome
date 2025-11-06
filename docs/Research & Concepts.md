# Project Two Reflections
  Predictive modeling with socioeconomic data reveals patterns in employment, income, and demographics. We used a Multilayer Perceptron (MLP) to predict if someone earns more or less than $50,000, using the Adult Income dataset. This dataset, based on U.S. Census records, lists age, education, occupation, gender, and marital status.
Though this is a basic binary classification, the dataset has social and historical inequalities that may affect model performance and fairness. We focused on both model design and performance, as well as on ethical issues, bias, and methods to reduce overfitting.

# Model Architecture
  The MLP uses 91 input features, created by one-hot encoding demographic and job variables. The model has two hidden layers with 128 and 64 neurons. The first layer finds broad patterns, and the second layer refines them. This keeps the model complex enough to learn without being too deep to be inefficient. We used ReLU activation in the hidden layers to introduce nonlinearity, enabling the model to make complex decisions and avoid vanishing gradients, resulting in faster, more stable training. The output layer has two neurons, each for one income class. This fits well with the CrossEntropyLoss function used during training. We trained the model for 20 epochs with the Adam optimizer at a learning rate of 0.001.

# Mitigating Overfitting

To help the model perform well on new data, we used several methods to prevent overfitting:
*Dropout Layers (0.3)
  *We added dropout layers with a 30% rate after each hidden layer. This helped the model generalize better by avoiding memorization of data patterns. 
*Monitoring Training vs. Validation Performance
   *We monitored accuracy and loss to check for differences between training and validation results. If validation stopped improving while training kept getting better, we ended training at 20 epochs to prevent overfitting.
*Controlled Learning Rate
  *Using the Adam optimizer with a learning rate of 0.001 helped the model learn steadily without fitting to random noise in the training data.

These methods helped the model perform well on new data and kept it from just memorizing the training set.

# Ethical Considerations
  The Adult Income dataset shows historical social inequalities, especially in how income varies by gender, race, and job type. These differences can be learned by the model, causing it to repeat or even strengthen unfair patterns. Even if we remove sensitive details like gender or race, the model can still guess them from related variables, such as job type, education, or marital status, which often link to protected traits. So, taking out obvious identifiers does not ensure fairness.
  Lack of model transparency makes this problem harder. MLPs are not easy to interpret, making it difficult to explain their predictions or identify sources of bias. When these models are used in real decisions such as hiring, lending, or insurance, this lack of clarity can lead to unfair or unaccountable outcomes that often harm marginalized groups.
  Because of these issues, using machine learning with socioeconomic data requires careful attention to bias, careful evaluation of how the model performs across different groups, and a clear explanation of its limits.
  
# Conclusion

  In this project, we built an MLP model to classify income levels with the Adult Income dataset. We balanced complexity and generalization in our design, and used dropout, limited training time, and careful validation checks to prevent overfitting. Still, because the dataset contains social inequalities, the ethical risks are serious. Using such models responsibly means being aware of bias, checking results for different groups, and avoiding real-world uses that could make economic gaps worse.

**Our analysis shows that it is important to consider both technical results and ethical responsibility when building predictive models.**

