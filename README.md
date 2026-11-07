# Lab08 - How a Neural Network Learns

## 1. Network Diagram

```text
Input Layer          Middle Layer         Output Layer

Food -------------\
                   \
Service -----------> Decision Node -----> LIKE / DISLIKE
                   /
Price ------------/
```

## 2. Team Roles

| Student | Role | Responsibility |
|---------|------|----------------|
| Lorenzo-Ste| Decision Node | Predict LIKE or DISLIKE |
| Zilan Lin | Input Feeder / Tracker | Read scenarios, reveal answers, track weights |

## 3. Initial Weight Tracker

Each star (⭐) represents one weight token.
More stars indicate greater importance in decision-making.

| Feature | Tokens | Weight |
|---------|--------|--------|
| Food | ⭐ | 1 |
| Service | ⭐ | 1 |
| Price | ⭐ | 1 |

All features start with equal weights.

## 4. Part A: Training Results

| Card | Food | Service | Price | Prediction | Actual | Correct? |
|------|------|---------|-------|------------|--------|----------|
| 1 | Great | Poor | Cheap | Like | Like | Yes |
| 2 | Bad | Great | Expensive | Dislike | Dislike | Yes |
| 3 | Good | Okay | Moderate | Like | Like | Yes |
| 4 | Poor | Poor | Cheap | Dislike | Dislike | Yes |
| 5 | Excellent | Excellent | Expensive | Like | Like | Yes |
| 6 | Okay | Bad | Moderate | Dislike | Dislike | Yes |
| 7 | Great | Okay | Cheap | Like | Like | Yes |
| 8 | Poor | Excellent | Expensive | Dislike | Dislike | Yes |
| 9 | Excellent | Poor | Moderate | Like | Like | Yes |
| 10 | Okay | Okay | Expensive | Like | Dislike | No |

### Training Accuracy

- Correct Predictions: 9/10
- Overall Accuracy: 90%

### Weight Adjustment Tracker

Each star (⭐) represents one weight token.

| Round | Food | Service | Price | Adjustment |
|-------|------|---------|-------|------------|
| Initial | ⭐ | ⭐ | ⭐ | Starting weights |
| Card 1 | ⭐ | ⭐ | ⭐ | No change |
| Card 2 | ⭐ | ⭐ | ⭐ | No change |
| Card 3 | ⭐ | ⭐ | ⭐ | No change |
| Card 4 | ⭐ | ⭐ | ⭐ | No change |
| Card 5 | ⭐ | ⭐ | ⭐ | No change |
| Card 6 | ⭐ | ⭐ | ⭐ | No change |
| Card 7 | ⭐ | ⭐ | ⭐ | No change |
| Card 8 | ⭐ | ⭐ | ⭐ | No change |
| Card 9 | ⭐ | ⭐ | ⭐ | No change |
| Card 10 | ⭐ | ⭐ | ⭐⭐ | Increased Price weight |

## 5. Part B: Testing Phase

### Testing Results

| Card | Food | Service | Price | Prediction | Actual | Correct? |
|------|------|---------|-------|------------|--------|----------|
| 11 | Good | Excellent | Cheap | LIKE | LIKE | YES |
| 12 | Bad | Bad | Expensive | DISLIKE | DISLIKE | YES |
| 13 | Excellent | Great | Moderate | LIKE | LIKE | YES |

### Testing Accuracy

- Correct Predictions: 3 / 3
- Overall Accuracy: 100 %

### Team Comparison

- Our Team Accuracy: TBD
- Other Team Accuracy: TBD
- Most Important Feature: TBD

## 6. Reflection Discussion

### Q1. How did your predictions improve?

My predictions were mostly correct besides one but I learned from my mistake and was able to better judge what was more important (between price, service and food) when deciding if a customer would like a restuarnt. So I think by trial and error the more you adjust weights the more sharp you would become.

### Q2. How did "weights" (tokens) help you learn
I think weights are there to help you understand moreso how important each feature is when making your decision. Like if food had more tokens it should mean that food had a bigger influence on wether we like the restaurant or not
. The tokens were meant to eb adjusted to help us guage how chagning weights can improve AI's decsions.

### Q3. What would happen with more layers or inputs?

If we added mroe layers or inputs I think our neural network wouldve had been able to take in alot more information and see even more difficult patterns. Instead of only the three that we had we could have also had maybe included where the restaurant was, how clean it was, the atmosphere etc. This could help with more accurate predicitons.

### Q4. How does this reflect how real AI works?

This activity definetly reflects well how AI works as neural networks learn by taking information, making predictions and adjusting the weight based on errors. Real AI systems do this process over and over again using large sets of data until they are able to be good at recognizing patterns and making decisions.

