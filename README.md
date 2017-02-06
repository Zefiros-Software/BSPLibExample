# BSPLib Example

## Installing ZPM

On Linux, run (this installation does not require privileges):

```
wget -O - https://raw.githubusercontent.com/Zefiros-Software/ZPM/master/script/install-zpm.sh | bash
```

On OSX:

```
wget -O - https://raw.githubusercontent.com/Zefiros-Software/ZPM/master/script/install-zpm-osx.sh | bash
```

On Windows:

```
powershell -command "Invoke-WebRequest -Uri https://raw.githubusercontent.com/Zefiros-Software/ZPM/master/script/install-zpm.bat -OutFile %TEMP%/install-zpm.bat" && %TEMP%/install-zpm.bat && set PATH=%PATH%;%ALLUSERSPROFILE%/zpm
```

### Modifying zpm.lua
The makefile generation is based on [premake 5](https://github.com/premake/premake-core) and configuration can be found in ``zpm.lua``.

## Generating the Makefile
By default there is no makefile available, so we generate this using:

```
./generate-makefile.sh
```

After this we should have ``edupack/Makefile`` available.

## Building

A release build:

```
cd edupack
make config=release_x86_64
```

A debug build:

```
cd edupack
make config=debug_x86_64
```

## Running
We now have built edupack. To run it we go to the binary folder.

For a release build:

```
cd bin/x86_64
./edupack
```

For a debug build:

```
cd bin/x86_64
./edupackd
```