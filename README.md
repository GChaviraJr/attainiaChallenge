# challenge
# User Activity Monitor

## For this exercise create an application using the Vue Javascript Framework.
One page of the application should display a table of the values found in users.json. By default this table should display all rows with a white background. On the same page there should be a button. When this button is clicked all user rows with a login count of 0 should have a red background. When the button is clicked again all recoreds whould have a white background.

A separate page of the application should dispaly a table of the values found in the json file like above. By default this table should have a white background. On the same page there should be a button. When this button is clicked all user rows with a login count greater than or equal to 1 should have a green background. When the button is clicked again all records should have a white background.

## My thoughts
I have never used Vue.js before and I have not used Javascript in quite a while. I have been using python and creating automation test scripts so this was fun to get back into. I was actually pressed for time so I just ran through and used the Vue docs, which are well written. There are things I thought of implementing if I had the time but since the requirements of this challenge are simple, I finished fairly quickly (about 2 hours). Overall this was a quick fun challenge and I enjoyed writing in Javascript again. This is why Cypress is a great tool because I could continue to work in Javascript and full test an application like this and still publish to Jenkins in order to perform CI/CD pipelines. Selenium will work too but since things are written dynamically its not excactly the fastest way to test a modern framework like this but since it has so many resources its still a great way to do so. 

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
