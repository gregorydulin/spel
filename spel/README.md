<!-- BEGIN TFDOCS -->
### Resources

No resources.

### Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_spel_identifier"></a> [spel\_identifier](#input\_spel\_identifier) | Namespace that prefixes the name of the built images | `string` | n/a | yes |
| <a name="input_spel_version"></a> [spel\_version](#input\_spel\_version) | Version appended to the name of the built images | `string` | n/a | yes |
| <a name="input_amigen7_extra_rpms"></a> [amigen7\_extra\_rpms](#input\_amigen7\_extra\_rpms) | List of package specs (rpm names or URLs to .rpm files) to install to the EL7 builders and images | `list(string)` | <pre>[<br>  "python36",<br>  "spel-release",<br>  "ec2-hibinit-agent",<br>  "ec2-net-utils",<br>  "https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/linux_amd64/amazon-ssm-agent.rpm"<br>]</pre> | no |
| <a name="input_amigen7_filesystem_label"></a> [amigen7\_filesystem\_label](#input\_amigen7\_filesystem\_label) | Label for the root filesystem when creating bare partitions for EL7 images | `string` | `""` | no |
| <a name="input_amigen7_package_groups"></a> [amigen7\_package\_groups](#input\_amigen7\_package\_groups) | List of yum repo groups to install into EL7 images | `list(string)` | <pre>[<br>  "core"<br>]</pre> | no |
| <a name="input_amigen7_package_manifest"></a> [amigen7\_package\_manifest](#input\_amigen7\_package\_manifest) | File containing a list of RPMs to use as the build manifest for EL7 images | `string` | `""` | no |
| <a name="input_amigen7_repo_names"></a> [amigen7\_repo\_names](#input\_amigen7\_repo\_names) | List of yum repo names to enable in the EL7 builders and images | `list(string)` | <pre>[<br>  "spel"<br>]</pre> | no |
| <a name="input_amigen7_repo_sources"></a> [amigen7\_repo\_sources](#input\_amigen7\_repo\_sources) | List of yum package refs (names or urls to .rpm files) that install yum repo definitions in EL7 builders and images | `list(string)` | <pre>[<br>  "https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm",<br>  "https://spel-packages.cloudarmor.io/spel-packages/repo/spel-release-latest-7.noarch.rpm"<br>]</pre> | no |
| <a name="input_amigen7_source_branch"></a> [amigen7\_source\_branch](#input\_amigen7\_source\_branch) | Branch that will be checked out when cloning AMIgen7 | `string` | `"master"` | no |
| <a name="input_amigen7_source_url"></a> [amigen7\_source\_url](#input\_amigen7\_source\_url) | URL that will be used to clone AMIgen7 | `string` | `"https://github.com/plus3it/AMIgen7.git"` | no |
| <a name="input_amigen7_storage_layout"></a> [amigen7\_storage\_layout](#input\_amigen7\_storage\_layout) | List of colon-separated tuples (mount:name:size) that describe the desired partitions for LVM-partitioned disks on EL7 images | `list(string)` | <pre>[<br>  "/:rootVol:5",<br>  "swap:swapVol:2",<br>  "/home:homeVol:1",<br>  "/var:varVol:2",<br>  "/var/log:logVol:2",<br>  "/var/log/audit:auditVol:100%FREE"<br>]</pre> | no |
| <a name="input_amigen8_extra_rpms"></a> [amigen8\_extra\_rpms](#input\_amigen8\_extra\_rpms) | List of package specs (rpm names or URLs to .rpm files) to install to the EL8 builders and images | `list(string)` | <pre>[<br>  "python39",<br>  "python39-pip",<br>  "python39-setuptools",<br>  "crypto-policies-scripts",<br>  "spel-release",<br>  "ec2-hibinit-agent",<br>  "ec2-net-utils",<br>  "https://s3.amazonaws.com/ec2-downloads-windows/SSMAgent/latest/linux_amd64/amazon-ssm-agent.rpm"<br>]</pre> | no |
| <a name="input_amigen8_filesystem_label"></a> [amigen8\_filesystem\_label](#input\_amigen8\_filesystem\_label) | Label for the root filesystem when creating bare partitions for EL8 images | `string` | `""` | no |
| <a name="input_amigen8_package_groups"></a> [amigen8\_package\_groups](#input\_amigen8\_package\_groups) | List of yum repo groups to install into EL8 images | `list(string)` | <pre>[<br>  "core"<br>]</pre> | no |
| <a name="input_amigen8_package_manifest"></a> [amigen8\_package\_manifest](#input\_amigen8\_package\_manifest) | File containing a list of RPMs to use as the build manifest for EL8 images | `string` | `""` | no |
| <a name="input_amigen8_repo_names"></a> [amigen8\_repo\_names](#input\_amigen8\_repo\_names) | List of yum repo names to enable in the EL8 builders and EL8 images | `list(string)` | <pre>[<br>  "spel"<br>]</pre> | no |
| <a name="input_amigen8_repo_sources"></a> [amigen8\_repo\_sources](#input\_amigen8\_repo\_sources) | List of yum package refs (names or urls to .rpm files) that install yum repo definitions in EL8 builders and images | `list(string)` | <pre>[<br>  "https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm",<br>  "https://spel-packages.cloudarmor.io/spel-packages/repo/spel-release-latest-8.noarch.rpm"<br>]</pre> | no |
| <a name="input_amigen8_source_branch"></a> [amigen8\_source\_branch](#input\_amigen8\_source\_branch) | Branch that will be checked out when cloning AMIgen8 | `string` | `"master"` | no |
| <a name="input_amigen8_source_url"></a> [amigen8\_source\_url](#input\_amigen8\_source\_url) | URL that will be used to clone AMIgen8 | `string` | `"https://github.com/plus3it/AMIgen8.git"` | no |
| <a name="input_amigen8_storage_layout"></a> [amigen8\_storage\_layout](#input\_amigen8\_storage\_layout) | List of colon-separated tuples (mount:name:size) that describe the desired partitions for LVM-partitioned disks on EL8 images | `list(string)` | <pre>[<br>  "/:rootVol:5",<br>  "swap:swapVol:2",<br>  "/home:homeVol:1",<br>  "/var:varVol:2",<br>  "/var/tmp:varTmpVol:2",<br>  "/var/log:logVol:2",<br>  "/var/log/audit:auditVol:100%FREE"<br>]</pre> | no |
| <a name="input_amigen_amiutils_source_url"></a> [amigen\_amiutils\_source\_url](#input\_amigen\_amiutils\_source\_url) | URL of the AMI Utils repo to be cloned using git, containing AWS utility rpms that will be installed to the AMIs | `string` | `""` | no |
| <a name="input_amigen_aws_cfnbootstrap"></a> [amigen\_aws\_cfnbootstrap](#input\_amigen\_aws\_cfnbootstrap) | URL of the tar.gz bundle containing the CFN bootstrap utilities | `string` | `"https://s3.amazonaws.com/cloudformation-examples/aws-cfn-bootstrap-py3-latest.tar.gz"` | no |
| <a name="input_amigen_aws_cliv1_source"></a> [amigen\_aws\_cliv1\_source](#input\_amigen\_aws\_cliv1\_source) | URL of the .zip bundle containing the installer for AWS CLI v1 | `string` | `""` | no |
| <a name="input_amigen_aws_cliv2_source"></a> [amigen\_aws\_cliv2\_source](#input\_amigen\_aws\_cliv2\_source) | URL of the .zip bundle containing the installer for AWS CLI v2 | `string` | `"https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip"` | no |
| <a name="input_amigen_build_device"></a> [amigen\_build\_device](#input\_amigen\_build\_device) | Path of the build device that will be partitioned to create the image | `string` | `"/dev/nvme0n1"` | no |
| <a name="input_amigen_fips_disable"></a> [amigen\_fips\_disable](#input\_amigen\_fips\_disable) | Toggles whether FIPS will be disabled in the images | `bool` | `false` | no |
| <a name="input_amigen_grub_timeout"></a> [amigen\_grub\_timeout](#input\_amigen\_grub\_timeout) | Timeout value to set in the grub config of each image | `number` | `1` | no |
| <a name="input_amigen_use_default_repos"></a> [amigen\_use\_default\_repos](#input\_amigen\_use\_default\_repos) | Modifies the behavior of `amigen_repo_names`. When true, `amigen_repo_names` are appended to the enabled repos. When false, `amigen_repo_names` are used exclusively | `bool` | `true` | no |
| <a name="input_aws_ami_groups"></a> [aws\_ami\_groups](#input\_aws\_ami\_groups) | List of groups that have access to launch the resulting AMIs. Keyword `all` will make the AMIs publicly accessible | `list(string)` | `[]` | no |
| <a name="input_aws_ami_regions"></a> [aws\_ami\_regions](#input\_aws\_ami\_regions) | List of regions to copy the AMIs to. Tags and attributes are copied along with the AMIs | `list(string)` | `[]` | no |
| <a name="input_aws_ami_users"></a> [aws\_ami\_users](#input\_aws\_ami\_users) | List of account IDs that have access to launch the resulting AMIs | `list(string)` | `[]` | no |
| <a name="input_aws_force_deregister"></a> [aws\_force\_deregister](#input\_aws\_force\_deregister) | Force deregister an existing AMI if one with the same name already exists | `bool` | `false` | no |
| <a name="input_aws_instance_type"></a> [aws\_instance\_type](#input\_aws\_instance\_type) | EC2 instance type to use while building the AMIs | `string` | `"t3.2xlarge"` | no |
| <a name="input_aws_region"></a> [aws\_region](#input\_aws\_region) | Name of the AWS region in which to launch the EC2 instance to create the AMIs | `string` | `"us-east-1"` | no |
| <a name="input_aws_source_ami_filter_centos7_hvm"></a> [aws\_source\_ami\_filter\_centos7\_hvm](#input\_aws\_source\_ami\_filter\_centos7\_hvm) | Object with source AMI filters for CentOS 7 HVM builds | <pre>object({<br>    name   = string<br>    owners = list(string)<br>  })</pre> | <pre>{<br>  "name": "CentOS 7.* x86_64,*-Recovery (No-LVM)-ACB-CentOS7-HVM-SRIOV_ENA",<br>  "owners": [<br>    "125523088429",<br>    "701759196663",<br>    "039368651566"<br>  ]<br>}</pre> | no |
| <a name="input_aws_source_ami_filter_centos8stream_hvm"></a> [aws\_source\_ami\_filter\_centos8stream\_hvm](#input\_aws\_source\_ami\_filter\_centos8stream\_hvm) | Object with source AMI filters for CentOS Stream 8 HVM builds | <pre>object({<br>    name   = string<br>    owners = list(string)<br>  })</pre> | <pre>{<br>  "name": "CentOS Stream 8 x86_64 *,spel-bootstrap-centos-8stream-hvm-*.x86_64-gp2",<br>  "owners": [<br>    "125523088429",<br>    "701759196663",<br>    "039368651566"<br>  ]<br>}</pre> | no |
| <a name="input_aws_source_ami_filter_ol8_hvm"></a> [aws\_source\_ami\_filter\_ol8\_hvm](#input\_aws\_source\_ami\_filter\_ol8\_hvm) | Object with source AMI filters for Oracle Linux 8 HVM builds | <pre>object({<br>    name   = string<br>    owners = list(string)<br>  })</pre> | <pre>{<br>  "name": "OL8.*-x86_64-HVM-*,spel-bootstrap-oraclelinux-8-hvm-*.x86_64-gp2",<br>  "owners": [<br>    "131827586825",<br>    "039368651566"<br>  ]<br>}</pre> | no |
| <a name="input_aws_source_ami_filter_rhel7_hvm"></a> [aws\_source\_ami\_filter\_rhel7\_hvm](#input\_aws\_source\_ami\_filter\_rhel7\_hvm) | Object with source AMI filters for RHEL 7 HVM builds | <pre>object({<br>    name   = string<br>    owners = list(string)<br>  })</pre> | <pre>{<br>  "name": "RHEL-7.*_HVM-*-x86_64-*-Hourly*-GP2",<br>  "owners": [<br>    "309956199498",<br>    "219670896067"<br>  ]<br>}</pre> | no |
| <a name="input_aws_source_ami_filter_rhel8_hvm"></a> [aws\_source\_ami\_filter\_rhel8\_hvm](#input\_aws\_source\_ami\_filter\_rhel8\_hvm) | Object with source AMI filters for RHEL 8 HVM builds | <pre>object({<br>    name   = string<br>    owners = list(string)<br>  })</pre> | <pre>{<br>  "name": "RHEL-8.*_HVM-*-x86_64-*-Hourly*-GP2",<br>  "owners": [<br>    "309956199498",<br>    "219670896067"<br>  ]<br>}</pre> | no |
| <a name="input_aws_ssh_interface"></a> [aws\_ssh\_interface](#input\_aws\_ssh\_interface) | Specifies method used to select the value for the host in the SSH connection | `string` | `"public_dns"` | no |
| <a name="input_aws_subnet_id"></a> [aws\_subnet\_id](#input\_aws\_subnet\_id) | ID of the subnet where Packer will launch the EC2 instance. Required if using an non-default VPC | `string` | `null` | no |
| <a name="input_aws_temporary_security_group_source_cidrs"></a> [aws\_temporary\_security\_group\_source\_cidrs](#input\_aws\_temporary\_security\_group\_source\_cidrs) | List of IPv4 CIDR blocks to be authorized access to the instance | `list(string)` | <pre>[<br>  "0.0.0.0/0"<br>]</pre> | no |
| <a name="input_azure_build_resource_group_name"></a> [azure\_build\_resource\_group\_name](#input\_azure\_build\_resource\_group\_name) | Existing resource group in which the build will run | `string` | `null` | no |
| <a name="input_azure_client_id"></a> [azure\_client\_id](#input\_azure\_client\_id) | Application ID of the AAD Service Principal. Requires either client\_secret, client\_cert\_path or client\_jwt to be set as well | `string` | `null` | no |
| <a name="input_azure_client_secret"></a> [azure\_client\_secret](#input\_azure\_client\_secret) | Password/secret registered for the AAD Service Principal | `string` | `null` | no |
| <a name="input_azure_cloud_environment_name"></a> [azure\_cloud\_environment\_name](#input\_azure\_cloud\_environment\_name) | One of Public, China, Germany, or USGovernment. Defaults to Public. Long forms such as USGovernmentCloud and AzureUSGovernmentCloud are also supported | `string` | `"Public"` | no |
| <a name="input_azure_custom_managed_image_name_centos7"></a> [azure\_custom\_managed\_image\_name\_centos7](#input\_azure\_custom\_managed\_image\_name\_centos7) | Name of a custom managed image to use as the base image for CentOS7 builds | `string` | `null` | no |
| <a name="input_azure_custom_managed_image_name_rhel7"></a> [azure\_custom\_managed\_image\_name\_rhel7](#input\_azure\_custom\_managed\_image\_name\_rhel7) | Name of a custom managed image to use as the base image for RHEL7 builds | `string` | `null` | no |
| <a name="input_azure_custom_managed_image_name_rhel8"></a> [azure\_custom\_managed\_image\_name\_rhel8](#input\_azure\_custom\_managed\_image\_name\_rhel8) | Name of a custom managed image to use as the base image for RHEL8 builds | `string` | `null` | no |
| <a name="input_azure_custom_managed_image_resource_group_name_centos7"></a> [azure\_custom\_managed\_image\_resource\_group\_name\_centos7](#input\_azure\_custom\_managed\_image\_resource\_group\_name\_centos7) | Name of the resource group for the custom image in `azure_custom_managed_image_name_centos7` | `string` | `null` | no |
| <a name="input_azure_custom_managed_image_resource_group_name_rhel7"></a> [azure\_custom\_managed\_image\_resource\_group\_name\_rhel7](#input\_azure\_custom\_managed\_image\_resource\_group\_name\_rhel7) | Name of the resource group for the custom image in `azure_custom_managed_image_name_rhel7` | `string` | `null` | no |
| <a name="input_azure_custom_managed_image_resource_group_name_rhel8"></a> [azure\_custom\_managed\_image\_resource\_group\_name\_rhel8](#input\_azure\_custom\_managed\_image\_resource\_group\_name\_rhel8) | Name of the resource group for the custom image in `azure_custom_managed_image_name_rhel8` | `string` | `null` | no |
| <a name="input_azure_image_offer"></a> [azure\_image\_offer](#input\_azure\_image\_offer) | Name of the publisher offer to use for your base image (Azure Marketplace Images only) | `string` | `null` | no |
| <a name="input_azure_image_publisher"></a> [azure\_image\_publisher](#input\_azure\_image\_publisher) | Name of the publisher to use for your base image (Azure Marketplace Images only) | `string` | `null` | no |
| <a name="input_azure_image_sku"></a> [azure\_image\_sku](#input\_azure\_image\_sku) | SKU of the image offer to use for your base image (Azure Marketplace Images only) | `string` | `null` | no |
| <a name="input_azure_keep_os_disk"></a> [azure\_keep\_os\_disk](#input\_azure\_keep\_os\_disk) | Boolean toggle whether to keep the managed disk or delete it after packer runs | `bool` | `false` | no |
| <a name="input_azure_location"></a> [azure\_location](#input\_azure\_location) | Azure datacenter in which your VM will build | `string` | `null` | no |
| <a name="input_azure_managed_image_resource_group_name"></a> [azure\_managed\_image\_resource\_group\_name](#input\_azure\_managed\_image\_resource\_group\_name) | Resource group name where the result of the Packer build will be saved. The resource group must already exist | `string` | `null` | no |
| <a name="input_azure_private_virtual_network_with_public_ip"></a> [azure\_private\_virtual\_network\_with\_public\_ip](#input\_azure\_private\_virtual\_network\_with\_public\_ip) | Boolean toggle whether a public IP will be assigned when using `azure_virtual_network_name` | `bool` | `null` | no |
| <a name="input_azure_subscription_id"></a> [azure\_subscription\_id](#input\_azure\_subscription\_id) | n/a | `string` | `null` | no |
| <a name="input_azure_virtual_network_name"></a> [azure\_virtual\_network\_name](#input\_azure\_virtual\_network\_name) | Name of a pre-existing virtual network in which to run the build | `string` | `null` | no |
| <a name="input_azure_virtual_network_resource_group_name"></a> [azure\_virtual\_network\_resource\_group\_name](#input\_azure\_virtual\_network\_resource\_group\_name) | Name of the virtual network resource group in which to run the build | `string` | `null` | no |
| <a name="input_azure_virtual_network_subnet_name"></a> [azure\_virtual\_network\_subnet\_name](#input\_azure\_virtual\_network\_subnet\_name) | Name of the subnet in which to run the build | `string` | `null` | no |
| <a name="input_azure_vm_size"></a> [azure\_vm\_size](#input\_azure\_vm\_size) | n/a | `string` | `"Standard_DS5_v2"` | no |
| <a name="input_openstack_flavor"></a> [openstack\_flavor](#input\_openstack\_flavor) | ID, name, or full URL for the desired flavor for the server to be created | `string` | `null` | no |
| <a name="input_openstack_floating_ip_network_name"></a> [openstack\_floating\_ip\_network\_name](#input\_openstack\_floating\_ip\_network\_name) | ID or name of an external network that can be used for creation of a new floating IP | `string` | `null` | no |
| <a name="input_openstack_insecure"></a> [openstack\_insecure](#input\_openstack\_insecure) | Boolean whether the connection to OpenStack can be done over an insecure connection | `bool` | `false` | no |
| <a name="input_openstack_networks"></a> [openstack\_networks](#input\_openstack\_networks) | List of networks by UUID to attach to this instance | `list(string)` | `[]` | no |
| <a name="input_openstack_security_groups"></a> [openstack\_security\_groups](#input\_openstack\_security\_groups) | List of security groups by name to add to this instance | `list(string)` | `[]` | no |
| <a name="input_openstack_source_image_name"></a> [openstack\_source\_image\_name](#input\_openstack\_source\_image\_name) | Name of the base image to use | `string` | `null` | no |
| <a name="input_spel_description_url"></a> [spel\_description\_url](#input\_spel\_description\_url) | URL included in the AMI description | `string` | `"https://github.com/plus3it/spel"` | no |
| <a name="input_spel_http_proxy"></a> [spel\_http\_proxy](#input\_spel\_http\_proxy) | Used as the value for the git config http.proxy setting in the builder nodes | `string` | `""` | no |
| <a name="input_spel_root_volume_size"></a> [spel\_root\_volume\_size](#input\_spel\_root\_volume\_size) | Size in GB of the root volume | `number` | `20` | no |
| <a name="input_spel_ssh_username"></a> [spel\_ssh\_username](#input\_spel\_ssh\_username) | Name of the user for the ssh connection to the instance. Defaults to `spel`, which is set by cloud-config userdata. If your starting image does not have `cloud-init` installed, override the default user name | `string` | `"spel"` | no |
| <a name="input_virtualbox_iso_url_centos7"></a> [virtualbox\_iso\_url\_centos7](#input\_virtualbox\_iso\_url\_centos7) | URL to the CentOS7 .iso to use for Virtualbox builds | `string` | `"http://mirror.facebook.net/centos/7/isos/x86_64/CentOS-7-x86_64-Minimal-2009.iso"` | no |
| <a name="input_virtualbox_iso_url_centos8"></a> [virtualbox\_iso\_url\_centos8](#input\_virtualbox\_iso\_url\_centos8) | URL to the CentOS8 .iso to use for Virtualbox builds | `string` | `"http://mirror.facebook.net/centos/8-stream/isos/x86_64/CentOS-Stream-8-x86_64-latest-dvd1.iso"` | no |
| <a name="input_virtualbox_vagrantcloud_username"></a> [virtualbox\_vagrantcloud\_username](#input\_virtualbox\_vagrantcloud\_username) | Vagrant Cloud username, used to namespace the vagrant boxes | `string` | `null` | no |

<!-- END TFDOCS -->