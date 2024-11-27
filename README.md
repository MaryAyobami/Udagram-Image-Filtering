
# Udagram Image Filtering Application

This project provides a Node.js-based application that allows users to filter images by applying simple filters. It is part of the Udacity Cloud Engineering Nanodegree and serves as an image-processing service for the Udagram cloud application.

## Features

- Allows users to upload images and apply filters.
- Exposes a RESTful API for image processing.
- Can be deployed using AWS Elastic Beanstalk.

## Setup Instructions

### Prerequisites

- Node.js and npm installed on your system.

### 1. Install Dependencies

In the project directory, run:

```bash
npm install
```

### 2. Run the Development Server

To start the server locally, run:

```bash
npm run dev
```

The server will be running at `http://localhost:8082` by default.

### 3. Image Filtering Endpoint

The microservice exposes an endpoint that allows you to filter images. To use it, make a request to:

```
GET /filteredimage?image_url={URL}
```

Where `{URL}` is the public URL of the image you want to filter.

The microservice will:
- Download the image from the provided URL.
- Apply a filter to the image.
- Return the filtered image.

### 4. Deploying to AWS

To deploy this microservice to AWS, follow these steps:

1. Initialize Elastic Beanstalk for the project:

   ```bash
   eb init
   ```

2. Create a new environment:

   ```bash
   eb create
   ```

3. Deploy your service:

   ```bash
   eb deploy
   ```
