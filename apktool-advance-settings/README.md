<div code-like box-like >
Apktool v2.0.2 - a tool for reengineering Android apk files
with smali v2.0.8 and baksmali v2.0.8
Copyright 2014 Ryszard Wi?niewski <brut .alll@gmail.com>
Updated by Connor Tumbleson <connor .tumbleson@gmail.com>
Apache License 2.0 (http://www.apache.org/licenses/LICENSE-2.0)

usage: apktool [-q|--quiet OR -v|--verbose]
 -advance,--advanced   prints advance information.
 -version,--version    prints the version then exits
usage: apktool [-q|--quiet OR -v|--verbose] if|install-framework [options] <framework .apk>
 -p,--frame-path <dir>   Stores framework files into </dir><dir>.
 -t,--tag <tag>          Tag frameworks using </tag><tag>.
usage: apktool [-q|--quiet OR -v|--verbose] d[ecode] [options] <file_apk>
    --api <api>                    The numeric api-level of the file to generate, e.g. 14 for ICS.
 -b,--no-debug-info                don't write out debug info (.local, .param, .line, etc.)
 -d,--debug                        Decode in debug mode. Check project page for more info.
    --debug-line-prefix <prefix>   Smali line prefix when decoding in debug mode. Default is "a=0;// ".
 -f,--force                        Force delete destination directory.
 -k,--keep-broken-res              Use if there was an error and some resources were dropped, e.g.
                                   "Invalid config flags detected. Dropping resources", but you
                                   want to decode them anyway, even with errors. You will have to
                                   fix them manually before building.
 -m,--match-original               Keeps files to closest to original as possible. Prevents rebuild.
 -o,--output <dir>                 The name of folder that gets written. Default is apk.out
 -p,--frame-path </dir><dir>             Uses framework files located in </dir><dir>.
 -r,--no-res                       Do not decode resources.
 -s,--no-src                       Do not decode sources.
 -t,--frame-tag <tag>              Uses framework files tagged by </tag><tag>.
usage: apktool [-q|--quiet OR -v|--verbose] b[uild] [options] <app_path>
 -a,--aapt <loc>         Loads aapt from specified location.
 -c,--copy-original      Copies original AndroidManifest.xml and META-INF. See project page for more info.
 -d,--debug              Builds in debug mode. Check project page for more info.
 -f,--force-all          Skip changes detection and build all files.
 -o,--output <dir>       The name of apk that gets written. Default is dist/name.apk
 -p,--frame-path </dir><dir>   Uses framework files located in </dir><dir>.
usage: apktool [-q|--quiet OR -v|--verbose] publicize-resources <file_path>
Make all framework resources public.

For additional info, see: http://ibotpeaches.github.io/Apktool/
For smali/baksmali info, see: http://code.google.com/p/smali/
</file_path></dir></loc></app_path></tag></dir></prefix></api></file_apk></tag></dir></framework></connor></brut></div>