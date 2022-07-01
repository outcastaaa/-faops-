# -faops-
在 GitHub 上建立一个 repo, 使用 Markdown 格式, 自己把 faops 的 tests/ 目录下的测试还原成可以运行的命令, 写一个关于 faops 的使用说明书. 每完成一段代码或文档, 用 GitHub Desktop 将本地的修改同步到 GibHub 上
## 介绍
 1. faops 操作 fasta 文件
 2. 在生物信息学中，FASTA格式是一种用于记录**核酸序列或肽序列**的文本格式，其中的核酸或氨基酸均以单个字母编码呈现。该格式同时还允许在序列之前定义名称和编写注释。这一格式最初由FASTA软件包定义，但现今已是生物信息学领域的一项标准。FASTA格式是BLAST组织数据的基本格式，无论是数据库还是查询序列，还是各种生物的基因组序列数据也都是用FASTA格式进行存储的，大多数情况都使用FASTA格式。另外，FASTA简明的格式降低了序列操纵和分析的难度，令序列可被文本处理工具和诸如Python、Ruby和Perl等脚本语言处理。

## 下载
```bash
brew install wang-q/tap/faops
git clone https://github.com/wang-q/faops
cd faops
make
```

## Faops 语句
```bash

Usage:     faops <command> [options] <arguments>
Version:   0.8.21

Commands:
    help           print this message
    count          count base statistics in FA file(s)
    size           count total bases in FA file(s)
    masked         masked (or gaps) regions in FA file(s)
    frag           extract sub-sequences from a FA file
    rc             reverse complement a FA file
    one            extract one fa record
    some           extract some fa records
    order          extract some fa records by the given order
    replace        replace headers from a FA file
    filter         filter fa records
    split-name     splitting by sequence names
    split-about    splitting to chunks about specified size
    n50            compute N50 and other statistics
    dazz           rename records for dazz_db
    interleave     interleave two PE files
    region         extract regions from a FA file

Options:
    There're no global options.
    Type "faops command-name" for detailed options of each command.
    Options *MUST* be placed just after command.
```
## 用法举例
* 用cat把序列信息写入test.fa文件
```bash
>1
ACCCCAGGACTCCCGAGGGTGGCCTGAGGGGGTTCCGACTCCCTGTTCGTCGGGCATGCC
CTGTGGCCTGGCACCCAGCCCTGAGCAGGGTGGCCTCTGCTGCTTGCTACCTCCACAGCC
CTTTTCAACTCTTGCCCTTTTGTCTGCAGCCCGCCACCTCTTCTGAAGGGCCTCTGCGTG
GCTTTTACCCCCTTTTTGTTTACCAAGGCTTTTTTTTTTTTTAATTCCTTTAAGTCACTT
GGCAGAATGGGCTGGGTGCAGAGAGTGTTCTTGCATGACGGAGCTGAGAGGGAGCCACTC
TCCAAAGGCTCTGTATTCCTGCCACTCAGGCTGTGTCTCCGGGGGAAAGGAGGGGGTCCA
TTACCCCGCTGAGGAGTTCAGATGTTCATGGTGGGGCTGGAGCTGCTGACACATGCAGCT
GAGCTGTCAGGCCCCCACATGCCCTTCTTTGAGAAGATGCTTGGGGGGCAAGGGCCTCAG
TCCTGCTTGGCTGCTCCTGTTTGTAGAGGTTTCCTTGCTGGGGAGGTAGGGAGGATGAGT
TATTCCCGCTTCACTCTCTGGTCTTGTCTGTCCAAAAAGGAATCCATCTTCTCGCCCACT
GCCTGCTTCCTCACCTGCCA
```
