# Templates for developing JSXGraph applets for Moodle (STACK and Moodle Filter)

You can use the templates for developing JSXGraph applets outside of Moodle (e.g. with VS Code). The templates provide a starting point for developing JSXGraph applets outside of the Moodle editors. In the head, the script for JSXGraph is included as well as styles for JSXGraph, MathJax, Font Awesome and our OTH-AW Moodle. The JSXGraph Script and Stylesheet can be included via CDN or from a local folder called `lib` (defaiult). When using the CDN-Option, you can specify the JSXGraph Version. There are also some local styles from our project IdeaL included (e.g. jxgbox layout, textbox). The body contains the markup structure of a moodle description or STACK question.

The Moodle Filter JSXGraph template provides the HTML structure for a Moodle description item (e.g. test descripting).
The STACK JSXGraph template provides the HTML structure for a STACK question along with feedback (commented out). You can use this template to develop JSXGraph applets for STACK questions.

Below the JSXGraph div, there is a local script tag that includes our boilerplate code for a JSXGraph applet (a board with axes and a point). There you can start creating your own jsxgraph constructions without the need to build everything from scratch.

In order to use the JSXGraph applets in Moodle, one has to copy the code, change the "jxgbox" in the `initBoard-Method` to `divid` (STACK) or `BOARDID` (Moodle-Filter), add STACK-related code if needed and paste the code into the Moodle editor for the question or description between the JSXGraph block (STACK) or the JSXGraph tags (Moodle-Filter).

These two templates aim to provide a starting point for developing JSXGraph applets outside of the Moodle editor and thus benefit from many useful features of a proper source code editor like VS Code. In order to use the templates for your own project, you should change the link to our Moodle OTH-AW Styles to your projects Moodle stylesheet, adapt the local JSXGraph Styles from our project Ideal to the styles you want to use in your project and tweak the boilerplate code if you want to start with a different layout.

Assuming you have a Moodle course with STACK questions, the workflow to use our template would be the following:
1. copy the STACK JSXGraph template from this repository and open it in VS Code
2. Change the JSXGraph Version to the Version in your Moodles STACK Installation (you can see the version by using `showCopyRight: true` when creating a board)
3. Replace our Moodle Stylesheet (https://moodle.oth-aw.de/theme/styles.php/boost_campus/1649880327_1632249341/all) with the styles of your Moodle (this is for emulating your Moodle system style and getting the STACK styles)
4. Change the CSS inside the local style tag (you can use some styles from your project)
5. Adapt the boilerplate code to match the layout and structure of your JSXGraph applets
6. Start developing your JSXGraph applets and use the template as code basis for new applets





