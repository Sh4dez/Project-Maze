# Project-Maze
Flashlight



     void Update()
  
    {
        flashlight.enabled = triggerFlashlight;
        
        //press "g" to turn on or off 
        if (Input.GetKeyDown("g"))
        
        {
            triggerFlashlight = !triggerFlashlight;
        }
        
        if (triggerFlashlight)
        {
            flashlightBattery -= Time.time * 0.001f; // reduce battery by 0.01
            if (flashlightBattery <= 0f)
            {
                triggerFlashlight = false;
            }
            
            else if (flashlightBattery <= 30)
            {
                flashlight.intensity -= Time.time * 0.0001f;
            }
        }
       
    }
