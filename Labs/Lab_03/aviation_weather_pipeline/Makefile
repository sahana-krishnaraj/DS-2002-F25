.PHONY: all fetch analyze clean

# default target is analyze
all: analyze

#run the fetch command
fetch:
	@echo "---Fetching the data from the Aviation Weather API---"
	bash ./fetch_metars.sh
	@echo "---Data has been fetched---"

analyze: fetch
	@echo "---Analyzing the Airport data---"
	bash ./analyze_data.sh
	@echo "---Analysis is complete! Please check weather_report.csv!"

clean:
	@echo "---Initiating clean up---"
	@echo "---Removing the weather_report.csv file and raw_metars directory---"
	rm -rf raw_metars weather_report.csv
	@echo "---Clean up is complete---"

