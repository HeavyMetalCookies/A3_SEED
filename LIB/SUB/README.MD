
    //:FOLDER_STRUCTURE:=====================================://

        000 : Zero dependencies on other "LIB/SUB" systems.
              Can depend on internal dependencies within:
              "A3/LIB/DEP".

        001 : One degree of dependency. Depends on something
              within "000" folder.

        002 : Two degrees of dependency. Depends on something
              within "001" folder.

        ### : Higher Degrees of dependency here.
              Dependency degree resolution:
              If a library depends on "000" and "998"
              the library goes in the "999" folder , not
              the "001" folder.

    //:=====================================:FOLDER_STRUCTURE://
    //:ALSO_SEE:=============================================://

        "A3/LIB/E_E/LIBMAIN" :
            All top level code that must [coordinate/couple]
            the sub library code.

        "A3/LIB/E_E/LIBCHAN" :
            Basically the build system. Chains together 
            all of the library code into final executable.

    //:=============================================:ALSO_SEE://
    //:STYLE_GUIDE:==========================================://

        UPPERCASE:
            NAMESPACES    (most except private: a3f & a3d)
            ACTIONS/VERBS (GET , PUT , TES/TEST)
            ABBREVIATIONS (CTO, LUT)
            
        LOWERCASE:
            variables : EX:         dll_fun
            datatypes : EX: A3D_DYNALIB_fun

        EXAMPLE NAMESPACING:

            PUBLIC  FUNC : A3F_DYNALIB_sometyp_CTO_sometyp
            PRIVATE FUNC : a3f_DYNALIB_sometyp_CTO_sometyp

            PUBLIC  DATA : A3D_DYNALIB_sometyp_LUT_sometyp
            PRIVATE DATA : a3d_DYNALIB_sometyp_LUT_sometyp

    //:==========================================:STYLE_GUIDE://