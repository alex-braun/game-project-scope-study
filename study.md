# Game Project Scope Study

## Required Readings

-   [Game Project](https://github.com/ga-wdi-boston/game-project)
-   [Game API](https://github.com/ga-wdi-boston/game-project-api)
-   [What is a User Story](http://searchsoftwarequality.techtarget.com/definition/user-story)

## Deliverables

After reading the `game-project` prompt and the `game-project-api` documentation
please do the following and be prepared to share and discuss during our next
class.

Submit detailed answers to these in this file via a pull request.

-   A wireframe of what your game project will look like.
  -Please see TickTackToe.vp and TickTackToeiPhone.vp.

-   The data structure you plan to use.

      -two events js files will handle all events that take place
      in forms; one for authentication events, one for game
      action events.
      -two api js files that will handle api GET,POST,PATCH,DELETE, and WATCH
      methods to either the authentication processes or games process.
      -A game.js file that will strictly handle game logic.
-   How you will take the markup of the game board and represent it in JS

      -jQuery event handlers that will register a 'click' from anywhere on
      the div, similar to the way we have been using buttons so far.

-   How you plan to approach this project.

      -I plan to first figure out the game logic.  Then I need to get this
      information created as an object (as outlined in the api git page),
      and sent as JSON.

-   4-8 user stories for your game project.
        - As a user, I would like to be able to switch between myself and
          another person to play the game.
        - I want to have the game keep track of my scores during each session.
        - I want to have a working game board that tells me the score.
        - As a user, I want to have my user name saved as well as my current
          game history.
        - I want there to be a notification when somebody wins.
        - As the administrator, I want this game to hold my user's scores in
        a database that can be accessed whenever the person is signed in.
        - I want there to be an option for the user's password to be updated if
          the at their request.

-   How you plan to keep your code modular.

      -Universal to both authentication and game actions:
        - app.js, which simply holds the api URL.
        - index.js, final step to javaScript communication.

      -For authentication:
        - index.html
          -  Takes form information for the authentication process and allows
          divs to be selected individually for the tic-tac-toe game board.
        - auth/events.js
          - Holds event handler functions for the authentication process
          and sends that information to getFormFields.js, which turns
          that data into objects.
          - Each new object is sent to api.js, which sends an ajax request
          to the server, and a success or failure notice will also set that as
          the new user, or delete a user, or log an error.
        - auth/api.js
          - creates the JSON string and sends ajax requests.
    -For game actions:
        - gameEvents.js
          - event handlers
          - sends to ajax request->success/failure functions->api
        - gameUi.js
        - gameApi.js
          again sent to getFormFields which turns this data into objects.
          The game choices need to be transformed into JSON, so an ajax request
          will be created.
          This process will update the 'cells' array in the JSON object.

-   What creative spin will you add to your project.

    -I want this game to flash when a game has been won, along with a notice
    of which player has won.
    -Media queries at popular screen sizes to make the game attractive
    at different screen sizes.

-   How you will use version control to backup / track your project.

    -Many git pushs will be performed on individual files, along with correct
    and descriptive explanations of what changes were made.
-   Do you plan to attempt any of the bonuses.

    -I would like to complete the bonuses if I can figure out how to get them
    to work!
