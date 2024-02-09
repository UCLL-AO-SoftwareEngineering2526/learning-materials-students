# Frontend should call backend

## 1. Acceptance Criteria

After this story your frontend app on Azure should display information from your backend app on Azure.

## 2. Implementation Details

Currently, your frontend app on Azure will probably talk to your backend running on `localhost`. It goes without saying that this won't be very successful...

Configure Next.js in production by using a separate configuration for every environment: https://nextjs.org/docs/pages/building-your-application/configuring/environment-variables.

You'll also need to configure a production environment for the backend to set the correct CORS configuration. See the README file in the backend repository for more info on how to set the allowed hosts. Figure out which
environment variable you need to configure on Azure in
order to activate this profile.

## Epilogue

Congratulations! You have a fully working automated pipeline that takes your source code and publishes it to Azure.

There is a lot more that we could do:

* For example, the frontend app is calling the backend app over the internet. Since they are both running on Azure, the frontend could call the backend over a local network.
* Here is an article detailing a more robust setup on Azure: https://azure.github.io/AppService/2022/12/02/n-tier-web-app.html#create-staging-slots-and-configure-continuous-deployment
* We won't go that far, you will learn more about Azure in the cloud courses.
