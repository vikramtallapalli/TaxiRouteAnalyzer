# TaxiRouteAnalyzer

To execute the project,

1. Set up the streaming of input data file using netcat Command – while read -r line ; do echo "$line"; sleep 1; done < /tmp/sorted_data.csv | nc -l -p 8787
2. External library simplelatlng-1.3.1.jar is required to be passed when submitting spark job
3. Trigger the spark project Command- spark-submit --class SparkApp --num-executors 4 --jars simplelatlng-1.3.1.jar TaxiRouteFinder.jar
