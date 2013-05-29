HW8
===

#INPUT

A = matrix(RR, 4, [0.11, 0.05, 0.3, 0.5,   
                   0.9, 0.2, 0.01, 0.25,   
                   0.63, 0.57, 0.5, 0.09,    
                   0.8, 0.03, 0.5, 0.8]); 

symbols = ['azusa', 'is', 'so', 'cute', '!']
B = matrix(RR, 4, 6, [0.35, 0.26, 0.1, 0.03, 0.5, 0.9,
                      0.03,  0.03,  0.4,  0.0,  0.2,   0.03,
                      0.001,  0.0,  0.0,  0.22,  0.33,   0.44,
                      0.99, 0.0, 0.12,  0.0,  0.78,  0.07])
initial = [1,0,0,0]
model = hmm.DiscreteHiddenMarkovModel(A, B, initial, symbols)
model
model.graph().plot(edge_labels=True,graph_border=True).show(figsize=5, svg=True)


#RESULTS



Transition matrix:
[0.11 0.05 0.3 0.5]
[0.9 0.2 0.01 0.25]
[ 0.63 0.57 0.5 0.09]
[0.8 0.03 0.5 0.8]
Emission matrix:
[  0.35  0.26  0.1   0.03  0.5   0.9]
[  0.03  0.03  0.4   0.0   0.2   0.03]
[  0.001 0.0   0.0   0.22  0.33  0.44]
[  0.99  0.0   0.12  0.0   0.78  0.07]
Initial probabilities: [1.0000, 0.0000, 0.0000, 0.0000]
symbols: ['azusa', 'is', 'so', 'cute', '!']
