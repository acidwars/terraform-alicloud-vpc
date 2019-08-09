
# Module `.`

Provider Requirements:
* **alicloud:** (any version)

## Input Variables
* `availability_zones` (default `[""]`): List available zones to launch several VSwitches.
* `cpu_core_count` (default `2`): CPU core count used to fetch instance types.
* `destination_cidrs` (required): List of destination CIDR block of virtual router in the specified VPC.
* `memory_size` (default `2`): Memory size used to fetch instance types.
* `nexthop_ids` (required): List of next hop instance IDs of virtual router in the specified VPC.
* `number_format` (default `"%02d"`): The number format used to output.
* `route_table_id` (required): The route table ID of virtual router in the specified VPC.
* `vpc_cidr` (default `"172.16.0.0/12"`): The cidr block used to launch a new vpc when 'vpc_id' is not specified.
* `vpc_description` (default `"A new VPC created by Terrafrom module tf-alicloud-vpc-cluster"`): The vpc description used to launch a new vpc when 'vpc_id' is not specified.
* `vpc_id` (required): The vpc id used to launch several vswitches.
* `vpc_name` (default `"TF-VPC"`): The vpc name used to launch a new vpc when 'vpc_id' is not specified.
* `vswitch_cidrs` (required): List of cidr blocks used to launch several new vswitches.
* `vswitch_description` (default `"New VSwitch created by Terrafrom module tf-alicloud-vpc-cluster."`): The vswitch description used to launch several new vswitch.
* `vswitch_name` (default `"TF_VSwitch"`): The vswitch name prefix used to launch several new vswitch.

## Output Values
* `availability_zones`
* `route_table_id`
* `router_id`
* `vpc_id`
* `vswitch`
* `vswitch_ids`

## Managed Resources
* `alicloud_nat_gateway.default` from `alicloud`
* `alicloud_route_entry.route_entry` from `alicloud`
* `alicloud_vpc.vpc` from `alicloud`
* `alicloud_vswitch.vswitches` from `alicloud`

## Data Resources
* `data.alicloud_instance_types.default` from `alicloud`
* `data.alicloud_zones.default` from `alicloud`

