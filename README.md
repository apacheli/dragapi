# dragapi

### About

Deno bindings for [PokéAPI](https://pokeapi.co/).

See the generated documentation
[here](https://doc.deno.land/https/github.com/apacheli/dragapi/raw/dev/mod.ts).

### Example

Make sure to enable `--allow-net`.

```ts
import { getPokemon } from "https://github.com/apacheli/dragapi/raw/dev/mod.ts";

while (true) {
  const input = prompt("Enter the ID or name of a Pokémon:");
  if (input) {
    try {
      console.log(await getPokemon(input));
    } catch {
      console.log("Couldn't find that Pokémon...");
    }
  } else {
    console.log(
      "You provided no input. Please try again! (use ctrl+c to exit)",
    );
  }
}
```
