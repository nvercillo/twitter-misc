# sshd on archlinux
#
# VERSION               0.0.1

FROM	 archlinux:latest
MAINTAINER 	Evaggelos Balaskas <evaggelos _AT_ balaskas _DOT_ gr>

# Update the repositories
RUN	 pacman -Syy

RUN pacman -S --noconfirm nano

# Install openssh
RUN	 pacman -S --noconfirm openssh

# Generate host keys
RUN  /usr/bin/ssh-keygen -A

# # Add password to root user
# RUN	 echo 'root:password' | chpasswd

# # Fix sshd
# RUN  sed -i -e 's/^UsePAM yes/UsePAM no/g' /etc/ssh/sshd_config

# Create 
# RUN  sudo useradd snvercil

# RUN  mkdir home/snvercil

# RUN  chown snvercil home/snvercil

# # add snvercil to sudoers group
# RUN  usermod -a -G sudo snvercil 

# RUN  su snvercil

# RUN  cd ~ 

# RUN  wget https://aur.archlinux.org/cgit/aur.git/plain/PKGBUILD?h=packer

# RUN  mv PKGBUILD\?h\=packer PKGBUILD

# RUN  pacman -U packer-20160325-1-any.pkg.tar.zst



# pacman -U packer-20160325-1-any.pkg.tar.zst

# packer -S  booster




# Expose tcp port
EXPOSE	 22

# Run openssh daemon
CMD	 ["/usr/sbin/sshd", "-D"]