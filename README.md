# ec2
swap file
### swap file 생성
sudo dd if=/dev/zero of=/swapfile bs=128M count=32
### swapfile 권한
sudo chmod 600 /swapfile
### swap 영역 생성
sudo mkswap /swapfile
### swap 공간에 swapfile 추가해서 사용 가능하게 함
sudo swapon /swapfile
### swapfile 설정 성공 확인
sudo swapon -s
### fstab 편집 -> 재부팅시에 활성화
sudo vi /etc/fstab

/swapfile swap swap defaults 0 0
