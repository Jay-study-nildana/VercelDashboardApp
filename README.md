# Next JS For Students

I am following along this Vercel Learning Project. This is the public repo that had to be created to do the deployment.

For more notes and example code, check out, [NextJSForStudents](https://github.com/Jay-study-nildana/NextJSForStudents)

# Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

# notes about .env file

First, look at these links as they will explain how to get the values for database and also authentication. These values you have to put in the env file. These values are unique to your project, so, you have to create them and I cannot share them here. 

1. https://nextjs.org/learn/dashboard-app/setting-up-your-database
2. https://nextjs.org/learn/dashboard-app/adding-authentication

Now, the .env file will look something like this 

```
POSTGRES_URL=""
POSTGRES_PRISMA_URL=""
POSTGRES_URL_NO_SSL=""
POSTGRES_URL_NON_POOLING=""
POSTGRES_USER=""
POSTGRES_HOST=""
POSTGRES_PASSWORD=""
POSTGRES_DATABASE=""

# `openssl rand -base64 32`
AUTH_SECRET=
AUTH_URL=

```
Remember the following points.

1. Copy the env secrets from your Vercel Dashboard and put it in this env file
1. VERY IMPORTANT: make sure your gitignore is ignoring .env file. 

# setting up PostGres

1. run the 'npm run seed' command and you should see something like this.
    ```
    Created "users" table
    Seeded 1 users
    Created "customers" table
    Seeded 10 customers
    Created "invoices" table
    Seeded 15 invoices
    Created "revenue" table
    Seeded 12 revenue
    ```
1. You should also check the data in the vercel dashboard and see the seeded data. Try a simple query like this.
    ```
    SELECT invoices.amount, customers.name
    FROM invoices
    JOIN customers ON invoices.customer_id = customers.id
    WHERE invoices.amount = 666;
    ```
1. artificial delay.
    1. in file data.ts, I have added a artificial delay of 3 seconds to simulate slow network access. you can comment it or uncomment it as required.
    1. here is the exact snippet.
        ```
            console.log('Fetching revenue data...');
            await new Promise((resolve) => setTimeout(resolve, 3000));

            const data = await sql<Revenue>`SELECT * FROM revenue`;

            console.log('Data fetch completed after 3 seconds.');
        ```
1. more stuff

# hire and get to know me

find ways to hire me, follow me and stay in touch with me.

1. https://jay-study-nildana.github.io/developerprofile/
1. https://thechalakas.com
