# System On Chip Simulation and Modeling written in Python

Github Code : https://github.com/Barun-S/litedram

==> Steps to Install and Run the Simulation: 
	--> Since the whole modeling is Python based, python installation is required.
		-> Install Python 3.6+, we install 3.8 using the command 
		   - $ sudo apt-get install python3.8
=> Install Build essential tools 
	- $ sudo apt-get install wget build-essential
=> Install Ninja Build
	- $ sudo apt-get install ninja-build
Installing required tools
	- $ sudo apt-get install libevent-dev libjson-c-dev flex bison
	- $ sudo apt-get install libfl-dev libfl2 zlibc zlib1g-dev
	- $ pip3 install setuptools
	- $ pip3 install requests
	- $ pip3 install pexpect
	- $ pip3 install meson
=> Install Litex
	--> Download the Litex setup using the command:
	    - $ wget https://raw.githubusercontent.com/enjoy-digital/litex/master/litex_setup.py
=> Change the permission of the setup file to make it executable
	- $ chmod +x litex_setup.py
=> Install using the command
	- $ ./litex_setup.py --init --install --user 
		--user to install to user directory
=> In future to Update Litex, run
	- $ ./litex_setup.py --update
=> Install a RISC-V toolchain
	- $ https://raw.githubusercontent.com/enjoy-digital/litex/master/litex_setup.py
	- $ python3 litex_setup.py gcc
	- $ sudo mkdir /usr/local/riscv
	- $ sudo cp -r $PWD/../riscv64-*/* /usr/local/riscv
=> Install Verilator
	- $ export PATH="/usr/lib/ccache:/usr/local/opt/ccache/libexec:$PATH"
	- $ git clone https://github.com/verilator/verilator
	- $ cd verilator
	- $ autoconf
	- $ ./configure
	- $ make -j$(nproc)
	- $ sudo make install
=> Install Project
	- $ python3 setup.py develop --user
=> Run Tests
	- $ export PATH=/usr/local/riscv/bin:$PATH
	- $ python3 setup.py test

Results: output.txt file contain the results of runnign all the testcases.
