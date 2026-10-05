=====================================================
 FOTO LOGIN SYSTEM - README
=====================================================

FILES IN THIS FOLDER
--------------------
index.html            Main login page (Student + Photo Journalist tabs)
forgot-password.html  Forgot password page
signup.html           Create new journalist account page
student-dashboard.html     Student page (opens from "Enter Gallery")
journalist-dashboard.html  Photo Journalist page (opens after Login)
images/               Put your department + Photo of the Month photos here
style.css             ALL colours, fonts, spacing and hover effects
README.txt            This file

IMPORTANT: Keep all files together in the SAME folder.
The pages find each other and style.css by file name.


HOW TO OPEN IN VISUAL STUDIO CODE
---------------------------------
1. Open Visual Studio Code.
2. Click File > Open Folder...
3. Choose the folder "foto-login-system" and click Select Folder.
4. Click a file on the left side to edit it.

HOW TO SEE THE PAGE
-------------------
- Right-click index.html in your folder and choose Open With > your browser.
  (Or double-click it.) index.html is the MAIN file.
- After you edit and save a file (Ctrl + S), refresh the browser (F5).
- When you add PHP, the pages must run on a server such as XAMPP.
  Put the folder inside htdocs, then open:
  http://localhost/foto-login-system/index.html


WHERE TO PUT YOUR PHP LINKS
---------------------------
Type your file name between the two quote marks.

index.html
  Line 29  <a class="btn-blue" href="student-dashboard.html">Enter Gallery</a>
           -> Student button. Opens the Student page now.
              Change it later if you want a PHP file here (example: gallery.php)
  Line 34  <form ... action="journalist-dashboard.html" method="POST">
           -> Photo Journalist login. Opens the Journalist page now.
              Later change it to your login file (example: login.php)

forgot-password.html
  Line 23  <form ... action="" method="POST">
           -> Send Reset Link. Example: action="send-reset.php"

signup.html
  Line 23  <form ... action="" method="POST">
           -> Create Account. Example: action="register.php"

Field names your PHP will read with $_POST:
  Login:      username, password
  Forgot:     email
  Sign up:    username, email, password, confirm_password

Links that already work:
  Forgot Password -> forgot-password.html
  Sign up         -> signup.html
  Back to Login / Log in -> index.html
  Enter Gallery   -> student-dashboard.html
  Login           -> journalist-dashboard.html (type anything in both boxes)


DASHBOARD PAGES
---------------
student-dashboard.html and journalist-dashboard.html are copies of your
designs. Only the Logout button (top right) works. Everything else is
just for show.
  Logout on the Student page      -> index.html#student (Student tab)
  Logout on the Journalist page   -> index.html#journalist (Journalist tab)
The numbers (1,049 photos, 14 Events, etc.) are typed in the HTML.
Change them there, or replace them with PHP later.

PHOTOS ON THE CARDS
-------------------
Put these files in the "images" folder (same names, .jpg):
  bsit.jpg  bsed.jpg  bshm.jpg  beed.jpg  photo-of-the-month.jpg
Until you add them, the cards show plain colours.
To change a name or path, see "dept-photo" and ".featured" in style.css.


COLOURS YOU CAN CHANGE FIRST
----------------------------
Open style.css. The colours are at the very top under "- COLOURS -".
Change the code after the colon (example: #2563eb).

  --blue          Active tab and all big buttons
  --blue-hover    Button colour when the mouse is over it
  --bg-dark       Darkest part of the background
  --bg-mid        Middle blue of the background
  --bg-glow       Soft glow at the top-right
  --card-bg       The centre box
  --tab-inactive  The tab that is not selected
  --link-color    "Sign up" and "Log in" links
  --bsit, --bsed, --bshm, --beed   Department card + button colours
  --red           Logout text
  --amber         Photo of the Month badge


SCHOOL LOGO (shows on every page)
---------------------------------
logo.png is the Cordova Public College logo with a transparent background.
It appears faded behind the box on all 3 pages.
In style.css, find the part called "SCHOOL LOGO":
  width / height   -> how big the logo is
  opacity          -> how faded it is (0.2 now; try 0.1 to 0.3)
To use a different logo, replace logo.png (keep the same name).
