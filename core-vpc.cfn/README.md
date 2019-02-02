# Core VPC

This module deploys a VPC with public and private subnets in each availabilty zone for the specified region.

## Resources

- VPC
- 2+ Public Subnets (depends on the number of availabilty zones in the region)
- 2+ Private Subnets (depends on the number of availabilty zones in the region)
- Internet Gateway
- 2+ Nat Gateway's (1 in each public subnet, depends on abailablity zones.)
- 1 Route table per private subnet
- 1 public route table

## Pricing

Pricing starts at \$0.045 per NAT gateway hour plus data processing and data transfer charges. Data processing costs are based on the amount of data processed by the NAT Gateway; data transfer costs are the usual costs to move data between an EC2 instance and the Internet. For more information, read about VPC Pricing at https://aws.amazon.com/vpc/pricing/.

## Deployemnt

To deploy this module execute the following commands from the project root.

```bash
pipenv run runway deploy vpc-core.cfn
```
