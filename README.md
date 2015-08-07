# Harness
Interactive remote PowerShell Payload

Description
Harness is remote access payload with the ability to provide a remote interactive PowerShell interface from a Windows system to virtually any TCP socket. The primary goal of the Harness Project is to provide a remote interface with the same capabilities and overall feel of the native PowerShell executable bundled with the Windows OS. 

Payload Features:
-	Remote PowerShell CLI
-	Multiline command processing similar to native PowerShell.exe
-	Supports remote importing of PowerShell modules without additional staging (requires supporting handler)
-	Unmanaged payload allows for white list bypassing
-	 Reflective payload allows for payload to be injected into other processes 

License:

Unless otherwise indicated all original Harness code is release under the MIT license. However, ReflectiveHarness draws heavily from the following projects, and would otherwise not have been possible:

https://github.com/leechristensen/UnmanagedPowerShell/tree/master/UnmanagedPowerShell
https://github.com/PowerShellEmpire/PowerTools/blob/master/PowerPick/ReflectivePick
https://github.com/stephenfewer/ReflectiveDLLInjection

Their respective licenses are included in any source code that was used. 

Installation:

Harness is bundled in a small Python framework. Python 3.4+ is required because the handler is implemented around the asyncio library. To install Python3.4 as an alternate install you can run the following commands:

	wget http://python.org/ftp/python/3.4.3/Python-3.4.3.tar.xz
	tar xf Python-3.4.3.tar.xz
	cd Python-3.4.3
	./configure --prefix=/usr/local --enable-shared LDFLAGS="-Wl,-rpath /usr/local/lib"
	make && make altinstall

Other than installing Python 3, installation only requires that you unzip the Harness folder to a location of your choosing. Currently the framework has only been tested on Kali Linux, and was not designed for Windows. 

Starting Harness:

	cd /Harness
	python3.4 harness.py




