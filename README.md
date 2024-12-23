
# Wordle-App while learning HTML, CSS, JS

## HTML

Tags : defines the semantic

Common HTML Tags: 

        - <a></a> : anchor Tag
            . <a href="http://www.wordle-app.com">Wordle-App</a>
        - <div></div> : Division/Divider Tag
            . <div> style="width: 100px; height: 100px; background-color: red;"></div>
            . Generic divider between different components/Tags.
        -  <span></span>
            . <p>This is <span style="test-decoration: underline">important</span>text</p>
        - <ol></ol>
            . <ol> ordered list 
                <li>An Item in the list</li>
                <li>Another item</li>
                <li>A yet differetn Item</li>
              </ol>

        - <ul></ul>
            . <ul> ordered list 
                <li>An Item in the list</li>
                <li>Another item</li>
                <li>A yet differetn Item</li>
              </ul>

        - <button></button> : To create a button on a page
            . <button>Click me!</button>
        
        - <img></img> : image Tag
            . <img src="http://pets-images.com" alt="an adorable puppy"/>


Input & Form Tags : 

    - <input /> : A box to give input 
        . <input type="color" />
        . <input type="radio" />
        . <input type="number" />, etc

    - <textarea></textarea> : creates a commment box 
    
    - <select></select>: used to select a dropdown menu
        . <select>
            <option>red</option>
            <option>black</option>
            <option>brown</option>
          </select>

    - <form></form> : A group of html tags related to gathering data from a user.
        . <form>
            <input placeholder="firstName>
            <input placeholder="lastName>            
          </form>


Table, Comments & hard return :

    - <table></table> : creates tables
        . <table>
            <thead>
                <tr>
                    <td> Names</td>
                    <td> points</td>
                </tr>
            </thead>
          </table>

    - <marquee></marquee> : text scrolls from end to end
        . <marquee>
            This is moving 
          </marquee>

    - comments: <!-- This is never gets shown to user --!>

    - A Note on Hard Returns : hard return spaces doesn't work in the tags
        . <p>
            This is some text

            This is some other txt.
          </p>
          The above one will not work.
        Work arounds :

        correct way:
        . <p>This is some text</p>
          <p>This is some other txt.</p>

        in-correct way:
        . <p>
            This is some text
            <br></br>
            This is some other txt.
          </p>  

Attribute, classes & IDs : { Used to modify the behaviour of the tags }

    - Attributes : 
        . <input type="text" /> 
            . attribute { type="text" }: key-> type and value-> text
        
    - Classes : Any tag can have a class 
        . <h3 class="the-red-one" >This one is red>/h3
            classes are defined in css, it defines what it does.

    - IDs :  Ids are unique
        . <h3 Id="brand"> my site Branding</h3>
        . <a href="ids">It directly links to IDs</a>

    - Note: Always try to use classes instead of Ids.


Organizing HTML :Mostly ecapsulate things in div...encapsulations in that particular tags ..it is preferential at the end.

    - <div class="social-posts>
        <h2 class="username" >@sassy_pants_mcgee</h2>
        <h3 class="posts" >Posted 15mins ago</h3>
      </div>
      . Here classes acts a documnetation.{ we actualy use them for styling }

Head & Meta Tags :
    - 
        . <!-- <!DOCTYPE html> -->
            <!-- <html lang="en">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                
            </body>
            </html> -->
