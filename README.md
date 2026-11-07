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
| 11 | Good | Excellent | Cheap | TBD | TBD | TBD |
| 12 | Bad | Bad | Expensive | TBD | TBD | TBD |
| 13 | Excellent | Great | Moderate | TBD | TBD | TBD |
