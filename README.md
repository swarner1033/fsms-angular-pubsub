![Build Status](https://github.com/actions/fsms-angular-pubsub/workflows/build/badge.svg))

# Angular Pub/Sub Framework for Angular versions

Angular publish subscribe framework powered by RxJX.

## Usage

- Run below to install

```
npm i -S fsms-angular-pubsub
```

- Initialize module for root in your angular root module

```ts
...

import { PubSubModule } from 'fsms-angular-pubsub'; // <= HERE

@NgModule({
declarations: [
   RootComponent,
   NavigationComponent,
   OverlayComponent
],
imports: [
   BrowserModule,
   FormsModule,
   HttpModule,
   PubSubModule.forRoot() // <= AND HERE
],
providers: [],
bootstrap: [RootComponent]
})

...
```

- Import & Inject `PubSubService` service where ever you want to use.

### Subscribe

```ts
import { PubSubService } from './pubsub.service';
...
constructor(private messageService: PubSubService) { }
...

messageService.subscribe({
        message: { type: 'orderready' },
        callback: () => console.log('happy'),
      });
```
### Publish

```ts
import { PubSubService } from './pubsub.service';
...
constructor(private messageService: PubSubService) { }
...

messageService.publish(message: { type: 'orderready' });
```

### Thank You!

**💖 Say 👋 to me!**
Rupesh Tiwari
<a href="https://www.rupeshtiwari.com"> www.rupeshtiwari.com</a> 
✉️ <a href="mailto:fullstackmaster1@gmail.com?subject=Hi"> Email Rupesh</a>
Founder of <a href="https://www.fullstackmaster.net"> Fullstack Master</a>

