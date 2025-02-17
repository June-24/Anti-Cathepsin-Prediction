doing feature elimination (217)

1. variance threshold method
reduced_features/Variance/B,S,D,K/1,2,3
B1-> 0.01 (186)
B2-> 0.1 (141)
B3-> 0.5 (114)



2. correlation based method
reduced_features/Correlation/B,S,D,K/1,2,3
B1-> 0.9 (168)
B2-> 0.5 (81)
B3-> 0.3 (45)



3. RFE method
reduced_features/RFE/B,S,D,K/1,2,3
B1-> 130
B2-> 90
B3-> 50


-------------------------------------------------------------
SO based on analysis what we saw was that
correlation dip a large amount after B2
so B2 is the limit for correlation

but RFE and variance remained steady even after B3
so we are trying to reduce it even further and try to get better results

1. Variance
B4-> 0.6
B5-> 0.7
B6-> 0.8

2. RFE
B4-> 40
B5-> 30
B6-> 20



--------------------------------------------------------------------
there was a big gap between the correlation features:
so made 6 constant updates:

final selections are:
varaince: 0.01, 0.1, 0.5, 0.6, 0.7, 0.8

correlation: 0.9, 0.8, 0.7, 0.6, 0.5, 0.4

RFE: 150, 130, 90, 50, 30, 20
