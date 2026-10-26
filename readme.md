EV Charging Station Analytics

Project Overview
---------------------------
A MySQL DBMS project that manages EV charging operations: stations and chargers, customers and their vehicles, charging sessions, payments, memberships, maintenance records, and station reviews. It also includes analytics queries for revenue, peak hours, and charger utilization.

ER Diagram
--------------
EV Charging Station Analytics - ER Diagram

Objectives
Manage stations, chargers, customers, and vehicles
Track charging sessions, energy used, and cost
Monitor payments (Paid, Pending, Failed, Refunded)
Manage membership plans and subscriptions
Maintain charger maintenance records and station reviews
Generate business analytics

Technologies Used
----------------------------
MySQL 8.0+, MySQL Workbench, SQL

Database Information
--------------------------------
Database Name: EV_Charging_Analytics_10T
Tables (10): stations, chargers, customers, vehicles, membership_plans, customer_memberships, charging_sessions, payments, maintenance_logs, station_reviews

Entity Relationships
--------------------------------
Parent Table	   Child Table	             Relationship
stations	     chargers	                1 : M
chargers	     charging_sessions	        1 : M
chargers	     maintenance_logs	        1 : M
stations	     station_reviews	        1 : M
customers	     vehicles	                1 : M
customers	     charging_sessions	        1 : M
customers	     customer_memberships	1 : M
customers	     station_reviews	        1 : M
vehicles	     charging_sessions	        1 : M
membership_plans     customer_memberships       1 : M
charging_session     payments                   1 : 1 (at most one payment per session)

customers and membership_plans form an M : M relationship, resolved through customer_memberships.

SQL Queries
---------------------
About 88 questions, each written as a comment above its query:

Level 1 – Easy: SELECT, DISTINCT, aliases, ORDER BY, LIMIT, WHERE
Level 2 – Intermediate: aggregates, GROUP BY, HAVING, joins, functions, CASE
Level 3 – Advanced: subqueries, CTEs, window functions, and 25 analytics questions (Q1–Q25)

SQL Operations Included
Database creation: CREATE DATABASE, CREATE TABLE, PRIMARY KEY, FOREIGN KEY, UNIQUE, CHECK, ENUM, DEFAULT
Data manipulation: INSERT, UPDATE, DELETE, SELECT
Database objects: 4 views, 9 indexes, 2 stored procedures, 2 stored functions, 3 triggers
Transactions and access control: COMMIT, ROLLBACK, SAVEPOINT, CREATE USER, GRANT, REVOKE

SQL Concepts Covered
Aggregate functions, GROUP BY / HAVING, CASE, COALESCE, NULLIF, string, numeric, and date functions, window functions (ROW_NUMBER, RANK, DENSE_RANK, NTILE, LAG, LEAD, running total, moving average), CTEs (including recursive), joins (INNER, LEFT, RIGHT, SELF), subqueries, correlated subqueries, EXISTS / NOT EXISTS, ANY / ALL, derived tables

Project Contents
-----------------
Database schema and sample data
About 88 SQL questions and queries
Views, indexes, procedures, functions, triggers
ER diagram