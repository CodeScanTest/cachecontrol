## Releasing

This is released from the `master` branch from `2.0.1` forward. Unless an older version needs patching, then it must be released from the maintenance branch, for instance `2.0.x` branch. If there is no maintenance branch for the release that needs patching, create it from the tag.

## Cutting the release

### Requires contributor access

- Check the [draft release notes](https://github.com/playframework/cachecontrol/releases) to see if everything is there
- Wait until [master build finished](https://travis-ci.com/github/playframework/cachecontrol/builds) after merging the last PR
- Update the [draft release](https://github.com/playframework/cachecontrol/releases) with the next tag version (eg. `2.2.0`), title and release description
- Check that Travis CI release build has executed successfully (Travis will start a [CI build](https://travis-ci.com/github/playframework/cachecontrol/builds) for the new tag and publish artifacts to Bintray)

### Requires Bintray access

- Go to [Bintray](https://bintray.com/playframework/maven/cachecontrol) and select the just released version
- Go to the Maven Central tab and sync with Sonatype (using your Sonatype TOKEN key and password) (you may watch progress in the [Staging repository](https://oss.sonatype.org/#stagingRepositories))

### Check Maven Central

- The artifacts will become visible at https://repo1.maven.org/maven2/com/typesafe/play/ 
