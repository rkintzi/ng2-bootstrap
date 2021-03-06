### Usage
```typescript
import {progressbar} from 'ng2-bootstrap';
```

### Annotations
```typescript
// class Progress
@Directive({
  selector: 'bs-progress, [progress]',
  properties: ['animate', 'max'],
  host: {
    'class': 'progress',
    '[attr.max]': 'max'
  },
  lifecycle: [LifecycleEvent.onInit]
})

// class Bar
@Component({
  selector: 'bar, [bar]',
  properties: ['type', 'value'],
  lifecycle: [LifecycleEvent.onInit, LifecycleEvent.onDestroy]
})

// class Progressbar
@Component({
  selector: 'progressbar, [progressbar]',
  properties: ['animate', 'max', 'type', 'value']
})
```

### Properties
**Note**: all components have same meaning of properties
  - `value` (`*number`) - current value of progress bar
  - `type` (`*string`) - provide one of the four supported contextual classes:
  `success`,`info`, `warning`, `danger`
  - `max` (`?number=100`) - maximum total value of progress element
  - `animate` (`?boolean=true`) - if `true` changing `value` of progress bar will be animated (*note*: not supported by Bootstrap 4)
