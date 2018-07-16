# HTML5-game
Simple HTML5 game
I want to make some front end changes to this repository

Deploy Backend Instructions

git repository: http://stash.denovolab.com/projects/ELG/repos/backend/browse

Requirements
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

Deploy Frontend instructions

DescriptionEdit
git repository: http://stash.denovolab.com/projects/ELG/repos/h5-game/browse

Install
clone project git clone http://puhach@stash.denovolab.com/scm/elg/h5-game.git some_work_directory
run command npm install
for dev:
set up your backend url in config/dev.env.js
run command npm run dev
site available on http://localhost:8080
for prod:
set up your backend url in config/prod.env.js
run command npm run build
copy all from dist directory to your public site directory
Langs
Change exists language translations:
change src/lang/**.js file
run command npm run build
copy all from dist directory to your public site directory
Add new language translations (Italian for example)
create file it.js in src/lang/ directory and add your translations. (loock on exists files for example)
import new translation file in src/lang/translations.js and add it to exported object. Example:
import en from './en';
import ch from './cn';
import ru from './ru';
import it from './it';

export default {
    en, cn, ru, it
}
add image with country flag and named like it.png to src/assets/images/icons/lang dirrectory
run command npm run build
copy all from dist directory to your public site directory
Lessons
For adding or deleting lessons do to your_backend_url/lessons
