## Unreleased

- **Breaking**
  - Changed response format for creating claims
    - All claim data is inside the `claim` key, and more data is present
      Example:
      ```json5
      // Before
      {
        "success": true,
        "id": "XXX",
        "expiration": 1588473164
      }
      
      // After
      {
        "success": true,
        "claim": {
          "id": "XXX",
          "expiration": 1588473164,
          "user": "a",
          "session": "b"
        }
      }
      ```

- Added tests (E2E)

## v0.1.1 - 2020-05-05

- Fixed bug with missing `errorCode` when duration is negative during claim creation
- Fix bug with incorrect `errorCode` when error is trigger during checking if a claim exists
- Added documentation on errors

## v0.1.0 - 2020-05-04

- Initial beta release
