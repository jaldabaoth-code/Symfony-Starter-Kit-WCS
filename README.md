<h1>Symfony Starter Kit WCS (Starter Kit - Symfony 5.*, WCS Web PHP)</h1>

### Starter Kit - Symfony 5.* created by WCS, we used for "Project 3" and "Hackathon"


---

## Starter Kit - Symfony 5.*

This repo contains <b>Starter Kit - Symfony 5.*</b> with <b>GrumPHP</b> we used on <b>Project 3 of WCS</b>.

![Wild Code School](https://wildcodeschool.fr/wp-content/uploads/2019/01/logo_pink_176x60.png)

This starter kit is here to easily start a repository for your students.

It's symfony website-skeleton project with some additional tools to validate code standards.

* GrumPHP, as pre-commit hook, will run 2 tools when `git commit` is run :
  
    * PHP_CodeSniffer to check PSR12 
    * PHPStan focuses on finding errors in your code (without actually running it)
    * PHPmd will check if you follow PHP best practices
     
  If tests fail, the commit is canceled and a warning message is displayed to developper.

* Github Action as Continuous Integration will be run when a branch with active pull request is updated on github. It will run :

    * Tasks to check if vendor, .idea, env.local are not versionned,
    * PHP_CodeSniffer, PHPStan and PHPmd with same configuration as GrumPHP.
 

#### Trainers instructions

1. Add your students team as contributor .
2. Disallow both on 'dev' and 'master' branches your students writing credentials. 
3. Disallow merge available while one approbation is not submitted on PR.

> You can watch this very tiny short video : (Loom : verrouillage branches GitHub)[https://www.loom.com/share/ad0c641d0b9447be9e40fa38a499953b]
4. For deploying on caprover : add two repository secrets (settings -> secrets)
    - CAPROVER_APP_NAME with the caprover app name as value
    - CAPROVER_PASSWORD with the caprover password

### Getting Started for Students

#### Prerequisites

1. Check composer is installed
2. Check yarn & node are installed

#### Install

1. Clone this project
2. Run `composer install`
3. Run `yarn install`
4. Run `yarn encore dev` to build assets

#### Working

1. Run `symfony server:start` to launch your local php web server
2. Run `yarn run dev --watch` to launch your local server for assets

#### Testing

1. Run `.vendor/bin/phpcs` to launch PHP code sniffer
2. Run `.vendor/bin/phpstan analyse src --level max` to launch PHPStan
3. Run `.vendor/bin/phpmd src text phpmd.xml` to launch PHP Mess Detector
3. Run `./node_modules/.bin/eslint assets/js` to launch ESLint JS linter
3. Run `../node_modules/.bin/sass-lint -c sass-linter.yml -v` to launch Sass-lint SASS/CSS linter

#### Windows Users

If you develop on Windows, you should edit you git configuration to change your end of line rules with this command :

`git config --global core.autocrlf true`

### Deployment

![Img caprover](https://captain.phprover.wilders.dev/icon-512x512.png)

To deploy on Cap Rover, follow [instructions in the manual](https://caprover.com/docs/get-started.html) and add, at least, two  *"Environmental Variables"* in *"App Configs"*  tab:

* `APP_ENV` with `prod`/`dev` value
* `DATABASE_URL` with the connection informations given by caprover when you create the related DB app.

Caprover configuration files are : 

* [captain-definition](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/captain-definition) Caprover entry point
* [Dockerfile](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/Dockerfile) Web app configuration for Docker container
* [docker-compose.yml](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-compose.yml) ...not use it's used 😅
* [docker-entry.sh](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/docker-entry.sh) shell instruction to execute when docker image is built
* [nginx.conf](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/nginx.conf) Nginx server configuration
* [php.ini](https://github.com/WildCodeSchool/sf4-pjt3-starter-kit/blob/master/php.ini) Php configuration



### Built With

* [Symfony](https://github.com/symfony/symfony)
* [GrumPHP](https://github.com/phpro/grumphp)
* [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)
* [PHPStan](https://github.com/phpstan/phpstan)
* [PHPMD](http://phpmd.org)
* [ESLint](https://eslint.org/)
* [Sass-Lint](https://github.com/sasstools/sass-lint)

### Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

### Versioning


### Authors

Wild Code School trainers team

### License

MIT License

Copyright (c) 2019 aurelien@wildcodeschool.fr

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Acknowledgments

---

## The Links

<a href="https://github.com/WildCodeSchool/orleans_0321_hackathon">Link to the repository of <b>Starter Kit WCS Web</b></a>
