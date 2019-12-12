# Legal_Dialogue_Summarization

For training and testing set:

each document in train and test directory is a court record, each line in the court record reprensents an utterance, format as follows.

[role]\t[spoken content]\t[controversy description]\t[label]

role: 1-judge,2-plaintiff,3-defendant,4-witness
spoken content: the spoken content which has been converted to id sequence
controversy description: controversy description which current spoken content belongs to. The content has been converted to id sequence. If current spocken content has no controversy, the value is 0.
label: 1-current utterance needs to be extracted. 0-current utterance does NOT need to be extracted

for example,

1 <s> w161 w76 w48 w63 w14 w29 w67 w116 w192 w1671 w200 </s>	0	0
2 <s> w35 w191 w505 w34 w63 </s>	0	0
2 <s> w45 w14 w365 w188 w11 w864 w77 w12 w17 w523 w2791 w30 </s>	0	0
2	<s> w599 w137 w2791 w30 w17 w128 w67 w2955 w1873 w525 w1294 w389 w856 w502 w184 w33 w78 w32 w276 w255 w1310 w33 </s>	0	0
2	<s> w64 w14 w19 w674 w38 w188 w11 w131 </s>	0	0
1	<s> w56 w38 w11 w48 w165 w58 w368 w29 w40 w116 </s>	0	0
3	<s> w45 w14 w4559 w915 w15 w38 w80387 w49 w1188 w110030 w24 w557 </s>	0	0
3	<s> w11 w102 w18623 w14 w80388 w105 w16 w530 w557 w300 </s>	<s> w3200 w14451 w18623 w3408 w4559 w10 w255 w557 w108 w49 w1488 w10 w3852 w28 w495 w8 w25 w12 w209 w10 w293 w127 w43 w27 w396 </s>	1
3	<s> w64 w14 w12 w235 w203 w15 w24 w4559 w500 w10 </s>	0	0
3	<s> w6361 w557 w2016 w229 w21 w45 w23 w45 w3350 w17 w10 w694 w47 w12 w120 w20 w41 </s>	<s> w982 w49 w229 w21 w133 w23 w45 w33 w43 w25 w1060 w135 w744 w120 w41 w8 w266 w435 w10 w928 w43 w396 w12 w24 w19 w98 w253 w3729 w10 w82 </s>	1

For privacy consideration, all the text content has been converted to id sequence. And we provide our vocabulary and embedding.
embedding/words.txt: the vocabulary
embedding/vector.txt: the word embedding corresponding to the vocab file
