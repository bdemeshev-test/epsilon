Обработка каждого выпуска
=========================

1. Все PNG-иллюстрации надо оптимизировать без потери качества
for i in *.png; do optipng -o7 -zm1-9 -preserve "$i" ; done
Если компьютер медленный, делаем
for i in *.png; do optipng -o7 -preserve "$i" ; done

Если какой-то PNG очень тяжёлый, перед этим ужимаем его с не заметной глазу (и тем более принтеру) потерей качества:
pngquant -s1 -f --ext .png --skip-if-larger --verbose *.png
