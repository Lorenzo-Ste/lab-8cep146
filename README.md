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
| 1 | Great | Poor | Cheap | Like | TBD | TBD |
| 2 | Bad | Great | Expensive | Dislike | TBD | TBD |
| 3 | Good | Okay | Moderate | Like | TBD | TBD |
| 4 | Poor | Poor | Cheap | Dislike | TBD | TBD |
| 5 | Excellent | Excellent | Expensive | Like | TBD | TBD |
| 6 | Okay | Bad | Moderate | Dislike | TBD | TBD |
| 7 | Great | Okay | Cheap | Like | TBD | TBD |
| 8 | Poor | Excellent | Expensive | Dislike | TBD | TBD |
| 9 | Excellent | Poor | Moderate | Like | TBD | TBD |
| 10 | Okay | Okay | Expensive | Like | TBD | TBD |

### Weight Adjustment Tracker

| Round | Food | Service | Price | Adjustment |
|-------|------|---------|-------|------------|
| Initial | 1 | 1 | 1 | Starting weights |
| Card 1 | TBD | TBD | TBD | TBD |
| Card 2 | TBD | TBD | TBD | TBD |
| Card 3 | TBD | TBD | TBD | TBD |
| Card 4 | TBD | TBD | TBD | TBD |
| Card 5 | TBD | TBD | TBD | TBD |
| Card 6 | TBD | TBD | TBD | TBD |
| Card 7 | TBD | TBD | TBD | TBD |
| Card 8 | TBD | TBD | TBD | TBD |
| Card 9 | TBD | TBD | TBD | TBD |
| Card 10 | TBD | TBD | TBD | TBD |
