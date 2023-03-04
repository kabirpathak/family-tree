# family-tree
Flutter based mobile application.

# Features in v1: 

- Will contain multiple family trees - not visible to users/profiles who are not a part of the tree.
- In order to join a family tree, a user has either create one, or be invited.

- Inside each family tree:
  - There will be multiple user profiles.
  - User profiles can be of two types:
    - Shadow: 
      - For users who are either deceased or haven't logged in to the app yet.
    - Active: 
      - For users who have logged in to the app, and have either:
        - Created their own profile and merged it with the existing tree.
        - Chosen an existing shadow profile as their own. In this case the shadow profile will be changed to active.
    
# User types: 

- Alpha: 
  - The person who created the family tree, or someone who was given admin priveleges by an exiting admin.
  - Will be able to create new profiles (both active (thier own) and shadow)

- Beta: 
  - Will be able to create his own profile, and can choose an existing shadow profile as their own.
  - Will not be able to create new shadow profiles.

# Notes: 

- Upon joining a family tree, all users will initially be Beta users.
- Except for the person who created the family tree.
- Selection of a shadow profile by a Beta user, will need to be approved by an admin.


# Important Tables:

1. User:
   - User and profile are different things.
   - Anyone who logs into the application becomes a user.
   - A user can have multiple profiles (1 in each family tree they're a part of)

1. Family Tree: 
   - Has many people (profiles).

2. Profile:
   - Belongs to family tree.
   - Has one user.
   - Has multiple spouse.
   - Has two parents.
   - Has multiple children.


