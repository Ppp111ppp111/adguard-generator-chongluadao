# AdGuard Generator for ChongLuaDao

This project automates the process of fetching and processing blacklist and whitelist URLs from the [ChongLuaDao API](https://api.chongluadao.vn/) and saves the results either locally or uploads them to a GitHub repository.

## Features

- Fetches blacklist and whitelist URLs from the ChongLuaDao API.
- Cleans and formats URLs.
- Saves the formatted list to local files (`blacklist.txt` and `whitelist.txt`).
- Automatically uploads the generated files to a GitHub repository (if a GitHub token is provided).

## Project Structure

The core of the project is defined in `index.js`, which consists of the following main functionalities:

- **Fetching Data**: Using the `undici` library's `Pool` to fetch data from the ChongLuaDao API.
- **Processing URLs**: Clean and format URLs, removing unwanted patterns.
- **Saving Data**: Save the processed lists to local files or upload them to a GitHub repository.

## Prerequisites

- Node.js (v14 or higher)
- A `.env` file with a GitHub token (if uploading to GitHub)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/your-repository/adguard-generator-chongluadao.git




2.Navigate to the project folder:

cd adguard-generator-chongluadao

3.Install dependencies:

npm install

4.Create a .env file in the root directory and add your GitHub token:

GH_TOKEN=your_github_token_here

5.Usage,  Run the project using Node.js:
  
node index.js

6.Explanation of Main Functions
getList(type):

Makes a GET request to the ChongLuaDao API for the given type (blacklist or whitelist).
Formats the returned URLs by removing unnecessary prefixes and symbols.
Filters out URLs that contain facebook and youtube.
saveList(fileName, list):

Saves the processed list of URLs either to a local file or uploads them to GitHub.
uploadToGithub(fileName, content):

Uploads the generated list to a GitHub repository.
Ensures that only modified content is uploaded.

7.Environment Variables:
GH_TOKEN: (Optional) GitHub personal access token for authenticating GitHub API requests. If this token is not set, the list will be saved locally instead of being uploaded to GitHub.

8.Dependencies
undici: An HTTP/1.1 client for Node.js.
dotenv: Loads environment variables from a .env file.

9.License
This project is licensed under the MIT License.


