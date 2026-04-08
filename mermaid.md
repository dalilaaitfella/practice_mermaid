1) Introduction: 

-Purpose:
This document explains how the Dungeon advenuture Game works and how it designed.

-Scope:

     .texted-based Dangeon Game.
     .Player moves through 5 levels stored in a linked list.
     .Players fight enemies using stack and Queue.
     .Supports a party of player controlled characters.

2) System Overview:
 
 - Design Aproach
     
     . Levels stored in linked list.
     . Enemies in each level stored in a stack.
     .Players turns managed usin a Queue.

     System diagram :








3) UML class diagram:
```mermaid
classDiagram
    class linkedlistType~T~ {
        Node~T~* head
        Node~T~* tail
        add(item)
        begin()
        end()
    }

    class Level {
        string name
        stack<Enemy> enemies
        addEnemy()
        getEnemies()
        printLevel()
    }

    class Stack~T~ {
        T* list
        int maxSize
        int topIndex
        push(item)
        pop()
        isEmptyStack()
    }

    class Enemy {
        string name
        int hp
        int attack
        getName()
        getHP()
        getAttack()
    }

    class player {
        string type
        int hp
        int attack
        getType()
        getHP()
        getTAttack()
    }

    class arrayQueue~T~ {
        T** list
        int maxQueueSize
        int queueFront
        int queueRear
        int count
        enqueue(item)
        dequeue()
        isEmptyQueue()
    }

    linkedlistType~T~ --> Level : uses
    Level --> Stack~T~ : uses
    player --> arrayQueue~T~ : uses






4) Behavior UML Diagram (sequence)