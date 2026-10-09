Changed

- **A restart whose stored tip is already current goes straight to tip follow.** The tip must meet minimum chain work and sit inside the configured max tip age (24 hours unless the operator set another). A heavier header chain still in the store still runs catch-up. How far peers advertise their height does not decide this.
