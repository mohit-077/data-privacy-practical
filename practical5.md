# Practical 5: Anonymization Techniques

## Aim

To study different data anonymization techniques such as k-anonymity, differential privacy and data masking, and apply them to a sample real-world dataset.

## Theory

Data anonymization is the process of modifying personal data so that an individual cannot be easily identified from the dataset.

Some common anonymization techniques are:

### 1. k-Anonymity

k-Anonymity makes sure that every record is similar to at least k-1 other records based on selected identifying attributes.

For example, if k = 2, each combination of quasi-identifiers should appear at least twice.

### 2. Differential Privacy

Differential privacy adds a controlled amount of random noise to the results of a query. This makes it difficult to determine whether a particular person's information was included in the dataset.

### 3. Data Masking

Data masking replaces sensitive information with hidden or modified values.

Example:

Original:
Phone = 9876543210

Masked:
Phone = 98765*****

### 4. Generalization

Generalization changes specific information into a broader category.

Example:

Age = 21

becomes:

Age Group = 20-25

### 5. Data Suppression

Data suppression means completely removing sensitive information from a dataset.

---

## Dataset Used

For this practical, a small student health survey dataset is used.

| Name | Age | City | Disease |
|------|-----|------|---------|
| Rahul | 21 | Delhi | Fever |
| Amit | 22 | Delhi | Cold |
| Neha | 21 | Delhi | Fever |
| Priya | 23 | Delhi | Cold |
| Karan | 24 | Delhi | Fever |

The name is personally identifiable information, while age and city can be used as quasi-identifiers.

---

## Python Program

    import random

    data = [
        ["Rahul", 21, "Delhi", "Fever"],
        ["Amit", 22, "Delhi", "Cold"],
        ["Neha", 21, "Delhi", "Fever"],
        ["Priya", 23, "Delhi", "Cold"],
        ["Karan", 24, "Delhi", "Fever"]
    ]

    print("Original Dataset")
    print("----------------")

    for row in data:
        print(row)

    # Data masking
    for row in data:
        row[0] = "****"

    # Generalization of age
    for row in data:
        row[1] = "20-25"

    print("\nAnonymized Dataset")
    print("------------------")

    for row in data:
        print(row)

    # Simple differential privacy example
    original_count = 3
    noise = random.randint(-1, 1)

    private_count = original_count + noise

    print("\nDifferential Privacy Example")
    print("----------------------------")
    print("Actual Count:", original_count)
    print("Privacy Protected Count:", private_count)

---

## Sample Output

    Original Dataset
    ----------------
    ['Rahul', 21, 'Delhi', 'Fever']
    ['Amit', 22, 'Delhi', 'Cold']
    ['Neha', 21, 'Delhi', 'Fever']
    ['Priya', 23, 'Delhi', 'Cold']
    ['Karan', 24, 'Delhi', 'Fever']

    Anonymized Dataset
    ------------------
    ['****', '20-25', 'Delhi', 'Fever']
    ['****', '20-25', 'Delhi', 'Cold']
    ['****', '20-25', 'Delhi', 'Fever']
    ['****', '20-25', 'Delhi', 'Cold']
    ['****', '20-25', 'Delhi', 'Fever']

The differential privacy value may change because random noise is added.

## Result

The dataset was successfully anonymized using data masking and generalization. The concepts of k-anonymity and differential privacy were also studied and demonstrated using a sample dataset.
