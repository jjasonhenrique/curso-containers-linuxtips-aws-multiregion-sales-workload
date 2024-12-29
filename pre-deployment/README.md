<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 5.82.2 |
| <a name="provider_aws.secondary"></a> [aws.secondary](#provider\_aws.secondary) | 5.82.2 |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_appautoscaling_policy.idempotency_read](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_policy) | resource |
| [aws_appautoscaling_policy.idempotency_write](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_policy) | resource |
| [aws_appautoscaling_policy.sales_read](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_policy) | resource |
| [aws_appautoscaling_policy.sales_write](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_policy) | resource |
| [aws_appautoscaling_target.idempotency_read](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_target) | resource |
| [aws_appautoscaling_target.idempotency_write](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_target) | resource |
| [aws_appautoscaling_target.sales_read](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_target) | resource |
| [aws_appautoscaling_target.sales_write](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/appautoscaling_target) | resource |
| [aws_dynamodb_table.idempotency](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/dynamodb_table) | resource |
| [aws_dynamodb_table.sales](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/dynamodb_table) | resource |
| [aws_dynamodb_table_replica.idempotency](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/dynamodb_table_replica) | resource |
| [aws_dynamodb_table_replica.sales](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/dynamodb_table_replica) | resource |
| [aws_ssm_parameter.primary](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ssm_parameter) | resource |
| [aws_ssm_parameter.secondary](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/ssm_parameter) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_active_states"></a> [active\_states](#input\_active\_states) | n/a | <pre>object({<br/>    us-east-1 = string<br/>    sa-east-1 = string<br/>  })</pre> | n/a | yes |
| <a name="input_dynamodb_idempotency"></a> [dynamodb\_idempotency](#input\_dynamodb\_idempotency) | n/a | <pre>object({<br/>    name                   = string<br/>    billing_mode           = string<br/>    point_in_time_recovery = bool<br/><br/>    read_min                 = number<br/>    read_max                 = number<br/>    read_autoscale_threshold = number<br/><br/>    write_min                 = number<br/>    write_max                 = number<br/>    write_autoscale_threshold = number<br/>  })</pre> | n/a | yes |
| <a name="input_dynamodb_sales"></a> [dynamodb\_sales](#input\_dynamodb\_sales) | n/a | <pre>object({<br/>    name                   = string<br/>    billing_mode           = string<br/>    point_in_time_recovery = bool<br/><br/>    read_min                 = number<br/>    read_max                 = number<br/>    read_autoscale_threshold = number<br/><br/>    write_min                 = number<br/>    write_max                 = number<br/>    write_autoscale_threshold = number<br/>  })</pre> | n/a | yes |
| <a name="input_project_name"></a> [project\_name](#input\_project\_name) | n/a | `string` | n/a | yes |
| <a name="input_region_primary"></a> [region\_primary](#input\_region\_primary) | n/a | `string` | n/a | yes |
| <a name="input_region_secondary"></a> [region\_secondary](#input\_region\_secondary) | n/a | `string` | n/a | yes |

## Outputs

No outputs.
<!-- END_TF_DOCS -->