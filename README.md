# Generating a new SSH key

    (1) Open Git Bash.
    (2) Paste the text below, substituting in your GitHub email address.

    $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    This creates a new ssh key, using the provided email as a label.

    > Generating public/private rsa key pair.
    
   ![This creates a new ssh key](https://user-images.githubusercontent.com/73681489/98067869-8622b200-1e80-11eb-85b7-8dc56bc8188a.png)


# Adding your SSH key to the ssh-agent

    (1) If you have GitHub Desktop installed, you can use it to clone repositories and not deal   with SSH keys.

    Ensure the ssh-agent is running. You can use the "Auto-launching the ssh-agent" instructions in "Working with SSH key passphrases",
    or start it manually:

    # start the ssh-agent in the background
    $ eval $(ssh-agent -s)
    > Agent pid 59566
    
   ![start the ssh-agent in the background](https://user-images.githubusercontent.com/73681489/98071147-c1c17a00-1e88-11eb-850b-b6a6c0584545.png)

    (2) Add your SSH private key to the ssh-agent. If you created your key with a different name, or if you are adding an existing
    key that has a different name, replace id_rsa in the command with the name of your private key file.

    $ ssh-add ~/.ssh/id_rsa
    
   ![Add your SSH private key to the ssh-agent](https://user-images.githubusercontent.com/73681489/98071369-59bf6380-1e89-11eb-9737-d042568ca1c9.png)


# Adding a new SSH key to your GitHub account


    (1) Copy the SSH key to your clipboard.

    If your SSH key file has a different name than the example code, modify the filename to match your current setup.
    When copying your key, don't add any newlines or whitespace.

    $ clip < ~/.ssh/id_rsa.pub
    # Copies the contents of the id_rsa.pub file to your clipboard
    
   ![Copy the SSH key to your clipboard](https://user-images.githubusercontent.com/73681489/98071447-91c6a680-1e89-11eb-91e4-ece91b18c135.png)

    (2) In the upper-right corner of any page, click your profile photo, then click Settings
    
   ![click Settings](https://user-images.githubusercontent.com/73681489/98071565-ebc76c00-1e89-11eb-9c8b-5f5b173349b5.png)

    (3) In the user settings sidebar, click SSH and GPG keys.
    
   ![click SSH and GPG keys](https://user-images.githubusercontent.com/73681489/98071688-33e68e80-1e8a-11eb-9d10-58099f3d8913.png)

    (4) In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air"

    (5) Paste your key into the "Key" field.
    
   ![ssh-key-paste](https://user-images.githubusercontent.com/73681489/98071793-84f68280-1e8a-11eb-88da-3448e67f40fd.png)

    (6) Click Add SSH key.
    
   ![ssh-add-key](https://user-images.githubusercontent.com/73681489/98071950-e880b000-1e8a-11eb-8391-7d6a09e110f8.png)

    (7) If prompted, confirm your GitHub password.
   
   ![sudo_mode_popup](https://user-images.githubusercontent.com/73681489/98072020-1239d700-1e8b-11eb-8f53-b50885d4bc98.png)


# How to find new ssh key in your pc when you generating a new ssh key

    (1) You go in c drive
    (2) Then you go in user
    (3) Then go in your pc name
    (4) Then go in .ssh key
