- reference:-
  - https://github.com/donnemartin/system-design-primer?tab=readme-ov-file#system-design-topics-start-here
  - https://takeuforward.org/system-design/complete-system-design-roadmap-with-videos-for-sdes
# System design
- Why system design
  - Ensures systems work reliably for global users.
  - Plans for issues like disasters, power outages, and crashes.
  - Keeps customers happy, boosting company revenue.
  - Engineers plan solutions before starting to code.
  - Builds systems that stay strong in tough situations.
- What is system design
  - Optimize processes and increase throughput using the same resources --> vertical scaling
  - preparing beforehand during non-peak hours --> preprocessing and cron job
  - keep backups and avoid single point of failure --> backups
  - Hire more resources --> horizontal scaling
  - microservice architecture
  - distributed system (partitioning)
  - load balancer
  - decoupling
  - logging and metrics calculation
  - extensible
 
- Scalability:-
  - Buy a bigger machine - vertical scaling
  - buy more machines - horizontal scaling
| Horizontal Scaling                | Vertical Scaling                |
|-----------------------------------|---------------------------------|
| Load balancing requiredss           | N/A                             |
| **Resilient**                     | Single point of failure         |
| Network calls (RPC)               | **Inter-process communication** |
| Data Inconsistency                | **Consistent**                  |
| **Scales well as users Increase** | Hard work limit                 |

- HTTP and HTTPS protocols
  - 
