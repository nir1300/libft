# libft

My first C library: a re-implementation of a set of standard C library functions, plus a few additional utilities and a small linked-list API. It is built as a static library, `libft.a`, and reused by my later 42 projects (`so_long`, `pipex`, `push_swap`).

Written for the 42 curriculum.

## Build

```bash
make          # builds libft.a
make bonus    # also adds the linked-list functions
make clean
make fclean
make re
```

Use it in a project:

```c
#include "libft.h"
```

```bash
cc main.c -L. -lft
```

## Contents

### Standard library re-implementations

| Area | Functions |
|------|-----------|
| Character tests | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint` |
| Case conversion | `ft_toupper`, `ft_tolower` |
| Strings | `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup` |
| Memory | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc` |
| Conversion | `ft_atoi` |

### Additional utilities

| Function | Purpose |
|----------|---------|
| `ft_substr` | extract a substring |
| `ft_strjoin` | concatenate two strings into a new one |
| `ft_strtrim` | trim a set of characters from both ends |
| `ft_split` | split a string on a delimiter into a NULL-terminated array |
| `ft_itoa` | integer to string |
| `ft_strmapi`, `ft_striteri` | apply a function to every character |
| `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd` | write to a file descriptor |

### Bonus: linked lists

A singly linked list built around `t_list`: `ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`, `ft_lstsize`, `ft_lstlast`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`.

## Notes

All functions that allocate memory return `NULL` on failure, and the code follows the 42 Norm. The `*_bonus.c` files contain the list functions and are only compiled by `make bonus`.
