# Templates for developing JSXGraph applets for Moodle (STACK and Moodle Filter)

## Information about this repository
This repository contains the JSXGraph templates for Moodle descriptions and STACK questions in Moodle from our project **IdeaL** (https://www.oth-aw.de/forschen-und-kooperieren/aktuelles-in-der-forschung/ideal/) that were used in the workshop *Tools and workflow for the development of interactive JSXGraph applets in a Moodle course* from the **JSXGraph Conference 2022** (https://jsxgraph.org/conf2022/program/).

## Motivation for the templates
In our project IdeaL, we came up with the idea of developing JSXGraph applets for our self-learning course ourtside of Moodle because of the limitations of the Moodle plain text editor.We use those templates as starting point for developing the applets in VS Code, which provides many useful features such as sxntax highlighting, code checking and code-completion. The use of a template ensures a consistent layout for all of our applets and provides a structure for the construction. As long as there is no text editor available for Moodle that has syntax highlighting and code checking, we will continue to use VS Code as our main source code editor for developing JSXGraph applets, because this speeds up the development process and avoids having to deal with endless searches for errors like a missing semicolon in the code. When using MAXIMA variables in your JSXGraph applet or you want to use the binding-functions (e.g. `stack_jxg.bind_point(stateRef, p)` from STACK, you cannot emulate this with our templates and workflow. Maybe we can find a way to make this possible in the future...

## Structure of the templates
In the head, the script for JSXGraph is included as well as styles for JSXGraph, MathJax, Font Awesome and our OTH-AW Moodle. The JSXGraph Script and Stylesheet can be included via CDN or from a local folder called `lib` (defaiult). When using the CDN-Option, you can specify the JSXGraph Version. There are also some local styles from our project IdeaL included (e.g. jxgbox layout, textbox). The body contains the markup structure of a moodle description or STACK question.

The Moodle Filter JSXGraph template provides the HTML structure for a Moodle description item (e.g. test descripting).
The STACK JSXGraph template provides the HTML structure for a STACK question along with feedback (commented out). You can use this template to develop JSXGraph applets for STACK questions.

Below the JSXGraph div, there is a local script tag that includes our boilerplate code for a JSXGraph applet (a board with axes and a point). There you can start creating your own jsxgraph constructions without the need to build everything from scratch.

In order to use the JSXGraph applets in Moodle, one has to copy the code, change the "jxgbox" in the `initBoard-Method` to `divid` (STACK) or `BOARDID` (Moodle-Filter), add STACK-related code if needed and paste the code into the Moodle editor for the question or description between the JSXGraph block (STACK) or the JSXGraph tags (Moodle-Filter).

These two templates aim to provide a starting point for developing JSXGraph applets outside of the Moodle editor and thus benefit from many useful features of a proper source code editor like VS Code. In order to use the templates for your own project, you should change the link to our Moodle OTH-AW Styles to your projects Moodle stylesheet, adapt the local JSXGraph Styles from our project Ideal to the styles you want to use in your project and tweak the boilerplate code if you want to start with a different layout.

## Example workflow
Assuming you have a Moodle course with STACK questions, the workflow to use our template would be the following:
1. copy the STACK JSXGraph template from this repository and open it in VS Code
2. Change the JSXGraph Version to the Version in your Moodles STACK Installation (you can see the version by using `showCopyRight: true` when creating a board)
3. Replace our Moodle Stylesheet (https://moodle.oth-aw.de/theme/styles.php/boost_campus/1649880327_1632249341/all) with the styles of your Moodle (this is for emulating your Moodle system style and getting the STACK styles)
4. Change the CSS inside the local style tag (you can use some styles from your project)
5. Adapt the boilerplate code to match the layout and structure of your JSXGraph applets
6. Use the VS COde extension Live Preview (https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server) to enable the live preview of the template as you code 
7. Start developing your JSXGraph applets and use the template as code basis for new applets
8. Copy the code for the applet, make some changes (change the string `"jxgbox"` to `divid`) and paste the code into teh Moodle editor for your STACK question





