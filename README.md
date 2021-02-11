Haricot
==

Custom paper fork used by [Beancraft](https://beancraft.ml). The fork is based 
off of the framework used in 
[Phoenix616's Origami](https://github.com/Phoenix616/Origami).

## License
The PATCHES-LICENSE file describes the license for api & server patches
by Kezz found in `./patches/api` and `./patches/server`. Other patches
are either licensed under MIT or another one specified in the patch file itself.

Everything else is licensed under the MIT license. 
See https://github.com/Phoenix616/Origami, 
https://github.com/Spottedleaf/Tuinity, https://github.com/pl3xgaming/Purpur,
https://github.com/starlis/empirecraft and https://github.com/electronicboy/byof
for the license of material used/modified by this project.

## Plugin developers
In order to use Haricot as a dependency just add the dependency below to 
your pom. There is no repository as development should be done on a locally 
installed copy of the API.

Origami-API maven dependency:
```xml
<dependency>
    <groupId>ml.beancraft</groupId>
    <artifactId>haricot-api</artifactId>
    <version>1.16.5-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
 </dependency>
 ```

## Building and setting up
Run the following commands in the root directory:

```
git submodule init
git submodule update
./haricot up
./haricot patch
```

This should initialize the repo such that you can now start modifying and 
creating patches. The folder `Haricot-API` is the api repo and the 
`Haricot-Server`folder is the server repo and will contain the source files you
will modify.

#### Creating a patch
Patches are effectively just commits in either `Haricot-API` or 
`Haricot-Server`. To create one, just add a commit to either repo and run
`./haricot rb`, and a patch will be placed in the `patches` folder. Modifying 
commits will also modify the corresponding patch file.

#### Building
Use the command `./haricot build` to build the api and server. Compiled jars
will be placed under `Haricot-API/target` and `Haricot-Server/target`.

#### Updating Paper upstream
Switch into the directory of the Paper submodule and pull changes in from the 
repository, then run `./haricot up` and `./haricot rb`.