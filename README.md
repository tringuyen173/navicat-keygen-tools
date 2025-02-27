# Navicat Keygen

[中文版README](README.zh-CN.md)

## 1. How does it work?

see [here](doc/how-does-it-work.md).

## 2. How to build

see [here](doc/how-to-build.md).

## 3. How to Use

1. Download navicat from https://drive.google.com/file/d/1GOA-5jYRnzAt8lZbSwSgzdUg17bGfX9b/view?usp=sharing

   And you will get a AppImage file. For example, `navicat15-premium-en.AppImage`.

   I assume that the AppImage file is in `~/Desktop` folder.

2. Extract all files in the AppImage to a directory. For example:

   ```console
   $ mkdir ~/Desktop/navicat15-premium-en
   $ sudo mount -o loop ~/Desktop/navicat15-premium-en.AppImage ~/Desktop/navicat15-premium-en
   $ cp -r ~/Desktop/navicat15-premium-en ~/Desktop/navicat15-premium-en-patched
   $ sudo umount ~/Desktop/navicat15-premium-en
   $ rm -rf ~/Desktop/navicat15-premium-en
   ```

3. [Build keygen and patcher.](doc/how-to-build.md)

4. Use `navicat-patcher` to replace the official public key.
   
   ```
   Usage:
       navicat-patcher [--dry-run] <Navicat Installation Path> [RSA-2048 Private Key File]

           [--dry-run]                   Run patcher without applying any patches.
                                         This parameter is optional.

           <Navicat Installation Path>   Path to a directory where Navicat locates
                                         This parameter must be specified.

           [RSA-2048 Private Key File]   Path to a PEM-format RSA-2048 private key file.
                                         This parameter is optional.
   ```

   __Example:__ 

   ```console
   $ ./bin/navicat-patcher ~/Desktop/navicat15-premium-en-patched
   ```

   It has been tested on __Navicat Premium 15.0.3 English For Linux__ version. 
   
   The following is an example of output:

   ```console
   **********************************************************
   *       Navicat Patcher (Linux) by @DoubleLabyrinth      *
   *                  Version: 1.0                          *
   **********************************************************

   Press ENTER to continue or Ctrl + C to abort.

   [+] Try to open libcc.so ... Ok!

   [+] PatchSolution0 ...... Ready to apply
      RefSegment      =  1
      MachineCodeRva  =  0x0000000001413e10
      PatchMarkOffset = +0x00000000029ecf40

   [*] Generating new RSA private key, it may take a long time...
   [*] Your RSA private key:
      -----BEGIN RSA PRIVATE KEY-----
      MIIEowIBAAKCAQEArRsg1+6JZxZNMhGyuM8d+Ue/ky9LSv/XyKh+wppQMS5wx7QE
      XFcdDgaByNZeLMenh8sgungahWbPo/5jmkDuuHHrVMU748q2JLL1E3nFraPZqoRD
      ...
      ...
      B1Z5AoGBAK8cWMvNYf1pfQ9w6nD4gc3NgRVYLctxFLmkGylqrzs8faoLLBkFq3iI
      s2vdYwF//wuN2aq8JHldGriyb6xkDjdqiEk+0c98LmyKNmEVt8XghjrZuUrn8dA0
      0hfInLdRpaB7b+UeIQavw9yLH0ilijAcMkGzzom7vdqDPizoLpXQ
      -----END RSA PRIVATE KEY-----
   [*] Your RSA public key:
      -----BEGIN PUBLIC KEY-----
      MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEArRsg1+6JZxZNMhGyuM8d
      +Ue/ky9LSv/XyKh+wppQMS5wx7QEXFcdDgaByNZeLMenh8sgungahWbPo/5jmkDu
      ...
      ...
      GrVJ3o8aDm35EzGymp4ON+A0fdAkweqKV6FqxEJqLWIDRYh+Z01JXUZIrKmnCkgf
      QQIDAQAB
      -----END PUBLIC KEY-----

   *******************************************************
   *                   PatchSolution0                    *
   *******************************************************
   [*] Previous:
   +0x0000000000000070                          01 00 00 00 05 00 00 00          ........
   +0x0000000000000080  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   +0x0000000000000090  00 00 00 00 00 00 00 00 40 cf 9e 02 00 00 00 00  ........@.......
   +0x00000000000000a0  40 cf 9e 02 00 00 00 00 00 10 00 00 00 00 00 00  @...............
   [*] After:
   +0x0000000000000070                          01 00 00 00 05 00 00 00          ........
   +0x0000000000000080  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   +0x0000000000000090  00 00 00 00 00 00 00 00 d0 d0 9e 02 00 00 00 00  ................
   +0x00000000000000a0  d0 d0 9e 02 00 00 00 00 00 10 00 00 00 00 00 00  ................

   [*] Previous:
   +0x00000000029ecf40  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   +0x00000000029ecf50  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   +0x00000000029ecf60  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   ...
   ...
   +0x00000000029ed0c0  00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00  ................
   [*] After:
   +0x00000000029ecf40  ef be ad de 4d 49 49 42 49 6a 41 4e 42 67 6b 71  ....MIIBIjANBgkq
   +0x00000000029ecf50  68 6b 69 47 39 77 30 42 41 51 45 46 41 41 4f 43  hkiG9w0BAQEFAAOC
   +0x00000000029ecf60  41 51 38 41 4d 49 49 42 43 67 4b 43 41 51 45 41  AQ8AMIIBCgKCAQEA
   ...
   ...
   ...
   +0x00000000029ed0c0  43 6b 67 66 51 51 49 44 41 51 41 42 ad de ef be  CkgfQQIDAQAB....

   [*] Previous:
   +0x0000000001413e10  44 0f b6 24 18 48 8b 44 24 28 8b 50 f8 85 d2 79  D..$.H.D$(.P...y
   +0x0000000001413e20  6f                                               o               
   [*] After:
   +0x0000000001413e10  45 31 e4 48 8d 05 2a 91 5d 01 90 90 90 90 90 90  E1.H..*.].......
   +0x0000000001413e20  90                                               .               

   [*] New RSA-2048 private key has been saved to
      /home/doublesine/github.com/navicat-keygen/RegPrivateKey.pem

   *******************************************************
   *           PATCH HAS BEEN DONE SUCCESSFULLY!         *
   *                  HAVE FUN AND ENJOY~                *
   *******************************************************
   ```

5. Repack files into a new AppImage:

   __Example:__

   ```console
   $ wget 'https://github.com/AppImage/AppImageKit/releases/download/continuous/appimagetool-x86_64.AppImage'
   $ chmod +x appimagetool-x86_64.AppImage
   $ ./appimagetool-x86_64.AppImage ~/Desktop/navicat15-premium-en-patched ~/Desktop/navicat15-premium-en-patched.AppImage
   ```

6. Run the newly-generated AppImage:

   ```console
   $ chmod +x ~/Desktop/navicat15-premium-en-patched.AppImage
   $ ~/Desktop/navicat15-premium-en-patched.AppImage
   ```

7. Use `navicat-keygen` to generate __snKey__ and __Activation Code__.

   ```
   Usage:
       navicat-keygen <--bin|--text> [--adv] <RSA-2048 Private Key File>

           <--bin|--text>    Specify "-bin" to generate "license_file" used by Navicat 11.
                             Specify "-text" to generate base64-encoded activation code.
                             This parameter must be specified.

           [--adv]                       Enable advance mode.
                                         This parameter is optional.

           <RSA-2048 Private Key File>   A path to an RSA-2048 private key file.
                                         This parameter must be specified.
   ```

   __Example:__

   ```console
   $ ./bin/navicat-keygen --text ./RegPrivateKey.pem
   ```

   You will be asked to select Navicat language and give major version number. After that an randomly generated __snKey__ will be given.

   ```console
   $ ./bin/navicat-keygen --text ./RegPrivateKey.pem
   **********************************************************
   *       Navicat Keygen (Linux) by @DoubleLabyrinth       *
   *                   Version: 1.0                         *
   **********************************************************

   [*] Select Navicat product:
   0. DataModeler
   1. Premium
   2. MySQL
   3. PostgreSQL
   4. Oracle
   5. SQLServer
   6. SQLite
   7. MariaDB
   8. MongoDB
   9. ReportViewer

   (Input index)> 1

   [*] Select product language:
   0. English
   1. Simplified Chinese
   2. Traditional Chinese
   3. Japanese
   4. Polish
   5. Spanish
   6. French
   7. German
   8. Korean
   9. Russian
   10. Portuguese

   (Input index)> 0

   [*] Input major version number:
   (range: 0 ~ 15, default: 12)> 15

   [*] Serial number:
   NAVM-RTVJ-EO42-IODD

   [*] Your name:
   ```

   You can use this __snKey__ to activate your Navicat preliminarily.
     
   Then you will be asked to input `Your name` and `Your organization`. Just set them whatever you want, but not too long.

   ```console
   [*] Your name: DoubleLabyrinth
   [*] Your organization: DoubleLabyrinth

   [*] Input request code in Base64: (Double press ENTER to end)
   ```
     
   After that, you will be asked to input request code. Now __DO NOT CLOSE KEYGEN__.

8. __Disconnect your network__. Find and click `Registration`. 
   
   Fill license key by __Serial number__ that the keygen gave and click `Activate`.

9. Generally online activation will fail and Navicat will ask you do `Manual Activation`, just choose it.

10. Copy your request code and paste it in the keygen. Input empty line to tell the keygen that your input ends.

    ```console
    [*] Input request code in Base64: (Double press ENTER to end)
    OaGPC3MNjJ/pINbajFzLRkrV2OaSXYLr2tNLDW0fIthPOJQFXr84OOroCY1XN8R2xl2j7epZ182PL6q+BRaSC6hnHev/cZwhq/4LFNcLu0T0D/QUhEEBJl4QzFr8TlFSYI1qhWGLIxkGZggA8vMLMb/sLHYn9QebBigvleP9dNCS4sO82bilFrKFUtq3ch8r7V3mbcbXJCfLhXgrHRvT2FV/s1BFuZzuWZUujxlp37U6Y2PFD8fQgsgBUwrxYbF0XxnXKbCmvtgh2yaB3w9YnQLoDiipKp7io1IxEFMYHCpjmfTGk4WU01mSbdi2OS/wm9pq2Y62xvwawsq1WQJoMg==

    [*] Request Info:
    {"K":"NAVMRTVJEO42IODD", "DI":"4A12F84C6A088104D23E", "P":"linux"}

    [*] Response Info:
    {"K":"NAVMRTVJEO42IODD","DI":"4A12F84C6A088104D23E","N":"DoubleLabyrinth","O":"DoubleLabyrinth","T":1575543648}

    [*] Activation Code:
    i45HIr7T1g69Cm9g3bN1DBpM/Zio8idBw3LOFGXFQjXj0nPfy9yRGuxaUBQkWXSOWa5EAv7S9Z1sljlkZP6cKdfDGYsBb/4N1W5Oj1qogzNtRo5LGwKe9Re3zPY3SO8RXACfpNaKjdjpoOQa9GjQ/igDVH8r1k+Oc7nEnRPZBm0w9aJIM9kS42lbjynVuOJMZIotZbk1NloCodNyRQw3vEEP7kq6bRZsQFp2qF/mr+hIPH8lo/WF3hh+2NivdrzmrKKhPnoqSgSsEttL9a6ueGOP7Io3j2lAFqb9hEj1uC3tPRpYcBpTZX7GAloAENSasFwMdBIdszifDrRW42wzXw==
    ```

11. Finally, you will get __Activation Code__ which looks like a Base64 string. 

    Just copy it and paste it in Navicat `Manual Activation` window, then click `Activate`. 
    
    If nothing wrong, activation should be done successfully.

12. Clean up:

    ```console
    $ rm ~/Desktop/navicat15-premium-en.AppImage
    $ rm -rf ~/Desktop/navicat15-premium-en-patched
    $ mv ~/Desktop/navicat15-premium-en-patched.AppImage ~/Desktop/navicat15-premium-en.AppImage
    ```

