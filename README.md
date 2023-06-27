<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/m-romberg/pixly-backend">
  </a>

<h3 align="center">Pix.ly Backend</h3>
  <p align="center">
     Pix.ly is a RESTful API for images and their metadata, leveraging bucket storage in AWS for all image uploads. Can be used with 
     <a href="https://github.com/m-romberg/pixly-frontend">Pix.ly frontend</a> for a full image gallery and soon to be image editing platform.
    <br />
    <a href="https://github.com/m-romberg/pixly-backend"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://madelynromberg-pixly.surge.sh/">View Demo</a>
    ·
    <a href="https://github.com/m-romberg/pixly-backend/issues">Report Bug</a>
    ·
    <a href="https://github.com/m-romberg/pixly-backend/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
Pix.ly is a RESTful API for images and their metadata, leveraging bucket storage in AWS for all image uploads. Can be used with 
     <a href="https://github.com/m-romberg/pixly-frontend">Pix.ly frontend</a> for a full image gallery and soon to be image editing platform.
<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Flask][Flask]][Flask-url]
* ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
* ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started
To get a local copy up and running follow these simple example steps.

### Prerequisites
* python3
* postgresql
* aws

### Installation

1. Set up an AWS Bucket at [https://aws.amazon.com/s3/](https://aws.amazon.com/s3/)
2. Clone the repo
   ```sh
   git clone https://github.com/m-romberg/pixly-backend.git
   ```
3. Install pip3 packages
   ```sh
    python3 -m venv venv
    source venv/bin/activate
  
    pip3 install -r requirements.txt
    ```
4. Enter your AWS bucket in `app.py`
   ```python
   AWS_BUCKET_URL = "https://madelynromberg-pixly.s3.us-west-1.amazonaws.com"
   ```
5. Create database in postgresql
   ```sh
   psql createdb pixly
   ```
6. Change databse link in `app.py`
  ```python
    app.config['SQLALCHEMY_DATABASE_URI'] = os.environ.get(
    "DATABASE_URL", 'postgresql:///pixly')  # must link to db
  ```
7. Run seed.py
  ```sh
    python3 seed.py
  ```

8. Run app in shell
  ```
    flask run
  ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Please refer to the [Demo](https://madelynromberg-pixly.surge.sh)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->
## Roadmap

- [ ] Add photo editing feature using Pillow
- [ ] Allow users to revert edited photos


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Madelyn Romberg - - madelyn@madelynromberg.com

Project Link: [https://github.com/m-romberg/pixly-backend](https://github.com/m-romberg/pixly-backend)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Sarah Graup](https://github.com/sarahgraup)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo_name.svg?style=for-the-badge
[contributors-url]: https://github.com/m-romberg/pixly-backend/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/m-romberg/pixly-backend/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/m-romberg/pixly-backend/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/m-romberg/pixly-backend/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/m-romberg/pixly-backend/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/madelyn-romberg
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[Flask]: https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white
[Flask-url]: [[https://reactjs.org/](https://flask.palletsprojects.com/en/2.3.x/)](https://flask.palletsprojects.com/en/2.3.x/)
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
