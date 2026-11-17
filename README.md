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

