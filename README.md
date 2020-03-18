Shopify - Translate your Shopify email notifications
In this 8 steps guide, you will see how to translate your email notifications on your Shopify website.

Weglot translates automatically all the content displayed on your website. Since the emails are not part of your website, Weglot cannot translate them automatically. However, with Weglot, it is possible to manually manage the content of the emails depending on the language of the order: with liquid code, it is possible to handle the translation of emails.

These instructions operate with order notifications but not the Gift Card Creation notification.

1. Open a text editor of your choice and paste the following liquid code
Depending on the languages managed on your website, you'll need to adjust the code: You'll need to change the language code in the 'when' lines.

Let's say, on a website, Weglot handles English as the original language, and French and Spanish as destination languages of translation. The liquid overall structure would be:

{% case attributes.lang %}   
{% when 'fr' %} 
EMAIL EN FRANÇAIS ICI
{% when 'es' %}   
EMAIL EN ESPAÑOL AQUI
{% else %}  
EMAIL IN THE ORIGINAL LANGUAGE HERE
{% endcase %}
The above code is only an example, so make sure to only input the languages managed on your Weglot app that you would like to add to the translation of the email.

Here is another example if you want to translate emails in German only:

{% case attributes.lang %}   
{% when 'de' %}   
EMAIL IN DEUTSCH HIER
{% else %}   
EMAIL IN THE ORIGINAL LANGUAGE HERE
{% endcase %}
This way, if an order has been placed in German, the customer will receive the content between the code line when 'de' and else, and if the customer has ordered in a different language than German, they will receive the content between the code line else and endcase.



2. In your Shopify admin area, go to Settings > Notifications and open the email you would like to translate
Let's say the 'Order Confirmation' email has to be translated:



3. Copy the email body


4. Go back to your text editor and replace the text 'EMAIL IN THE ORIGINAL LANGUAGE HERE' with the code you copied (if English is your original language)
In this example, the original language is English so the content 'EMAIL IN THE ORIGINAL LANGUAGE HERE' has been replaced by the code.



5. Then replace 'EMAIL EN FRANÇAIS ICI' with the same code, and change the sentences into the translated ones. Do the same for other languages like 'EMAIL EN ESPAÑOL AQUI'.
For example, for French, you will change 'Thank you for your purchase!' by 'Merci pour votre achat !'

Make sure you only alter the sentences. You must not translate any liquid code in between {% %} or {{ }}



6. Once you have finished replacing every field for every language, copy all the content of the text editor and paste it in your Shopify admin > Notifications, in the notification you would like to edit
In this case, the email edited is 'Order Confirmation':



7. Same steps for the title of the email
You can do exactly the same thing for the subject of the email: In a text editor, copy and paste the code and replace the fields by the translation of the subject, like this for example:



Then paste this into the 'Email subject' field:



8. Click the button 'Save' on the top right
You're done! Your customer should receive the email in their language.
