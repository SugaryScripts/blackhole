**1. Boot from a Manjaro Live Medium:**

- You'll need a USB drive with a recent Manjaro ISO burned onto it. Boot your computer from the USB drive.

**2. Open a Terminal:**

- Once the live environment loads, open a terminal window.

**3. Enter Chroot Environment:**

- Use the following command to enter a chroot environment. If you have multiple Manjaro installations, you'll be prompted to choose the correct one.
    
    ```
    manjaro-chroot -a
    ```
    

**4. Reset Password:**

- Now you're in a root-like environment for your installed Manjaro. Here's how to reset passwords:
    
    - Reset Root Password (if applicable, be cautious):
        
        ```
        passwd
        ```
        
        - Enter and confirm your new root password.
    - Reset Your User Password:
        
        ```
        passwd <username>
        ```
        
        - Replace `<username>` with your actual username.
        - Enter and confirm your new user password.

**5. Exit and Reboot:**

- Once you've reset the passwords, exit the chroot environment:
    
    ```
    exit
    ```
    
- Reboot your computer normally. You should be able to log in with your new password.