# AWS Costs, Economics and Billing Practices

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