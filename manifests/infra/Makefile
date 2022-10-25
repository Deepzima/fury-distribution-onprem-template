define check
	kubectl config current-context | grep $1 || (echo ERROR: wrong cluster && exit 1)
endef
MODULE="."

.PHONY: build
build:
	kustomize build $(MODULE)

.PHONY: diff
diff:
	kustomize build $(MODULE) | kubectl diff -f - | less -SR

.PHONY: deploy
deploy:
	kustomize build $(MODULE) | kubectl apply -f - | grep -v unchanged
