NAME = libftprintf.a
CC = gcc
CFLAGS = -Wall -Wextra -Werror
HEADER = -I libft.h
SRCS = ft_printf.c\
		print_c.c\
		print_d.c\
		print_s.c\
		print_u.c\
		print_p.c\
		print_xX.c\
		put_num_dx.c
OBJS = $(SRCS:%.c=%.o)

all: $(NAME)

$(NAME): $(OBJS)
	ar rc $(NAME) $(OBJS)
%.o:%.c
	$(CC) $(CFLAGS) $(HEADER) -o $@ -c $<
clean:
	rm -f $(OBJS)
fclean: clean
	rm -f $(NAME)
re: fclean all
test: $(NAME)
	$(CC) $(CFLAGS) $(HEADER) $(NAME) main.c &&./a.out
t: $(NAME)
	$(CC) $(CFLAGS) $(HEADER) $(NAME) main.c
test-: $(NAME)
	$(CC) $(NAME) main.c &&./a.out

.PHONY: all clean fclean re 