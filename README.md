# Ray Tracer Cube Texturizado

Raytracer en Rust que renderiza un cubo con textura Fabric006 https://ambientcg.com/view?id=Fabric006 e iluminacion difusa (Lambert)
## Como correrlo
```
cargo run --release
```

## Estructura

- `src/vec3.rs`: vector 3D y normalizacion.
- `src/material.rs`: color difuso del material.
- `src/light.rs`: luz puntual de la escena.
- `src/texture.rs`: carga la imagen y muestrea el color segun coordenadas UV.
- `src/cube.rs`: interseccion rayo-caja (metodo de slabs), normales y UV por cara.
- `src/ray_intersect.rs`: trait `RayIntersect` y el enum `Object` de la escena.
- `src/raytracer.rs`: `cast_ray` (ambiente + difusa) y el loop de `render`.
- `src/framebuffer.rs`: framebuffer de software sobre una ventana de raylib.
- `src/main.rs`: arma la escena y el loop principal.
