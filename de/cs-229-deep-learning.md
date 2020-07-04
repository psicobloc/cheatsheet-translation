**1. Deep Learning cheatsheet**

&#10230; Deep-Learning-Spickzettel

<br>

**2. Neural Networks**

&#10230; Neuronale Netze

<br>

**3. Neural networks are a class of models that are built with layers. Commonly used types of neural networks include convolutional and recurrent neural networks.**

&#10230; Neuronale Netze sind eine Klasse von Modellen die in Schichten aufgebaut sind. Gängige Typen neuronaler Netze sind unter anderem faltende und rekurrente neuronale Netze.

<br>

**4. Architecture ― The vocabulary around neural networks architectures is described in the figure below:**

&#10230; Architektur ― Das Vokabular rund um Architekturen neuronaler Netze ist in folgender Abbildung beschrieben: 

<br>

**5. [Input layer, hidden layer, output layer]**

&#10230; [Eingabeschicht, versteckte Schicht, Ausgabeschicht]

<br>

**6. By noting i the ith layer of the network and j the jth hidden unit of the layer, we have:**

&#10230; Sei i die i-te Schicht des Netzes und j die j-te verborgene Einheit der Schicht, so ist:

<br>

**7. where we note w, b, z the weight, bias and output respectively.**

&#10230; wobei w, b und z jeweils Gewicht, Verzerrung und Ausgabe bezeichnen.

<br>

**8. Activation function ― Activation functions are used at the end of a hidden unit to introduce non-linear complexities to the model. Here are the most common ones:**

&#10230; Aktivierungsfunktion ― Aktivierungsfunktionen werden am Ende einer verborgenen Schicht benutzt um nicht-lineare Komplexität zu ermöglichen. Am häufigsten werden folgende Funktionen angewendet:

<br>

**9. [Sigmoid, Tanh, ReLU, Leaky ReLU]**

&#10230; [Sigmoid, Tanh, ReLU, undichte ReLU (Leaky ReLU)]

<br>

**10. Cross-entropy loss ― In the context of neural networks, the cross-entropy loss L(z,y) is commonly used and is defined as follows:**

&#10230; Kreuzentropieverlust ― Im Kontext neuronaler Netze wird der Kreuzentropieverlust L(z,y) gebräuchlicherweise benutzt und definiert wie folgt:

<br>

**11. Learning rate ― The learning rate, often noted α or sometimes η, indicates at which pace the weights get updated. This can be fixed or adaptively changed. The current most popular method is called Adam, which is a method that adapts the learning rate.**

&#10230; Lernrate ― Die Lernrate, oft mit α oder manchmal mit η bezeichnet, gibt an mit welcher Rate die Gewichtungen aktualisiert werden. Die Lernrate kann konstant sein oder dynamisch angepasst werden. Die aktuell populärste Methode, Adam, aktualisiert die Lernrate dynamisch.

<br>

**12. Backpropagation ― Backpropagation is a method to update the weights in the neural network by taking into account the actual output and the desired output. The derivative with respect to weight w is computed using chain rule and is of the following form:**

&#10230; Fehlerrückführung (backpropagation) ― Fehlerrückführung aktualisiert die Gewichte in neuronalen Netzen durch Einberechnung der tatsächlichen und der gewünschten Ausgabe. Die Ableitung nach der Gewichtung w wird mit Hilfe der Kettenregel berechnet und hat die folgende Form:

<br>

**13. As a result, the weight is updated as follows:**

&#10230; Das Gewicht wird wie folgt aktualisiert:

<br>

**14. Updating weights ― In a neural network, weights are updated as follows:**

&#10230; Das Aktualisieren der Gewichte ― In neuronalen Netzen werden die Gewichtungen wie folgt aktualisiert:

<br>

**15. Step 1: Take a batch of training data.**

&#10230; Schritt 1: Nimm ein Bündel von Lerndaten.

<br>

**16. Step 2: Perform forward propagation to obtain the corresponding loss.**

&#10230; Schritt 2: Führe Vorwärtsausbreitung durch um den dazugehörigen Verlust zu erhalten.

<br>

**17. Step 3: Backpropagate the loss to get the gradients.**

&#10230; Schritt 3: Führe Fehlerrückführung mit dem Verlust durch um die Gradienten zu erhalten.

<br>

**18. Step 4: Use the gradients to update the weights of the network.**

&#10230; Schritt 4: Verwende die Gradienten um die Gewichte im Netz zu aktualisieren.

<br>

**19. Dropout ― Dropout is a technique meant at preventing overfitting the training data by dropping out units in a neural network. In practice, neurons are either dropped with probability p or kept with probability 1−p**

&#10230; Aussetzen ― Aussetzen ist eine Technik um eine Überanpassung der Lerndaten zu verhindern bei der Einheiten in einem neuronalen Netz ausfallen. In der Praxis setzen Neuronen entweder mit Wahrscheinlichkeit p aus oder werden mit Wahrscheinlichkeit 1-p behalten.

<br>

**20. Convolutional Neural Networks**

&#10230; Faltende neuronale Netzwerke (convolutional neural networks, CNN)

<br>

**21. Convolutional layer requirement ― By noting W the input volume size, F the size of the convolutional layer neurons, P the amount of zero padding, then the number of neurons N that fit in a given volume is such that:**

&#10230; Vorraussetzung für eine faltende Schicht ― Sei W das Eingangsvolumen, f die Größe der Neuronen der faltenden Schicht, P die Anzahl der aufgefüllten Nullen, dann ist die Anzahl der Neuronen N die in ein gegebenes Volumen passen:  

<br>

**22. Batch normalization ― It is a step of hyperparameter γ,β that normalizes the batch {xi}. By noting μB,σ2B the mean and variance of that we want to correct to the batch, it is done as follows:**

&#10230; Bündelnormalisierung ― Ein Schritt des Hyperparameters γ,β welcher das Bündel {xi} normalisiert. Seien μB der Mittelwert und σ2B die Varianz von dem Wert mit dem der Batch korrigiert werden soll, dann gilt folgendes:

<br>

**23. It is usually done after a fully connected/convolutional layer and before a non-linearity layer and aims at allowing higher learning rates and reducing the strong dependence on initialization.**

&#10230; Wird üblicherweise nach einer vollständig verbundenen/faltenden Schicht und vor einer nicht-linearen Schicht durchgeführt und bezweckt die Erhöhung der Lernrate und eine Reduzierung der starken Abhängigkeit von der Initialisierung.

<br>

**24. Recurrent Neural Networks**

&#10230; Rekurrente neuronale Netze (recurrent neural networks, RNN)

<br>

**25. Types of gates ― Here are the different types of gates that we encounter in a typical recurrent neural network:**

&#10230; Typen von Gattern ― Verschiedene Typen der einzelnen Gattern die man in einem LSTM Block vorfindet:

<br>

**26. [Input gate, forget gate, gate, output gate]**

&#10230; [Eingangsgatter, Vergessgatter, Ausgangsgatter, Speichergatter]

<br>

**27. [Write to cell or not?, Erase a cell or not?, How much to write to cell?, How much to reveal cell?]**

&#10230; [Zelle beschreiben oder nicht?, Zelle löschen oder nicht?, Wieviel in die Zelle schreiben?, Wieviel um die Zelle aufzudecken?]

<br>

**28. LSTM ― A long short-term memory (LSTM) network is a type of RNN model that avoids the vanishing gradient problem by adding 'forget' gates.**

&#10230; LSTM ― Ein langes Kurzzeitgedächtnis (long short-term memory, LSTM) gehört zu der Klasse der RNN, welches durch Hinzufügen von Vergessgattern das Problem der verschwindenden Gradienten vermeidet. 

<br>

**29. Reinforcement Learning and Control**

&#10230; Bestärkendes Lernen und bestärkende Regelung

<br>

**30. The goal of reinforcement learning is for an agent to learn how to evolve in an environment.**

&#10230; Das Ziel des bestärkenden Lernens ist einen Agenten zu traineren welcher selbstständig lernt sich in einer Umgebung zu entwickeln.

<br>

**31. Definitions**

&#10230; Definitionen

<br>

**32. Markov decision processes ― A Markov decision process (MDP) is a 5-tuple (S,A,{Psa},γ,R) where:**

&#10230; Markow-Entscheidungsproblem ― Ein Markow-Entscheidungsproblem (Markow decision process, MDP) ist ein 5-Tupel (S,A,{Psa},γ,R), wobei

<br>

**33. S is the set of states**

&#10230; S die Menge von Zuständen ist

<br>

**34. A is the set of actions**

&#10230; A die Menge von Aktionen ist

<br>

**35. {Psa} are the state transition probabilities for s∈S and a∈A**

&#10230; {Psa} die Übergangswahrscheinlichkeiten von s∈S und a∈A sind

<br>

**36. γ∈[0,1[ is the discount factor**

&#10230; γ∈[0,1[ der Discount-Faktor ist

<br>

**37. R:S×A⟶R or R:S⟶R is the reward function that the algorithm wants to maximize**

&#10230; R:S×A⟶R oder R:S⟶R die Belohnungsfunktion ist die der Algorithmus zu maximieren wünscht

<br>

**38. Policy ― A policy π is a function π:S⟶A that maps states to actions.**

&#10230; Strategie ― Die Strategie π ist die Funktion π:S⟶A welche Zustände auf Aktionen abbildet.

<br>

**39. Remark: we say that we execute a given policy π if given a state s we take the action a=π(s).**

&#10230; Hinweis: Wir führen eine gegebene Strategie π aus wenn wir für einen gegebenen Zustand s die Aktion a=π(s) tätigen.

<br>

**40. Value function ― For a given policy π and a given state s, we define the value function Vπ as follows:**

&#10230; Wertfunktion ― Für eine gegebene Strategie π und einen gegebenen Zustand s definieren wir die Wertfunktion Vπ wie folgt:

<br>

**41. Bellman equation ― The optimal Bellman equations characterizes the value function Vπ∗ of the optimal policy π∗:**

&#10230; Bellman-Gleichung ― Die optimale Bellman-Gleichung charakterisiert die Wertfunktion Vπ∗ der optimalen Strategie π∗:

<br>

**42. Remark: we note that the optimal policy π∗ for a given state s is such that:**

&#10230; Hinweis: wir bezeichnen die optimale Strategie π∗ für einen gegebenen Zustand s sodass:

<br>

**43. Value iteration algorithm ― The value iteration algorithm is in two steps:**

&#10230; Wert-Interationsalgorithmus ― Der Wert-Iterationsalgorithmus hat zwei Schritte:

<br>

**44. 1) We initialize the value:**

&#10230; 1) Wir initialisieren den Wert:

<br>

**45. 2) We iterate the value based on the values before:**

&#10230; 2) Wir iterieren den Wert aufbauend auf dem vorherigen Wert:

<br>

**46. Maximum likelihood estimate ― The maximum likelihood estimates for the state transition probabilities are as follows:**

&#10230; Maximum-Likelihood-Schätzung ― Die Maximum-Likelihood-Schätzungen für die Zustandsübergangswahrscheinlichkeiten sind wie folgt: 

<br>

**47. times took action a in state s and got to s′**

&#10230; Anzahl Ausführung Aktion a in Zustand s führt zu s′

<br>

**48. times took action a in state s**

&#10230; Anzahl Ausführung Aktion a in Zustand s

<br>

**49. Q-learning ― Q-learning is a model-free estimation of Q, which is done as follows:**

&#10230; Q-Lernen ― Q-Lernen ist eine modellfreie Schätzung von Q welche wie folgt durchgeführt wird: 

<br>

**50. View PDF version on GitHub**

&#10230; Finde die PDF-Version auf GitHub

<br>

**51. [Neural Networks, Architecture, Activation function, Backpropagation, Dropout]**

&#10230; [Neuronale Netze, Architektur, Aktivierungsfunktion, Fehlerrückführung, Aussetzen]

<br>

**52. [Convolutional Neural Networks, Convolutional layer, Batch normalization]**

&#10230; [Faltende neuronale Netzwerke, faltende Schicht, Bündelnormalisierung]

<br>

**53. [Recurrent Neural Networks, Gates, LSTM]**

&#10230; [Rekurrente neuronale Netze, Gatter, LSTM]

<br>

**54. [Reinforcement learning, Markov decision processes, Value/policy iteration, Approximate dynamic programming, Policy search]**

&#10230; [Bestärkendes Lernen, Markow-Entscheidungsproblem, Wert-Strategie-Iteration, näherungs-dynamische Programmierung, Strategiesuche]
