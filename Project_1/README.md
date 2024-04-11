# Static Website Deployment to Amazon S3 using GitHub Actions

## Overview

In this project, we demonstrate how to automate the deployment process of a static website to Amazon S3 using GitHub Actions. The static website consists of HTML, CSS, and optionally JavaScript files. By leveraging GitHub Actions, we ensure that any changes pushed to the repository trigger an automated deployment pipeline, making the deployment process efficient and hassle-free.

## Project Structure

The project is organized as follows:

- `index.html`: The main HTML file containing the structure of the static website.
- `style.css`: The CSS file containing styles for the static website.
- `.github/workflows/deploy-to-s3.yml`: GitHub Actions workflow file responsible for deploying the website to Amazon S3.
- `README.md`: This README file providing an overview of the project and instructions for setting up and deploying the website.

## Setup Instructions

To deploy your static website to Amazon S3 using GitHub Actions, follow these steps:

1. Develop your static website: Modify the `index.html` and `style.css` files to customize your website's content and appearance.
2. Set up Amazon S3:
   - Create an S3 bucket to host your website.
   - Configure static website hosting in the bucket properties.
   - Set a bucket policy to allow public read access to the website files.
3. Configure GitHub repository secrets:
   - Generate AWS credentials in the IAM service of the AWS Management Console.
   - Add the AWS access key ID and secret access key as secrets in your GitHub repository settings.
4. Create GitHub Actions workflow:
   - Define a workflow file (`deploy-to-s3.yml`) in the `.github/workflows` directory of your repository.
   - Configure the workflow to sync your website files with the S3 bucket using the `s3-sync-action` action.
5. Push changes and trigger deployment:
   - Commit your changes to the repository.
   - Push the commit to GitHub to trigger the GitHub Actions workflow.
   - Monitor the workflow execution in the "Actions" tab of your GitHub repository.
   - Verify the deployment by accessing your website via the S3 bucket's website URL.

## Resources

- [AWS Management Console](https://aws.amazon.com/console/): Access the AWS Management Console to create and manage your S3 bucket and IAM users.
- [GitHub Actions](https://docs.github.com/en/actions): Learn more about GitHub Actions and how to automate your workflows.
- [jakejarvis/s3-sync-action](https://github.com/jakejarvis/s3-sync-action): GitHub Action used in this project for syncing files with an S3 bucket.

## License

This project is licensed under the [MIT License](LICENSE).
