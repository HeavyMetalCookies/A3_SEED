    //:ABOUT_A3_SEED:========================================://

        A3 is Data Oriented Design template for new C 
        projects. It is based on lessons learned from my
        AAC2020 library code. 

        It has a few goals in mind:

        1. ZERO guesswork as to order in which files are
           included. You need to solve the dependency 
           graph manually in the LIBCHAN.

        2. No artificial dependency loops. All data files
           are included before all function files.

        3. Minimization of code surface area.
           Do __NOT__ break a function into re-usable logic
           until that logic __IS__ re-used. Not "might" 
           be re-used but __IS__ re-used.
           #YAGNI#

        4. Be able to find your way around by avoiding
           forward declarations. A referenced function
           will always be defined ABOVE it's call site.

           Exceptions for unit tests. But in cases where
           the function is BELOW instead of above,
           a forward declaration should be directly
           above the function call.

           EXAMPLE:

                void A3F_MyFunctionLowerInFile( void );
                     A3F_MyFunctionLowerInFile( void );

        5. Try to avoid camel case. And when it is used,
           it is only used for functions.

           CAPITALS : namespaces + functions + type macros
           LOWERCASE: variables  + structs

        6. All FILESCOPE tokens must have library prefix:

           Feel free to change library prefix.
           I went with this because it is easy to see
           that it is my library code and tell wether it
           is function or data with a quick glance.

           1. A3F_ (public  function)
           2. a3f_ (private function)
           3. A3D_ (public  data    )
           4. a3d_ (private data    )
        
    //:========================================:ABOUT_A3_SEED://
    //:PROJECT_STRUCTURE:====================================://

        DOC : Documentation.

        LIB : Library Code.
              LIB/DEP : 3rd party dependencies.
              LIB/SUB : Sub Libraries that make up project.
              LIB/E_E : Everything Else.

        MOD : Procedurally Generated MOD folder to allow
              people to hack the game after it has launched
              the first time. The .exe file creates this
              at runtime.

        !!!!!!!!!!!!!! NO_OTHER_TOP_LEVEL_FOLDERS !!!!!!!!!!!!!!

    //:====================================:PROJECT_STRUCTURE://