# nail-polish
My Project is about an online nail polish store where the users are able to purchase products and their products are delivered for free.
   The application is live here [https://nail-polish.herokuapp.com/](https://nail-polish.herokuapp.com/).
   ## UX
   This project is for all people who would wish to buy nail polish online.
   - As a user I would like to have a navigation bar where i can navigate though the website.
   - As a user I would like to have a cart icon where I can be able to fill my details for shipping.
   - As a user I would like to have a price tag of each product.
   - As a user I would like to have a form where I can be able fill my details.
   - As a user I would like to have a payment functionality where I can be able to pay for my products.
   ### Wireframes
   #### mockup
   Please find my paper and pen mockup [Here](https://scontent.farn2-1.fna.fbcdn.net/v/t1.15752-9/120795507_341266307110985_2249962487274967487_n.jpg?_nc_cat=105&_nc_sid=ae9488&_nc_ohc=NO9rZ44qiAIAX8NxZnR&_nc_ht=scontent.farn2-1.fna&oh=3ee02c54466d29efbcbae5a4fb7e595c&oe=5F9F6987)
   ## features
   #### Existing features
   ##### Navbar
   - Where one can navigate through the  website.
   ##### store page 
   - It consists of all carousel, products and their prices.
   ##### cart page 
   - It constists of; 
     - continue shopping button.
     - images of all items in the cart.
     - names of the items in the cart.
     - prices of thr items in the cart.
     - quantity of the items in the cart.
     - total amount of the items in the cart.
    
   ##### checkout page
   - It consists of; 
     - form where the user can fill name, email and the shipping information.
     - back to cart button.
     - order summery where the user is able the details of the products purchased.
     - pay button where the user is able to pay for the products.
   ##### payment page
   - consist of a paypal buttons where the user is able to pay for the products.
   
   ## Technologies used
   ###### HTML5
   - It was used to create a markup
   ###### css3
   - Used to style the element of HTML code.
   ###### Javascript
   - To write the functionality of the project.
   ###### jQuery
   - To write the functionality of the project.
   ###### Bootstrap
   - It was used to help style the website and with grid layout of it.
   ###### MongoDB 
   - It was used as non-related database for the project.
   ###### w3c validator
   - It was used to check HTML code 
   - It was used to check Css stylings.
   ###### GitHub
   - Used for version control, code backup and site deployment.
   ###### Heroku
   - Used for live deployment.
   ## Testing
   ##### Store page 
   - Go to the store page check if the carousel is working.
   - Check if the images of the products are well placed.
   - Click on the add to cart button to see if is working. 
   ##### cart page
   - Click on the add to cart button and see if it will be added in the cart icon.
   - Check if continue shopping and checkout buttons are working.
   - Check if the images, names, prices, quantities and toatal amount of the products in the cart are visible.
   ##### checkout Page
   - Click on the checkout button and check if you can see the form, back to cart button and order summery.
   ##### payment page page
   - Click on pay button and see if it will direct you to paypal buttons.
   ##### Mobile responsive
   - Each page was checked through the live preview by inspecting it in dev tools and choosing different screen sizes.
   ## Bugs/Problem Encountered
   - I was having problem deploying my project to heroku and installation of whitenoise.
   ##### Deploying my project
   - I used Gitpod workspace and added content with the following commands to push to GitHub;
   1. Git add "file name".
   2. Git commit -m "commit message"
   3. git push 
   - It was later pushed to Heroku through this steps;
   1. Create "requirements.txt" file
      pip3 freeze > requirements.txt
   2. Create "Procfile" file
      web: gunicorn..
   3. Login Heroku
   4.Setting Config Vars: Heroku homepage - Select "nail-polish" project - Setting - Click "Reveal Config Vars" - Create Config Vars and save
   - Then install whitenoise using 
      pip3 install whitenoise
   - I made sure staticfiles are configured correctly
      STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')
   - I made sure I was using the static template tag to refer to your static files, rather that writing the URL directly
      {% load static %}
   - I placed WhiteNoise middleware directly after the Django security middleware
                MIDDLEWARE = [
  'django.middleware.security.SecurityMiddleware',
  'whitenoise.middleware.WhiteNoiseMiddleware',
  # ...
  ]
  - Added compression and caching support in setting.py
     STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'
  - Used a Content-Delivery Network
     STATIC_HOST = os.environ.get('DJANGO_STATIC_HOST', '')
     STATIC_URL = STATIC_HOST + '/static/'
  - disabled Django’s static file handling and allow WhiteNoise to take over simply by passing the --nostatic option to the runserver command
     'whitenoise.runserver_nostatic',
   - Type commands as below for git add / commit / git push
   - git add
   - git commit -m "commit message" 
   - git push
  - Type commands as below for git remote
  1. git remote add heroku
  2. git push -u heroku main
  3. git remote -v
  4. Run the webpage
  ## Credits
  - Code Institute tutor team for their help throughout the project.
  - Igor Code Institute tutor for his help with heroku.
  - Telusko and Freak on youtube tutorials.
  ###### Photos
  - The photo were obtained from [https://www.pexels.com](https://www.pexels.com).
  - Telusko and Freak on youtube tutorials.
   

  
