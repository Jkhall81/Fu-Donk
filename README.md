# Fu Donk Task Manager

This is a fullstack application build with Next.js, Tailwind CSS, typescript, Clerk (Nextjs Auth), Prisma, Shadcn/UI, Zustand, Lodash, Zod, and a few other javascript / typescript packages. This site allows users to create an organization, create boards, create lists within those boards, and within each list to create tasks. The board features background images supplied by the unsplash API, and within a board there is drag and drop functionality to be able to move around tasks within or between lists. Users can create an account via an email address, or log in with a google or github account, courtesy of clerk.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Getting Started](#getting-started)
- [Frontend](#frontend)
- [Backend](#backend)
- [Deployment](#deployment)
- [Testing](#testing)
- [Bugs](#bugs)
- [License](#license)

## Features

This site has stripe payment functionality built in. Stripe is currently in test mode on the project. Users can purchase a subscription, to create more than 5 boards, or manage a current subscription via the built in stripe portal. Users can register and log in via credentials or a github or google account. Once logged in, users can create organizations, invite other users via email, and create boards, lists, and tasks. Once inside a board there is drag and drop functionality, via hello-pangea/dnd, to move tasks and lists around the board. Items within a board can be copied, deleted, or renamed. There is also an activity log that shows a history changes made to a board, complete with times and an avatar picture of the user that made the specific change. When creating a board images from unsplash can be selected for the background, when hovering on an image you can see the name of the photographer that produced the image, and visit the photographer's unsplash page via a link.

## Technologies

- Frontend

  - Next.js
  - Tailwind CSS
  - Shadcn/UI

- Backend
  - Prisma
  - PostgreSQL Database

## Getting Started

The Project code can be found here: https://github.com/Jkhall81/Fu-Donk. In production I used a mySQL database in a docker container. The docker-compose.yml that I used is included in the repo. To use it you just need to modify the prisma schema. Also the project does not include an .env file with all the environment variables that the project needs to run.

Below is a list of all the environment variables that I used to make the application run:
NEXT_PUBLIC_APP_URL
STRIPE_WEBHOOK_SECRET
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY
CLERK_SECRET_KEY
NEXT_PUBLIC_CLERK_SIGN_IN_URL
NEXT_PUBLIC_CLERK_SIGN_UP_URL
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL
NEXT_PUBLIC_UNSPLASH_ACCESS_KEY
STRIPE_API_KEY
POSTGRES_URL
POSTGRES_PRISMA_URL
POSTGRES_URL_NO_SSL
POSTGRES_URL_NON_POOLING
POSTGRES_USER
POSTGRES_HOST
POSTGRES_PASSWORD
POSTGRES_DATABASE

To get these you would need a stripe, clerk, and unsplash developer account. Also database variables will vary depending on what service you use.

## Frontend

This project's front end was created using Next.js and Tailwind CSS.

fu-donk.vercel.app

## Backend

The backend is made up of the ORM Prisma, and a PostgreSQL database hosted by Vercel.

## Deployment

Everything for this application is hosted on Vercel.

## Testing

Work in progress.

## Bugs

Seems to be bug free as of now. Thank you TypeScript!

## License

This project use an MIT license.
