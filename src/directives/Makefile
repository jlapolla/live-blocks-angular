# Directive source files
$(eval $(d)files := $(d)lb-input.js)

define $(d)template
$(eval include helpdoc.mk)
$(eval include watch.mk)

$(call helpdoc,$(d)directives.js)
$(d)directives.js: $($(d)files) $(d)header.js $(d)footer.js
	cat $(d)header.js $($(d)files) $(d)footer.js > $(d)directives.js

.PHONY: $(d)clean
$(call helpdoc,$(d)clean)
$(d)clean:
	rm -f $(d)directives.js

.DEFAULT_GOAL := help

endef

$(eval $($(d)template))
$(eval $(d)template :=)
$(eval $(d)files :=)

