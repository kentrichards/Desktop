# UI Feedback

## Specific

*Contrast*

Many buttons don’t meet minimum contrast requirements (minimum recommended for standard interface elements is 4.50:1, while buttons with green backgrounds in SPARC are only 2.03:1), which might make reading these controls difficult for certain users.

- [Contrast checker](https://webaim.org/resources/contrastchecker/)
- [WCAG Contract guidelines](https://webaim.org/articles/contrast/#sc143)

![contrast.png](./UI%20Feedback%20Attachments/contrast.png)

*Selects "zoom in" when focused*

When focused, certain `select` elements "zoom in", partially obscuring the text.

![Screencast from 2024-09-27 14-37-43.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2014-37-43.mp4)

![Screencast from 2024-09-27 14-38-45.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2014-38-45.mp4)

*Inconsistent drop down appearance and behaviour*

There are two kinds of drop down menus here that look and behave differently. Violates "principle of least surprise."

![Screencast from 2024-09-27 14-51-48.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2014-51-48.mp4)

*Labels and form controls out of alignment*

![Pasted image 20240927145631.png](./UI%20Feedback%20Attachments/Pasted%20image%2020240927145631.png)

*Drop down menu cut off when table has too few elements*

![Screencast from 2024-09-27 14-57-38.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2014-57-38.mp4)

*Unclear UI state*

This is the "completed" view of Task Manager, but the only indication of that is the small "View Incompleted Tasks" button. A user trying to find their active tasks might easily become confused about why the task they are expecting to find isn't showing up, before realizing they are on the wrong view.

Also, I think "View Incompleted Tasks" is a little awkward. A better label might be "View In-Progress Tasks".

![Pasted image 20240927150035.png](./UI%20Feedback%20Attachments/Pasted%20image%2020240927150035.png)

*"View Task" actually edits*

Pressing "View Task" opens the task to be edited, and there isn't a "Cancel" or go back button. Confusing behaviour given the original button's name.

![Screencast from 2024-09-27 15-05-36.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2015-05-36.mp4)

*Changing default behaviour of textarea*

The small size change when the textarea is focused is strange to me. More importantly, the default resize behaviour of HTML textareas (controlled by clicking and holding on the button right corner on the input) is being reimplemented in client side JS — resulting in a much slower version of the behaviour HTML gives you for free!

![Screencast from 2024-09-27 15-09-13.mp4](./UI%20Feedback%20Attachments/Screencast%20from%202024-09-27%2015-09-13.mp4)

*Creative Dashboard*

Filtering the creative dashboard by clicking on the items on the left feels unintuitive to me. Clicking the entries under "Stats" hides them, whereas clicking the entries under "Writers" shows them. I didn't realize either option would filter the list (I think a more natural control would be a checkbox). It's also quite unclear what filter you have applied (by stats or by writers).

Clicking on an entry under "Writers" switches to filtering by writers, but to go back to filtering by stats you have to unclick all selected writers. Contradictory functionality.

I also think there is too much colour here in general. What's important? What are we trying to highlight? When everything is highlighted, nothing stands out. More conservative use of colour (with badges, accents, borders, etc.) may improve clarity/help the user focus on what matters most.

![Pasted image 20240927160716.png](./UI%20Feedback%20Attachments/Pasted%20image%2020240927160716.png)

## Miscellany

- Required fields should be marked with an asterisk.
- Several different implementations of "Search" on different pages, eschewing the principle that parts of the software that do the similar things should look similar.