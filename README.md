<h1>Angular 18 : Internationalization</h1>
<p>Internationalization (i18n) in Angular is the process of designing your application to support multiple languages and locales, enabling it to reach a global audience. This involves preparing your app to adapt to various languages and regional settings without requiring significant code changes.<p>
<hr>

<h1>Steps to Implement Internationalization:</h1>

<p><b>Step 1: Set Up the Angular Application:</b> Begin by creating a new Angular application and adding the Angular localization package</p>
<p>Bash: 
ng new my-i18n-app
cd my-i18n-app
ng add @angular/localize</p>

<p><b>Step 2: Mark Text for Translation:</b>Use the i18n attribute to mark the text in your templates that need translation. For example, in your app.component.html:</p>
<p><h1 i18n="site header|An introductory header for the site">Welcome to our website!</h1><p>

<p><b>Step 2: Extract Translation Files:</b>Angular provides a tool to extract marked text into a translation file. Run:</p>
<p>Bash: ng extract-i18n --output-path src/locale</p>
<span><i>This command generates a messages.xlf file in the specified directory, containing the text to be translated.</i></span>

<p><b>Step 4: Translate the Text:</b>Duplicate the messages.xlf file for each target language (e.g., messages.fr.xlf for French) and provide the translations within these files</p>

<p><b>Step 5: Configure Angular for Multiple Locales:</b>Update the angular.json file to define the supported locales:</p>

<p><b>Step 6: Build and Serve the Application:</b>Build the application for each locale:</p>
<p>Bash: ng build --localize</p>
<p>This command generates locale-specific versions of your application in the dist directory. You can then serve or deploy the version corresponding to the desired locale.</p>


