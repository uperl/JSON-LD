# JSON::LD ![static](https://github.com/uperl/JSON-LD/workflows/static/badge.svg)

Load and dump JSON files

# SYNOPSIS

```perl
use JSON::LD;

DumpFile("foo.json", { a => 1 });
my $data - LoadFile("foo.json:");
```

# DESCRIPTION

**NOTE**: Not to be confused with [JSON-LD](https://metacpan.org/pod/JSONLD).

Ever want to load JSON from a file?  Ever forget which module it is that you are
supposed to be using now?  Is it [JSON](https://metacpan.org/pod/JSON) or [JSON::PP](https://metacpan.org/pod/JSON::PP) or [JSON::XS](https://metacpan.org/pod/JSON::XS) or
[JSON::Syck](https://metacpan.org/pod/JSON::Syck) or [Cpanel::JSON::XS](https://metacpan.org/pod/Cpanel::JSON::XS) (how many Ns are in Cpanel?  For some reason
I am bad at spelling) or [JSON::MaybeXS](https://metacpan.org/pod/JSON::MaybeXS) or 
`JSON::XS::TheNextForkBecausePreviousMaintainerTurnedOutToBeADouche`.
Which file mode are you supposed to be using again?  It's UTF-8 but I think I'm
supposed to read it as binary?  I forget and I have a headache now.

This module is for you.  It uses a similar interface to [YAML](https://metacpan.org/pod/YAML) for loading
and dumping files.

# FUNCTIONS

All functions are exported by default.

## DumpFile

```
DumpFile($filename, $data);
```

Dumps the data in `$data` to `$filename` as properly encoded JSON.  If `$data`
cannot be represented as JSON or if there is an IO error it will throw an
exception.

## LoadFile

```perl
my $data = LoadFile($filename);
```

Loads the data in JSON format from `$filename`.  If the JSON in `$filename`
is not properly formatted or encoded or if there is an IO error it will throw
an exception.

# CAVEATS

This module is a parody.  However the struggle is real.

# SEE ALSO

- [JSON::MaybeXS](https://metacpan.org/pod/JSON::MaybeXS)
- [Path::Tiny](https://metacpan.org/pod/Path::Tiny)

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2024 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
