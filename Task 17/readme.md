# Task 17: DynamoDB Table Creation (Basic)

## Simple Definition

DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance.

## Objective

To create a DynamoDB table and insert sample items to understand serverless database basics.

## Architecture Overview

Application  
↓  
DynamoDB Table  
↓  
NoSQL Data Storage

## Steps

### Step 1: Create DynamoDB Table

1. Go to DynamoDB → Create Table.
2. Enter table name.
3. Define Primary Key:
   - Partition Key (e.g., id).
4. Use default settings.
5. Create table.

### Step 2: Insert Sample Items

1. Open table.
2. Click Explore table items.
3. Click Create item.
4. Add attributes (id, name).
5. Save item.

### Step 3: Query Table

1. Use Scan option.
2. Confirm inserted data appears.

## Verification

* Table status = Active.
* Items inserted successfully.
* Data visible in console.

## Conclusion

Successfully created and managed a DynamoDB table, demonstrating understanding of serverless NoSQL database services.