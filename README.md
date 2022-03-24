# create policies and roles using aws cli

- create user

```
aws iam create-user --user-name abdelali
```

- create iam policy

```
aws iam create-policy --policy-name example-policy --policy-document file://example-policy.json
```

- attach iam policy to an existed user

```
aws iam attach-user-policy --user-name abdelali --policy-arn "arn:aws:iam::123456789012:policy/example-policy"
aws iam list-attached-user-policies --user-name abdelali
```

- create a role and assign policies to it

```
aws iam create-role --role-name example-role --assume-role-policy-document file://example-role-trust-policy.json
aws iam attach-role-policy --role-name example-role --policy-arn "arn:aws:iam::aws:policy/AmazonRDSReadOnlyAccess"
aws iam list-attached-role-policies --role-name example-role
```

- refer to the below link to generate iam policies for your services

[aws generate polices](https://awspolicygen.s3.amazonaws.com/policygen.html)

- refer to the below commands to see the available cli commands

[cli commands](https://docs.aws.amazon.com/cli/latest/reference/kms/)
