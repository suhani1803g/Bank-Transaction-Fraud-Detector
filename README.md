# Bank-Transaction-Fraud-Detector
A Bank Transaction Fraud Detector is a system that monitors customer transactions to identify unusual patterns, suspicious activities, or anomalies. It helps prevent fraud by flagging and blocking potentially unauthorized or fraudulent transactions in real time.
# 🏦 Bank Transaction Fraud Detector

This is a simple Python script that detects potential fraudulent transactions based on basic rules.

## 🚀 Code Example

```python
# Simple Bank Transaction Fraud Detector

# Sample transaction data: (transaction_id, amount, location, time)
transactions = [
    (1, 200, "Delhi", "10:30"),
    (2, 5000, "Mumbai", "11:00"),
    (3, 15000, "London", "11:05"),
    (4, 300, "Delhi", "11:10"),
]

# Rule-based fraud detection
def detect_fraud(transaction):
    transaction_id, amount, location, time = transaction
    
    # Example rules:
    if amount > 10000:  # unusually high amount
        return True
    if location not in ["Delhi", "Mumbai"]:  # unexpected location
        return True
    return False

# Check each transaction
for txn in transactions:
    if detect_fraud(txn):
        print(f"⚠️ Fraudulent Transaction Detected: {txn}")
    else:
        print(f"✅ Legitimate Transaction: {txn}")

