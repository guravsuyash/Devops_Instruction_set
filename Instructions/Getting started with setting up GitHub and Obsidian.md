# Desktop
1. Sign up on GitHub create a account
2. Install Obsidian onto Desktop as well as Phone 
3. Set Obsidian path for vault by opening the folder where your repository is stored or by creating a new vault
4. Once done set up Git
   
	```git config --global user.name "FIRST_NAME LAST_NAME"```
	
    ```git config --global user.email "MY_NAME@example.com"```
5. Navigated to the directory where your repository is stored 
6. Use the following command to initialize the repository and add remote to it
   
	`git init`
	
    **Note add ssh link for private repository**    
    
    `git remote add "Link_to_your_repository"`  
1. Once done you can push/pull your code
# Mobile phone
1. Download Termux for CLI
>https://f-droid.org/repo/com.termux_118.apk
2. Download Obsidian from Play Store
3. Once download install Termux
4. Update it using the following commands 

	`apt update && apt upgrade`

	**On prompting on something Type Y and Hit enter**

5. Once done install Git and OpenSSH using

	`pkg install git openssh`
	
	**On prompting on something Type Y and Hit enter**

6. Once done grant termux permission to use the storage

	`termux-setup-storage`
7. Once permission is granted create a directory in storage by navigating to it
	
	`cd storage`
	
	`mkdir .ssh`
8. The directory that we created would be used to authenticate with GitHub using ssh keys
9. Navigate to this directory using

	 `cd .ssh`

10. Use the following command to generate key for ssh
	
	`ssh-keygen -t ed25519 -C "youremail@address.com"`

**On prompting anything keep pressing enter until the key is generated**
12. Once done change the permission of the key to be readable using the following command
	
	chmod ugo+r "key_name.pub"

13. Now follow step from Desktop 

	 [Step 4 and Step 6 of Desktop Setup](#Desktop)

14. Open Github navigate to Settings>SSH and GPG keys
![123](https://github.com/guravsuyash/Testrepo/assets/55230261/b9528f39-24da-41f5-8253-f7172388df7a)

15. Under SSH Keys click on new SSH key

16. Copy paste the generated key from the termux by using cat command

	 `cat "key_name.pub"`

17. Give your key a title and paste it and click on add SSH key
18. Once done SSH key is added, check for authentication 

	 `ssh -T git@github.com`

19. It would prompt something type yes for the first time 
20. And authentication would be successful 