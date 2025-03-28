# Test Cases for the 2025 Htsget Compliance Hackathon

## Post Request
- Htsget server may optionally accept POST requests (Pass/Skip)
- Post Request same url should be 200 (otherwise test results in Skip)
- Post Request with params should return InvalidInput


## Service Info
- Test info implemented for read and variant endpoints and 200 response
- Use the json schema at ga4gh/htsget/schemas/serviceInfoResponse.json modify if needed
- Test info [htsget][datatype] matches either reads or variants depending on path
- Test info [htsget][formats] for BAM and CRAM