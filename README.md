<p align ='center'>
<img src="https://user-images.githubusercontent.com/79885974/184529420-5ff3bd42-7c43-4399-87f6-4d832c1c5b26.jpg" alt="Spotify">
</p>
<h1 align = "center" >Spotify To Youtube MP3 <h1/>
  
# Description
In this project i try to access to the Spotify song of a user and then get those song's name and artist then convert it to Youtube MP3 because Spotify Free won't allow you to donwload their song's. I used flask to set up some endpoints and using OAuth to iteract with Spotify API to get the access to user's playlist

# Instruction
## Step 1: Install setup file
```
python setup.py install
```
## Step 2: Setup the redirect url and get the clientid and clientsecret
   * Go to [Spotify Developer](https://developer.spotify.com/) click "Dashboard", log in to your Spotify account then click create an app an name that app some random thing ( it doesn't matter ).
   * Then click "edit setting" and paste these 4 links in the Redirect URIs: 
            <h5>1. http://localhost:5000/authorize</h5>
            <h5>2. http://localhost:5000/authorize/</h5>
            <h5>3. http://127.0.0.1:5000/authorize</h5>
            <h5>4. http://127.0.0.1:5000/authorize/</h5>
  *Doing this will help spotify know where to redirect the user back when the done talking*
  
  * Then copy your app **clientid** and **clientsecret** and paste in it the SpotifyOAuth object in the **create_sp_oauth()** inside of **app.py**. Don't show anyone the **clientsecret** cause they can access to your data.
## Step 3: Run the app.py with Flask
 ```
flask run
```
## Step 4: Run the downloadvideos.py 
```
python downloadvideos.py
```
  
There you go!!!

