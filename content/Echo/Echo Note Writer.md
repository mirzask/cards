---
tags:
  - echo
  - lifehack
  - researchideas
draft: true
---

# Stroke Volume

Continuity Equation


```python

```

# Cardiac Output

- Inputs:
	- heart rate
	- stroke volume
```python
HR = input("Heart Rate: ")
SV = input("Stroke Volume: ")

# Divide by 1000 to get in L (instead of mL)
CO = (HR * SV) / 1000
```