<!-- fetched 2026-10-13 from https://www.cockroachlabs.com/docs/stable/postgresql-compatibility by sweep-shape-compat.py; text extracted from the provider's own page -->

PostgreSQL Compatibility - CockroachDB 
 Documentation Index
 Fetch the complete documentation index at: /llms.txt 
 Use this file to discover all available pages before exploring further.
 Skip to main content 
 CockroachDB home page 
 Cockroach Continuum 
 Search...
 ⌘ K 
 Get started free 
 Get started free 
 Search... 
 Navigation 
 PostgreSQL Compatibility
 Get Started 
 Guides 
 Tutorials 
 Reference 
University 
 Continuum Home 
 Get Started 
 Continuum Overview 
 Get Started with Cockroach Continuum 
 Create a Continuum Organization 
 CockroachDB Documentation 
 On this page 
 Unsupported features PostgreSQL range types 
 Other unsupported features 
 Partially supported features Export a CockroachDB schema with pg_dump 
 Before you begin 
 Choose a compatibility mode 
 Export and restore a CockroachDB schema 
 Generate PostgreSQL-oriented schema definitions 
 Known limitations for PostgreSQL dump tools 
 Multiple active portals 
 Advisory locks 
 Features that differ from PostgreSQL Overflow of float 
 Precedence of unary ~ 
 Precedence of bitwise operators 
 Integer division 
 Shift argument modulo 
 Locking and FOR UPDATE 
 CHECK constraint validation for INSERT ON CONFLICT 
 Column name from an outer column inside a subquery 
 SQL compatibility 
 PostgreSQL Compatibility
 Copy page Copy page 
 Copy page Copy page 
 CockroachDB supports the PostgreSQL wire protocol and the majority of PostgreSQL syntax. This means that existing applications built on PostgreSQL can often be migrated to CockroachDB without changing application code. 
 CockroachDB is compatible with version 3.0 of the PostgreSQL wire protocol (pgwire) and works with the majority of PostgreSQL database tools such as , , and so on. Consult this link for a full list of supported . CockroachDB also works with most PostgreSQL drivers and ORMs. 
 CockroachDB reports PostgreSQL version 18 in the server_version and server_version_num , and the tables in the schema are aligned with the PostgreSQL 18 system catalogs. 
 When a client connects, CockroachDB sends all the startup status parameters that drivers expect from PostgreSQL 18. These parameters include search_path , default_transaction_read_only , in_hot_standby , and scram_iterations . Because CockroachDB has no primary/standby distinction, drivers that read in_hot_standby to detect standby servers always receive off . 
 However, CockroachDB does not support some of the PostgreSQL features or behaves differently from PostgreSQL because not all features can be easily implemented in a distributed system. This page documents the known list of differences between PostgreSQL and CockroachDB for identical input. That is, a SQL statement of the type listed here will behave differently than in PostgreSQL. Porting an existing application to CockroachDB will require changing these expressions. 
 This document does not discuss strategies for porting applications that use SQL features CockroachDB does not support. 
 ​ 
 Unsupported features 
 The following PostgreSQL features are not supported in CockroachDB v26.3: 
 ​ 
 PostgreSQL range types 
 CockroachDB does not support PostgreSQL range types. 
 ​ 
 Other unsupported features 
 Events.
 Drop primary key.
 Each table must have a primary key associated with it. You can . 
 XML functions.
 Column-level privileges.
 XA syntax.
 Creating a database from a template.
 .
 Foreign data wrappers.
 Session-scoped advisory lock functions. Transaction-scoped advisory locks are supported. Refer to .
 ​ 
 Partially supported features 
 The following PostgreSQL features are partially supported in CockroachDB v26.3. 
 ​ 
 Export a CockroachDB schema with pg_dump 
 New in v26.3: CockroachDB supports using PostgreSQL 18’s pg_dump command to export the schema definitions from a CockroachDB database. Use the plain-text dump format to recreate the schema in another CockroachDB database or to generate PostgreSQL-oriented schema definitions. 
 For operational backups and disaster recovery, use CockroachDB BACKUP and RESTORE . Unlike pg_dump , CockroachDB backup and restore jobs provide distributed execution, job management, and CockroachDB-specific recovery capabilities. 
 ​ 
 Before you begin 
 Install the PostgreSQL 18 client tools . The examples on this page use PostgreSQL 18.3.
 Use a that can access every schema object to export.
 Before restoring a schema, create an empty target database.
 ​ 
 Choose a compatibility mode 
 The pg_dump_compatibility session variable controls the metadata and syntax that CockroachDB presents to pg_dump . 
 Value
 Behavior
 Use when
 off 
 Disables dump-specific catalog and syntax adjustments. This is the default for other clients.
 You do not want dump compatibility behavior.
 cockroachdb 
 Applies PostgreSQL catalog and OID compatibility fixups, hides CockroachDB-internal objects, and preserves CockroachDB-specific syntax.
 The schema will be restored into CockroachDB.
 postgres 
 Applies the catalog and OID fixups, hides CockroachDB-internal objects, and suppresses CockroachDB-specific storage parameters and locality syntax.
 The schema definitions must use PostgreSQL-oriented syntax.
 A client with an exact, case-sensitive application_name of pg_dump , pg_restore , or pg_dumpall automatically uses pg_dump_compatibility=cockroachdb . CockroachDB emits a NOTICE when it selects this mode. An explicit value in the connection string, including off or postgres , overrides automatic selection. 
 Automatic mode selection for pg_restore and pg_dumpall does not indicate end-to-end support for those tools. Refer to Known limitations . 
 ​ 
 Export and restore a CockroachDB schema 
 For a CockroachDB-target schema, allow CockroachDB to select pg_dump_compatibility=cockroachdb automatically. To dump the bank database schema in plain format, run: 
 pg_dump \ 
 --dbname=" $SOURCE_URL " \ 
 --schema-only \ 
 --format=plain \ 
 --no-owner \ 
 --no-privileges \ 
 --file=bank-schema.sql 
 $SOURCE_URL is the for the source CockroachDB database. 
 pg_dump automatically uses pg_dump_compatibility=cockroachdb , so CockroachDB-specific definitions remain in bank-schema.sql . 
 To restore the schema into an empty bank database on another CockroachDB cluster with psql , run: 
 psql \ 
 --dbname=" $TARGET_URL " \ 
 --set=ON_ERROR_STOP=on \ 
 --file=bank-schema.sql 
 $TARGET_URL is the for the empty target CockroachDB database. 
 As an alternative to psql , restore the plain script with the : 
 cockroach sql --url=" $TARGET_URL " --file=bank-schema.sql 
 PostgreSQL 18 pg_dump scripts use the \restrict and \unrestrict metacommands to prevent other backslash commands in a plain-text dump from running on the client. The supports these commands and preserves restricted mode across files included with \i or \ir . 
 ​ 
 Generate PostgreSQL-oriented schema definitions 
 To generate PostgreSQL-oriented schema definitions, explicitly set pg_dump_compatibility=postgres in the source connection string. In a , pass the setting with the URL-encoded options parameter: 
 pg_dump \ 
 --dbname="postgresql://{user}:{password}@{host}:26257/bank?sslmode=verify-full&options=-c%20pg_dump_compatibility%3Dpostgres" \ 
 --schema-only \ 
 --format=plain \ 
 --no-owner \ 
 --no-privileges \ 
 --file=bank-schema-for-postgres.sql 
 Replace {user} , {password} , and {host} with the source CockroachDB connection parameters. 
 The postgres mode removes CockroachDB-specific syntax that the compatibility layer recognizes. It does not translate every CockroachDB type, expression, or feature to a PostgreSQL equivalent. Review the script and test the restore on the target PostgreSQL version. 
 ​ 
 Known limitations for PostgreSQL dump tools 
 Only schema-only dumps in plain format are supported. Data dumps, non-plain archive formats, pg_restore , and pg_dumpall are not supported.
 pg_dump dumps one database and does not include cluster-wide objects such as and .
 Unvalidated domain added with ALTER DOMAIN ... ADD CONSTRAINT ... NOT VALID might not be included in the dump. Verify that these constraints are present before restoring it.
 CockroachDB stores a sequence value without PostgreSQL’s separate is_called state. CockroachDB-to-CockroachDB round trips preserve the stored value. If setval(sequence, value, false) uses a value other than the sequence start value, pg_dump reports (value - increment, true) rather than (value, false) .
 PostgreSQL-oriented output might require manual changes for CockroachDB-specific objects and for the unsupported or partially supported features described on this page.
 ​ 
 Multiple active portals 
 CockroachDB v26.3 supports pgwire’s multiple active portals as a . The feature is off by default, and can be enabled by setting the to true . 
 When set to true , multiple portals can be open at the same time, with their execution interleaved with each other. In other words, these portals can be paused. 
 This feature has the following limitations: 
 Only read-only without are supported.
 Postqueries (which are how CockroachDB executes , for example) are not supported.
 is not supported for multiple active portals; instead queries execute on the only.
 Only the latest execution of a statement from a pausable portal is recorded by the .
 In addition to the known issues, additional performance testing is needed. 
 ​ 
 Advisory locks 
 CockroachDB supports transaction-scoped advisory locks: pg_advisory_xact_lock , pg_advisory_xact_lock_shared , pg_try_advisory_xact_lock , and pg_try_advisory_xact_lock_shared . Each function takes either a single INT key or two INT4 keys. A lock is tied to the transaction that acquires it and is released when the transaction commits or rolls back. For function descriptions, refer to . 
 Transaction-scoped advisory locks behave as follows: 
 The lock keyspace is scoped to the current database, matching PostgreSQL: the same key refers to different locks in different databases.
 pg_advisory_xact_lock and pg_advisory_xact_lock_shared wait until the lock is available. If the is set, an acquisition that waits longer than the timeout fails with the error canceling statement due to lock timeout .
 pg_try_advisory_xact_lock and pg_try_advisory_xact_lock_shared do not wait. They return false if the lock is not immediately available.
 If transactions deadlock on advisory locks, CockroachDB fails one of the transactions with a . As in PostgreSQL, the failed transaction must be retried by the client.
 Granted and waiting advisory locks are reported in the view.
 In a cluster that is upgrading to v26.3, the advisory lock functions return an error until the upgrade is finalized. 
 Session-scoped advisory locks are not supported. The session-scoped functions fall into two groups: 
 pg_advisory_lock , pg_advisory_lock_shared , and pg_try_advisory_lock_shared are not defined. Calling them returns an error.
 pg_try_advisory_lock , pg_advisory_unlock , pg_advisory_unlock_shared , and pg_advisory_unlock_all are defined for compatibility, but do not acquire or release locks. They silently succeed without any effect: pg_try_advisory_lock , pg_advisory_unlock , and pg_advisory_unlock_shared always return true , and pg_advisory_unlock_all performs no action.
 ​ 
 Features that differ from PostgreSQL 
 Note, some of the differences below only apply to rare inputs, and so no change will be needed, even if the listed feature is being used. In these cases, it is safe to ignore the porting instructions. 
 ​ 
 Overflow of float 
 In PostgreSQL, the float type returns an error when it overflows or an expression would return Infinity: 
 postgres=# select 1e300::float * 1e10::float; 
 ERROR: value out of range: overflow 
 postgres=# select pow(0::float, -1::float); 
 ERROR: zero raised to a negative power is undefined 
 In CockroachDB, these expressions instead return Infinity: 
 SELECT 1e300:: float * 1e10:: float ; 
 ?column? 
 ------------ 
 +Inf 
 (1 row) 
 SELECT pow( 0 :: float , - 1 :: float ); 
 pow 
 -------- 
 +Inf 
 (1 row) 
 ​ 
 Precedence of unary ~ 
 In PostgreSQL, the unary ~ (bitwise not) operator has a low precedence. For example, the following query is parsed as ~ (1 + 2) because ~ has a lower precedence than + : 
 SELECT ~ 1 + 2 ; 
 ?column? 
 ------------ 
 0 
 (1 row) 
 In CockroachDB, unary ~ has the same (high) precedence as unary - , so the above expression will be parsed as (~1) + 2 . 
 Porting instructions: Manually add parentheses around expressions that depend on the PostgreSQL behavior. 
 ​ 
 Precedence of bitwise operators 
 In PostgreSQL, the operators | (bitwise OR), # (bitwise XOR), and & (bitwise AND) all have the same precedence. 
 In CockroachDB, the precedence from highest to lowest is: & , # , | . 
 Porting instructions: Manually add parentheses around expressions that depend on the PostgreSQL behavior. 
 ​ 
 Integer division 
 In PostgreSQL, division of integers results in an integer. For example, the following query returns 1 , since the 1 / 2 is truncated to 0 : 
 SELECT 1 + 1 / 2 ; 
 ?column? 
 ------------ 
 1.5 
 (1 row) 
 In CockroachDB, integer division results in a decimal . CockroachDB instead provides the // operator to perform floor division. 
 Porting instructions: Change / to // in integer division where the result must be an integer. 
 ​ 
 Shift argument modulo 
 In PostgreSQL, the shift operators ( << , >> ) sometimes modulo their second argument to the bit size of the underlying type. For example, the following query results in a 1 because the int type is 32 bits, and 32 % 32 is 0 , so this is the equivalent of 1 << 0 : 
 SELECT 1 :: int << 32 ; 
 ?column? 
 -------------- 
 4294967296 
 (1 row) 
 In CockroachDB, no such modulo is performed. 
 Porting instructions: Manually add a modulo to the second argument. Also note that CockroachDB’s type is always 64 bits. For example: 
 SELECT 1 :: int << (x % 64 ); 
 ​ 
 Locking and FOR UPDATE 
 CockroachDB supports the SELECT FOR UPDATE statement, which is used to order transactions by controlling concurrent access to one or more rows of a table. 
 For more information, see . 
 ​ 
 CHECK constraint validation for INSERT ON CONFLICT 
 CockroachDB validates constraints on the results of statements, preventing new or changed rows from violating the constraint. Unlike PostgreSQL, CockroachDB does not also validate CHECK constraints on the input rows of INSERT ON CONFLICT statements. 
 If this difference matters to your client, you can INSERT ON CONFLICT from a SELECT statement and check the inserted value as part of the SELECT . For example, instead of defining CHECK (x > 0) on t.x and using INSERT INTO t(x) VALUES (3) ON CONFLICT (x) DO UPDATE SET x = excluded.x , you could do the following: 
 > INSERT INTO t (x) 
 SELECT if (x <= 0 , crdb_internal.force_error( '23514' , 'check constraint violated' ), x) 
 FROM ( values ( 3 )) AS v(x) 
 ON CONFLICT (x) 
 DO UPDATE SET x = excluded.x; 
 An x value less than 1 would result in the following error: 
 pq: check constraint violated 
 ​ 
 Column name from an outer column inside a subquery 
 CockroachDB returns the column name from an outer column inside a subquery as ?column? , unlike PostgreSQL. For example: 
 > SELECT ( SELECT t. * ) FROM ( VALUES ( 1 )) t(x); 
 CockroachDB: 
 ?column? 
 ------------ 
 1 
 PostgreSQL: 
 x 
 --- 
 1 
 ​ 
 SQL compatibility 
 Click the following link to find a full list of . 
 CockroachDB home page youtube x linkedin instagram 
 Product
 CockroachDB CockroachDB Cloud Compare Pricing Get CockroachDB Sign In 
 Resources
 Guides Webinars Videos Architecture Overview FAQ Security 
 Learn & Support
 Docs University Developers Forum Slack Support Portal Contact Us 
 Company
 About Blog Careers Customers News Privacy Terms of Use
