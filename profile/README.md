# OrionECS

A comprehensive and high-performance **Entity Component System (ECS)** framework written in TypeScript, designed for building games, simulations, and interactive applications.

## About

OrionECS provides a modern, type-safe approach to component-based architecture with a focus on performance and developer experience. Whether you're building a game engine, simulation system, or any application that benefits from composition over inheritance, OrionECS has you covered.

## Key Features

- **Efficient Entity Management** - Object pooling and optimized component storage
- **Advanced Query System** - Support for ALL, ANY, and NOT queries with tag-based filtering
- **Priority-Based Systems** - Configurable execution order with lifecycle hooks
- **Component Archetypes** - Improved cache locality for better performance
- **Memory Management** - Automatic pooling with built-in profiling and metrics
- **Change Detection** - Component versioning for selective updates
- **Entity Relationships** - Parent/child hierarchies with automatic cleanup
- **Plugin System** - Extensible architecture for custom features
- **Prefabs** - Template-based entity creation
- **Serialization** - World state snapshots for save/load functionality

## Quick Start

```bash
npm install @orion-ecs/core
```

```typescript
import { EngineBuilder } from '@orion-ecs/core';

const game = new EngineBuilder()
  .withFixedUpdateFPS(60)
  .withDebugMode(true)
  .build();

game.createSystem('MovementSystem', {
  all: [Position, Velocity],
  tags: ['active']
}, {
  priority: 10,
  act: (entity, position, velocity) => {
    position.x += velocity.x;
    position.y += velocity.y;
  }
});
```

## Resources

| Resource | Link |
|----------|------|
| Main Repository | [OrionECS](https://github.com/tyevco/OrionECS) |
| Documentation | See the docs folder in the main repo |
| NPM Package | [@orion-ecs/core](https://www.npmjs.com/package/@orion-ecs/core) |

## Contributing

We welcome contributions! Check out the main [OrionECS repository](https://github.com/tyevco/OrionECS) for contribution guidelines and open issues.

## License

MIT