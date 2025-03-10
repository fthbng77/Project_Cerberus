## Micro-XRCE-DDS-Gen Installation 


```
git clone https://github.com/eProsima/Micro-XRCE-DDS-Gen.git
```

Install dependencies:
```
cd Micro-XRCE-DDS-Gen
git submodule init
git submodule update
```

Build with Grandle:
```
./gradlew assemble
```

Add path to ./bashrc:
```
export PATH=$PATH: ~/Micro-XRCE-DDS-Gen/scripts
```
