# Use components from the Design System

You can copy example code from the GOV.UK Design System to add page elements like radios and text inputs - we call these 'components'.

## HTML and Nunjucks

HTML is the language used to create web pages.

Nunjucks is another language we can run in the Prototype Kit, to make HTML for us. Short, simple Nunjucks code can create much longer, more complex HTML.

In the Design System, components have both Nunjucks and HTML example code. Either will work in the Prototype Kit.

## Add radios to question 1

1. Go to the [stacked radios](https://design-system.service.gov.uk/components/radios/#stacked-radios) section of the Design System.
2. Select the **Nunjucks** tab, then **Copy code**.
3. Open `juggling-balls.html` in your `app/views` folder.
4. Replace the 2 example `<p>...</p>` paragraphs with the code you copied.
5. The example comes with a heading that is connected to the answers for accessibility, so delete the old `<h1>` tag with "How many balls can you juggle?".

### Customise the example code

1. Change the `text` from "Where do you live?" to "How many balls can you juggle?"
2. Change the `idPrefix` and `name` to `how-many-balls` 
3. We only want 3 options not 4, so delete the last of the `items` including the comma from the previous item:
```
    ,
    {
        value: "northern-ireland",
        text: "Northern Ireland"
    }
```
4. Change the `value` and `text` in the `items` to:
  - 3 or more
  - 1 or 2
  - None - I cannot juggle

Your page should now look like this:

![Screenshot of the question page with radios](/public/images/docs/tutorial-radios.png)

## Add a textarea to question 2

1. Go to the [textarea](https://design-system.service.gov.uk/components/textarea/) page of the Design System.
2. Select the **Nunjucks** tab, then **Copy code**.
3. Open `juggling-trick.html` in your `app/views` folder.
4. Replace the 2 example `<p>...</p>` paragraphs with the code you copied. 
5. Delete the old `<h1>` tag with "What is your most impressive juggling trick?" (again the example code comes with an accessible heading for the question).

### Customise the example code

1. Change the `text` from "Can you provide more detail?" to "What is your most impressive juggling trick?"
2. Change the `id` and `name` to `most-impressive-trick`
3. We don't need a hint, so remove it and the comma just before it:
```
,hint: {
    text: "Do not include personal or financial information, like your National Insurance number or credit card details."
}
```

Your page should now look like this:

![Screenshot of the question page with a textarea](/public/images/docs/tutorial-textarea.png)

[Next (Show the user's answers on your 'Check your answers' page)](show-users-answers)
