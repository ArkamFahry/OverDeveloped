---
id: u0tckorg6m3tdccwwvww6we
title: Third Normal Form 3nf
desc: ''
updated: 1673934799406
created: 1673765736892
---

Although [[Second Normal Form (2NF)|nibm.dse.dbms.normalization.second-normal-form-2nf]] relations have less redundancy than those in [[1NF |nibm.dse.dbms.normalization.first-normal-form-1nf]], they may still suffer from update anomalies. If we update only one tuple and not the other, the database would be in an inconsistent state. This update anomaly is caused by a transitive dependency. We need to remove such dependencies by progressing to Third Normal Form (3NF).
