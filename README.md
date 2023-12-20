# flarum

How to install Flarum?

In fact, many people know how to install "flarum" because it is stated on their websites. In contrast to people who do it for a fee, I will explain it to you simply, as if I were explaining it to people who are just starting out.
My explanation will be for cpanel. When purchasing hosting, do not forget to ask whether your terminal access is open. Because we will install plugins and scripts from here.
I assume you have installed Composer, you can look for simple download methods by searching the internet.
First of all you set your php version to 8.0.
"We found the hosting, entered our panel and, thinking that you are waiting in the terminal, I continue."
STEPS
Step1: cd public_html

Step2: You wait for the files to be uploaded by entering the code I specified. " composer create-project flarum/flarum . --stability=beta "

Step3: After the files are uploaded, we go to the "file manager" section and move the contents of the "public" file to the "public_html" folder and delete the public folder completely.

Step4: Go to the "index.php" folder and type 
"$site = require '../site.php';" We change the part as follows 
"$site = require './site.php';"

Step5: We save and exit, now it is our turn to enter site.php and change lines 47-49 as follows
    'base' => __DIR__,
    'public' => __DIR__,
    'storage' => __DIR__.'/storage',

Step6: We saved it and finally, we go to config.php and write our own domain on line 18 and save it.
Step7: Now we can create a database. We create a database and enter our site and we are greeted by the "flarum installer". After filling in the information, our site will be activated.

For plugins: https://extiverse.com/
for icons: https://fontawesome.com/

If you have questions, telegram: @dufyfuck
