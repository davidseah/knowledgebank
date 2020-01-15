# How to learn graphics programming

You don't need all of the following to get a job but just start the path and continue learning and learning.

Interview earlier than you think you're qualified and listen to feedback. Learning on a job is a lot easier than learning on the side. 

1. Don't use any commercial engine or framework to start. There's far too many "magic" involved that will prevent you from understanding what's going on. You can always reference them or use them later. 
2. Expect to have ~3 projects going on at once. When you get bored of one, hop to the other and keep cycling between them for the rest of your career. 
3. Have a prototype engine. Pick an API\( preferably Vulkan as I believe the spec is clearer for beginners than the D3D12 doc\). Don't bother wrapping anything, don't make it pretty, just make it work. This is where the majority of your experiments will happen. 
4. Have a path-tracer\(software rasterizer\). Follow Matt Pharr's book on [physically based ray tracing](https://www.amazon.com/Physically-Based-Rendering-Theory-Implementation/dp/0128006455) more or less to the letter, start to finish. 
5. Have a "production engine" which you'd release to the wild if you so choose. Use, to the best of your ability, good abstractions to abstract out platform and API differences. Attempt to chase throughput with multi threading and graph- based abstraction. 
6. Study and know linear algebra, projection geometry, geometric algebra/quaternions/dual quats, multivariate calculus, signal theory, fourier/harmonic analysis and discrete math.
7. Study and know data structures, particularly acceleration structures but also understand the importance of !/D cache utilization, effects of branching and have a feeling for the latency involved. 
8. Start reading papers and try to implement one to start. I'd recommend the unreal BRDF paper. Understand derivations and try to reproduce the results. 
9. Learn about compression and aliasing. Write a BCn codec. Read about how video codecs work \( the techniques are transferable\). Research and experiment with the various AA techniques out there\(MSAA, MLAA, FXAA, TXAA, etc\)
10. 


