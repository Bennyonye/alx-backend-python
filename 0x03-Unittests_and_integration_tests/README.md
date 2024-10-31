# Unit and Integration Testing in Python

This project demonstrates writing unit and integration tests in Python 3. Below is an overview of tasks and implementations.

## Requirements
- `parameterized` module

## Project Overview

1. **Parameterize Tests**  
   - Created `TestAccessNestedMap` to test `utils.access_nested_map` with different input cases.
   - Implemented tests for both valid cases and exceptions using `@parameterized.expand`.

2. **Mock HTTP Calls**  
   - Tested `utils.get_json` in `TestGetJson` by patching `requests.get` to return mock JSON payloads.

3. **Memoization Tests**  
   - Verified memoization with `TestMemoize` class, ensuring that `a_method` is called only once.

4. **Testing Client Library**  
   - Tested `GithubOrgClient.org`, `_public_repos_url`, `public_repos`, and `has_license` methods, mocking external calls as needed.
   
5. **Integration Testing with Fixtures**  
   - Integrated `TestIntegrationGithubOrgClient`, utilizing `fixtures.py` to ensure comprehensive functionality testing of `public_repos` based on specific payloads.

For full details on tasks and implementation, refer to the files [test_utils.py](test_utils.py) and [test_client.py](test_client.py).
