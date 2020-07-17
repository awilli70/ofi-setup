# OFI Alumni Dev Environment Setup
#### The quick and easy way

Note: While not required, I would recommend using VSCode when working on this application.  
My recommended plugins are:
- Auto Close Tag
- Babel JavaScript  

If you're on windows it has an extension for connecting to the WSL filesystem, which is super handy.  
Once you have access to a shell prompt, clone/fork the ofi-alumni repository to your own system.  

### MacOS
1. Install [Node.js](https://nodejs.org/en/download/) and [Homebrew](https://brew.sh/)
2. Using homebrew, install [Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable) and [MongoDB community drivers](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/)
3. I heavily recommend the package [npm-install-missing](https://www.npmjs.com/package/npm-install-missing) for managing the dependencies - after installing, type `$ npm-install-missing` in the root, client, and server directories.
4. Type `$ brew services start mongodb-community`
5. To start the application locally, type `$ npm run dev` - Hopefully, the app will launch with the client in localhost:3000 and the server in localhost:5000

### Windows
1. Install the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10). I personally recommend WSL 1 for this application
2. Select and install your preferred Linux distribution from the Windows store
3. Follow the Linux steps

### Linux
Note that your installation process will likely vary based upon the distribution you use
1. Install [Node.js](https://nodejs.org/en/download/package-manager/)
2. Install Yarn using your preferred package manager ([Yarn](https://classic.yarnpkg.com/en/docs/install/#mac-stable))
3. Install [MongoDB Community Drivers](https://docs.mongodb.com/manual/administration/install-on-linux/) (Note: If using the WSL, MongoDB says they don't have working drivers. They're also liars. The standard Linux installation works (I tested it))
4. At this point, you can now follow the MacOS instructions starting from 3.

#### Hopefully this helps!

## Other resources for a quick start with ReactJS, Express, and Mongoose
[React:](https://reactjs.org/docs/introducing-jsx.html) The ReactJS documentation is fantastic!  
I recommend 2, 4-7, and 10-11 in Main Concepts, and 1-4 in Hooks to get a quick start.  
We also use [SemanticUI React](https://react.semantic-ui.com/) to help style our components. It is awesome, and odds are if you want a specific layout, SemanticUI has a component (and snippets) to help you out.  
The code base uses both functional components with hooks and class based components with lifecycle methods.  
Functional components generate cleaner code, but have a lot less documentation/support, while Class based components have weird behavior with setting state and lifecycle methods that result in bulkier code.  
The nice thing about React is that the components are plug and play no matter what component type you choose, so it ultimately comes down to preference.  
[This](https://wattenberger.com/blog/react-hooks) article by Amelia Wattenberger is an awesome resource, and I think makes a pretty convincing case for hooks

[Express:](https://itnext.io/getting-started-with-express-js-for-the-impatient-9177fc0e1b49) This is a decent resource for getting started, but I'm not sure if it's enough to feel comfortable with Express.  
Honestly, the best way to learn express is to make yourself familiar with the server directory starting with app.js, and moving on to the routes folder. It shows the general pattern we use and provides templates for new routes.
MDN has decent tutorials, but they don't always match up with our server - ditto for the Express documentation, which isn't great for learning but is pretty useful for debugging!

[Mongoose:](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose) This is basically all you need to get started with Mongoose.
Beyond this, the mongoose documentation is decent albeit a little confusing, and there are a lot of other resources available (esp. StackOverflow)
