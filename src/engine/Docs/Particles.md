The easiest way to create a `ParticleEmitter` is to use the 
[Particle Tester](http://excaliburjs.com/particle-tester/) to generate code for emitters.

## Example: Adding an emitter

```js
var actor = new ex.Actor(...);
var emitter = new ex.ParticleEmitter(...);
emitter.emitterType = ex.EmitterType.Circle; // Shape of emitter nozzle 
emitter.radius = 5;
emitter.minVel = 100;
emitter.maxVel = 200;
emitter.minAngle = 0;
emitter.maxAngle = Math.PI * 2;
emitter.emitRate = 300; // 300 particles/second
emitter.opacity = 0.5;
emitter.fadeFlag = true; // fade particles overtime
emitter.particleLife = 1000; // in milliseconds = 1 sec
emitter.maxSize = 10; // in pixels
emitter.minSize = 1;
emitter.particleColor = ex.Color.Rose;
// set emitter settings
emitter.isEmitting = true;  // should the emitter be emitting
// add the emitter as a child actor, it will draw on top of the parent actor
// and move with the parent
actor.add(emitter);
// or, alternatively, add it to the current scene
engine.add(emitter);
```

Note: When overriding the draw method, make sure to call ```super.draw``` or draw all of the actor's children manually.
