# History

## 0.3.1
* Update `grunt-lib-phantomjs` to 0.3.0

## 0.3.0
* You may now specify which reporter you want to use (thanks SBoudrias)
* Growl only shows notices on failures

```js
sampleTest: {
    src: ['test.js'],
    options: {
        reporter: 'Nyan'
        mocha: {
            ui: 'tdd'
        }
    }
}
```

## 0.2.2
* Updating grunt/gruntplugin dependencies to rc6.
* Added travis.yml
* Added .jshintrc and jshint to Gruntfile.js
* Migrated documentation and Gruntfile.js to grunt-contrib standards

## 0.2.0
* **Grunt >=0.4.0 only, MIGRATION REQUIRED if updating from 0.1.x**
* Uses grunt-lib-phantomjs for easy PhantomJS installation!
* If things are not working right, try removing and installing via npm again.
* Config changes required
    * `tasks/mocha/mocha-helper.js` has been moved to `phantomjs/bridge.js`, if you are including it manually, you must change the path/filename
    * Task options are now nested in the `options` key per task/target

```js
all: {
    src: ['test.js'],
    options: {
        mocha: {
            ui: 'tdd'
        },
        run: true
    }
}
```

## 0.1.7
* Fix bad legacy mocha check for mocha < 1.4.2 (rohni)

## 0.1.6
* Add ability to pass mocha config options (grep, etc) via grunt task config. (gamtiq)
* Add option to not include `mocha-spec-helper.js` and auto-inject/run with the `run` config option. Note: Still not required for AMD. This requires an if-statement in your HTML spec to check for PhantomJS environment, it's either that or include the helper. See `example/test2.html`. (gamtiq)

## 0.1.5
* Fix total duration when testing multiple html spec files in a single task. (chevalric)

## 0.1.4
* **Critical fix:** Compatibility with Mocha 1.4.2 (iammerick)
    * If you use `mocha-helper.js` for non-AMD and you want to use Mocha >1.4.2, you replace it with the one in this update.

## 0.1.3
* Remove grunt from deps

## 0.1.2
* Added example for non-AMD usage. Modified mocha-helper to be included in page (optional)
* Added duration

## 0.1.1

* Consistency
* Make growl optional

## 0.1.0

init