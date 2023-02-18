# AWS Costs, Economics and Billing Practices

_16% of the exam_questions about 8-10 questions_

* EC2 Instances are priced as follows
    * On-Demand: EC2 capacity billed to the second.
        * Pay for what you use.
        * Use case: Applications are under development, workloads are not expected to run for more than a year, no upfront payment or long-term committment, unpredictable workloads but don't want to be interrupted.
        * On-Demand Capacity Reservation: It is possible to buy upfront capacity to mitigate against capacity contraints in an AZ.
    * Spot: unused EC2 capacity on sale.
        * Pay the least but no guarantee of runtimes or interruptions.
        * Use case: Start and stop time of the workload does not matter. 90% savings over On-Demand. When your workload is feasable only at the lowest pricepoints. Spot price in effect at the beginning of each hour.
    * Reserved: Upfront capacity reservation committment for long running workloads.
        * Pay upfront with a contract to get discounts.
        * Use case: Save 75% versus On-Demand and willing to pay upfront for 1 or 3 year reservation. 
        * Flexibility: All upfront, partial upfront or no upfront is possible. A contract is required. Provides convertible types at 54% discount - change tenancy, OS or region.
    * Dedicated: Dedicated bare metal rental and host exclusively for you.
        * Use Case: Save 70% off of On-Demand. Software that is licensed based on per-core, per-socket or per-VM. Regulations that require tenancy exclusivity.
        * Dedidicated host is a physical server, dedicated instance runs on a host.
    * Savings Plan: Compute usage committment for 1 or 3 years applicable across multiple compute services.
        * Save upto 72% off of On-Demand.
        * Use Case: For flexibility across various services like Lambda, Fargate, and EC2.
        * This is a billing convenience nothing to do with a capacity reservation.
* Lambda Pricing
    * Computer Time - no charge for times that code is not running.
    * Duration - duration of compute and memory usage while execution is counted.
    * Free Tier - the free tier includes 1 million free requests each month
    
    # Leveraging the Well-Architected Framework
[AWS Well Architected](https://aws.amazon.com/architecture/well-architected/?wa-lens-whitepapers.sort-by=item.additionalFields.sortDate&wa-lens-whitepapers.sort-order=desc&wa-guidance-whitepapers.sort-by=item.additionalFields.sortDate&wa-guidance-whitepapers.sort-order=des=) helps cloud architects build secure, high-performaning, resilient, and efficient infrastructure for a variety of applications and workloads.

1. Operational Excellence
    * Plan for and anticipate failure. 
    * Deploy smaller, reversible changes. 
    * Script operations as code. 
    * Learn from failure and refine.
    * Use case: AWS Code Commit for versioning application as well as infrastructure.
1. Security
    * Automate security tasks.
    * Encrypt data in transit and at rest.
    * Assign only the least privileges required.
    * Track who did what and when.
    * Ensure security at all application layers.
    * Use case: CloudTrail to log all actions performed on your account.
1. Reliability
    * Recover from failure automatically.
    * Scale horizontally for resilience.
    * Stop guessing capacity.
    * Manage change through automation.
    * Test recovery procedures.
    * Use Case: RDS and multi-AZ deployments.
1. Performance Efficiency
    * Use serverless architectures first.
    * Use multi-region deployments.
    * Delegate tasks to a cloud vendor.
    * Experiement with virtual resources.
    * Use Case: Lambda to run serverless compute workloads.
1. Cost Optimization
    * Utilize consumption-based pricing.
    * Implement Cloud Financial Management.
    * Measure overall efficiency.
    * Pay only for resources your application requires.
    * Use case: S3 Intelligent Tiering to automatically move your data between access tiers based on usage patterns.
1. Sustainability
    * Understand your impact.
    * Establish sustainability goals.
    * Maximize utilization.
    * Use managed services.
    * Reduce downstream impact.
    * Use Case: EC2 Auto-scaling to scale down when demand is low.

