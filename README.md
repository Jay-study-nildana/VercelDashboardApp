# Next JS For Students

I am following along this Vercel Learning Project. This is the public repo that had to be created to do the deployment.

For more notes and example code, check out, [NextJSForStudents](https://github.com/Jay-study-nildana/NextJSForStudents)

# Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.

# About .env file and setting up PostGres

1. First, you should create a .env file
1. Copy the env secrets from your Vercel Dashboard and put it in this env file
1. VERY IMPORTANT: make sure your gitignore is ignoring .env file. 
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
1. more stuff

# hire and get to know me

find ways to hire me, follow me and stay in touch with me.

1. https://jay-study-nildana.github.io/developerprofile/
1. https://thechalakas.com