# Reinforcement Learning Tutorial

An interactive tutorial series for learning Reinforcement Learning (RL) fundamentals through hands-on experimentation.

## 📁 Project Structure

```
rl-tutorial/
├── examples/
│   └── chapter-1/
│       └── chapter-1.html
└── README.md
```

## 🎯 Learning Objectives

### Chapter 1: The Core of Reinforcement Learning
- **Interactive Maze Game**: Guide a robot (🤖) to cheese (🧀) in a 5x5 grid world
- **Reward Design**: Experiment with different reward functions and see their impact
- **Q-Learning Implementation**: Watch Q-values update in real-time as the agent learns
- **Experiment Analysis**: Compare different training strategies and their outcomes
- **Reward Hacking**: Discover how agents can exploit poorly designed reward systems

## 🔧 Technical Concepts

### Reinforcement Learning Fundamentals
- **Agent-Environment Interaction**: The core feedback loop of RL
- **States, Actions, Rewards**: The fundamental components of RL problems
- **Q-Learning Algorithm**: Value-based learning with exploration vs exploitation
- **Reward Function Design**: How reward structure shapes agent behavior
- **Policy Optimization**: Finding optimal strategies through trial and error

### Key RL Components
```
Environment:
├── State Space (5x5 grid positions)
├── Action Space (Up, Down, Left, Right)
└── Reward Function (Goal, Wall, Step penalties)

Agent:
├── Q-Table (State-Action value estimates)
├── Learning Rate (0.1)
├── Discount Factor (0.9)
└── Exploration Rate (0.3 → 0.01)
```

### Learning Process
1. **Exploration**: Agent tries random actions to discover environment
2. **Q-Value Updates**: Learning from rewards and future state values
3. **Exploitation**: Agent uses learned Q-values to choose best actions
4. **Convergence**: Q-values stabilize as agent finds optimal policy

## 🛠️ Interactive Features

### Step-by-Step Learning
1. **Manual Play**: Experience the challenge yourself
2. **Theory Introduction**: Understand RL concepts
3. **Reward Design**: Create custom reward functions
4. **Agent Training**: Run learning episodes and observe Q-values
5. **Analysis**: Compare different training strategies

### Experimentation Tools
- **Preset Reward Functions**: Default, Timid, Lazy agents
- **Custom Rewards**: Design your own reward structure
- **Training Episodes**: Run 10 or 100 learning episodes
- **Performance Metrics**: Average steps, rewards, and efficiency
- **LLM Integration**: Generate prompts for deeper analysis

## 📚 Learning Outcomes

### Core RL Concepts
- **Reward Maximization**: Agents learn to maximize cumulative rewards
- **Exploration vs Exploitation**: Balancing learning and performance
- **Value Function Approximation**: Q-values represent action quality
- **Policy Improvement**: Iterative refinement of decision-making

### Practical Insights
- **Reward Design is Critical**: Poor rewards lead to unexpected behaviors
- **Reward Hacking**: Agents find loopholes in reward functions
- **Multiple Metrics Matter**: Steps, rewards, and efficiency all count
- **Hyperparameter Sensitivity**: Learning rates affect training stability

## 🚀 Getting Started

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd rl-tutorial
   ```

2. **Open Chapter 1**:
   ```bash
   open examples/chapter-1/chapter-1.html
   ```

3. **Start Learning**:
   - Complete the 5-step interactive tutorial
   - Experiment with different reward functions
   - Run training episodes and analyze results
   - Compare agent behaviors across different settings

## 🔍 Code Examples

### Q-Learning Update Rule
```javascript
const newQ = oldQValue + LEARNING_RATE * (reward + DISCOUNT_FACTOR * maxFutureQ - oldQValue);
```

### Action Selection (ε-greedy)
```javascript
function chooseAction(pos) {
    if (Math.random() < explorationRate) return Math.floor(Math.random() * 4);
    const qValues = getQValues(pos);
    return qValues.indexOf(Math.max(...qValues));
}
```

### Reward Function Design
```javascript
const presets = {
    default: { goal: 10, wall: -5, step: -0.1 },
    timid: { goal: 10, wall: -100, step: -0.1 },
    lazy: { goal: 10, wall: -1, step: 0.1 }
};
```

## 📈 Advanced Topics

### Future Tutorial Chapters
- **Reward Shaping**: Intermediate rewards for faster learning
- **Hyperparameter Tuning**: Optimizing learning rates and exploration
- **Complex Environments**: Larger mazes and dynamic obstacles
- **Deep Q-Networks**: Neural network-based value approximation
- **Policy Gradient Methods**: Direct policy optimization

### RL Applications
- **Game AI**: Strategy games, robotics navigation
- **Autonomous Systems**: Self-driving cars, drone control
- **Recommendation Systems**: Content personalization
- **Resource Management**: Energy optimization, inventory control

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add new tutorial chapters or improve existing ones
4. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy Learning! 🤖🧀** 