# Capstone 3 Notes

## API (backend)

### Hosted:

http://microbloglite.us-east-2.elasticbeanstalk.com

### Run on Your Computer

https://github.com/DevelopIntelligenceBoulder/microbloglite-capstone-backend

## Frontend

Starter Frontend:
https://github.com/craigmckeachie/microblog

1. Create a capstone3 folder (in your LearnToCode/capstones folder).
2. Open a gitbash on Windows or Mac Terminal in the capstone3 folder
3. In your terminal: 
```
   # Make sure you are in the capstone3 folder
   npm install -g degit
   degit https://github.com/craigmckeachie/microblog
   ```

4. Open the capstone3 folder or the microblog folder in VS Code

## Pages

## account/login.html

- functionality working, just needs styles
- POST /auth/login

## account/registration.html

- need to create from scratch
- POST /api/users

## account/profile.html

- GET /api/users/{username}
- DO NOT create POST here even though the PDF says to do it, do it in `posts/posts-create.html`
- if you tackle the `account/profile-edit.html (stretch goal)` you will need a button (`<a class="btn btn-primary">) or link on this page to go to the edit page and you will pass the user id in the querystring
- needs to have a logout button in the navigation that works

## account/profile-edit.html (stretch goal)

- Update user's biography
  - /api/users/{username}

## index.html

    - home/landing
    - in the original starter project (not the one you are using) this page also had the login form

## posts/posts.html

- GET /api/posts
- consider using Bootstrap lists to display posts (or cards?)
  - https://getbootstrap.com/docs/5.3/components/list-group/
- needs to have a logout button in the navigation that works

## posts/posts-create.html

- POST /api/posts
- should contain a form with a `<textarea>` (like input type="text")
- a button to create the "post"
- needs to have a logout button in the navigation that works
