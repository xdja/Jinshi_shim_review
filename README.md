-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
- 郑州信大捷安信息技术股份有限公司(Zhengzhou Xindajiean Information Technology Co.,Lt)(www.xdja.com)
- Zhengzhou, HeNan, China
- Xindajiean established in 2004, which is a Hi-Tech Enterprise professional on designing Security Chip innovatly, Cloud Security Service Platform R&D, Embed-OS R&D, and providing Mobile&IoT Security Service Safeguard.
- President: Xiantong Ma

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
- JinShi Desktop OS is a U-Disk security OS based on Ubuntu, which runs in USB device isolately to avoid destroying the data in local storage.

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
- Jinshi is a customer-oriented linux-based security OS, only running normally in secure-boot-enable status on any AMD64 device, through which to avoid the hidden danger when customer disable secure boot.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:Xipeng Gong
- Position:Sernior Director
- Email address:Gongxipeng@xdja.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
    https://pgp.mit.edu/pks/lookup?op=get&search=0x81861E35
    
-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name:Hong Sheng
- Position:Sernior Director
- Email address:Shenghong@xdja.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
    https://pgp.mit.edu/pks/lookup?op=get&search=0x891090EB

-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
- shim tag:15
- https://github.com/rhboot/shim/releases/tag/15

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
- https://github.com/rhboot/shim 

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
- No patches have been applied

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
- OS:
    - ubuntu18.04.3 (www.ubuntu.com/download/desktop/thank-you?version=18.04.3&architecture=amd64)
- Toolchain:
     - binutils 2.30 (2.30-21ubuntu1~18.04.2)
     - gnu-efi 3.0.8 (3.0.8-0ubuntu1~18.04.1)
     - gcc 7.4.0 (Ubuntu 7.4.0-1ubuntu1~18.04.1)
     - make 4.1 (4.1-9.1ubuntu1)
- MAKE-STEP:
    - cd /path/to/shim/
    - sudo apt-get install gnu-efi
    - sudo apt-get install make
    - sudo mkdir /usr/lib64
    - sudo mkdir /usr/lib64/gnuefi
    - sudo cp /usr/lib/crt0-efi-x86_64.o /usr/lib64/gnuefi
    - sudo cp /usr/lib/libefi.a  /usr/lib64/gnuefi
    - sudo cp /usr/lib/libgnuefi.a /usr/lib64/gnuefi
    - sudo make VENDOR_CERT_FILE=xdja_jinshi.cer > build.log

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
- No patches
- https://github.com/xdja/Jinshi_shim_review/blob/master/build.log

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
- No
