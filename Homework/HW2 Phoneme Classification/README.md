<h1>Analyze & Results</h1>
<p>
  I first ran the base model and got this accuracy rate: <b>0.49814</b>
</p>
<p>
  Then per the homework request, I compared 2 models:
  <ul>
    <li>one narrower and deeper : hidden_layers = 6 , hidden_dim = 1024. Accuracy: 0.69252 </li>
    <li>the other wider and shallower : hidden_layers = 2 , hidden_dim = 1750. Accuracy: 0.70414 </li>
  </ul>
  It looks that the wider and shallower one does better on the current parameter setting. But the difference is not huge.</br>
  I also noticed that for both models, after ~ 6 epochs, while the training accuracy is increasing, the validation accuracy is decreasing, indicating there is likely overfitting.
</p>

<p>
  Then I changed the parameters back and added one dropout layer. I tested these 3 dropout rates:
  <ul>
    <li>when dropout rate = 0.25, accuracy = 0.4631</li>
    <li>when dropout rate = 0.5, accuracy = 0.42053</li>
    <li>when dropout rate = 0.75, accuracy = 0.33683</li>    
  </ul>
  This indicates that a much higher dropout rate is likely to lead lower accuracy level.
</p>

<p>
  After tuning the hyperparameter several times, and modifying the model instructions, I got a model with an accuracy of <b>0.75609</b>, here are the final parameter sets:
  <h3>Hyperparameters</h3>
  <ul>
    <li>concat_nframes : 3 -> 19</li>
    <li>train_ratio : 0.75 -> 0.9 </li>
    <li>batch size : 512 -> 2048 </li>
    <li>num epoch : 10 -> 50 </li>
    <li>hidden layer : 2 -> 6 </li>
    <li>hidden dimension : 64 -> 1024</li>
  </ul>
    <h3>Model Structure</h3>
  <ul>
    <li>applied batch normalization</li>
    <li>applied dropout, rate = 0.25</li>
  </ul>
</p>

<h1>Future Work</h1>
Though my model passed the strong baseline, it didn't pass the boss one. Can consider applying a more complex model, like RNN.

<h1>Reference Materials</h1>
<ul>
  <li><a href="https://blog.csdn.net/iwill323/article/details/127812090?spm=1001.2101.3001.6650.4&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-4-127812090-blog-120186614.235%5Ev38%5Epc_relevant_anti_vip&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-4-127812090-blog-120186614.235%5Ev38%5Epc_relevant_anti_vip&utm_relevant_index=9">A homework done by others which contains many useful resources (language is in Chinese)</a></li>
   <li><a href="https://zhuanlan.zhihu.com/p/483475612">Another homework, this one made me realize that no need to think about the things I haven't learned yet, like scheduler, I can just focus on finding the parameter sets that can make the model pass the strong baseline.(language is in Chinese)</a></li>
</ul>
