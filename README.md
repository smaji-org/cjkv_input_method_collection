## CJKV Input Method Collection

This is a subproject of [Smaji CJKV](https://cjkv.smaji.org).

This repository is a collection of cjkv input method encoding.

Based on this input method encoding repository, input method configuration files are generated and synchronized among users of this project.

In this way, we can always input any cjkv characters easily.


### Directory structure

    .
    └── glyph
        ├── 4e20
        │   └── 0
        │       ├── cangjie5
        │       └── zhengma
        ├── 4e21
        │   ├── 0
        │   │   ├── cangjie5
        │   │   └── zhengma
        │   └── e01ef
        │       ├── cangjie5
        │       └── zhengma
        ├── 697c
        │   └── 0
        │       ├── cangjie5
        │       └── zhengma
        └── 2b744
            └── 0
                ├── cangjie5
                └── zhengma

All glyphs have their individual directory, placed in the `glyph` directory. In each glyph directory, input method encoding files are placed and the content of the files are corresponding input method encoding as the file name denoted.

### File structure

697c(楼) is unambiguous in zhengma encoding, so the content of the file is

    fuzm

The file contains only one line of encoding.

2b744(𫝄) is ambiguous in zhengma encoding, it can be interpreted as throw + 人 or throw-throw + press, so the content of the file consists of two lines

    mod
    ods

### Processing flow

1.  submit a pull request, or create an issue if you are not familiar with git
    -   fix or make new files containing input method encoding, follow the directory and file structure

2.  provide basic information of the glyphs the pull request will alter
    -   the corresponding glyphs in the [cjkv\_glyph\_collection](https://github.com/smaji-org/cjkv_glyph_collection) library.

3.  collaborators will verify the input method encoding manually

4.  discussing and modification

5.  merge the pull request

