# Max Dore Shadowing Kick Off

Service Partner: if you don't have the bandwidth at certain times, a Service Partner
                 might be able to help you out

We do this upgrade first, before the Production upgrade, so we know what's ahead
- If we encounter any issues, we know how to handle them beforehand



**QUESTION**
If there are any issues during the Production Upgrade, they will be handed off to
a queue, and will re-appear at the end of the process

For me to get a better understanding of your use of the platform, what areas do
you most utilize?




It's **important** to note that your `instance` will work exactly as it did in `Express`,
you'll just be gaining access to __new features__ you can choose to use _when you want_
- If you want to use Workflows and Enterprise SLAs, you'll have to do a few things
`Workflows:` in the filter navigator, type in `approval engines`
- At the current moment, some approval rules and execution plans are being run
  - If you want to utilize a workflow on that table, you have to come into this
    table here and ensure that the engines are turned off, so the system knows
    what to do
  - If you want to use workflows on tables, turn the engines off
`SLAs:` when you want to use Enterprise SLAs, change this value to `false`


type into **filter navigator:** `sys_properties.list`
type into **name field:** `com.snc.sla.run_old_sla_engine`


"Best practice is to..." versus "Best practice states that...."
