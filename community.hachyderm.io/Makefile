default: help

hugo: ## Build the hugo site for CI
	npm install postcss-cli
	hugo --minify

submodule: ## Build the git submodule
	git submodule update --init --recursive

dev: submodule ## Run the local server
	hugo serve . --bind=0.0.0.0

issues: ## Find all the FIXMEs
	grep -ri "FIXME" content/en

fixme: issues

drafts: ## Find all the drafts
	find "content/en" -type f -name "*.draft"

.PHONY: help
help:  ## 🤔 Show help messages for make targets
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[32m%-30s\033[0m %s\n", $$1, $$2}'
