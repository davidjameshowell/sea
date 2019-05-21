Sea
===

clone of seashells.io

## Setup
```
git clone https://github.com/navigaid/sea
cd sea
go run .
```

## Play
```
exec 3<>/dev/tcp/127.0.0.1/1337
jq . <(head -n1 <(jq -c --unbuffered . <(cat <&3)))
echo hello >&3
echo world >&3
htop >&3
neofetch >&3

neofetch | nc localhost 1337

neofetch > /dev/tcp/127.0.0.1/1337

cat <(neofetch) - | nc localhost 1337

htop | nc localhost 1337

clear | nc localhost 1337
```

## Refs
- https://stackoverflow.com/questions/32684119/exit-when-one-process-in-pipe-fails/53382807#53382807
- https://news.ycombinator.com/item?id=14739479
- https://github.com/anishathalye/seashells
- https://github.com/mthenw/frontail
- https://seashells.io/
