[![Actions Status](https://github.com/sanko/Acme-EvilInsult/actions/workflows/ci.yml/badge.svg)](https://github.com/sanko/Acme-EvilInsult/actions) [![MetaCPAN Release](https://badge.fury.io/pl/Acme-EvilInsult.svg)](https://metacpan.org/release/Acme-EvilInsult)
# NAME

Acme::EvilInsult - Programmatically Generate Evil Insults

# SYNOPSIS

```perl
use Acme::EvilInsult qw[insult];
say insult( ); # stringify
```

# DESCRIPTION

Acme::EvilInsult provides 'evil' 'insulting' statements generated by the RESTful Evil Insult Generator API.

# METHODS

These functions may be imported by name or with the `:all` tag.

## `insult( [...] )`

Tear someone down.

```perl
my $shade = insult( ); # Random insult
print insult( language => 'fr' ); # stringify
```

You may request specific insults by passing parameters.

Expected parameters include:

- `language`

    Insult's language. The default is `en`. Supported languages include: `en`, `fr`, `cn`, `ja`, `es`, etc.

On success, an insult is returned as a blessed hash reference containing the following data:

- `active`

    Boolean value. If true, the insult is part of the public API.

- `comment`

    This often provides contextual information about the insult's source of the insult itself.

- `created`

    ISO 8601 date.

- `createdby`
- `insult`
- `language`

    The language of the insult.

- `number`

    The numeric id of the insult.

- `shown`

    A running tally indicating how many times this insult has been seen.

# LICENSE & LEGAL

Copyright (C) Sanko Robinson.

This library is free software; you can redistribute it and/or modify it under the terms found in the Artistic License
2\. Other copyrights, terms, and conditions may apply to data transmitted through this module.

Insults are generated by the [Evil Insult Generator](https://evilinsult.com/).

# AUTHOR

Sanko Robinson <sanko@cpan.org>
