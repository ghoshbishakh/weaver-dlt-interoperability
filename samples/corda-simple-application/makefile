.PHONY: build-local
build-local:
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew clean installDist jar

.PHONY: build-refresh-dependencies-local
build-refresh-dependencies-local:
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew clean build --refresh-dependencies

.PHONY: build-cordapp-local
build-cordapp:-local 
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew jar

.PHONY: build-cli-local
build-cli-local:
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew installDist

.PHONY: test-local
test-local:
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew test

.PHONY: build
build:
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew clean installDist jar

.PHONY: build-refresh-dependencies
build-refresh-dependencies:
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew clean build --refresh-dependencies

.PHONY: build-cordapp
build-cordapp: 
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew jar

.PHONY: build-cli
build-cli:
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew installDist

.PHONY: test
test:
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew test

.PHONY: initialise-vault
initialise-vault:
	./scripts/initialise-vault.sh

.PHONY: initialise-vault-docker
initialise-vault-docker:
	./scripts/initialise-vault-docker.sh

.PHONY: get-access-control-policies
get-access-control-policies:
	./clients/build/install/clients/bin/clients get-access-control-policies

.PHONY: get-verification-policies
get-verification-policies:
	./clients/build/install/clients/bin/clients get-verification-policies

.PHONY: get-security-groups
get-security-groups:
	./clients/build/install/clients/bin/clients get-security-groups

.PHONY: publish-cordapps
publish-cordapps:
	echo "Publishing CorDapps to Artifactory..."
	./gradlew publishContractsPublicationToMavenRepository
	./gradlew publishWorkflowsPublicationToMavenRepository

.PHONY: clean-local
clean-local:
	cp clients/build.gradle.local clients/build.gradle
	cp contracts-kotlin/build.gradle.local contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.local workflows-kotlin/build.gradle
	./gradlew clean

.PHONY: clean
clean:
	cp clients/build.gradle.remote clients/build.gradle
	cp contracts-kotlin/build.gradle.remote contracts-kotlin/build.gradle
	cp workflows-kotlin/build.gradle.remote workflows-kotlin/build.gradle
	./gradlew clean
