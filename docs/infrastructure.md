> # Infrastructure

![infrastructure_diagram](./pictures/infrastructure_diagramm.png)

> > ## AWS

> > > ### RDS PostgreSQL Database

    DB-Instance-Name: `database-1`

    URL: `database-1.c75ep9wpacjf.us-east-1.rds.amazonaws.com`

    Port: `5432`

AWS RDS Database Service: Relational database to storing information data

> > > ### Elastic Beanstalk

    Env-Name: `udagram-api-dev`

    URL: `udagram-api-dev.eba-2scvhfru.us-east-1.elasticbeanstalk.com`

AWS Elastic Beanstalk Service: The server runs on Elastic Beanstalk and provide the API. Back-End API build files are stored on S3 Storage Service.

> > > ### S3 Buckets

**Mediastorage:**

    ARN: `mymediaawsbucket`

The mediastorage stores the media-files that are uploaded. The backend have a connection to this bucket.

**Frontend:**

    ARN: `ismkaya-udagram`

    URL: `http://udagram-ui-bucket-2022.s3-website-us-east-1.amazonaws.com `

The frontend build is hosted on a S3-Bucket that is publicitly reachable and configured for hosting static websites.

**Backend-Build-Storage:**

    ARN: `elasticbeanstalk-us-east-1-945862613618`

This S3-Bucket stores the backend builds. The builds are deployd with eb-cli via pipeline.
