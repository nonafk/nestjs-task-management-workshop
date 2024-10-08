Windows: Environment Variables
Windows users only: Environment Variables

In the upcoming lectures I will set up environment variables via NPM scripts. This is not supported in Windows by default.

To overcome this, please install the cross-env NPM package globally.

If you are using NPM:

npm install -g cross-env

If you are using Yarn:

yarn global add cross-env



Continuing further

Following this section, you will end up adding environment variables to your package.json scripts.



For example, in the lecture "Setting up ConfigModule", you will end up with:

"start:dev": "STAGE=dev nest start --watch",

You will need to add "cross-env" to that script, otherwise it will not work. So the final result should be:

"start:dev": "cross-env STAGE=dev nest start --watch",


And this should be the case for every script you have in your package.json that requires env variables (in this course we do start:dev, start:debug, start:prod, and test.