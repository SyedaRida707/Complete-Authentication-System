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

1. Sab se pehle user application par register karta hai. Jab tak user register nahi karega, hum usay application ke kuch features, jaise comment aur like karne ki permission nahi denge.

2. User apni details server ko bhejta hai. Server un details ko database mein save kar leta hai.

3. Database mein user ka record save hone ke baad us user ko ek unique ID milti hai.

4. Server us ID ko use karke ek token create karta hai. Is token mein user ki pehchan se related data hota hai, jaise uski ID.

5. Server token create karne ke baad response mein woh token user ko bhej deta hai.

6. Ab jab bhi user server ko koi request bhejta hai, toh woh request ke saath apna token bhi bhejta hai.

7. Chahe user 10 requests bheje, 1000 ya 100,000 requests bheje, wohi token har protected request ke saath bhej sakta hai, jab tak token valid hai.

8. Ab server ko pehle request bhejne wale user ki pehchan nahi hoti thi, lekin ab request ke saath token aa raha hai.

9. Server us token ko check aur verify karta hai. Token mein user ki ID hoti hai, toh server samajh jata hai ke yeh request kis user ki hai.

10. Is tarah server user ko identify kar leta hai aur samajh jata hai ke request kis user ki taraf se aayi hai.

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


## Morgan (Logger Middleware)

- **Logger:** Application ki activities aur requests ka record rakhna.
- **Morgan:** Express.js ka third-party logging middleware.
- **Purpose:** HTTP requests ki information terminal par display karna.
- **Installation:** `npm install morgan`

## Morgan Predefined Formats

Morgan middleware ke different predefined formats (modes) hote hain. Inhein use karke hum decide karte hain ke terminal mein HTTP request ki information kis format mein display hogi.


Morgan provides five predefined logging formats:

1. **combined:** Displays detailed request information, including IP address, date, method, URL, status code, response size, referrer and user-agent.

2. **common:** Displays request information similar to combined but excludes referrer and user-agent.

3. **dev:** Displays request information in a concise and colorful format. Mainly used during development.

4. **short:** Displays request information in a shorter format, including IP address, method, URL, status code and response time.

5. **tiny:** Displays minimum request information, including method, URL, status code, response size and response time.

### Example

`app.use(morgan('dev'));`

**Remember:** Morgan formats decide how HTTP request logs are displayed in the terminal.

## npx vs npm run

### 1. npx
- Used to run a locally installed package directly from the terminal.
- Example:

```bash
npx nodemon server.js
```

### 2. npm run
- Used to execute commands written inside the `scripts` section of `package.json`.
- Example:

```json
"scripts": {
  "dev": "nodemon server.js"
}
```

Run the script using:

```bash
npm run dev
```

### Why is `npx` not required in package.json?

`npm run` automatically searches for locally installed packages inside `node_modules/.bin` and executes them. Therefore, we don't need to write `npx` in the script.

**Note:** Both commands can run Nodemon.

