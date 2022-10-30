# Kaggle output downloader

<img src="https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white">
<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
<img src="https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white">

## Introduction

[Kaggle](http://kaggle.com/) is a platform for build machine learning notebooks. It can be seen that people has used it to crawl data from websites, and scheduled it to run repeatly (e.g. daily, weekly). 

However, the [Kaggle API](https://github.com/Kaggle/kaggle-api) only has the API to download the latest output (not by versions). If the notebooks scheduled to run daily, download these output manually may require a huge cost. Because of that reason, this repository propose a tool to automatically fetch all the version of a Kaggle kernel (notebook).

## Usage

Run the script as following:

```bash
python src/kaggle-downloader.py \
    -u <username> \
    -e <email> \
    -p <password> \
    -n <notebook>
```

Furthermore, you can provide the user's information with a file named `credential.json` with the following format:
```json
{
    "username": "<username>",
    "password": "<password>",
    "email": "<email>",
}
```

Then, easily call the source as follow:
```bash
python src/kaggle-downloader.py \
    -c <credential_path>
    -n <notebook>
```

## Contribution

This repository is owned by [phuc16102001](https://github.com/phuc16102001).

You are welcome to pull request, but please discuss with me for major changes.

## License

[MIT](https://choosealicense.com/licenses/mit/)
