Create responsive web pages
The web pages should be responsive and resize according to the screen.

On small screens:

the Which City photo and text should be below each other,
and the Favourite Subjects sections should be below each other - the photos and the text should be along side each other.
On larger screens:

the Which City photo and text should be next each other,
and the Favourite Subjects sections should be next each other.
Page content
Your web page should have the following sections

Intro
A section with your full name and a photo of yourself with Table Montain in the background.

Which city?
Add a section to your page about a city you would like to visit. Tell us why and add one photo of this city to your page.

A foreign language
Tell us what foreign language you would like to learn and why. This should not be a South African Language. Add a table with 3-5 phrases in your language of choice that maps english phrases to the language you chose.

Favourite subjects
Add a section to your page about your three favourite subjects during your studies.

The three subjects:

should be next to each other on a big screen
and be below each other on a small screen.
Add a photo or small diagram that describes or relates to each subject. OR use a placeholder image for each subject something like this or one of these.

Above the 3 subjects state which qualification you completed at which institution.

Gather the information for your web page.
Use the Google document that will be shared with you via Google Classrooms to complete all the information that you will need to add to you web page.

You will need this to create the JSON file described below.

Files and folders to create
Create a folder called materialize_webpage in your projects folder.

Create and index.html HTML file for your web page using Materialize.

Use ViteJS with Handlebars to share the information for the web pages from a JSON file.

Create a JSON file called data.json in your project route with this structure:

{
    "user" : {
        "fullName": "",
        "photo" : ""
    },
    "city" : {
        "name" : "",
        "photo" : "",
        "description" : ""
    },
    "foreignLanguage" : {
        "language" : "",
        "phrases" : [{
            "englishPhrase" : "",
            "foreignLanguage" : ""
        },
        {
            "englishPhrase" : "",
            "foreignLanguage" : ""
        }]
    },
    "favouriteSubjects" : [
        {
            "name" : "",
            "description" : ""
        },
        {
            "name" : "",
            "description" : ""
        },
        {
            "name" : "",
            "description" : ""
        }
    ]
}
Import the JSON file into your HandlebarsJS context using this command:

import data from './data.json';
And then in the ViteJS setup add data:

export default {
  plugins: [handlebars({
    context : {
        /*
        previous setup here
        */
        data   // add this
    }
  })],
};
Make it responsive
Make sure both your webpages are responsive. They should look good on small and larger screens.

Resize Images
Ensure that all images that you are using for your web page are resized according
