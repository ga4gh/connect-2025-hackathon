# Instructions for the 2025 Htsget Compliance Hackathon

We recommend creating a virtual environment to install the dependancies for the htsget compliance suite
```
python -m venv /path/to/new/virtual/environment
source /path/to/new/virtual/environment/bin/activate
```

Proceed to install the following
```
apt-get install samtools bcftools tabix uv  (OSX: brew install samtools uv)
uv venv .
pip install crypt4gh
```

Clone the Repo
```
git clone https://github.com/ga4gh/htsget-compliance.git
cd htsget-compliance
python setup.py install
```

Quick run the compliance suite
```
htsget-compliance https://htsget.ga4gh-demo.org
```

Submit the report to GA4GH Testbed API
```
htsget-compliance https://htsget.ga4gh-demo.org --submit-id 1edb5213-52a2-434f-a7b8-b101fea8fb30 --submit-token K5pLbwScVu8rEoLLj8pRy5Wv7EXTVahn --submit --testbed-url https://testbed-api.staging.ga4gh.org/reports
```
# Test Cases
## Service Info Phase
- Create a new phase to test Service Info endpoints (Completed in template)
- Test if service info implemented for read and variant endpoints and 200 response (Pass/Fail) (Completed in template)
- Use the json schemas located at ga4gh/htsget/schemas/ 
- Test info [htsget][datatype] matches either reads or variants depending on path (Pass/Fail)
- Test info [htsget][formats] for BAM and CRAM (Pass/Fail)

## Post Request Tests for Read and Variant Endpoints
- Htsget server may optionally accept POST requests (Pass/Skip)
- Post Request same url should be 200 (otherwise test results in Skip)
- Post Request with params should return InvalidInput


