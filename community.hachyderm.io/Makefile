default: help

.PHONY: hugo
hugo: ## Build the hugo site for CI
	npm ci
	npm run build:production

.PHONY: dev
dev: ## Run the local server
	npm ci
	npm run build

.PHONY: issues
issues: ## Find all the FIXMEs
	grep -ri "FIXME" content/en

.PHONY: fixme
fixme: issues

.PHONY: drafts
drafts: ## Find all the drafts
	find "content/en" -type f -name "*.draft"

.PHONY: help
help:  ## 🤔 Show help messages for make targets
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[32m%-30s\033[0m %s\n", $$1, $$2}'
