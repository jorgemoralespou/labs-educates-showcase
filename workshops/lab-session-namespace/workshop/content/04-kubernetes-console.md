To provide a visual way of viewing workloads deployed to the Kubernetes cluster
an embeded Kubernetes console can be enabled.

```dashboard:open-dashboard
name: Console
```

A workshop user can then navigate using the console to view the deployment
and associated pods, as well as access logs.

If you want to provide a more guided experience, it is possible to provide
clickable actions which will switch what the console is showing.

```dashboard:reload-dashboard
prefix: Console
title: View deployment for "blog"
description: ""
name: Console
url: {{ingress_protocol}}://console-{{session_namespace}}.{{ingress_domain}}/#/deployment/{{session_namespace}}/blog?namespace={{session_namespace}}
```

For command line warriors, `k9s` can be used from the command line:

```terminal:execute
command: k9s
```

with basic navigation still possible through prompted text input:

```terminal:input
text: ":deployments"
endl: true
```

Exit `k9s` when done.

```terminal:input
text: ":quit"
endl: true
```
