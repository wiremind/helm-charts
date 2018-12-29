
default: test

RELEASE := helm-es-multi

install:
	helm dep update
	helm upgrade --wait --timeout=600 --install $(RELEASE) .

test: install
	helm test $(RELEASE)

purge:
	helm del --purge $(RELEASE)
