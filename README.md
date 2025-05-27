# Public Lookups

The files in this folder are **published publicly** for consumers of our quote to bind API to use. Don't put any lookups that are sensitive or should be private in this folder.

If you need to add sensitive lookup data, add it in the `private-lookups` folder of this package and merge it into the lookups object in `index.ts` similar to what's being done right now.

If you update the lookups in this directory, you might also want to copy the files you updated over to the public mirror at https://github.com/gobranch/lookups
