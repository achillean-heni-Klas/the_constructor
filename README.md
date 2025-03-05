# node-log

stupid simple logging. no levels. no formatters. just write to file.

```javascript
const log = require('node-log')

log('server started')
log('user login:', userId)
log('error:', err.message)
```

writes to `app.log` with timestamp. done.

### why

winston has 47 options. pino needs configuration. console.log disappears.

i just wanted append-to-file with dates.

### options (all optional)

```javascript
log.config({
  file: 'custom.log',  // default: app.log
  maxSize: '10mb',     // default: unlimited
  rotate: true         // default: false
})
```

### that's it

no transports. no levels. no json parsing. just text in a file.

MIT
