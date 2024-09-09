###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetGPUSwapchainParameters

Changes the swapchain parameters for the given claimed window.

## Header File

Defined in [<SDL3/SDL_gpu.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gpu.h)

## Syntax

```c
SDL_bool SDL_SetGPUSwapchainParameters(
    SDL_GPUDevice *device,
    SDL_Window *window,
    SDL_GPUSwapchainComposition swapchain_composition,
    SDL_GPUPresentMode present_mode);
```

## Function Parameters

|                                                            |                           |                                                    |
| ---------------------------------------------------------- | ------------------------- | -------------------------------------------------- |
| [SDL_GPUDevice](SDL_GPUDevice) *                           | **device**                | a GPU context.                                     |
| [SDL_Window](SDL_Window) *                                 | **window**                | an [SDL_Window](SDL_Window) that has been claimed. |
| [SDL_GPUSwapchainComposition](SDL_GPUSwapchainComposition) | **swapchain_composition** | the desired composition of the swapchain.          |
| [SDL_GPUPresentMode](SDL_GPUPresentMode)                   | **present_mode**          | the desired present mode for the swapchain.        |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) if successful,
[SDL_FALSE](SDL_FALSE) on error.

## Remarks

This function will fail if the requested present mode or swapchain
composition are unsupported by the device. Check if the parameters are
supported via
[SDL_WindowSupportsGPUPresentMode](SDL_WindowSupportsGPUPresentMode) /
[SDL_WindowSupportsGPUSwapchainComposition](SDL_WindowSupportsGPUSwapchainComposition)
prior to calling this function.

[SDL_GPU_PRESENTMODE_VSYNC](SDL_GPU_PRESENTMODE_VSYNC) and
[SDL_GPU_SWAPCHAINCOMPOSITION_SDR](SDL_GPU_SWAPCHAINCOMPOSITION_SDR) are
always supported.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_WindowSupportsGPUPresentMode](SDL_WindowSupportsGPUPresentMode)
- [SDL_WindowSupportsGPUSwapchainComposition](SDL_WindowSupportsGPUSwapchainComposition)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGPU](CategoryGPU)
