# LR2-RBPO

sudo apt install lcov

cd /home/user/projects/FFmpeg

make clean

CC="gcc" CFLAGS="-fprofile-arcs -ftest-coverage" CXX="g++" CXXFLAGS="-fprofile-arcs -ftest-coverage" LDFLAGS="-fprofile-arcs -ftest-coverage" ./configure --disable-shared

make

find . -type f -executable

./ffmpeg -version

./ffmpeg -i /home/user/projects/input/inputfile.mp4 -c:v mpeg4 -q:v 5 -c:a aac /home/user/projects/output/outputfile.mkv

find . -name "*.gcno"

find . -name "*.gcda"

lcov -o ffmpeg.cov -c -d ./ --ignore-errors inconsistent,usage,deprecated --rc lcov_branch_coverage=1 --rc lcov_excl_line=1

genhtml -o cov_report ffmpeg.cov

![image](https://github.com/user-attachments/assets/23839450-c604-4f21-975d-b4f10d97f5a4)
