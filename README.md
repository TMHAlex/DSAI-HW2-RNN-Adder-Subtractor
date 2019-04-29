# DSAI-HW2-RNN-Adder-Subtractor

***Coding Part***

1. Adder (A,B: 3 digits)
2. Subtractor (A-B, A>=B)
3. Combine adder and subtractor

***Report Part***

○ Analyze the results under different number of digits, training epoch, training size, etc
○ Can we apply the same training approach for multiplication?




***Report Answer***

1.different number of digits : 不同的digits會降低預測的準確度，以加法為例999+999=1998 其答案為4位數字，如果將題目最大數字控制在500以下時，
  兩個三位數字相加等於三位數，可以提升其預測準確度。
  
2.training epoch : 有效的增加訓練次數有助於提升預測準確度，但是會有一個臨界值，當超過訓練次數臨界值時，準確度可能會不增反降，影響預測結果。

3.training size : 越多的training data能夠提升預測準確度，以減法為例，作業預設為18000筆訓練資料，其準確度在85%左右，
                  當我將trainging data增加到54000筆時，準確度會上升到95%以上。
                  
4.對於將此方法應用到乘法器中，我認為是可行的，但是如果用其RNN設定及訓練資料相同時準確度會很低，因為兩個最大可為三位數的數字相乘，
  其產生的結果會到六位數，會大大的影響預測，或許可以藉由提升trainging data的數量、training epoch 、RNN的結構來提升其準確度

