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
  After tuning the hyperparameter several times, and modifying the model instructions, I got a model with an accuracy of , here are the final parameter sets:
  <h2>Hyperparameters</h2>
  <ul>
    <li>concat_nframes : 3 -> 19</li>
    <li>train_ratio : 0.75 -> 0.9 </li>
    <li>batch size : 512 -> 2048 </li>
    <li>num epoch : 10 -> 50 </li>
    <li>hidden layer : 2 -> 6 </li>
    <li>hidden dimension : 64 -> 1024</li>
    <li></li>
    <li></li>
  </ul>
    <h2>Model Structure</h2>
  <ul>
    <li>applied batch normalization</li>
    <li>applied dropout, rate = 0.25</li>
  </ul>
</p>


