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
  npx degit https://github.com/craigmckeachie/microblog microblog
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

## Checklist

## Home (also referred to as landing in pdf)

Should display:
Create Account (link can style as button)
Log in (link can style as button)
see twitter home page when logged out

## Login page

Prominently feature a Login form.
Some starting code has been provided and login is working (try not to break it).
Focus here on making the form look nice and behave as expected.
After login, automatically redirect the user to the "Posts" page. Later
To see how to do this see `profile/auth.js`
Provide a link to your Registration page.
Since this is your website, you don't need to name everything the same as we name them
in this document. For example, your "Registration" page may be called "Sign up" and
your "posts" may be "remarks," etc.

## Registration page

Prominently feature a functioning sign-up form.
You will need to perform a request to the MicroblogLite API to register a user
and redirect the user to the Login page for the user to sign in for the first time.
See `profile/auth.js` for an example of how to redirect

## Posts page

- Prevent access to this page unless the visitor is logged in. (already done)
  - This page should be inside the "walled garden." If the visitor is not logged in, they should
    be redirected to the Login page instead of being shown user content.
- Provide a link to the Profile page.
- Include a working Logout button.
  A function will be provided for you in `profile\auth.js`.
- Display posts from all users. You will need to perform a request to the MicroblogLite API to get all posts
- Each post should display its content, author, and timestamp. This will require a
  request.

## Create Post

- Provide a working form for creating a post.
- This will require a request.

## Profile page

- Prevent access to this page unless the visitor is logged in. (already done)

  - This page should be inside the "walled garden." If the visitor is not logged in, they should
    be redirected to the Login page.

- Request the user that is logged and display their information including their bio
- Provide a link to the Posts page.
- Include a working Logout button.
  - A function to do this is already done in `profile\auth.js`
- Include a link to an edit profile page (stretch)

## Edit Profile (stretch goal)

- Prominently feature a form to edit the user's bio including a button to save it
- When the button is clicked save the updated user information

## Delete Post (stretch goal)
