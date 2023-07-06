<h1>reasons for training failed</h1>
<ol>
<li>reached critical point(gradient = 0)</li>
        local minima
        saddle point
        smaller batch size + momentum may help escape critical points
        
<li>learning rate was fixed</li>
        use adaptive learning rate
            large step at flat error face
        learning rate scheduling 
            learning rate decay
            warm up
            
<li>batch size was large</li>
        use smaller batch size
        
<li>loss function was not appropriate</li>
        consider cross entropy for classification
<ol>
