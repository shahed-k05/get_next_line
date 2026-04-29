*This activity has been created as part of the 42 curriculum by syasin.*
# Get Next Line

This project implements the `get_next_line` function in C.  
It reads a file line by line, returning one line per call.  

## Files

- `get_next_line.c` – main function implementation  
- `get_next_line_utils.c` – helper functions  
- `get_next_line.h` – function prototypes and includes  

## Usage

```c
int main()
{
    int fd;
    char *line;
    int lines = 1;

    fd = open("test.txt", O_RDONLY);

    while ((line = get_next_line(fd)) != NULL)
    {
        printf("%d->%s", lines++, line);
        free(line);
    }

    close(fd);
}
