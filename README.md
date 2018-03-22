# x86_64-linux cheatsheats

Plain files for syscalls, errnos, signals, registers, x86_64 instructions

For use with [cheat](https://github.com/chrisallenlane/cheat):

```console
$ export CHEATPATH=$CHEATPATH:/path/to/this/repo/pages
$ cheat syscalls
$ cheat registers
$ cheat errno
$ cheat EPERM
$ cheat instructions
$ cheat ADD
$ cheat signals
$ cheat SIGHUP
```

## Introspect libc

(only glibc at the moment)

```
python3 libc.py repl
Type help or ? to list commands.
> print MAP_FAILED
0xffffffffffffffff
> print PROT_WRITE|PROT_READ
3
# defaults to print command
> &errno
0x7f3cb86b3fe0
> type MAP_FAILED
void*
> type memcmp
int (void const*, void const*, unsigned long)
> size "struct timeval"
16
> offset "struct timeval" "tv_usec"
8
> members "struct timeval"
struct timeval {
    __time_t tv_sec;
    __suseconds_t tv_usec;
}
> quit
```
