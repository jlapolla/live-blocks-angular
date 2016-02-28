# Require submodules
include require.mk
$(call ,$(call require,$(d)directives/Makefile))

define $(d)template
$(eval include helpdoc.mk)
$(eval include watch.mk)

$(call helpdoc,$(d)src.js)
$(d)src.js: $(d)directives/directives.js $(d)header.js $(d)footer.js $(d)config.js
	cat $(d)header.js $(d)directives/directives.js $(d)config.js $(d)footer.js > $(d)src.js

.PHONY: $(d)clean
$(call helpdoc,$(d)clean)
$(d)clean: $(d)directives/clean
	rm -f $(d)src.js

.DEFAULT_GOAL := help

endef

$(eval $($(d)template))
$(eval $(d)template :=)

