這是tensorflow2.X 版本的單純DCGAN 跟paper不一樣的是他沒inpainting,所以有個loss沒加,之後有訓練好的權重再丟上來

如果要inpainting的只有1.X版本的 https://github.com/ChengBinJin/semantic-image-inpainting

0. 輸入輸出: input:random 100,output:64,64,3
1. data : 64,64,3 celeb dataset
2. model 架構 : G:100 -> 4,4,1024 -> 8,8,512 -> 16,16,256 -> 32,32,128 -> 64,64,3
3.              D: 64,64,3 -> 64,64,64 -> 64,64,128 -> 1
4. loss 函數 : BinaryCrossentropy
5. 訓練機制
