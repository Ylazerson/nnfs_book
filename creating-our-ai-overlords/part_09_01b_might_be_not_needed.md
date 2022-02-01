# B"H 

### Intro


<u>**Scenario A: 1 neuron in current layer, 1 in next layer**</u>

So far, we have performed an example backward pass with a **single neuron**, which received a **singular derivative**, `deriv_from_next_layer` (from "next" layer) to apply the chain rule. 

<br>

---

<u>**Scenario B: 1 neuron in current layer, mulitple in next layer**</u>

Let’s consider **multiple neurons** in the next layer. 

A **single neuron** of the current layer connects to all of them — they all receive the output of this neuron. 

What will happen during backpropagation? 
- Each neuron from the next layer will return a partial derivative of its function with respect to this input. 
- The neuron in the current layer will receive a vector consisting of these derivatives. 
- We need this to be a **singular value** for a singular neuron. 
- To continue backpropagation, we need to **sum** this vector.

<br>

---

<u>**Scenario C: Multiple neurons in current layer, mulitple in next layer**</u>

During backpropagation: 
- Each neuron from the current layer will receive a vector of partial derivatives the same way that we described for Scenario B. 
- With a layer of neurons, it’ll take the form of a list of these vectors, or a 2D array. 
- Each neuron in the next layer is going to output a gradient of the partial derivatives with respect to all of its inputs. 
- From all the neurons in the next layer this will form a list of these vectors. 

