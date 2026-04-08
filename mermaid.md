# Software Design Document (SDD)

## 1) Introduction

**Purpose:**  
This document explains how the Dungeon Adventure Game works and how it is designed.

**Scope:**  
- Text-based Dungeon Game  
- Player moves through 5 levels stored in a linked list  
- Players fight enemies using stack and queue  
- Supports a party of player-controlled characters  

---

## 2) System Overview

**Design Approach:**  
- Levels are stored in a linked list  
- Enemies in each level are stored in a stack  
- Player turns are managed using a queue  

**System Diagram:**  
*(You can add a diagram image here if available)*  

---

## 3) UML Class Diagram

```mermaid
classDiagram
    class LinkedListT {
        Node* head
        Node* tail
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

    class StackT {
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

    class Player {
        string type
        int hp
        int attack
        getType()
        getHP()
        getTAttack()
    }

    class ArrayQueueT {
        T** list
        int maxQueueSize
        int queueFront
        int queueRear
        int count
        enqueue(item)
        dequeue()
        isEmptyQueue()
    }

    LinkedListT --> Level : uses
    Level --> StackT : uses
    Player --> ArrayQueueT : uses