# Payment System Python Project

## Overview

This is a simple **Payment Transaction System** built in **Python**.
It demonstrates:

* Python **OOP concepts** (abstract classes, inheritance, private variables)
* Python **data structures** (list, set, dictionary)
* **Duplicate transaction detection**
* **Docker containerization** for easy deployment
* Ready for Git and Docker workflow

---

## Project Structure

```
payment-system/
├── app.py
├── requirements.txt
├── Dockerfile
├── payment/
│   ├── __init__.py
│   ├── base.py
│   ├── upi.py
│   └── card.py
└── data/
    ├── __init__.py
    └── storage.py
```

---

## Features

* **Multiple payment methods**: UPI, Card
* **Duplicate transaction detection** using a `set`
* **Private balance variable** for secure tracking
* **Global transaction limit**
* Easy to **extend with new payment methods**

---

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/neesiraj/payment-system.git
cd payment-system
```

### 2. Install Python dependencies (if any)

```bash
pip install -r requirements.txt
```

### 3. Run locally

```bash
python app.py
```

Expected output:

```
Paid using UPI: 1000
Transaction successful
Duplicate transaction!
Paid using Card: 2000
Transaction successful
Balance: 2000
[{'id': 'TXN1', 'amount': 1000, 'method': 'UPI'}, {'id': 'TXN2', 'amount': 2000, 'method': 'Card'}]
```

---

## Docker Usage

### Build Docker Image

```bash
docker build -t payment-app .
```

### Run Docker Container

```bash
docker run payment-app
```

* Output will be same as running locally
* Containerized app is portable and can run anywhere with Docker

---

## Notes

* The project uses **Python 3.10+**
* `payment` folder is a **package** with abstract and child classes
* `data` folder stores **transaction storage**
* Duplicate transactions are prevented using a **set**

---

## Future Enhancements

* Add **more payment methods** (PayPal, Wallet, etc.)
* Implement **transaction reports**
* Add **unit tests**
* Integrate with **GitHub Actions** for CI/CD (optional)

---

## Author

Neeraj Rajput
