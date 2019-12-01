# UpdatableORM
Custom ORM built specifically to track integer field changes in batches while avoiding collisions and integrity issues.

# Purpose
This ORM was built for a specific project that requires intense batch processing which would be drastically slower if all changes had to be applied to the DB live.  So this solution allows a set of objects to be defined in memory in a way that their changes are tracked and later sent to the DB without conflicting with other concurrent processes.

The original use case is for an AI, but it could easily apply to other uses.

# Caution
Although this ORM is designed to be quite flexible, it imposes a rigid model which is described in details in the source code, namely in _src/Updatable.php_'s header.  You are therefore advised to read it carefully and choose wisely.



