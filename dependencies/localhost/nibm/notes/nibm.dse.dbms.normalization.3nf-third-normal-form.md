---
id: u0tckorg6m3tdccwwvww6we
title: 3nf Third Normal Form
desc: ''
updated: 1673934799406
created: 1673765736892
---

Although [[Second Normal Form (2NF)|nibm.dse.dbms.normalization.2nf-second-normal-form]] relations have less redundancy than those in [[1NF|nibm.dse.dbms.normalization.1nf-first-normal-form]], they may still suffer from update anomalies. If we update only one tuple and not the other, the database would be in an inconsistent state. This update anomaly is caused by a transitive dependency. We need to remove such dependencies by progressing to Third Normal Form (3NF).
