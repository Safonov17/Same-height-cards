# Как сделать карточки с разным контентом одинаковыми по высоте
# How to make cards with different content the same height

## Before
![Before](/img/Before.png)

Достаточно прописать для класса "card" высоту 100%  
It is enough to set the height of 100% for the "card" class

## After
![After](/img/After.png)

Все хорошо, но теперь кнопка на первой карточке так и просится вниз  
Everything is fine, but now the button on the first card is asking to go down

Для этого пишем следующим классам дополнительный свойства:  
To do this, add additional properties to the following classes:

.card {  
    display: flex;  
    flex-direction: column;  
}  
.card__content {  
    display: flex;  
    flex-direction: column;  
    align-items: flex-start;  
    flex-grow: 1;  
}  
.card__button {  
    margin-top: auto;  
}  

## Finally
![Finally](/img/Finally.png)