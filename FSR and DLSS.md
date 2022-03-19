# What is Fidelity FX Super Resolution?

Fidelity FX Super Resolution, normally referred to as FSR, is a technology that uses an upscale pass and a sharpening one to artificially increase the image resolution to the desired one.

## Why use FSR?

When dealing with high-resolution or complex games, a high-performing GPU can sometimes struggle due to the resolution, complexity, or even bad optimization, and technologies to upscale enters to turn more circumvent these problems.

## When to use FSR

Due to FSR being an addition to the render pipeline, it adds frame time latency at the same time it improves performance, a trade that favors games without a competitive nature or can simply save the game to low-end computers.

## What is upscale?

Upscale is when an image gets converted to a higher resolution, something that causes the final image to be blocky and bland, as the pixels get enlarged.

As the drawbacks of upscaling are the graphical quality loss, algorithms exist to mitigate that, like Anti-Aliasing which reduces jagged lines and denoisers that reduce render noise.

## Why sharpen an image?

When upscaling, the borders get less defined as it can sometimes cause the forms in the image to lose their borders, or some thin lines are completely erased, so a sharpening pass helps to improve the quality of the final render.

## How it is implemented?

FSR uses a standard render pipeline to ensure the best quality and avoid problems, with an order that prioritizes not introducing much noise into the final render.

![FSR pipeline](https://gpuopen.com/wp-content/uploads/2021/07/fsr_where_in_frame_source_light.png)

As implementing it can sometimes be challenging, it needs to be tested as image artifacts happen and are considered a common issue, with other common issues being listed below.

*   rendering noise
*   blocky image
*   distortion
*   Important assets with fine lines being erased
*   Anti-aliasing applied after FSR or not being applied at all

## How to test FSR?

To test FSR, it is important to focus on the dependencies and weaknesses of the algorithm, like focusing on the render pipeline order like introducing noise before the FSR being applied, rendering related crashes, and interaction with other features like dynamic resolution or raytracing that can cause problems depending on how the tech was implemented.

# What is Deep learning super sampling?

Deep learning super sampling also known as DLSS is an upscale technology similar to FSR that uses deep learning to upscale and treat images with the promise of offering high performance with artificially created high resolutions that seem close to a native resolution one by allowing the majority of the rendering pipeline to occur in a lower resolution than the intended output.

## How does it work?

DLSS uses a low-resolution image, motion vectors, depth, exposure, and brightness information in with each piece of information is used by the algorithm to understand and upscale while applying temporal anti-aliasing using the motion vectors and a denoiser using Nvidia Image Denoiser(NIS).

As DLSS is a Temporal Anti-aliasing Upsample(TAAU), it does not create new data from the information provided by the engine, it tries to recover data from previous frames, making low-resolution textures still being low resolution, and it is the motive that Nvidia recommends that developers use texture resolutions higher than the normal for the source resolution.

## Why use DLSS?

Due to DLSS allowing the majority of the rendering pipeline to run on lower resolutions, it can boost performance and allow smoother gameplay to the end-user.

## When using DLSS?

As DLSS is adding process time to the render pipeline like the FSR, it is better to use it on non-competitive games to not impact the frame times.

## Problems that can happen

*   Noise in the final render due to a problem on NIS or added after the NIS pass.
*   Ghosting in the final render especially on darker ambients dua to the TAA part of the pipeline
*   Low texture quality when the developers did not follow Nvidia recommendations
*   Fine lines flicker when displayed close to each other like in a fence or ventilation grill.
*   Important assets with fine lines being erased due to the limited information about them on the low-resolution raw image
*   The conflict between other rendering options like Danymic resolution that DLSS does not support and can cause major issues