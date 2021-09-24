# Troubleshooting
This section covers some common errors or problems you might run into while
using your Managed Service for TimescaleDB account.

## Database is low on disk, memory, or CPU
When your database reaches 90% of your allocated disk, memory, or CPU resources,
an automated message is sent to the email address listed on your account. The
email looks like this:

```txt
Your Managed Service for TimescaleDB service, in project "ExampleAccount", is running low on
CPU. Running low on CPU affects performance and could affect service
availability. Please either optimize your usage pattern or reduce the workload,
and consider upgrading to a larger plan to avoid service outage.
```

You can resolve this by logging in to your Managed Service for TimescaleDB
account and increasing your available resources. From the Managed Service for
TimescaleDB Dashboard, select the service that you want to increase resources
for. In the `Overview` tab, locate the `Service Plan` section, and click
`Upgrade Plan`. Select the plan that suits your requirements, and click
`Upgrade` to enable the additional resources.

If you run out of resources regularly, you might need to consider using your
resources more efficiently. Consider enabling [compression][howto-compression],
using [continuous aggregates][howto-caggs], or
[configuring data retention][howto-dataretention] to reduce the amount of
resources your database uses. If you still need help, reach out to our [support
team][timescale-support] to have a conversation.

[howto-compression]: /timescaledb/:currentVersion:/how-to-guides/compression
[howto-caggs]: /timescaledb/:currentVersion:/how-to-guides/continuous-aggregates
[howto-dataretention]: /timescaledb/:currentVersion:/how-to-guides/data-retention
[timescale-support]: https://www.timescale.com/support