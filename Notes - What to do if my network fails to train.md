<h1>Reasons for Training Failed & How to fix</h1>
<ol>
<li>Reached Critical Point (gradient = 0)
    <ul>
        <li> Critical point type:
            <ul>
                <li>local minima</li>
                <li>saddle point</li>
            </ul>
        </li>
        <li> smaller batch size + momentum may help escape critical points </li>
    </ul>
</li>
<li>learning rate was fixed
        <ul>
                <li>use adaptive learning rate
                <ul>
                         <li>large step at flat error face</li>
                </ul>
                 </li>
        </ul>
         <ul>
                <li>learning rate scheduling </li>
                <ul>
                        <li>learning rate decay</li>
                        <li>warm up</li>
                </ul>                 
        </ul>
</li>

<li>batch size was large
        <ul>
                <li>use smaller batch size</li>
        </ul>
</li>    
<li>loss function was not appropriate
        <ul>
                <li>consider cross entropy for classification</li>
        </ul>

</li>
</ol>
