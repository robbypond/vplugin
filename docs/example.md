# Example
This plugin will produce output for your gradle project similar to:

	:versions
	Searching repositories:
		MavenRepo at https://repo1.maven.org/maven2/
		BintrayJCenter at https://jcenter.bintray.com/
		maven at http://maven.tmatesoft.com/content/repositories/releases/

	Dependency                                             Using              Update
	----------                                             -----              ------
	com.github.nwillc:almost-functional                    1.6.+ ->            1.7.7
	junit:junit                                             4.11
	org.assertj:assertj-core                               1.7.0
	com.h2database:h2                                    1.4.182
	com.github.nwillc:contracts                            1.6.2

It will show you what your dependency pattern is using, and if the pattern doesn't match the latest version it will suggest the update version.

**NB:** Artifacts that release with oddball naming like adding *beta* or *rc* etc. may upset the order sort. 

## Invoking the Task
To invoke the vplugin task simply:

	gradle versions
