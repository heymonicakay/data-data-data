# Entity Relationship Diagrams

In this chapter, you will be working with the dbdiagram.io site's diagramming tool, so visit that site and register an account. Then open their diagramming tool.

## Videos to Watch Before Class

### Databases and Normalization

1. [Database Tutorial for Beginners](https://www.youtube.com/watch?v=wR0jg0eQsZA)
1. [MicroNugget: How to Normalize Databases](https://www.youtube.com/watch?v=upS2HlUj1gI)
1. [Basic Concept of Database Normalization - Simple Explanation for Beginners](https://www.youtube.com/watch?v=xoTyrdT9SZI)

### Entity Relationship Diagrams

1. [Entity Relationship Diagram (ERD) Tutorial - Part 1](https://www.youtube.com/watch?v=QpdhBUYk7Kk)
1. [Entity Relationship Diagram (ERD) Tutorial - Part 2](https://www.youtube.com/watch?v=-CuY5ADwn24)

## Artists and Paintings

In the next couple chapters, you will be learning how to store two objects in your database that are related to each other through what's called a foreign key.

To prepare you for that, you need to create your first visualization of entities and their relationship in [dbdiagram](https://dbdiagram.io/).

Open a new diagram in dbdiagram, then copy the following text and paste it into the editor on the left side of the screen.


```html
Table Artists {
    id int pk
    age int
    name varchar
    phone varchar
}

Table Paintings {
    id int pk
    title varchar
    medium varchar
    artistId int
}

Ref: "Artists"."id" < "Paintings"."artistId"

```
For now, the foreign key is the `artistId` attribute on the **`Paintings`** entity in the diagram. It is a numeric representation of the entire artist object that is stored in another collection (_or 'table' in database-speak_).

Hover over the line connecting the two tables. Notice the **1** next to the **`Artists`** table, and the * next to the **`Paintings`** table, indicating that this relationship is a **one-to-many** relationship. In this relationship, **one** artist can be related to **many** paintings. However, a **single** painting can only be related to **one** artist.

---

> **Tips:**

> **varchar** = Variable length character value
>
> **int** = Integer value  (e.g. 2, 81, 2054)
>
> **double** - Double precision floating point number (e.g. 1.414, 3.14159)
>
> **pk** = Primary key field

> **timestamp** = Timestamp field

> **date** = Date field
