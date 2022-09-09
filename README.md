# krista_labs
@startuml

left to right direction
actor "Читатель" as reader
rectangle {
usecase "Читает новости" as read
usecase "Комментирует" as comment
usecase "Оценивает" as rate
usecase "Делится новостями" as share
}

left to right direction
actor "Модератор" as moder
rectangle {
usecase "Пишет новости" as write
usecase "Редактирует новости" as edit
usecase "Предлагает к опубликованию" as offerNews
}

left to right direction
actor "Писатель" as writer
rectangle {
usecase "Выкладывает новости" as loadNews
usecase "Проверяет комментарии" as checkComment
usecase "Удаляет новости" as deleteNews
usecase "Удаляет комментарии" as deleteComment
}

reader -- read
reader -- comment
reader -- rate
reader -- share

moder -- loadNews
moder -- checkComment
moder -- deleteNews
moder -- deleteComment

writer -- write
writer -- edit
writer -- offerNews

@enduml

![lab1_diagrams](https://user-images.githubusercontent.com/46898265/189305356-8558235c-1834-4a76-a5b3-87a6c3d5d06d.svg)


