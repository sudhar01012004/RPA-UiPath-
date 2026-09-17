**Create variable**
 
  MovieRating
  MovieName

Add Input Dialog activity.
 
 **Dialog title** → “Movie Rating”
 
 **Input label** → “Enter the movie name”

 **Input type** → Text Box

 **Value entered** → MovieName

Add Use Application/Browser.
 
 Indicate Microsoft Edge screen.

Inside do

→ Add Type Into activity → indicate search bar.
 Type into → MovieName + “imdb”

→ Add Click activity.
 Indicate search icon → run it.

→ Add another Click activity.
 Indicate the IMDb link → run it.
 Enter movie name → it will automatically go to the rating page.
Minimize Edge → open UiPath Studio.

again add use application browser activity
indicate rating screen fully

→ Add Get Text → indicate the rating text.
 Save to → MovieRating

→ Add Message Box.
 “Movie Name:” + MovieName + vbCrLf + “Movie Rating:” + MovieRating
