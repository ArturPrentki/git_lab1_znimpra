# Lab. 11 - Laboratorium problemowe 1 - “Robot w labiryncie”

Robot zna odległość od celu oraz swoją pozycję w środowisku, dzięki odometrii. Umożliwia to wyznaczanie potencjalnej pozycji celu za pomocą co najmniej 3 niewspółliniowych pomiarów względem pozycji startowej.

1. Wykonujemy ruch robotem do zebrania pomiarów i wyznaczenia pozycji celu \
Subscriptions: 
- /odom 
- /distance \
Published Topics: 
- /goal_pose 
2. Za pomocą slam_toolbox tworzymy mapę zajętości [a link](https://github.com/SteveMacenski/slam_toolbox) \
Subscriptions: 
- /odom 
- /scan \
Published Topics: 
- /map 
3. Korzystając z algorytmu planowania ścieżki (np. RRT*, A*) ze stack'a Nav2 wyznaczamy trasę do wyznaczonego wcześniej celu, aktualizując podczas jazdy robota mapę zajętości i ścieżkę. \
Subscriptions: 
- /map 
- /goal_pose 
