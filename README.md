# CBT266
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. 
Due to amazing work by Alison Zhang and Jake Choi repos are no longer deleted.

```
//***FILE 266 is from Sam Golob, who updated the tape mapping       *   FILE 266
//*           program called SS0104 from Florida Power Corporation. *   FILE 266
//*           This code is used to measure the footages of files    *   FILE 266
//*           on the CBT Tape, as though they were on a 6250 bpi    *   FILE 266
//*           tape reel.  As is, that is what this code is used     *   FILE 266
//*           for, but it can be used for other purposes.  The      *   FILE 266
//*           report is quite excellent for showing, in general,    *   FILE 266
//*           what is on a tape.  Added is a related tape copying   *   FILE 266
//*           program called SS0278.                                *   FILE 266
//*                                                                 *   FILE 266
//*           Please look at member BM2312DE, which is a short      *   FILE 266
//*           article that will tell you some general information   *   FILE 266
//*           about both of the programs which are found on this    *   FILE 266
//*           file.                                                 *   FILE 266
//*                                                                 *   FILE 266
//*           If you fix this code, for use with any density        *   FILE 266
//*           tape, and with cartridge, please send it to me to     *   FILE 266
//*           test, so I can update this file in your name.         *   FILE 266
//*           Thanks.  (S.Golob - 08/96).                           *   FILE 266
//*                                                                 *   FILE 266
//*           Note:  Fixed to avoid the CNTRL FSM invocation that   *   FILE 266
//*                  was causing I/O errors on some MVS systems.    *   FILE 266
//*                  (05/28/04 - SBG)                               *   FILE 266
//*           Note:  Fixed to record over 10000 total feet.         *   FILE 266
//*                  (12/16/12 - SBG)                               *   FILE 266
//*           Note:  Fixed to replace WKDATE routine with TODAY     *   FILE 266
//*                  routine, in SS0104. (12/18/12 - SBG)           *   FILE 266
//*           Note:  Eliminated SPM instructions from the $ENTER    *   FILE 266
//*                  and $RTRN macros, so they would not cause      *   FILE 266
//*                  a fixed-point overflow abend S0C8, when        *   FILE 266
//*                  measuring long tapes.  (12/11/23 - SBG)        *   FILE 266
//*           Note:  Eliminated forced user abends when I/O errors  *   FILE 266
//*                  occur.  This can be reversed.  See member      *   FILE 266
//*                  $$NOTE02.  (12/20/23 - SBG)                    *   FILE 266
//*           Note:  Fixed SS0278 to never alter the input tape.    *   FILE 266
//*                                                                 *   FILE 266
//*           Also included here, is one other of Florida Power's   *   FILE 266
//*           programs, a tape duplicating program, which runs      *   FILE 266
//*           (almost) as coded in the mid 1970's, right out of     *   FILE 266
//*           the box.  The program is called SS0278 and aliased    *   FILE 266
//*           with the name DUPTAPE.  As coded, the blocksize of    *   FILE 266
//*           the tape blocks is limited to 32K.                    *   FILE 266
//*                                                                 *   FILE 266
//*           SS0278 was fixed to not alter the input tape in any   *   FILE 266
//*           way (which the original version did).  An older       *   FILE 266
//*           version (called SS0278O) was included here, in case   *   FILE 266
//*           somebody wants the result of the old program, but     *   FILE 266
//*           without the mistakes that were coded there.  That     *   FILE 266
//*           version alters the HDR2 and EOF2 records to say that  *   FILE 266
//*           the tape was a "copied tape", etc., putting that      *   FILE 266
//*           information into the JOBNAME and STEPNAME fields      *   FILE 266
//*           of the HDR2 and EOF2 tape labels in the output tape.  *   FILE 266
//*           And it uses "today's date" as the "Created Date"      *   FILE 266
//*           instead of the original create date from the          *   FILE 266
//*           original tape.                                        *   FILE 266
//*                                                                 *   FILE 266
//*           Note:  You have to code the $ENTER and $RTRN macros   *   FILE 266
//*                  with the option, SPM=NO.                       *   FILE 266
//*                                                                 *   FILE 266
//*           I want to acknowledge the big help of one of the      *   FILE 266
//*           original authors, Gordon P. West.  Thanks, Gordon.    *   FILE 266
//*           Other people were involved in the writing of these    *   FILE 266
//*           programs as well as Gordon.  And he does not have     *   FILE 266
//*           any memory of any of the original mistakes in the     *   FILE 266
//*           program.  Anyway, I think I fixed all the mistakes.   *   FILE 266
//*                                                                 *   FILE 266
//*           email:  sbgolob@cbttape.org                           *   FILE 266
//*                                                                 *   FILE 266
//*           email:  gordon@westgp.us                              *   FILE 266
//*                                                                 *   FILE 266
```
