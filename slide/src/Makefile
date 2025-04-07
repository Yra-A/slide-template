# .PHONY: live build clean

# live:
# 	@echo "Previewing main slides..."
# 	-@reveal-md main.md -w --scripts https://cdn.tonycrane.cc/heti/heti.js,heti_worker.js --template template.html || true

# build:
# 	@echo "Building main slides..."
# 	@reveal-md main.md --scripts https://cdn.tonycrane.cc/heti/heti.js,heti_worker.js --template template.html --static ../site --assets-dir assets
# 	@rm ../site/main.html

# clean:
# 	@echo "Cleaning up..."
# 	rm -rf ../site/

.PHONY: live build clean

# Default to 'main.md' if no filename is provided
FILE ?= main.md

live:	
	@echo "Previewing slides from $(FILE)..."
	-@reveal-md $(FILE) -w --scripts https://cdn.tonycrane.cc/heti/heti.js --scripts ./heti_worker.js --template template.html || true

build:
	@echo "Building slides from $(FILE)..."
	@reveal-md $(FILE) --scripts https://cdn.tonycrane.cc/heti/heti.js --scripts ./heti_worker.js --template template.html --static ../$(FILE) --assets-dir assets
	@rm ../site/$(basename $(notdir $(FILE))).html

clean:
	@echo "Cleaning up..."
	rm -rf ../site/