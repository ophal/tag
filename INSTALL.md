Installation instructions
=========================

NOTE: Following SQL commands are compatible with SQLite3, you'll need to adapt them for another database engine.

1. Create schema:

CREATE TABLE tag(id INTEGER PRIMARY KEY AUTOINCREMENT, name VARCHAR(255));
CREATE UNIQUE INDEX unq_idx_tag_name ON tag (name);
CREATE TABLE field_tag(entity_type VARCHAR(255), entity_id INTEGER, tag_id INTEGER, PRIMARY KEY (entity_type, entity_id, tag_id));
