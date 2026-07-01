# EightFold

The pipeline consists of seven stages:

First, the application detects the type of each input file, such as a recruiter CSV or a resume.

Next, the parser extracts candidate information like name, email, phone number, skills, education, and experience.

The normalization module standardizes values such as phone numbers, skill names, and dates.

The merge module combines information from multiple sources and resolves conflicts using predefined source-priority rules.

After merging, confidence scores are assigned, and provenance information is maintained for every field.

Finally, the output is projected into the required JSON format based on a runtime configuration and validated before being written to the output file.



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
