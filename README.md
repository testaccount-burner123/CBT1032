# CBT1032
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE1032 is from Ben Marino, and is a sophisticated "service   *   FILE1032
//*           provider", which allows you to provide multiple       *   FILE1032
//*           services to any address space in the system.  This    *   FILE1032
//*           product uses a stacking PC which performs the         *   FILE1032
//*           multiple services.                                    *   FILE1032
//*                                                                 *   FILE1032
//*           Documentation is provided by several members in this  *   FILE1032
//*           pds.  The first place you should look is in member    *   FILE1032
//*           $DOC, which describes the basic architecture and      *   FILE1032
//*           functionality of the ZXPC product.  The next place    *   FILE1032
//*           you should look, is member $INSTALL.  This member     *   FILE1032
//*           contains 6 simple steps which are necessary to        *   FILE1032
//*           install the product.                                  *   FILE1032
//*                                                                 *   FILE1032
//*           To install the product, you first have to assemble    *   FILE1032
//*           and linkedit it, so you have to see member ZXPCLINK.  *   FILE1032
//*                                                                 *   FILE1032
//*           Then look at member $ZLISTEN, which contains examples *   FILE1032
//*           of how to use the "system event listener" facility.   *   FILE1032
//*           There is also another facility which allows you to    *   FILE1032
//*           add or delete a module from dynamic LPA.  And there   *   FILE1032
//*           is more:                                              *   FILE1032
//*                                                                 *   FILE1032
//*      To see a list of all facilities which this product can     *   FILE1032
//*      provide, look in member $DOC2.                             *   FILE1032
//*                                                                 *   FILE1032
//*      LIST OF SERVICES CURRENTLY PROVIDED BY THIS PRODUCT        *   FILE1032
//*      (as it is currently written - you can add more services    *   FILE1032
//*      by writing your own PC routine - by simply adding a        *   FILE1032
//*      subroutine in module XPCSRV.)  In routine XPCSRV, there    *   FILE1032
//*      is a model that you can clone, to provide whatever         *   FILE1032
//*      service you want.  The model is called, "MODEL".           *   FILE1032
//*                                                                 *   FILE1032
//*      ZLISTEN - System events listener facility.                 *   FILE1032
//*                Defines a listener routine that receives         *   FILE1032
//*                control when a specified system event            *   FILE1032
//*                occurs. The listener routine can execute         *   FILE1032
//*                under the TCB and address space where the        *   FILE1032
//*                event occurs, under a different TCB or           *   FILE1032
//*                under a TCB of different address space.          *   FILE1032
//*                                                                 *   FILE1032
//*      ZDYNLPA - Dynamic-LPA facility.                            *   FILE1032
//*                Add/delete modules to/from dynamic-LPA. The      *   FILE1032
//*                module can be added in pageable or fixed         *   FILE1032
//*                storage and page protected storage.              *   FILE1032
//*                                                                 *   FILE1032
//*      ZPROT   - Virtual storage validation facility.             *   FILE1032
//*                The TPROT instruction does not distinguish       *   FILE1032
//*                between a valid and invalid storage              *   FILE1032
//*                address. When the referenced page is             *   FILE1032
//*                swapped out, TPROT sets translation not          *   FILE1032
//*                available condition code 3.                      *   FILE1032
//*                                                                 *   FILE1032
//*                ZPROT handles what TPROT does not. It            *   FILE1032
//*                validates a storage address by determining       *   FILE1032
//*                if the storage key and PSW key match. ZPROT      *   FILE1032
//*                switches to the caller's PSW key and does        *   FILE1032
//*                fetch and store into the page. An invalid        *   FILE1032
//*                fetch and store is handled by its FRR            *   FILE1032
//*                routine. ZPROT sets a return code in             *   FILE1032
//*                register 15 that indicates the result of         *   FILE1032
//*                the storage validation test as follows:          *   FILE1032
//*                                                                 *   FILE1032
//*                R15 - return code                                *   FILE1032
//*                 00 - address is valid                           *   FILE1032
//*                 04 - 0C4-4  Protection Exception                *   FILE1032
//*                 08 - 0C5-5  Addressing Exception                *   FILE1032
//*                 12 - 0C4-10 Segment Translation Exception       *   FILE1032
//*                 16 - 0C4-11 Page Translation Exception          *   FILE1032
//*                 20 - Internal service routine failure           *   FILE1032
//*                                                                 *   FILE1032
//*      ZGETMEM - Storage management facility.                     *   FILE1032
//*                Obtains private storage outside the primary      *   FILE1032
//*                address space by simply specifying the           *   FILE1032
//*                STOKEN, JOBname, STCname, or TSUname of the      *   FILE1032
//*                target address space.                            *   FILE1032
//*                                                                 *   FILE1032
//*      ZFREMEM - Storage management facility.                     *   FILE1032
//*                Releases private storage outside the             *   FILE1032
//*                primary address space by simply specifying       *   FILE1032
//*                the STOKEN, JOBname, STCname, or TSUname of      *   FILE1032
//*                the target address space.                        *   FILE1032
//*                                                                 *   FILE1032
//*      ZCOPY   - Data copy facility.                              *   FILE1032
//*                Copies data across address spaces without        *   FILE1032
//*                the use of SQA/CSA storage buffers by            *   FILE1032
//*                simply specifying the STOKEN, JOBname,           *   FILE1032
//*                STCname or TSUname of the target address         *   FILE1032
//*                space.                                           *   FILE1032
//*                                                                 *   FILE1032
//*      ZAUTH   - Authorization facility.                          *   FILE1032
//*                Changes jobstep authorization to allow you       *   FILE1032
//*                to issue the MODESET Supervisor call             *   FILE1032
//*                without suffering S047 ABENDs.                   *   FILE1032
//*                                                                 *   FILE1032
```
