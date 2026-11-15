---
'@composio/core': patch
'@composio/python-sdk': patch
---

Clean strict-mode tool arguments using every object or array alternative in `anyOf` and `oneOf`, including nested properties and referenced schemas. Optional arguments declared only in later alternatives no longer forward an invalid `null`; an explicit `null` accepted by any declaring alternative is preserved. Schema structure traversal is cycle-safe and raises an error if its depth or 2,000-visit budget is exceeded, rather than returning partially cleaned arguments.
