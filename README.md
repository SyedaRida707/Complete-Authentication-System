# What is Authentication?
Authentication is the process of verifying the identity of a user to make sure they are who they claim to be.

**Easy Meaning: Authentication ka matlab hai user ki identity (pehchaan) verify karna.**

**Remember: Authentication = Who are you?**

*Real-Life Example*
- Suppose you want to log in to Facebook:
1. Enter your email.
2. Enter your password.
3. Facebook checks your credentials.
4. If correct → Login successful.
5. If incorrect → Login rejected.
**This process is called Authentication.**

# How Authentication System Works?

1. **User Registration:** First, the user registers on the application by providing their details.

2. **Data Storage:** The server receives the user's details and saves them in the database.

3. **User ID:** When the user's record is saved in the database, the user gets a unique ID.

4. **Token Generation:** The server creates a token using the user's ID. The token contains information related to the user's identity.

5. **Token Response:** The server sends the generated token back to the user in the response.

6. **Sending Requests:** Whenever the user sends a protected request to the server, the user also sends the token with that request.

7. **Token Verification:** The server receives the token and verifies it to check whether it is valid.

8. **User Identification:** The server reads the user's ID from the token and identifies which user is sending the request.

9. **Access:** After successful authentication, the server allows the user to access the requested protected feature.

## Remember

**In simple words:** A token helps the server identify which authenticated user is sending a request.


### Token Expiration

1. **Token Expiry:** Every token has a validity period or time limit. For example, some tokens remain valid for 3 hours, while others remain valid for 5 days.

2. **Token Expire:** When the token's validity period ends, the token expires.

3. **Login Again:** After the token expires, the user may need to log in again.

4. **New Token:** When the user successfully logs in again, the server generates a new token and sends it back in the response.

5. **Use New Token:** Now, the user sends the new token with their next protected requests.

## Remember

**Expired Token = Login Again = New Token**

