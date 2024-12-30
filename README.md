# LR2-RBPO

sudo apt install lcov

cd /home/user/projects/FFmpeg

CC="gcc --coverage" CXX="g++ --coverage" ./configure --disable-shared

make

find . -name *.gcda

lcov -o ffmpeg.cov -c -d

genhtml -o cov_report ffmpeg.cov
