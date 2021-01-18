# General Environment Setup
_________________
## Python
* Download Miniconda and install following the instructions https://docs.conda.io/en/latest/miniconda.html 
* VSCode and system setup
	1. Add Conda environment https://stackoverflow.com/questions/54828713/working-with-anaconda-in-visual-studio-code
		- Change teminal in vscode to cmd, it should be able to activate conda automatically		
		- Now, we want to activate conda in powershell as well. Change settings.json to below.   
		{  
				
				"workbench.editorAssociations": [],  
				"terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",  
				"terminal.integrated.shellArgs.windows": ["/K", "C:\\Users\\cheng\\miniconda3\\Scripts\\activate.bat C:\\Users\\cheng\\miniconda3"],  
				"python.condaPath": "C:\\Users\\cheng\\miniconda3\\Scripts\\conda.exe"
			
			}
	2. Add below paths on path in "Environment Variables" for both system variables and user variables (Advanced in System Properties) 
		- C:\Users\cheng\miniconda3
		- C:\Users\cheng\miniconda3\Scripts
		- C:\Users\cheng\miniconda3\Library\bin
	3. Other linkes can be useful
		* https://stackoverflow.com/questions/59519338/dll-load-failed-the-specific-module-could-not-be-found-vscode-numpy		
		* https://stackoverflow.com/questions/54828713/working-with-anaconda-in-visual-studio-code
		* https://stackoverflow.com/questions/54063285/numpy-is-already-installed-with-anaconda-but-i-get-an-importerror-dll-load-fail
		* https://code.visualstudio.com/docs/python/environments#:~:text=To%20do%20so%2C%20open%20the,Settings%2C%20with%20the%20appropriate%20interpreter.
		* https://medium.com/@udiyosovzon/how-to-activate-conda-environment-in-vs-code-ce599497f20d
		* https://towardsdatascience.com/get-your-computer-ready-for-machine-learning-how-what-and-why-you-should-use-anaconda-miniconda-d213444f36d6
		* https://www.practicaldatascience.org/html/setup_environment.html
		* https://blog.csdn.net/yctjin/article/details/80184988		

## VScode
* Download VScode and install following the instructions https://code.visualstudio.com/ 
* Extensions
	- Python
	- SQL Formatter
	- SSH FS  
		Open settings: File > Preferences > Settings  
		Modify user settings.json by searching for the term "json", click "Edit in settings.json" links  
		{  
		
				"sshfs.configs": [
					{
						"host": "YOUR_EDGE_NODE.*****.com",  
						"label": "YOUR_EDGE_NODE",  
						"name": "YOUR_EDGE_NODE",  
						"password": "YOUR_PASSWORD",  
						"root": "/users/YOUR_AID",  
						"username": "YOUR_AID"

					}
				],  
				"editor.rulers": [80],    
				"terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",  
				"window.zoomLevel": -1,  
				"sql-formatter.uppercase": true  
		} 
	- Hive SQL
	- Jupyter
	- Python Docstring Generator

## Git
* Download Git and install following the instructions https://git-scm.com/download/win  
* Generate ssh key from local computer and register it on Github account https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh 
	- Windows 
		0. Open Git Bash
		1. Checking for existing SSH keys - might need to create folder ~/.ssh
		2. Generating a new SSH key and adding it to the ssh-agent - remember adding to ssh-agent
		3. Adding a new SSH key to your GitHub account - make an unique SSH key on Github account
		4. Testing your SSH connection - follow the instructions
		5. (Working with SSH key passphrases)

## Cmder
* Download Cmder and install following the instructions https://cmder.net/

## Google Cloud