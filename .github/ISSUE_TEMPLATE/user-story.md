---
name: User Story
about: This template is for creating user stories
title: ''
labels: ''
assignees: ''

---

statuspage=# \dt
           List of relations
 Schema |   Name   | Type  |   Owner    
--------+----------+-------+------------
 public | monitors | table | statuspage
(1 row)

statuspage=# \d monitors
                             Table "public.monitors"
        Column        |           Type           | Collation | Nullable | Default 
----------------------+--------------------------+-----------+----------+---------
 id                   | uuid                     |           | not null | 
 name                 | character varying(100)   |           | not null | 
 url                  | character varying(2083)  |           | not null | 
 interval_seconds     | integer                  |           | not null | 
 expected_status_code | integer                  |           | not null | 
 timeout_seconds      | integer                  |           | not null | 
 created_at           | timestamp with time zone |           | not null | 
Indexes:
    "monitors_pkey" PRIMARY KEY, btree (id)

statuspage=#
