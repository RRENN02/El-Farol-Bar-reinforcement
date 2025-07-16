# El Farol Bar Problem with Reinforcement Learning and LSTM Agents
El Farol Bar Problem (Arthur, 1994): Every week, a group of people decides independently whether to go to a popular bar. If the bar is too crowded, they don't enjoy it. If too few people go, it's not lively enough. Each person must predict attendance and decide whether to go.
---

## El Farol Bar Problem with Reinforcement Learning and LSTM Agents

### Overview

The El Farol Bar Problem is a classic scenario where agents decide weekly attendance at a bar based on past attendance patterns, trying to avoid overcrowding or underutilization. This project uses reinforcement learning (Q-learning) coupled with Long Short-Term Memory (LSTM) networks to model agent decision-making and predict attendance trends.

### Project Structure

* **Parameters**:

  * `N_AGENTS`: 100 agents simulate decision-making.
  * `BAR_CAPACITY`: Maximum attendees before discomfort.
  * `TOO_FEW`: Minimum attendees prompting agent dissatisfaction.
  * `WEEKS`: Simulation duration in weeks.
  * `SEQUENCE_LENGTH`: Length of LSTM sequences, maintaining a 1:3 ratio to weeks.

* **Components**:

  * **LSTM Predictor**: Each agent employs an LSTM model trained on historical attendance data to predict future attendance trends.
  * **Q-learning Agent**: Agents utilize Q-learning to determine whether to attend based on predicted and peer-averaged attendance forecasts.
  * **Social Dynamics**: Agents communicate with a subset of peers, influencing decisions through communication trust weights.
  * **Simulation**: Simulates weekly attendance decisions over the specified number of weeks, adjusting strategies based on rewards and attendance outcomes.

### How It Works

1. **Initialization**: Agents start with random initial attendance histories and LSTM models trained on this data.
2. **Prediction and Decision**: Each agent predicts attendance using its LSTM model and combines this prediction with peer-averaged forecasts to decide attendance.
3. **Learning and Adaptation**: Agents use Q-learning to update attendance decisions based on rewards tied to attendance outcomes (e.g., overcrowding or underutilization).
4. **Simulation**: The simulation iterates over weeks, adjusting attendance strategies based on past performance and social influences.
5. **Results**: Tracks average epsilon values (exploration rates) and attendance outcomes over the simulation period.

### Implementation Details

* **Technologies**: Python with TensorFlow/Keras for LSTM modeling and reinforcement learning, NumPy for simulation mechanics.
* **Outcome**: Provides insights into optimal attendance strategies under dynamic bar conditions, showcasing the interplay between individual decisions and collective outcomes.

### Future Improvements

* Enhance LSTM model architecture and hyperparameters.
* Integrate more complex social interaction dynamics.
* Extend to real-world scenarios with additional environmental factors.

### Conclusion

This project demonstrates how reinforcement learning and LSTM networks can tackle complex decision-making scenarios like the El Farol Bar Problem, offering insights into adaptive behavior and social dynamics in dynamic environments.
