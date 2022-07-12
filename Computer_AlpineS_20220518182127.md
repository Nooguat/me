# Alpine services issues
for alpine, the only way to restart the services correctly is by controlling them directly
example with sshd

```/etc/init.d/sshd restart ```
not 
```rc-service sshd restart ```


[Sources]
