# Example
This plugin will produce output for your gradle project similar to:

	:versions

	Dependency                                             Using              Update
	----------                                             -----              ------
	com.github.nwillc:almost-functional                    1.6.+ ->            1.7.7
	junit:junit                                             4.11
	org.assertj:assertj-core                               1.7.0
	com.h2database:h2                                    1.4.182
	com.github.nwillc:contracts                            1.6.2

It will show your what your dependency pattern is using, and if the pattern doesn't match the latest version it will suggest the update version.

## Updating build.gradle
To use this plugin you'll need to add the following apply:

	apply plugin: 'com.github.nwillc.vplugin'

And modify your buildscript entry as follows:

	buildscript {
	    repositories {
	           mavenCentral()
		}
		dependencies {
		        classpath 'com.github.nwillc:vplugin:1.+'
		}
	}

## Invoking the Task
To invoke the vplugin task simply:

	gradle versions
