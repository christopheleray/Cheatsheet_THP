# CheatSheet about [heroku](https://heroku.com)

## How to install Heroku: 

[](https://devcenter.heroku.com/articles/heroku-cli)
[](https://devcenter.heroku.com/articles/getting-started-with-rails5)

*heroku version:*

` $ heroku --version `

*Create app:*

`$ heroku create`

*herolku login:* 

`$ heroku login`

*CLI Plugin:*

` $ heroku plugins:install someplugin`

*Heroku update: *

`$ heroku update`

*Uninstall Heroku:*

` $ brew uninstall heroku `

*Add an ssh key:* 
` $ heroku keys:add ` 

*To find out where the executable is located, run which:*

`$ which heroku`

--------
## How to uplaod an Rails app: 

####First create the app  in your favorite folder

*App with sqlite DB:* 

` $ rails new nom_de_ta_super_app *`

*App with postrges DB:*
` $  'rails new -d postgresql'`

*App without DBwithout Activerecord:*

` $  rails new myApp --skip-active-record` 

## How to create/manage Heorku app: 

*Create your app:*

` $ heroku create mon-nom-de-super-app`

*how to rename the app*

` $ heroku apps:rename nouveau-nom-de-ton-app `

then add the file to your git, commit, and push to heroku: 

` $ git push heroku master`

*IMPORTANT: migrate your DB if you have any DB:* 

`$ heroku run rails db:migrate`

*open the app:*

` $ heroku open`

*herocu logs:*

`$ heroku logs`

` $ heroku logs --tail`

*Access to the app in console:*

`$ heroku run rails console`

-------------------

##Update your Gemfile if Sqlite DB:*
```ruby 
gem 'sqlite3'
et remplace la par :
group :development, :test do
  gem 'sqlite3'
end 

group :production do
  gem 'pg'
end
```

*then Install bundle without production gems:*

` $ bundle install --without production`

## If postregss, make sure to create the DB first

` $ rails db:create`

` $ rails db:migrate`

------

Others documentation:

[Add production key in production Heroku way](https://devcenter.heroku.com/articles/config-vars#setting-up-config-vars-for-a-deployed-application)

[Add production key in production the best way](https://www.viget.com/articles/storing-secret-credentials-in-rails-5-2-and-up/)



