# UI Feedback 2

*Specify accepted file types to reduce mental burden on the user*

This form control for uploading attachments says "doc/pdf/mp3/wav" only, but the HTML `<input type="file" />` element doesn't enforce that requirement. By using the `accept` attribute and the MIME-types of the files we want, we can make it so the user's file picker only shows valid files (by default). This can help reduce the mental overhead of inputting the right data, by removing invalid entries.

![file attachment](./UI%20Feedback%20Attachments/file-attachment.png)

*Second file attachment control doesn't specify accepted file types*

This similar looking file attachment control doesn't tell the user what file types are allowed. Does that mean anything is permitted? If so, we should tell the user that too.

![file attachment 2](./UI%20Feedback%20Attachments/inconsistent-file-attachment.png)

*Different appearance for similar functionality*

This file picker has default browser styles, clashing with the rest of the page and inconsistent with other file pickers.

![file attachment 3](./UI%20Feedback%20Attachments/inconsistent-file-appearance.png)

Another inconsistent control.

![alt text](./UI%20Feedback%20Attachments/upload.png)

*Dub Request asset form*

No label on this select.

![unlabelled select](./UI%20Feedback%20Attachments/unlabelled-select.png)

All input fields should have labels. Placeholders are useful for providing example input, but they fail as labels because they disappear once the user enters something. This can become confusing when the user reviews the form before submitting, or even while they are filling out a particular field. What am I supposed to enter here again? I can't tell without removing what I've already entered. The icons help, but aren't sufficient as a replacement.

![placeholders instead of labels](./UI%20Feedback%20Attachments/no-labels.png)

*Confusing breadcrumbs*

Breadcrumbs are a great way to situate the user in a complex hierarchy and allow them to navigate back through it, but the breadcrumbs in SPARC don't effectively accomplish this goal.

For one, they are often cluttered. In the breadcrumbs below, both the home icon and "Home" redirect to the landing page (redundancy), and worse, so does "Creative"! The "Creative" link redirects to `/creative`, but because there is no such page, that ends up redirecting to the homepage as well. Home ⇒ Creative ⇒ Dub Request is the correct hierarchy (and the one the user would need to follow in the sidebar to reach Dub Request), but it isn't actually reflected in the system because there is no Creative page.

This seems to be a common issue throughout SPARC. Features are presented hierarchically, but the system is only organized hierarchically in the sidebar. For example, although Dub Request is found under Creative Tools in the sidebar and breadcrumbs, its URL is sparcmediahub.com/dub and (as mentioned) there is no sparcmediahub.com/creative.

![breadcrumbs](./UI%20Feedback%20Attachments/breadcrumbs.png)

There is also the fact the "Dub Request" is repeated on both ends of the breadcrumbs, with a slash after the first, making the hierarchy appear to begin and end at the same spot. While it's tempting to highlight the page title, we don't really need to here. For one, there are tons of places that indicate the current page (URL, sidebar, breadcrumbs, the page itself usually). I would suggest a better approach would be to remove the first "Dub Request" and have the breadcrumbs display Home / Creative (if it exists) / **Dub Request**.

![breadcrumbs homepage](./UI%20Feedback%20Attachments/breadcrumbs-home.png)

On the homepage, the breadcrumbs are entirely redundant — this whole navigation element could be removed to give the user more screen real estate. Especially since Home and Dashboard are the same thing, and presenting them as separate might be confusing.

*Form submission fails without informing the user*

![failure gif](./UI%20Feedback%20Attachments/error.gif)

*Enhance empty pages*

Usually, little attention is paid to "empty states", like the Video Requests page when there is no content to display. But an easy way to enhance the character of a page is to customize its empty state. Along with improving the page's appearance, we can take this as an opportunity to provide information to the user and make it easier for them to start populating the page with content.

![empty table](./UI%20Feedback%20Attachments/empty-table.png)

For example, we could display a "No video requests found" message here, with a button to create one (or whatever, I'm not actually sure what content goes in this table). Here's an example from the book *Refactoring UI* of enhancing a page when it would otherwise display an empty table.

![enhanced default](./UI%20Feedback%20Attachments/refactoring-ui.png)

*Input length?*

What do the "##" and "###" signify?

If we are asking the user for a short answer (two- or three-characters) it might be helpful to reduce the width of the input field. As the [GOV.UK Design System](https://design-system.service.gov.uk/components/text-input/) puts it, under the "Use appropriately-sized text inputs" section, we can "help users understand what they should enter by making text inputs the right size for the content they’re intended for." If a user is asked to input a small amount of text (e.g. their credit card's CVC code) a full width text input might be confusing.

On the other hand, if the number signs indicate the user should enter a number, a numeric placeholder and/or a HTML `<input type="number" />` may be clearer.

![input length?](./UI%20Feedback%20Attachments/image.png)
