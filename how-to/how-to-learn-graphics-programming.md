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
10. Study other engines, preferably specialized engines as opposed to general-purpose engines. Check out talks from  - [https://twitter.com/MichalDrobot](https://twitter.com/MichalDrobot) - [https://twitter.com/MyNameIsMJP](https://twitter.com/MyNameIsMJP) - [https://twitter.com/mirror2mask](https://twitter.com/mirror2mask)
11. Learn to use the tools at your disposal. Core dumps, GPU dumps. Frame dumps, visualizers etc. Write your own tools when needed. [https://renderdoc.org/](https://renderdoc.org/) is especially useful when getting acquainted with the graphics pipeline for the first time. 
12. Ask tons of questions. Graphics is really broad and no matter how much I lean about any given topic, there's always someone that knows more than I do. Experts are usually really gracious about helping out and giving advice.
13. When you're in the industry try to shadow an artist work from time to time. \(lighting, texture, modeler, vfx technical etc.\). Seeing their workflow helps you understand how the content pipeline pieces together. You also get ideas on how to improve things. 
14. Don't spend too much time being intimidated. Take techniques/ methods/algorithms one at a time. Slow and consistent improvement is much better than trying to cram it all in at once.
15. Be quick to admit when you don't know something \(especially to yourself!\) or you'll cheat yourself of a learning opportunity. Embrace the fact that you get to work in a field that has so much to explore and learn and do. 
16. At the same time don't accept what you read online as gospel truth either. Sometimes things change\(hardware, drivers, apis, but also our understanding of the best way to do things\).
17. Don't get caught up in debates on A technique vs B technique\(eg. forward vs deferred, ect\) Learn what the techniques are and what the tradeoffs are. Implementation complexity also counts as tradeoff. 





