Чем отличаются CharacterController от CharacterController 2   (Тем что в первом когда игрок прыгает то скорость меняется на обычную, а во втором скорость остаётся такой какой она была на земле тоесть если на земле игрок бежал то он сохранит скорость во время прыжка.)
ПЕРЕМЕННЫЕ: 
controller: Компонент CharacterController, который используется для управления движением персонажа.

speed: Скорость движения персонажа при обычной ходьбе.

runSpeed: Скорость движения персонажа при беге.

jumpHeight: Высота прыжка персонажа.

gravity: Значение гравитации, которое применяется к персонажу.

maxStamina: Максимальное количество выносливости персонажа.

staminaDrainRate: Скорость расхода выносливости при беге.

staminaRecoveryRate: Скорость восстановления выносливости.

staminaRecoveryDelay: Задержка восстановления выносливости после её истощения.

currentStamina: Текущая выносливость персонажа.

staminaRecoveryTimer: Таймер задержки восстановления выносливости.

velocity: Вектор скорости персонажа.

isGrounded: Флаг, указывающий, находится ли персонаж на земле.

currentSpeed: Текущая скорость персонажа.

В CharacterController
МЕТОДЫ: 
Start():устанавливаются начальные значения переменных currentStamina, staminaRecoveryTimer и currentSpeed.

Update():вызываются функции для обработки движения, выносливости, прыжков и применения гравитации.

HandleMovement(): Метод для обработки движения персонажа. Проверяет, находится ли персонаж на земле, и рассчитывает вектор движения в зависимости от ввода пользователя. Также управляет скоростью персонажа в зависимости от состояния бега.

HandleStamina(): Метод для обработки выносливости персонажа. Уменьшает выносливость при беге и восстанавливает её, когда персонаж не бежит. Также управляет таймером задержки восстановления выносливости.

HandleJump(): Метод для обработки прыжков персонажа. Проверяет, нажата ли кнопка прыжка, и находится ли персонаж на земле, чтобы выполнить прыжок.

ApplyGravity(): Метод для применения гравитации к персонажу. Увеличивает значение velocity.y в зависимости от гравитации и перемещает персонажа с учетом гравитации.
