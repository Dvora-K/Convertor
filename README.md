# Image to PDF Converter

A Python script that converts images (JPEG format) to a PDF file.

## Features
- Convert a single image to PDF
- Convert all images in a directory to a single PDF
- Dockerized for easy setup and usage

## Installation

### Clone the Repository
```bash
git clone https://github.com/Dvora-K/Convertor.git
cd Convertor
```
#### Build the Docker Image
Replace `IMAGE_NAME` with your desired image name.
```bash
docker build -t IMAGE_NAME .
```

#### Run the Docker Container
Replace `CONTAINER_NAME` with your desired container name, `YOUR_PDF` with the desired PDF output name, and `IMAGE_NAME` with the name of your Docker image.
```bash
docker run --name CONTAINER_NAME -v $PWD/images:/app/images -v $PWD/output:/app/output --rm -e PDF_NAME=YOUR_PDF IMAGE_NAME /app/images
```

## Environment Variables
- `PDF_NAME`: The name of the output PDF file (default is `output.pdf`)

## Example

### Directory Structure
Assume you have the following directory structure:
```
/my_project
    /images
        image1.jpg
        image2.jpg
        ...
    /output
```

### Running the Script
```bash
docker run --name my_converter -v $PWD/images:/app/images -v $PWD/output:/app/output --rm -e PDF_NAME=my_images_pdf my_image_name /app/images
```
This will generate `my_images_pdf.pdf` in the `output` directory.
