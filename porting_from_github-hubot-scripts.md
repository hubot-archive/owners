# How to port from github.com/github/hubot-scripts

So you want to help out moving from https://github.com/github/hubot-scripts/ to
a new repo in the https://github.com/hubot-scripts org. This is great, but there's
a couple things we need to standardize for the port so we don't miss anything.

- First, make sure you've created the repo in the correct location, you should
have used [this](https://github.com/organizations/hubot-scripts/repositories/new) link
to make it.

- We have standardized on `hubot-<name-of-script>`, as the repo and npm name.

- We have also standardized on the [hubot-example](https://github.com/hubot-scripts/hubot-example) directory
structure, so please put that in the repo you've created.

- Go ahead and put the script from the original `src/scripts` directory, into the new `src/` directory.

- We have decided to add a WARNING to the script to the original `src/scripts` to say we've moved the script,
here's a template, please put the warning right after the `module.exports`.

```json
module.exports = (robot) ->

 robot.logger.warning "new-awesome-script.coffee has moved from hubot-scripts to its own package. See https://github.com/hubot-scripts/hubot-new-awesome-script installation instructions"
```

- Go ahead and put in a PR to the original repo saying you've ported the repo with the warning, you should be good done! :metal:
