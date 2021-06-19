
    //:FOLDER_STRUCTURE:=====================================://

        DEP : Dependencies. Project has ZERO external 
              dependencies. Keep committed dependencies to
              small header only libraries.
        
              Example: LodePNG

        SUB  : Sub libraries. The core of the engine.

        E_E  : Everything Else.
               We don't want too much branching. So things
               like "main code" that will eventually be
               extracted from our "A3.C11" file should be
               put somewhere into "E_E" folder.

    //:=====================================:FOLDER_STRUCTURE://