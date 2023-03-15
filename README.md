There are 3 different use cases we have to support. The differences lie in the setting of liferay.workspace.modules.dir in the `gradle.properties`.

1. includesModulesDir ( liferay.workspace.modules.dir=modules )

With the given exclusion (liferay.workspace.modules.excludes.dir=analytics,blogs-test,my-test-sample2,my-test-sample5), these projects should build:
	my-test-sample4
2. includesNullDir ( #liferay.workspace.modules.dir || empty gradle.properties )
3. includesStarDir ( liferay.workspace.modules.dir=* )

With the given exclusion (liferay.workspace.modules.excludes.dir=analytics,blogs-test,my-test-sample2,my-test-sample5), these projects should build:
	my-test-project,my-test-sample1,my-test-sample3,blogs-api,blogs-service