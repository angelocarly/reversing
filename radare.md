# Radare2 notes
```
r2 <binary>
radare2 <binary>
```

## General
- Help `?`
- Analyze binary
  - `aaa`
- Seek
  - Go to address or function
  - `s <string>`

## Modes
### Visual 'V'
- Switch views: `p`
  - Reverse switch `P`
- Open prompt: `shift+:`
- Go into function `enter`
  - return `u`
- Exit visual mode `q`

## Doing stuff
### Cross referencing
- `:` `axt`
- `:` `axf`
- (a)nalysis -> (x)cross refs -> (t)o
- (a)nalysis -> (x)cross refs -> (f)rom

### View imports/exports
- (i)nfo -> (i)mports
- (i)nfo -> (E)xports

### List all function
- (a)nalysis (f)unction (l)ist  +  (l)verbose !!!!

### Get strings
- (i)nfo (z)trings
- (i)nfo (z)trings (z)ALL

### Rename function
- (a)nalysis (f)unction (n)ame

### Flags spaces
- List flag spaces / select all spaces
  - `fs`
- Select specific space
  - `fs <name>`
- Show selected space
- `f`

### Searching
`/ <string>`

Search for wide characters
- `[0x00000000]> /w Hello`
Case insensitive
- `[0x0040488f]> /i Stallman`
Hexadecimal escape sequence
- `[0x00000000]> / \x7FELF`
Hexadecimal string
- `[0x00000000]> /x 7F454C46`

The results are stored in the searches flag space
