ISSUE1: Bootstrap not loading FIX: https://laracasts.com/discuss/channels/laravel/error-in-node-modulesbootstrapdistjsbootstrapesmjs-60-41

admin:~/environment/ruby-gems-bootcamp (main) $ rails s
-----------------------------------------------------------------------------------------------------------------------------------------
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
=> Booting Puma
=> Rails 6.1.4.1 application starting in development 
=> Run `bin/rails server --help` for more startup options
Puma starting in single mode...
* Puma version: 5.5.0 (ruby 2.7.2-p137) ("Zawgyi")
*  Min threads: 5
*  Max threads: 5
*  Environment: development
*          PID: 4072
* Listening on http://127.0.0.1:8080
* Listening on http://[::1]:8080
Use Ctrl-C to stop

Started GET "/" for 220.253.67.85 at 2021-09-29 09:41:22 +0000
Cannot render console from 220.253.67.85! Allowed networks: 127.0.0.0/127.255.255.255, ::1
Processing by StaticPagesController#landing_page as HTML
  Rendering layout layouts/application.html.erb
  Rendering static_pages/landing_page.html.erb within layouts/application
  Rendered static_pages/landing_page.html.erb within layouts/application (Duration: 2.5ms | Allocations: 285)
[Webpacker] Compiling...
[Webpacker] Compilation failed: <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
Hash: a6da3f63819e8d4c052c
Version: webpack 4.46.0
Time: 6073ms
Built at: 09/29/2021 9:41:31 AM
                                     Asset       Size       Chunks                         Chunk Names
    js/application-3c3d04c1e687d9831550.js   1.33 MiB  application  [emitted] [immutable]  application
js/application-3c3d04c1e687d9831550.js.map   1.47 MiB  application  [emitted] [dev]        application
                             manifest.json  364 bytes               [emitted]              
Entrypoint application = js/application-3c3d04c1e687d9831550.js js/application-3c3d04c1e687d9831550.js.map
[./app/javascript/channels sync recursive _channel\.js$] ./app/javascript/channels sync _channel\.js$ 160 bytes {application} [built]
[./app/javascript/channels/index.js] 211 bytes {application} [built]
[./app/javascript/packs/application.js] 611 bytes {application} [built]
[./app/javascript/stylesheets/application.scss] 664 bytes {application} [built]
[./node_modules/css-loader/dist/cjs.js?!./node_modules/postcss-loader/src/index.js?!./node_modules/sass-loader/dist/cjs.js?!./app/javascript/stylesheets/application.scss] ./node_modules/css-loader/dist/cjs.js??ref--6-1!./node_modules/postcss-loader/src??ref--6-2!./node_modules/sass-loader/dist/cjs.js??ref--6-3!./app/javascript/stylesheets/application.scss 315 bytes {application} [built]
[./node_modules/webpack/buildin/module.js] (webpack)/buildin/module.js 552 bytes {application} [built]
    + 9 hidden modules

---------------------------------------------------------------------------------------------------------------------------------------
ERROR in ./node_modules/bootstrap/dist/js/bootstrap.js
Module not found: Error: Can't resolve '@popperjs/core' in '/home/ubuntu/environment/ruby-gems-bootcamp/node_modules/bootstrap/dist/js'
----------------------------------------------------------------------------------------------------------------------------------------
 @ ./node_modules/bootstrap/dist/js/bootstrap.js 59:141-166 59:215-250
 @ ./app/javascript/packs/application.js


warning ../../package.json: No license field

  Rendered layout layouts/application.html.erb (Duration: 9439.4ms | Allocations: 6009)
Completed 200 OK in 9462ms (Views: 9448.9ms | ActiveRecord: 0.0ms | Allocations: 8568)


^C- Gracefully stopping, waiting for requests to finish
=== puma shutdown: 2021-09-29 09:46:35 +0000 ===
- Goodbye!
Exiting
admin:~/environment/ruby-gems-bootcamp (main) $ npm i @popperjs/core <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<FIX
npm WARN old lockfile 
npm WARN old lockfile The package-lock.json file was created with an old version of npm,
npm WARN old lockfile so supplemental metadata must be fetched from the registry.
npm WARN old lockfile 
npm WARN old lockfile This is a one-time fix-up, please be patient...
npm WARN old lockfile 

added 1 package, changed 2 packages, and audited 995 packages in 1m

74 packages are looking for funding
  run `npm fund` for details

7 moderate severity vulnerabilities

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
npm notice 
npm notice New minor version of npm available! 7.21.1 -> 7.24.1
npm notice Changelog: https://github.com/npm/cli/releases/tag/v7.24.1
npm notice Run npm install -g npm@7.24.1 to update!
npm notice 
admin:~/environment/ruby-gems-bootcamp (main) $ rails s
The dependency tzinfo-data (>= 0) will be unused by any of the platforms Bundler is installing for. Bundler is installing for ruby but the dependency is only for x86-mingw32, x86-mswin32, x64-mingw32, java. To add those platforms to the bundle, run `bundle lock --add-platform x86-mingw32 x86-mswin32 x64-mingw32 java`.
=> Booting Puma
=> Rails 6.1.4.1 application starting in development 
=> Run `bin/rails server --help` for more startup options
Puma starting in single mode...
* Puma version: 5.5.0 (ruby 2.7.2-p137) ("Zawgyi")
*  Min threads: 5
*  Max threads: 5
*  Environment: development
*          PID: 4666
* Listening on http://127.0.0.1:8080
* Listening on http://[::1]:8080
Use Ctrl-C to stop




Started GET "/" for 220.253.67.85 at 2021-09-29 09:49:47 +0000
Cannot render console from 220.253.67.85! Allowed networks: 127.0.0.0/127.255.255.255, ::1
Processing by StaticPagesController#landing_page as HTML
  Rendering layout layouts/application.html.erb
  Rendering static_pages/landing_page.html.erb within layouts/application
  Rendered static_pages/landing_page.html.erb within layouts/application (Duration: 3.6ms | Allocations: 285)
[Webpacker] Compiling...


[Webpacker] Compiled all packs in /home/ubuntu/environment/ruby-gems-bootcamp/public/packs <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
[Webpacker] warning ../../package.json: No license field

[Webpacker] Hash: 33ed3a8073289a3a4acf
Version: webpack 4.46.0
Time: 7460ms
Built at: 09/29/2021 9:49:58 AM
                                     Asset       Size       Chunks                         Chunk Names
    js/application-641a19ce7ef4cb7b45ce.js   1.49 MiB  application  [emitted] [immutable]  application
js/application-641a19ce7ef4cb7b45ce.js.map   1.56 MiB  application  [emitted] [dev]        application
                             manifest.json  364 bytes               [emitted]              
Entrypoint application = js/application-641a19ce7ef4cb7b45ce.js js/application-641a19ce7ef4cb7b45ce.js.map
[./app/javascript/channels sync recursive _channel\.js$] ./app/javascript/channels sync _channel\.js$ 160 bytes {application} [built]
[./app/javascript/channels/index.js] 211 bytes {application} [built]
[./app/javascript/packs/application.js] 611 bytes {application} [built]
[./app/javascript/stylesheets/application.scss] 664 bytes {application} [built]
[./node_modules/css-loader/dist/cjs.js?!./node_modules/postcss-loader/src/index.js?!./node_modules/sass-loader/dist/cjs.js?!./app/javascript/stylesheets/application.scss] ./node_modules/css-loader/dist/cjs.js??ref--6-1!./node_modules/postcss-loader/src??ref--6-2!./node_modules/sass-loader/dist/cjs.js??ref--6-3!./app/javascript/stylesheets/application.scss 315 bytes {application} [built]
[./node_modules/webpack/buildin/module.js] (webpack)/buildin/module.js 552 bytes {application} [built]
    + 67 hidden modules

  Rendered layout layouts/application.html.erb (Duration: 10943.3ms | Allocations: 6103)
Completed 200 OK in 10967ms (Views: 10951.6ms | ActiveRecord: 0.0ms | Allocations: 8663)


Started GET "/privacy_policy" for 220.253.67.85 at 2021-09-29 09:50:01 +0000
Cannot render console from 220.253.67.85! Allowed networks: 127.0.0.0/127.255.255.255, ::1
Processing by StaticPagesController#privacy_policy as HTML
  Rendering layout layouts/application.html.erb
  Rendering static_pages/privacy_policy.html.erb within layouts/application
  Rendered static_pages/privacy_policy.html.erb within layouts/application (Duration: 1.4ms | Allocations: 151)
[Webpacker] Everything's up-to-date. Nothing to do
  Rendered layout layouts/application.html.erb (Duration: 22.1ms | Allocations: 3028)
Completed 200 OK in 27ms (Views: 26.5ms | ActiveRecord: 0.0ms | Allocations: 3529
