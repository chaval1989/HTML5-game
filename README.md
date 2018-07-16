# HTML5-game
Simple HTML5 game
I want to make some front end changes to this repository

Deploy Backend Instructions
git repository: http://stash.denovolab.com/projects/ELG/repos/backend/browse

Requrements
=============
- php >=5.6
- composer
- npm

Install
=============

- clone project `git clone http://puhach@stash.denovolab.com/scm/elg/backend.git your_directory`
- copy `.env.example` rename it to `.env` and set your configuration
- run command `composer install`
- set `777` permissions for directories `storage` and `bootstrap/cache`
- run command `php artisan key:generate`
- run command `php artisan migrate --seed` (database must be already exists and that host, db-name, user-name and password must be included in `.env` file)
- in file `comparison.sh` change absolute path to your absolute path for directory `detect_align_voice`
- run command `npm install`
- run command `npm run prod`
