**On prompting anything keep pressing enter until the key is generated**
12. Once done change the permission of the key to be readable using the following command

	```
	chmod ugo+r "key_name.pub"
	```

13. Now follow step from Desktop 

	 [Step 4 and Step 6 of Desktop Setup](#Desktop)

14. Open Github navigate to Settings>SSH and GPG keys
![123](https://github.com/guravsuyash/Testrepo/assets/55230261/b9528f39-24da-41f5-8253-f7172388df7a)

15. Under SSH Keys click on new SSH key

16. Copy paste the generated key from the termux by using cat command

	 ```
	 cat "key_name.pub"
	 ```

17. Give your key a title and paste it and click on add SSH key
18. Once done SSH key is added, check for authentication 

	 ```
	 ssh -T git@github.com
	 ```

19. It would prompt something type yes for the first time 
20. And authentication would be successful 