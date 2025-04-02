# Test Cases for the 2025 Htsget Compliance Hackathon

We recommend to install a virtual environment to run the htsget compliance suite
```python -m venv /path/to/new/virtual/environment```
```source /path/to/new/virtual/environment/bin/activate```

Proceed to install the following
```apt-get install samtools bcftools tabix uv  (OSX: brew install samtools uv)```
```uv venv .```
```pip install crypt4gh ```

Clone the Repo
```git clone https://github.com/ga4gh/htsget-compliance.git```
```cd htsget-compliance```
```python setup.py install```

## Service Info Phase
- Create a new phase to test Service Info endpoints
- Test info implemented for read and variant endpoints and 200 response (Pass/Fail)
- Use the json schema at ga4gh/htsget/schemas/serviceInfoResponse.json modify if needed
- Test info [htsget][datatype] matches either reads or variants depending on path (Pass/Fail)
- Test info [htsget][formats] for BAM and CRAM (Pass/Fail)

## Post Request Tests for Read and Variant Endpoints
- Htsget server may optionally accept POST requests (Pass/Skip)
- Post Request same url should be 200 (otherwise test results in Skip)
- Post Request with params should return InvalidInput


