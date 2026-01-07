# iam-permissions-management
## Setting up Tags
I've set up two EC2 instances in order to test the effectiveness of the permission settings. I've used tags to label them.
<img width="1419" height="546" alt="image" src="https://github.com/user-attachments/assets/51e8e807-71b1-4e09-a479-0f61e0df51f3" />

## Setting up New Policy
I've set up a policy using JSON that allows all EC2 related actions to all EC2 instances that have the "Env" tag "development." It denies creating and deleting tags for all EC@ instances.
<img width="2061" height="1033" alt="image" src="https://github.com/user-attachments/assets/8aaa1bd6-867a-4e5a-b15e-a3e53831f659" />

## New User Group
Here I've set up a new user group that follows the created policy.
<img width="2089" height="426" alt="image" src="https://github.com/user-attachments/assets/787393c3-d32b-431e-8b9f-0dea6624bd71" />

I've set up a user to put in the group as well.
<img width="2036" height="546" alt="image" src="https://github.com/user-attachments/assets/40ce5e44-c69a-474e-836b-044f882a0053" />

## Testing Policy
I've signed in as the new user. Below, we can see some permissions have already been denied.
<img width="2531" height="1172" alt="image" src="https://github.com/user-attachments/assets/1f62dd71-b7da-4f41-bd6f-75bd0ba6d146" />

As this user, I have attempted to stop the production instance. Since the user was part of the group in which we created the policy, this action was not successful.
<img width="2552" height="1175" alt="image" src="https://github.com/user-attachments/assets/48a26d61-2355-49d2-a477-ce06618c02e8" />

