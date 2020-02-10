# OpenGL

## State machine

OpenGL is by itself a large state machine: a collection of variables that define how OpenGL should currently operate. The state of OpenGL is commonly referred to as the OpenGL context. When using OpenGL, we often change its state by setting some options, manipulating some buffers and then render using the current context.

Whenever we tell OpenGL that we now want to draw lines instead of triangles for example, we change the state of OpenGL by changing some context variable that sets how OpenGL should draw. As soon as we change the context by telling OpenGL it should draw lines, the next drawing commands will now draw lines instead of triangles.

When working in OpenGL we will come across several state-changing functions that change the context and several state-using functions that perform some operations based on the current state of OpenGL. As long as you keep in mind that OpenGL is basically one large state machine, most of its functionality will make more sense.



## Objects

The OpenGL libraries are written in C and allows for many derivation.



## VBO

Example:

```cpp
// 0. Copy our vertices array in a buffer for OpenGL to use
glBindBuffer(GL_ARRAY_BUFFER, VBO);
glBufferData(GL_ARRAY_BUFFER, sizeof(vertices), vertices, GL_STATIC_DRAW);

// 1. then set the vertex attributes pointers
glVertexAttribPointer(0, 3, GL_FLOAT, GL_FALSE, 3 * sizeof(float), (void*)0);
glEnableVertexAttribArray(0);

// 2. use our shader program when we want to render an object
glUseProgram(shaderProgram);

 // 3. now draw the object
 someOpenGLFunctionThatDrawsOurTriangle(); 
```

## Wireframe Mode

To draw your triangles in wireframe mode, you can configure how OpenGL draws its draws its primitives via 

```cpp
glPolygonMode(GL_FRONT_AND_BACK, GL_LINE);
```

The first argument says we want to apply it to the font and back of all triangles and the second line tell us to draw them as lines. 

Any subsequent drawing calls will render the triangles in wireframe mode until we set it back to its default using 

```cpp
glPolygonMode(GL_FLOAT_AND_BACK, GL_FILL);
```

