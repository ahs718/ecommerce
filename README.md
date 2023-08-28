# Ecommerce

This repository holds the source for for both an ecommerce admin panel/dashboard along with a frontend ecommerce store website.

View the store website [here!](https://ecommerce-store-ahs718.vercel.app/)

View the admin dashboard website [here!](https://ecommerce-admin-ahs718.vercel.app/)

## [Admin Dashboard](https://ecommerce-admin-ahs718.vercel.app/)

The ecommerce admin dashboard gives the user management access, as well as the ability to create/update/delete various properties:

-   Stores, which hold all of the below.
-   Categories for products.
-   Billboards, with customizable images and text assigned to each category.
-   Products, with customizable images, their price, and whether it is featured or archived.
-   Colors assigned to each product.
-   Sizes assigned to each product.

Below the tables holding the above information, API keys to retrieve the specific information are dynamically presented as the user navigates the table. For example, when on the products page, the API keys to fetch either a single product or multiple products for that specific store is displayed underneath the table.

Users also have access to view orders when users check out items from the frontend store, showcasing its payment status, as well as the user's phone number and address once the order is paid.

The ecommerce admin dashboard additionally includes the ability to toggle between light-mode and dark-mode.

## [Store](https://ecommerce-store-ahs718.vercel.app/)

The store section, displayed for customers, fetches the products from the database using the API key created through the admin dashboard. In the store section, users have the ability to:

-   View featured products on the home page.
-   View items by category via the navigation bar, which changes dynamically based on the categories added in the admin dashboard.
-   Filter products by size.
-   Filter products by color.
-   Go to an individual products page by clicking on the product card, showing an image gallery, price, and other suggested products.
-   Preview the product by clicking the expand button on the product card, also showing an image gallery, and price.
-   Add products to cart via the product page, product preview model, and the shopping cart button when hovering on the product cart, and save cart contents in local storage so the cart content is preserved upon page refresh.
-   Stripe payment integration (**only in test mode, not connected to any business account**) which allows users to checkout, and subsequently archives the items the user purchases.

Using the stripe payment integration, webhooks allow the admin dashboard listen for created orders and successfull checkouts to automatically create and update the order entries and display them on the admin dashboard.

## Tech Stack

### Frontend

-   [Next.js](https://nextjs.org/) - React framework
-   [TypeScript](https://www.typescriptlang.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [shadcn/ui](https://ui.shadcn.com/)

### Backend

-   [PlanetScale](https://planetscale.com/) - serverless MySQL database
-   [Prisma](https://www.prisma.io/) - ORM
-   [Clerk](https://clerk.com/) - user authentication
-   [Cloudinary](https://cloudinary.com/) - image uploads
