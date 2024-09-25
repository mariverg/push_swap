NAME = push_swap
ARCHIVE = push_swap.a
CC = gcc
CFLAGS = -Wall -Werror -Wextra -g -O2 
MAKE_LIB = ar -rcs

SRCS = error_free.c\
		main.c\
		push_command.c\
		push_swap_command.c\
		push_swap_init.c\
		reverse_rotate_command.c\
		split.c\
		stack_init.c\
		stack_init.c\
		swap_command.c\
		tiny_sort.c\

OBJS = $(SRCS:.c=.o)

all : $(NAME)

$(NAME) : $(ARCHIVE)
	$(CC) $< -o $@

$(ARCHIVE) : $(OBJS)
	$(MAKE_LIB) $(ARCHIVE) $^

%.o : %.c 
	$(CC) $(CFLAGS) -c $< -o $@ 

bonus : 
	cd ../checker_bonus && make
	
clean :
	rm -f $(OBJS) $(ARCHIVE)

fclean : clean
	rm -f $(NAME)
	cd ../checker_bonus && make fclean

re : fclean all

.PHONY : all clean fclea re