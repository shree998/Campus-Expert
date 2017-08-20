Workshop Outline:

Title: Constructing a Basic Neural Network with PyTorch

  Learning Goals
    1. Understanding how a neural network works
    2. Learn to implement a neural network
    3. Be able to connect function of NN with practical applications
  
  Introduction
    Start with question such as "does anyone know what a neural network is?"
    *Show really complex neural network diagram* and tell participants they're going to know that diagram and all its uses like the back
    of their hand by the end of the workshop. Mention a few applications of NNs, so audience keeps them in mind, and then explain at end
    to tie their understanding together.
    
  Step 1: Structure of Neural Network
    - Start with most basic NN; feed-forward.
    - Input layer, hidden layer, and output layer - describe them, and how they are connected (weights and gradients).
  
  Step 2: How to Use a Neural Network
    - Follow flow of input through network
    - Detail how backpropagation works; find error from expected output, and feed it backwards through the network to update the weights
    - Probably not going into nitty-gritty details of the math, as PyTorch (and all other ML frameworks) does that for you
    
  Step 3: Implementation of Simple Neural Network with PyTorch
    - Show code snippet, and ask someone to walk me through it - hopefully fosters sense of competitiveness within attendees, encouraging
      everyone to do so
    - Probably the hardest part of the presentation for beginners, as everyone will be introduced to libraries/functions they don't know
    - PyTorch's website has a good implementation of a simple NN in their 60min crash course
      Link --> pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html
    - I predict this section to have a lot of questions, so pause here and answer them. Hopefully will have a few other mentors around who
      can go around and help others understand everything so far
      
  Step 4: Real World Applications of a Neural Network
    - Give two examples, image recognition and natural language processing, and explain how they use neural networks to perform their
      respective functions
    - Ask attendees to think of a piece of technology that needs neural networks to work - gets them thinking about everything they've
      learned so far, to apply their newfound knowledge practically - break out into groups of 3 people to discuss
    - After about 3 minutes, ask if any groups would like to share what they came up with - tests their understanding
    
  Conclusion:
    - "These basic application of neural networks lay out the foundations of advanced machine learning applications, such as autonomous
      cars, which depend on huge neural networks to identify their surroundings accurately and drive accordingly"
    - Briefly mention the multiple ways to customize neural networks to suit your specific needs (ReLU, etc.)
    - Provide some links of good follow-up tutorials to check out
  
  Notes:
    - May want to go into more detail, such as the math behind backpropagation as well as gradient descent, and maybe describe different
      types of functions that adjust weights
    - Will prefer to have some mentors who can keep everyone on track
    - Will be part of a club I'm in - Machine Intelligence Community.
    
