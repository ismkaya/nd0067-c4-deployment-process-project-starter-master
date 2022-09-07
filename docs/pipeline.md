> # CircleCI Pipeline Process

> > ## Trigger

To start the deployment process, push new commits into the `master`-branch from the GitHub Repo that is linked with CircleCI.

> > ## Build Process Steps

> > > ### Install

-   Installing Node on system
-   Installing the front-end and then the back-end dependencies

> > > ### Lint

-   Lint the front-end code

> > > ### Build

-   Runs the build script for the front-end and then the back-end

> > ## Manual Approval

After the build is successfully done, the pipeline holds the process and waits for manual approval.

The deployment process ends till the build process completed successfully.

> > ## Deployment Process Steps

> > > ### Install

-   Installing Node on system
-   Installing and setup eb-cli & aws-cli

> > > ### Deploy

-   Deploy the back-end
    -   Installing dependencies
    -   Build
    -   Set environment variables
    -   Deploy with eb-cli
-   Deploy the front-end
    -   Installing dependencies
    -   Build
    -   deploy with aws-cli

> > ## Workflow

1. Build
2. Manual approval after successful completed building process
3. Deploy
