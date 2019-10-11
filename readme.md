﻿[English readme]
strings+ command scan binary file, print all ascii strings and all unicode strings. it can run in windows and linux, it can run in x86 and x64.

Format:
[strings+] [path] [-n [filename]] [-q] [-l [length]] [-h]
    [strings+]      command name, if windows that is strings+.exe, if linux that is strings+
    [path]          source files' directory, example: c:\mydir  or /home/mydir
    [-n [filename]] source files wildcard, example: -n *.exe
    [-q]            be quiet, no output message. example: -q
    [-l [length]]   filter string's max length, no less than 2. example: -l 3
    [-h]            show help message.
Sample in windows:
    1. path:>strings+.exe [path]                scan all files in [path]
    2. path:>strings+.exe [path] -n [filename]  scan [filename] in [path]
    3. path:>strings+.exe [path] -n [*.*]       scan *.* in [path]
    4. path:>strings+.exe [path] -n [*.exe] -l 3  scan string that length <= 3 from *.exe in [path]

Sample in linux:
    1. $./strings+ [path]                scan all files in [path]
    2. $./strings+ [path] -n '[filename]'  scan [filename] in [path]
    3. $./strings+ [path] -n '[*.*]'       scan *.* in [path]
    4. $./strings+ [path] -n '[*.exe]' -l 3  scan string that length <= 3 from *.exe in [path]
Output:
    Output to a file named [path]/t.[filename].txt
    
    
������˵����
strings+ �������ɨ��������ļ�����ӡ�����е�ascii���ַ����������е�unicode�ַ�����������������windowsƽ̨������linuxƽ̨��

��ʽ:
[strings+] [path] [-n [filename]] [-q] [-l [length]] [-h]
    [strings+]      �������������windows��Ϊstrings+.exe�������linuxƽ̨����strings+
    [path]          ��Ҫɨ����ļ�������Ŀ¼����ע����Ŀ¼��������ȫ·�������������ļ�����������: c:\mydir  or /home/mydir
    [-n [filename]] -nѡ�ָ��Ҫɨ����ļ����ļ��������԰���ͨ���*,?��������: -n *.exe������-n my.bin
    [-q]            -qѡ�ָ����Ĭ���У�����ʱ����ӡ������. ����: -q
    [-l [length]]   -lѡ�ָ��һ���ַ������ȹ��ˣ�ɨ��������ַ����������С��ָ�����ȣ��򱻺��ԣ�������ȱ�����ڵ���2. ����: -l 3
    [-h]            -hѡ���ʾ������Ϣ.
windows�µ�ʹ�þ���:
    1. path:>strings+.exe [path]                  ɨ��[path]Ŀ¼�����е��ļ�
    2. path:>strings+.exe [path] -n [filename]    ɨ��[path]Ŀ¼��ƥ��[filename]���ļ�
    3. path:>strings+.exe [path] -n [*.*]         ɨ��[path]Ŀ¼�����е��ļ�
    4. path:>strings+.exe [path] -n [*.exe] -l 3  ɨ��[path]Ŀ¼��*.exe�ҳ���<=3���ַ���
    

Sample in linux:
    1. $./strings+ [path]                	   ɨ��[path]Ŀ¼�����е��ļ�
    2. $./strings+ [path] -n '[filename]'    ɨ��[path]Ŀ¼��ƥ��[filename]���ļ�
    3. $./strings+ [path] -n '[*.*]'         ɨ��[path]Ŀ¼�����е��ļ�
    4. $./strings+ [path] -n '[*.exe]' -l 3  ɨ��[path]Ŀ¼��*.exe�ҳ���<=3���ַ���
������:
    ɨ��������ַ������ᱣ�浽һ���ı��ļ��������ļ������ں�Դ�ļ���ͬ��Ŀ¼�£�����ļ������ƺ�Դ�ļ�������ƥ�䣬����ļ���������ʽΪ��[path]/t.[Դ�ļ���].txt��