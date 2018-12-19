# Factor #3: Async serverless

Factor #3 is to use serverless backends for compute. As Factor #2 gives us a reliable eventing system, we can trigger serverless apps to execute business logic on these events. Each serverless app should have the following properties:

- **Idempotent**: The code should be prepared for atleast-once (for same event) delivery of events.
- **Out-of-order**: Events may not be guaranteed to be received in the order of creation. The code should not depend on any expected sequence of events.

## Traditional vs 3factor

| Traditional                       | 3factor (Factor #3)                    |
| -------------                     | -------------                          |
| Deploy on VMs or containers       | Deploy on serverless platforms         |
| Manage the runtime yourself       | Platform manages the runtime           |
| Requires operational expertise    | Does not require operational expertise |
| Implement auto-scale, if possible | Auto-scaling by default                |

## Benefits

Serverless, although still maturing, promises many capabilities:

1. No ops: Serverless manages the runtime of the application and reduces the operational burden on the team as much as possible.

2. Free scale: Serverless auto-scales based on utilization without having to setup any additional infrastructure.

3. Cost: Serverless is priced on a per-request basis. Hence, it is very cost-efficient for bursty workloads which would otherwise be billed on traditional infrastructure even while not being used.

## Reference implementation

Coming soon.

## Video

Coming soon.