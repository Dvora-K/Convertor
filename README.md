# convertor
A script that converts from an image to a PDF file

## DOWNLOAD
    git clone https://github.com/Dvora-K/Exam.git
## BUILD

you can insert image name from you to IMAGE_NAME
    
    docker build -t IMAGE_NAME .
## RUN
    docker run --name CONTAINER_NAME -v $PWD/images:/app/images -v $PWD/output:/app/output --rm -e PDF_NAME=YOUR_PDF IMAGE_NAME images
