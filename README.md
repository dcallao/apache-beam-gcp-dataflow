# apache-beam-example
### Install
```
pip install -r requirements.txt
```

### Usage
#### Run locally using DirectRunner
```
python main.py \
--input data/<path-to-apache-log-file>.log \
--output filtered-data.txt
```

#### Run on dataflow
```
python main.py \
--input gs://<path-to-apache-log-file>.log \
--output gs://<output-file-path>/filtered-data.txt \
--runner DataflowRunner \
--project <gcp-project-id>\
--temp_location gs://<google-cloud-storage-bucket>/temp \
--setup_file setup.py
```