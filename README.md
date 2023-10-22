# PalatePixels : Image-based Recipe Retrievel System

PalatePixels is a web application for recognizing Indian recipes from images and providing recipe details. The project is divided into three parts:

1. [Image Encoding](#image-encoding)
2. [Recipe Scraping](#recipe-scraping)
3. [Web Application](#web-application)

## Image Encoding

The Image Encoding part of the project uses a pre-trained DenseNet201 model to generate encodings for food images. The encodings are saved in a text file (`encodings.txt`) along with the names of the recipes in another text file (`enc_names.txt`).

To run the Image Encoding part, make sure to change the file paths for the image dataset before running the script. You can use the provided encodings to later recognize recipes from images.

## Recipe Scraping

The Recipe Scraping script is responsible for scraping detailed information about Indian recipes from websites. It includes the following steps:

- Reading recipe names and URLs from a CSV file (`links.csv`).
- Scraping recipe data, including name, cooking time, calories, ingredients, and directions.
- Downloading images related to the recipes and organizing them into directories.

The scraped data is saved in a JSON file (`indian_recipes.json`) for later use. Before running the script, ensure you have the necessary Python libraries installed and a valid dataset of Indian recipes.

## Web Application

The Web Application is a Django-based application that utilizes the encodings and scraped data to recognize recipes from user-uploaded images. It can also display detailed recipe information, including images, calories, cooking time, ingredients, and directions.

To use the Web Application:

1. Set up the Django environment in your preferred development environment.

2. Provide the necessary paths to the encodings text file (`encodings.txt`) and the JSON data file (`indian_recipes.json`) in the Web Application code.

3. Start the Django development server and access the web application in your browser at `http://localhost:8000`.

4. Upload an image containing an Indian recipe to the application.

5. The application will recognize the recipe and display its details.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



