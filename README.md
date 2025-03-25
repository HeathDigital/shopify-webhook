# Shopify Webhook
This app is built using:
- NodeJS via Typescript
- Express
- GraphQL
- Shopify's Admin api
- Nodemailer

### Setup
1. Add the following values to your **.env** file:

| Variable               | Value                                              | Example                              |
|------------------------|----------------------------------------------------|--------------------------------------|
| `SHOPIFY_STORE_URL`     | Your store url                                     | `[my-store].myshopify.com`             |
| `SHOPIFY_ACCESS_TOKEN`  | Your Shopify app's access token                   | `...`                                |
| `API_SECRET`            | Your app's API secret                              | `...`                                |
| `PORT`                  | The port you want to run this application on locally | `3000`                               |
| `VARIANT_ID`            | The ID of the variant you would like to check against | `gid://shopify/ProductVariant/[0123456789]` |
| `EMAIL_HOST` | Your email host | `smtp.gmail.com` |
| `EMAIL_PORT` | Your email port setting | `465` |
| `EMAIL_USER_NAME` | The email Sender's name | `John Peters` |
| `EMAIL_USER_ADDRESS` | Your email address | `john@snowmail.com` |
| `EMAIL_USER_PASSWORD` | Your email's password | `H*tWater!` |

2. Start your development server and connect to a tunneling service to gain access to `https`. We reccomend using local tunnel for development.
    - Install linux: `npm install -g localtunnel`

    ```
    - lt --port [your port]
    - npm run dev
    ```

3. Once you have your **url**; navigate to `settings > notifications > webhooks > create webhook`.

    Enter the following configuration for your webhook:
    1. **event** = `product update`
    2. **format** = `JSON`
    3. **url** = The Tunneling Url recieved from **Step 2**
    4. **webhook** = `Latest`

### Running application
1. Test webhook from shopify to test if data is logged upon testing
2. Navigate to product page & edit the pricing of products.
3. Ensure shopify has access to the following scopes `write_products, read_products`

## License  
This project is licensed under the **MIT License**.

---

### **Contributors**  
- **Moses Sangobiyi** – Developer  
