# Python Assignment 2: Data Structures & Conditional Statements

A data analysis project focused on using Python's fundamental data structures (**Lists, Dictionaries, Sets**) and **Conditional Logic** to process, classify, and analyze customer support ticket records.

---

## 📌 Project Overview
The objective of this assignment is to demonstrate the practical application of core Python data structures and conditional statements by processing real-world customer support data. The code automates workload distribution analysis and identifies high-detail customer complaints.

### Key Deliverables:
1. **Data Structure Operations:** Storing and mapping support ticket records using Python Dictionaries and Lists.
2. **Priority Categorization:** Counting and grouping tickets by urgency levels using conditional logic (`if-else`)[cite: 1].
3. **Text Length Inspection:** Processing issue descriptions using string splitting and dynamic iteration (`enumerate()`) to extract complex issues[cite: 1].

---

## 📊 Key Findings & Results

### 1. Priority Breakdown
- **High Priority Tickets:** 4[cite: 1]
- **Medium Priority Tickets:** 3[cite: 1]
- **Low Priority Tickets:** 3[cite: 1]
- **Total Tickets Analyzed:** 10

### 2. Longest Issue Description Detection
- **Ticket Number:** `TCK101`
- **Customer Name:** `Arun`
- **Cleaned Issue:** `Payment got debited from account but order status shows failed`
- **Word Count:** `10` words

---

## 💻 Tech Stack & Concepts Used

- **Language:** Python 3.x
- **Development Environment:** Jupyter Notebook / Google Colab[cite: 1]
- **Core Concepts:**
  - **Data Structures:** Dictionaries (Key-Value pairs), Lists (Sequences)
  - **Control Flow:** `for` loops, `if-elif-else` conditional evaluation
  - **Built-in Functions:** `enumerate()`, `len()`, `.split()`[cite: 1]

---

## 🚀 Code Implementation

```python
# Iterating through tickets to find the longest issue description
max_word_count = 0
longest_index = 0

for i, desc in enumerate(ticket_data['Cleaned_Issue']):
    word_count = len(str(desc).split())
    if word_count > max_word_count:
        max_word_count = word_count
        longest_index = i

print("\nTicket with Longest Issue Description:")
print(f" Ticket Number: {ticket_data['Ticket_No'][longest_index]}")
print(f" Customer Name: {ticket_data['Customer_Name'][longest_index]}")
print(f" Cleaned Issue: {ticket_data['Cleaned_Issue'][longest_index]}")
print(f" Word Count   : {max_word_count}")