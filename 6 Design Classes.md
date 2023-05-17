## Классы проектирования
### Обоснование
В проекте есть несколько мест повышенной сложности, для которых потребуется придумать модель.   
В первую очередь, стоит продумать интерфейс передачи данных о ходе во время боя. Надо придерживаться YAGNI и при этом делать интерфейс так, 
что бы в будущем была возможность быстро и просто адаптировать его, например, для боев через интернет.

### Список классов
- Move - Bridge - Передает и высчитывает результат хода каждого игрока(человека или NPC). 
- Timer - Singleton -  С начала входа в систему и в любом ее месте продолжается отсчет времени, которое еще можно провести в игре.
- Store - Bridge - Хранение данных на клиенте, но можно будет адаптировать и для сервера.