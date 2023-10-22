###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GetProperty

Get a property on a set of properties 

## Syntax

```c
void* SDL_GetProperty(SDL_PropertiesID props, const char *name);

```

## Function Parameters

|               |                                   |
| ------------- | --------------------------------- |
| **props**     | the properties to query           |
| **name**      | the name of the property to query |

## Return Value

Returns the value of the property, or NULL if it is not set.

## Thread Safety

It is safe to call this function from any thread, although the data
returned is not protected and could potentially be freed if you call
[SDL_SetProperty](SDL_SetProperty)() or
[SDL_ClearProperty](SDL_ClearProperty)() on these properties from another
thread. If you need to avoid this, use
[SDL_LockProperties](SDL_LockProperties)() and
[SDL_UnlockProperties](SDL_UnlockProperties)().

## Version

This function is available since SDL 3.0.0.

## Related Functions

* [SDL_SetProperty](SDL_SetProperty)

----
[CategoryAPI](CategoryAPI)
