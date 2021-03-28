setup:
  增加數值按鈕(A0)
  確認按鈕(A1)
  減少數值按鈕(A2)
  RC Vout ADC(A3)
  DAC(D13)
  compile後板子上會顯示數值，選定DAC的頻率後，run: sudo python3 FFT.py，並按下確認鍵
  FFT.py會sample 40個點做FFT 分析

我的cutoff freq 在 318 Hz，以下附上200Hz以及400Hz的結果

python : 400Hz
![image](https://drive.google.com/file/d/1xlW-DpQQ_hlPGU_9K3Ag2b870WRB8hFB/view?usp=sharing)

picoscope : 400Hz
![image](https://drive.google.com/file/d/1GXjFEFY4ib8MxxsIUYix16HJY6qdRtho/view?usp=sharing)

python : 200Hz
![image](https://drive.google.com/file/d/1h35bKnq_s3Chw_rnEbhzsmxJv8opjOge/view?usp=sharing)

picoscope : 200Hz
![image](https://drive.google.com/file/d/1NVttp_DZMwD2BlYEOTNK5mGQEqwFUIQc/view?usp=sharing)

可以發現 400Hz的波型明顯被low pass filter 給降低振福了(picoscope裡的藍線是Vout，紅線是Vin)，FFT分析400Hz的高度也明顯降低，顯示RC電路的功效
