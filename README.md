# Install:

pip:

    pip install --force-reinstall git+https://github.com/DesmondN1ckl/RKPairip/RKPairip.git

uv:

    uv tool install 

# Uninstall

pip:

    pip uninstall pairip

uv:

    uv tool uninstall pairip



# Usage Example


RKPairip ( Input Mode )
-----

**Mode `-i` ➸ Default APKEditor ( Input Your APK Path )**

    RKPairip -i YourApkPath.apk

**Flag: `-a` ➸ Decompile With APKTool**

    RKPairip -i YourApkPath.apk -a

**Flag: `-n` ➸ Pairip New Method By NullRE**

    RKPairip -i YourApkPath.apk -n

**Flag: `-s` ➸ Merge Skip ( Do U Want Last Dex Add Seprate )**

    RKPairip -i YourApkPath.apk -s
    
**Flag `-r` ➸ Pairip Dex Fix ( Try After Translate String to MT )**

    RKPairip -i YourApkPath.apk -r

**Flag: `-x` Hook CoreX ( For Unity / Flutter & Crashed APK )**

    RKPairip -i YourApkPath.apk -x


RKPairip ( Merge Mode )
-----

**Mode `-m` ➸ Anti-Split ( Only Merge APK )**

`Supported Extensions ( .apks / .apkm / .xapk )`

    RKPairip -m YourApkPath.apks


RKPairip ( Credits Mode )
-----

**Mode `-C` ➸ Show Instructions & Credits**

    RKPairip -C


Fix Dex Regex
-------------

**Manually Repair Dex Regexs**


**Patch 1**

`regex`

    (# direct methods\n.method public static )FuckUByRK\(\)V([\s\S]*?.end method)[\w\W]*
    
`Replace`

    $1constructor <clinit>()V$2

**Patch 2**

`regex`

    sget-object v0, L[^;]+;->[^:]*:Ljava/lang/String;\s+const-string v1, ("(\d+.java:\d+)")\s+.line \d+\s+.local v0, "(\d+.java:\d+)":V\s+invoke-static \{v0\}, LRK_TECHNO_INDIA/ObjectLogger;->logstring\(Ljava/lang/Object;\)V
    
`Replace`

    const-string v0, $1

**Patch 3**

`regex`

    invoke-static \{\}, L[^;]+;->callobjects\(\)V\n
    
`Replace`

    # Nothing(Means Empty) 

**Patch 4**

`regex`

    (\.method public.*onReceive\(Landroid/content/Context;Landroid/content/Intent;\)V\s+\.(registers|locals) \d+)[\s\S]*?const-string/jumbo[\s\S]*?(\s+return-void\n.end method)
    
`Replace`

    $1$3


**Patch 5**

`Search 1st without regex`

    pairip
    
`Search regex in Current Results`

    invoke.*pairip/(?!licensecheck/).*

`Replace`

    # Nothing(Means Empty) 



# Credits from original creator:

## 🇮🇳 Welcome By Techno India 🇮🇳

[![Telegram](https://img.shields.io/badge/TELEGRAM-CHANNEL-red?style=for-the-badge&logo=telegram)](https://t.me/rktechnoindians)
  </a><p>
[![Telegram](https://img.shields.io/badge/TELEGRAM-OWNER-red?style=for-the-badge&logo=telegram)](https://t.me/RK_TECHNO_INDIA)
</p>
