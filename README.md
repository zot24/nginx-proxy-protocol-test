# How to

http://docs.aws.amazon.com/elasticloadbalancing/latest/classic/enable-proxy-protocol.html

```
aws elb describe-load-balancers --profile development
```

```
aws elb create-load-balancer-policy --load-balancer-name israel --policy-name israel-ProxyProtocol-policy --policy-type-name ProxyProtocolPolicyType --policy-attributes AttributeName=ProxyProtocol,AttributeValue=true --profile development
```

```
aws elb set-load-balancer-policies-for-backend-server --load-balancer-name israel --instance-port 80 --policy-names israel-ProxyProtocol-policy --profile development
```

# Resources

- https://davidbeath.com/posts/elb-nginx-proxy-forwarding.html