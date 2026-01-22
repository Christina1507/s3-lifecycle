# Amazon S3 Lifecycle Management

## Description
This project demonstrates the implementation of Amazon S3 Lifecycle policies to automatically transition objects between storage classes and delete data after a defined period. The goal is to optimize storage costs while maintaining data availability.

---

## Technologies Used
- Amazon S3
- S3 Lifecycle Rules
- S3 Storage Classes (Standard, Standard-IA, Glacier)
- IAM (for access control)

---

## Architecture Overview
- Objects are stored in an S3 bucket
- Lifecycle rules manage object transitions based on age
- Older data is moved to lower-cost storage classes
- Expired data is automatically deleted

---

## S3 Lifecycle Configuration Steps

### Step 1: Create S3 Bucket
- Created an S3 bucket with a unique name
- Enabled versioning (optional)

### Step 2: Configure Lifecycle Rule
- Navigated to the **Management** tab of the S3 bucket
- Created a new lifecycle rule
- Applied rule to the entire bucket or specific object prefix

### Step 3: Configure Transition Actions
- Transition objects to **S3 Standard-IA** after 30 days
- Transition objects to **S3 Glacier** after 90 days

### Step 4: Configure Expiration Actions
- Permanently delete objects after 180 days
- Expire non-current object versions (if versioning enabled)

### Step 5: Review and Enable Rule
- Reviewed lifecycle rule configuration
- Enabled the rule to start automated data management

---

## Validation
- Uploaded sample objects to the S3 bucket
- Verified lifecycle rule configuration
- Confirmed objects transitioned according to defined policies

---

## Outcome
- Automated data lifecycle management implemented
- Storage costs reduced by transitioning data to lower-cost tiers
- No manual intervention required for data cleanup

---

## Key Learnings
- Understanding S3 storage classes and lifecycle policies
- Automating data transitions and expiration
- Cost optimization using AWS managed services
- Managing versioned objects with lifecycle rules
