SHELL := /bin/bash
.DEFAULT_GOAL := help

strawberry-debug: ## Open strawberry debug server. link: http://0.0.0.0:8000/graphql
	poetry run strawberry server app

# https://postd.cc/auto-documented-makefile/
help: ## Draw help message
	@grep -h -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'