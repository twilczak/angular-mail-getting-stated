## Angular Getting Started - Web mail client  

### Step 0 - Baseline

1. Download / Install Node.js :  
   https://nodejs.org/en/download/
    
   This will give you both node and npm

2. Install Angular-CLI

   `$ npm install -g @angular/cli`
   
   verify:
   ```
   $ ng --version
       _                      _                 ____ _     ___
      / \   _ __   __ _ _   _| | __ _ _ __     / ___| |   |_ _|
     / △ \ | '_ \ / _` | | | | |/ _` | '__|   | |   | |    | |
    / ___ \| | | | (_| | |_| | | (_| | |      | |___| |___ | |
   /_/   \_\_| |_|\__, |\__,_|_|\__,_|_|       \____|_____|___|
                  |___/
   @angular/cli: 1.4.9
   node: 6.11.4
   os: darwin x64

   ```
   === Success!!
   
### Step 1 - Initialize new project with Angular-CLI

1. Initialize project
    
   `$ ng new angular-mail --style=scss`
   
   Creates project directory, initializes git project, with common project defaults, including:
   - src directory with a single page, app module and app component
   - unit test configuration with jasmine and karma
   - e2e test configuration with protractor
   - configuration files for typescript
   - installs all required libraries
   
2. Verify project

   `$ ng serve --open`
   
   Starts the development server and opens a browser on the index page
   
3. Run some unit tests
  
   `$ ng test`
   
   Watches for file changes and re-runs tests

### Step 2 - Mailbox Infrastructure

1. Add Global Styles
    
    Resets + commonly used clases
    
2. Create mail-message class. 
   
   `$ ng generate class mail-message`
   
   Add properties to class: id (default to null), subject, sender, recipient, dateSent, body. 
   
3. Create mail.service
   
   `$ ng genreate service mail`
   
   Add methods to get inbox and outbox messages, and handle errors

### Step 3 - Mailbox Component

1. Add Routes

    Used to navigate through different parts of the system. 
    
    Always start with routes as a way of getting an early understanding of how components are composed and interact with each other    

    Without components angular router complains

2. Add mailbox component

   `$ ng generate component mailbox`
       
   Smart components responsible for gathering data and event handling (wiring)
       
   Typically don't have much styling, because they are not presenting anything
  
   Don't forget to namespace your components!
