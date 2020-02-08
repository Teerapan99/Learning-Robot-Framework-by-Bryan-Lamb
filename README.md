# Learning-Robot-Framework-by-Bryan-Lamb
Run Script option

    1.Command
    2.batch file
    3.Task Scheduler
    4.saucelabs.com (via command )
    5.Jenkins (remote exec on saucelabs.com)
    
Run Command
      
     robot -d results folder/my-script.robot ->run แล้วไฟล์ result จะแยกไปอยู่ใน folder results
     robot -d results --include smoke tests/my-script.robot 
     robot -d Path/folder -i smoke tests/my-script.robot 

Run Script .bat file

     1. Create Taxt file
     2.add Commands
       @echo off
       cd path/folder script
          call robot -d results tests/my-script.robot 
          call robot -d results --include smoke tests/my-script.robot 
          call robot -d Path/folder -i smoke tests/my-script.robot
       
       Ex.
       @echo off
       cd path/folder script
       call robot -d results tests/my-script.robot 
       
        or Ex. กรณีที่อยากแยก results file and run brower ต่างๆด้วย file .bat
       @echo off
       cd path/folder script
       call robot -d Path/folder(เก็บResults) -v BROWSER:ie or chrome or filefox tests/my-script.robot 
       
      3.Save the file
      4.Change .txt extention to .bat
      5.Double Click the .bat file to excuete
      
  Run Script Task Schedule
  
      Create New Task
      Point at .bat file
      Triggering
         On Demand
         Scheduled
