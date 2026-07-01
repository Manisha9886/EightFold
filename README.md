# EightFold

How to Run
Step 1 - Install dependencies
pip install -r requirements.txt

Step 2 - Run with default output
python cli.py input-dir sample_inputs --out output.json
Then open output.json to see the merged, normalized candidate profiles.
  
Step 3 - Run with custom config
python cli.py - input-dir sample_inputs --config schema/example_config.json --out output_custom.json
This reshapes the output — only the fields you want, renamed however you like.

Step 4 — Run the tests
python -m pytest tests/ -v
You should see 9 passed — all tests green.
