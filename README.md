# NLP_INTRODUCTION
---
---



![RNN INTRO](https://github.com/MANOJ-S-NEGI/NLP_INTRODUCTION/assets/99602627/c6c56de4-d228-4b6b-9bd7-fd8bd62beb09)

<table>
  <tr>
    <th>SimpleRNN</th>
    <th>LSTM</th>
    <th>GRU</th>
  </tr>
  <tr>
    <td>
    A Simple Recurrent Neural Network (SimpleRNN) is a type of recurrent neural network (RNN) that processes sequences of data by maintaining a hidden state. It's a type of neural network layer that can be used for tasks 
      involving sequential or time-series data.<br><br>

  1. Recurrent Neurons:
     * SimpleRNNs have recurrent neurons, which allow them to maintain a form of memory about previous information in a sequence.

  2. Hidden State:
     * At each time step, a SimpleRNN takes both the current input and the previous hidden state as input. The hidden state acts as a form of memory that is updated and passed along through time.
  
  3. Mathematical Operation:
     * The output at each time step is computed as a function of the current input and the previous hidden state, similar to the operations in a feedforward neural network.

  4. Vanishing Gradient Problem:
     * SimpleRNNs can suffer from the vanishing gradient problem, which can make it difficult to learn long-term dependencies in sequences.
  
  5. Limited Context:
     * Due to their structure, SimpleRNNs have difficulty capturing long-term dependencies in sequences. As a result, they are often limited to tasks where the context window is relatively small.
  
  
  6. Drawbacks:
      * Due to the vanishing gradient problem, SimpleRNNs are often not suitable for tasks that require capturing long-term dependencies. More advanced recurrent units like LSTM (Long Short-Term Memory) and GRU (Gated Recurrent Unit) have been developed to address this issue.
   
  </td>
<td>
 Long Short-Term Memory (LSTM) is a type of recurrent neural network (RNN) architecture that is designed to handle long-range dependencies in sequential data.

Characteristics of LSTM:

1. **Memory Cells**:
   - The fundamental building block of an LSTM is the memory cell. These cells have the ability to store information over long sequences, which helps in capturing long-term dependencies.

2. **Gating Mechanisms**:
   - LSTMs use gating units to control the flow of information into and out of the memory cell. These gates are controlled by sigmoid and tanh activation functions, allowing the network to learn when to forget, input, and output information.

3. **Forget Gate**:
   - The forget gate decides what information to discard from the previous cell state. It's a sigmoid layer that outputs values between 0 and 1. A value of 1 means "keep this" while a value of 0 means "forget this".

4. **Input Gate**:
   - The input gate decides what new information to store in the cell state. It consists of a sigmoid layer and a tanh layer. The sigmoid layer decides which values to update, and the tanh layer creates a vector of new candidate values that could be added to the state.

5. **Update to Cell State**:
   - The cell state is updated by combining the values from the forget gate (information to discard) and the input gate (new information to add).

6. **Output Gate**:
   - The output gate decides what to output based on the current cell state. It's a sigmoid layer that determines which parts of the cell state are going to be output.

7. **Backpropagation Through Time (BPTT)**:
   - Like other recurrent layers, LSTM uses the BPTT algorithm to learn from sequences by unrolling the network through time and backpropagating the gradients.

8. **Vanishing Gradient Problem**:
   - LSTMs are designed to mitigate the vanishing gradient problem that can occur in standard RNNs, which makes them better at learning long-term dependencies.


    
  </td>

  <td>
Gated Recurrent Units (GRU) is another type of recurrent neural network (RNN) architecture, introduced by Cho et al. in 2014. It's similar to Long Short-Term Memory (LSTM) in that it's designed to handle long-range dependencies in sequential data. However, it simplifies the architecture and combines some of the functions of LSTM units.

**Characteristics of GRU:**

1. **Gating Mechanisms**:
   - Like LSTMs, GRUs use gating units to control the flow of information. However, GRUs have only two gates: a reset gate and an update gate, whereas LSTMs have three gates.

2. **Reset Gate**:
   - The reset gate controls how much of the previous state to forget. It is computed using a sigmoid activation function and determines which information to discard from the previous state.

3. **Update Gate**:
   - The update gate determines how much of the previous state to keep and how much of the new candidate values to add. It also uses a sigmoid activation function.

4. **Candidate State**:
   - In GRUs, there is no separate candidate state like in LSTMs. Instead, a new candidate state is computed directly from the previous state and the current input.

5. **Update to State**:
   - The new state is computed by combining the values from the reset gate (information to forget) and the candidate state.

6. **Output**:
   - In GRUs, the output is simply the same as the current state. There is no separate output gate like in LSTMs.

7. **Vanishing Gradient Problem**:
   - GRUs, like LSTMs, are designed to mitigate the vanishing gradient problem that can occur in standard RNNs.

8. **Simpler Architecture**:
   - GRUs have a simpler architecture compared to LSTMs, which can make them computationally more efficient and easier to train.

Overall, GRUs have shown effectiveness in various tasks involving sequential data and are an alternative to LSTMs. The choice between using an LSTM or a GRU often depends on the specific task and dataset, and it's common practice to experiment with both to see which one performs better.
    
  </td>
  </tr>
</table>

