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

## CSS

Css is not a programming language, It is just a rules that we give to browser.

    - Sample rule :
        . h1 {
            color:red;
            // color -> property ,
            // red -> value.{ takes named-color names, hex-color: RGB values, hsl(0, 100%, 50%) }
        }
        <h1>This text appears in red</h1>

        . h1 {
            color: limegreen;
            font-size: 60px;
            font-weight: normal;
            text-decoration: underline;
            text-transform: uppercase;
            border: 3px solid pink;
        }

    - css cascade :
        . Specificity: Specificity is a score calculated based on the type of selectors used. More specific selectors (e.g., #id, .class) take precedence over less specific selectors (e.g., div, h1).

            . The specificity hierarchy is typically:
                Specificity (ID > class > element).

                Inline styles (styles directly in the style attribute of an element).
                IDs (#id).
                Classes, pseudo-classes, and attributes (.class, :hover, [type="text"]).
                Elements and pseudo-elements (div, p, ::before, ::after).
                Example:

                    <h1 class="heading" id="main-heading">Hello, World!</h1>

                    /* Low specificity (element selector) */
                    h1 {
                        color: green;
                    }

                    /* Medium specificity (class selector) */
                    .heading {
                        color: blue;
                    }

                    /* High specificity (ID selector) */
                    #main-heading {
                        color: red;
                    }

                    In this case, the text will be red because the ID selector #main-heading has the highest specificity.

            . Source Order:

                If two CSS rules have the same specificity, the last rule defined in the CSS file will take precedence. This is why it's important to structure CSS in a logical order, as later rules can override earlier ones.
                Example:
                    p {
                        color: yellow;
                    }

                    p {
                        color: orange;
                    }
                    In this case, the text in the <p> element will be orange because the second rule is applied last.

IDs and !important : - IDs:
Specificity (ID > class > element).

            Inline styles (styles directly in the style attribute of an element).
            IDs (#id).
            Classes, pseudo-classes, and attributes (.class, :hover, [type="text"]).
            Elements and pseudo-elements (div, p, ::before, ::after).

        1. Specificity of ID Selectors
            In CSS, specificity is a measure of how "specific" a selector is. More specific selectors have higher precedence when multiple rules target the same element. The specificity of a selector is determined by a
            numerical score, which can be broken down as follows:

                Inline styles (highest specificity) → score: 1000
                IDs → score: 100
                Classes, pseudo-classes, and attributes → score: 10
                Element selectors (e.g., div, p) → score: 1

            ID Specificity:

            ID selectors are assigned a specificity score of 100. This makes them more specific than class selectors (which score 10) and element selectors (which score 1).

            Example:
                The following selectors have the following specificity scores:
                    #header (ID) → 100
                    .menu (Class) → 10
                    div (Element) → 1
            Because the ID selector has a higher specificity score, it will override any rules defined by classes or element selectors, even if they appear later in the CSS.

    - Importance:
        Styles marked with !important override all other rules, regardless of specificity.
        Example:
            h1 {
                color: red !important;
            }

            h1 {
                color: blue;
            }
        In this case, the h1 text will be red, even though there's a rule later that sets it to blue. The !important rule has higher priority.
