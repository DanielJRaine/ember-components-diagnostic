# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    A gallery of fine art pieces.  At the top level, you could have sections, i.e., sculptures, portraits, still-lifes.  Further down, each section could have a
    list view where each piece has a title header, an image, and a description.  Each title header, image container, and description box could be its own component.  
    Furthermore, each section could be a component made of the previous subcomponents (which would all probably be on the top level because of how generic they are).
    You could also have multiple galleries for each artist, making a gallery itself another component of components of components.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    A template.hbs which handles styling the HTML and the component's structure/UI layer and a
    component.js which is responsible for the component's behavior, its actions, its state, and data-binding.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    ember generate component contacts/my-contact
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.phoneNumber as |phoneNumber|}}
        {{my-contact/my-phone phoneNumber=phoneNumber}}
    {{/each}}
    ```
