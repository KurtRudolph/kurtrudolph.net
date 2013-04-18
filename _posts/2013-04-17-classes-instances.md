---
layout: post
title: "Classes and The Instances of One's self"
subtitle: ""
description: ""
category: Developer
tags: ['ruby', 'hacker', 'methods', 'self']
---

## <a id='ExampleCode'> </a>ExampleCode

The following sections of code are functionally equivalent (Please see the [AlternateExampleCode](#AlternateExampleCode) if you are not familiar with `attr`, `attr_reader`, etc.):

#### <a id='ExampleCode0'> </a>ExampleCode0
    class Die
      attr_reader :sides
      def initialize sides
        @sides = sides
      end
    
      def roll
        rand 1..@sides
      end
    end

#### <a id='ExampleCode1'> </a>ExampleCode1
    class Die
      attr_reader :sides
      def initialize sides
        @sides = sides
      end
    
      def roll
        rand 1..self.sides
      end
    end  

### <a id='FollowUpQuestion'> </a>FollowUpQuestion
Why does the following code raise an error?

    class Die
      # in case you didn't notice, the following line is commented out...
      # attr_reader :sides
      def initialize sides
        @sides = sides
      end
    
      def roll
        rand 1..self.sides
      end
    end  


## <a id='AlternateExampleCode'> </a>AlternateExampleCode
The following sections of code are functionally equivalent

#### <a id='AlternateExampleCode0'> </a>AlternateExampleCode0
    class Die
      def initialize sides
        @sides = sides
      end
    
      def sides
        @sides
      end
    
      def roll
        rand 1..@sides
      end
    end

#### <a id='AlternateExampleCode1'> </a>AlternateExampleCode1
    class Die
      def initialize sides
        @sides = sides
      end
    
      def sides
        @sides
      end
    
      def roll
        rand 1..self.sides
      end
    end  

### <a id='AlternateFollowUpQuestion'> </a>AlternateFollowUpQuestion
Why does the following code raise an error?

    class Die
      def initialize sides
        @sides = sides
      end
    
    =begin
      # in case you didn't notice, the following is commented out...
      def sides
        @sides
      end
    =end

      def roll
        rand 1..self.sides
      end
    end