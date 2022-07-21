# libemojicons

[![](https://img.shields.io/github/v/tag/thechampagne/libemojicons?label=version)](https://github.com/thechampagne/libemojicons/releases/latest) [![](https://img.shields.io/github/license/thechampagne/libemojicons)](https://github.com/thechampagne/libemojicons/blob/main/LICENSE)

A **C** library to parse :emoji: notation to unicode representation.

### Installation & Setup

#### 1. Clone the repository
```
git clone https://github.com/thechampagne/libemojicons.git
```
#### 2. Navigate to the root
```
cd libemojicons
```
#### 3. Build the project
```
cargo build
```

### Example

```c
#include <stdio.h>
#include <emojicons.h>

int main()
{
  char* res = emojicons_emoji_formatter("Hello World :smile:");
  if (res == NULL)
  {
    printf("Something went wrong\n");
    return -1;
  }
  printf("%s\n", res); // Hello World 😄
  emojicons_free(res);
  return 0;
}
```

### References
 - [emojicons](https://github.com/jiri/rust-emojicons)

### License

This repo is released under the [MIT](https://github.com/thechampagne/libemojicons/blob/main/LICENSE).
