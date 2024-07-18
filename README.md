Activate the virtual Python environment:

virtualenv tweeper

  cd tweeper
  source bin/activate

Activate the Tweep feed:

  python tweeper.py

Test the pipeline locally:

  python pipeline.py --streaming

Run the pipeline with Cloud Dataflow:

  python pipeline.py --streaming --runner DataflowRunner \
  --project <YOUR_PROJECT_NAME> \
  --temp_location gs://<YOUR_BUCKET_NAME>/temp \
  --staging_location gs://<YOUR_BUCKET_NAME>/staging \
  --region us-central1 \
  --job_name tweeps
