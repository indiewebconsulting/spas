# Single Page Applications

![Single Page Applications](583A2B8D-8622-4E2E-A03D-F5DF6C7268E8.png)

## Check back soon for live Heroku, AWS EC2 and ARM64 Hybrid Cloud demonsteration links!
We're migrating a lot of our services and properties right now and need a bit of time. Until then, enjoy the code!

## In Process - we care about DevOps before we care about our customers
- Build automation with Jenkins
- Build script testing with Dockerfile integrations
- Release management in AWS (S3 for cube.indiewebconsulting.com and EC2 for flights.indiewebconsulting.com)
- Release management in IWC's Intranet (Prod-facing origin servers)
- Release management in Suite Potato Pi ARM64v8 SBC with Amlogic S905x SoC

## Here's how to build things to break your own things from our things. Things.

### [Flights App](https://github.com/indiewebconsulting/spas/tree/master/aspnetcore-react-redux)
- Clone the IWC spas repository with `git clone http://git.indiewebconsulting.com/spas.git` and then `cd spas/aspnetcore-react-redux` to enter the ASP .NET Core "Flight Search" App.
- Build the latest version of the app using Docker by entering `$ sudo docker-compose build`. You can modify the building Docker image inside docker-compose.yml, to use your own Dockerhub namespace.
- Once a successful build is complete, run `docker-compose up -d` to run the Flights app in daemon mode, which will start a Web server on port `:3000`.
- Open `http://localhost:3000` to see the production-ready ASP .NET Core 2.1 application in your browser.

### [Rubix App](https://github.com/indiewebconsulting/spas/tree/master/rubix-demos)
- Clone the IWC spas repository with `git clone http://git.indiewebconsulting.com/spas.git` and then `cd spas/rubix-demos` to enter the React for Web Single Page Application.
- Build the latest version of the app using Docker by setting `$ sudo docker-compose -f docker-compose.prod.yml build` for a production release or `$ sudo docker-compose -f docker-compose.yml build` for the developer release.
- Once a successful build is complete, run `docker-compose up -d` to run the Rubix demo app in daemon mode, which will start a Web server on port `:8080`.
- Open `http://localhost:8080` to see the React app rendered in your browser.
- You can also run `$ cd spas/rubix-demos/src ; npm install` to install required libraries locally instead of building from Docker. Aftern running `npm install`, run `npm run-script build` to build a publicly releasable static folder of files. Or, run `npm run-script start` to open the application for developing locally.

## ./rubix-demos
### Seasonally in-process React playground and self-education tool
This hybrid ReactJS playground is Jen's first attempt at a more meaningful SPA experience, having done "like a billion" landing pages across a ten year FTE marketing developer position.

It's a floating, draggable cube, displaying nine of the latest Instagram images on each side, from a selectable set of hashtags. Some complex theming implementations at a demonstratable level, including Redux state management of the cube and Instagram requests, with Redux Sagas.

### Status: Ongoing
### Version: 0.3.6
### Condition
Typically only a few minor bugs, but ReactJS continues to grow in complexity with each new release of itself or its many npm packages.  So, you get what you pay for - something free and shiny to look at! If you pound that "watch" or "star" icon, you can be notified when Jen pushes something new. 

### Implementation Dependencies
See package.json for the full list. Below are some highlights.
- React 16.2.0
- Redux 3.7.2
- Webpack
- Style, URL, and SVG loaders
- NodeJS > 8
- Build and server tools 

---

## ./aspnetcore-react-redux
### Retired ASP .NET Core MVC with Microsoft excel to JSON Web Service demonstration.
This was an attempt at taking the more "boilerplate-y" React templates for Visual Studio and producing a .NET Core SPA early in the development of .NET Core 2.

### Status: Retired
### Version: 1 (only 1)

### Implementation Dependencies
- .NET Core 2.1 with matching SDK
- Docker, for building an outputted, self-contained Web app that runs on any Linux box, even without .NET Core installed.
- React
- Redux
- NodeJS > 8
- Webpack
- A more current working knownedge of ASP .NET and C# than Jen has. SDK had several updates since Jen wrote this SPA in 2017.




