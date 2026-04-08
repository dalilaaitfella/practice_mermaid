classDiagram
    class linkedlistType_T_ {
        Node_T_* head
        Node_T_* tail
        add(item)
        begin()
        end()
    }

    class Level {
        string name
        stack_Enemy_ enemies
        addEnemy()
        getEnemies()
        printLevel()
    }

    class Stack_T_ {
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

    class arrayQueue_T_ {
        T** list
        int maxQueueSize
        int queueFront
        int queueRear
        int count
        enqueue(item)
        dequeue()
        isEmptyQueue()
    }

    linkedlistType_T_ --> Level : uses
    Level --> Stack_T_ : uses
    player --> arrayQueue_T_ : uses