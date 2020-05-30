# Installations
    # Install React App Globally
        > npm i -g create-react-app

    # Create React App
        > create-react-app desktop-app --template typescript

        # Add Electron Application
            > npm add -D electron

        # env variables for all OSs
            > npm install cross-env

# For Windows *Fix Error of `PUBLIC_URL=./ react-scripts build`
    1. Quick Solution
        > set PUBLIC_URL=https://dsomething.cloudfront.net&&npm run build
        This will also generate index.html with: 
            <script type="text/javascript" src="https://dsomething.cloudfront.net/static/js/main.ec7f8972.js">
    2. Permanent Solution
        Create a file called .env at your project root(same place where package.json is located).
        In this file write this(no quotes around the url):
        > PUBLIC_URL=https://dsomething.cloudfront.net
        This will also generate index.html with:
            <script type="text/javascript" src="https://dsomething.cloudfront.net/static/js/main.ec7f8972.js">
    Source: https://stackoverflow.com/questions/42686149/cant-build-create-react-app-project-with-custom-public-url

    3. The 2nd Permanent Solution without 1 & 2
        > npm install cross-env 
    

# Build Web Command
    Only run this commands if the scripts already configure in package.json

    # Usual Command
        > npm run-script build:web

# Run Electron Application
    First, do the Build Web Command.
    1. Build First the electron
        > npm run-script build:desktop
    2. Run
        > npm run-script start:desktop

# Setting up our Desktop app project with TypeScript + Electron.js + React.js over Create React App.
# https://www.youtube.com/watch?v=MBnWbLzuST8