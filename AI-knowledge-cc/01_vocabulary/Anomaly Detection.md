# Anomaly Detection

## Definition (English)
Anomaly detection is the identification of rare items, events, or observations that differ significantly from the majority of the data — often used for fraud detection, system health monitoring, and quality control.

## Chinese
异常检测 — 识别与大多数数据显著不同的稀有项、事件或观察结果，常用于欺诈检测、系统监控和质量控制。

## German
die Anomalieerkennung / die Ausreißererkennung

## Intuition
Think of a security guard watching surveillance footage for 8 hours. Most of the time, nothing unusual happens. But when someone climbs over a fence instead of using the gate, it stands out immediately. Anomaly detection algorithms do the same thing — they learn what "normal" looks like and flag anything unusual.

## Example
A bank uses Isolation Forest (an unsupervised anomaly detection algorithm) to identify fraudulent credit card transactions. The model flags purchases that are unusually large, in unusual locations, or at unusual times compared to the customer's normal spending pattern — without needing examples of historical fraud.

## Spoken Version
"Anomaly detection finds the outliers — the transactions, behaviors, or events that don't fit the normal pattern. It's critical for fraud detection and system monitoring."

## German Workplace Example
"Wir setzen Anomalieerkennung ein, um ungewöhnliche Transaktionen in Echtzeit zu identifizieren und Betrug zu verhindern."

## Related Concepts
[[Unsupervised Learning]], [[Unlabeled Data]], [[Clustering]]

## Tags
#unsupervised-learning #anomaly-detection #fraud-detection
