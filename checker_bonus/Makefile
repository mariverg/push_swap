NAME = checker
CC = gcc
CFLAGS = -Wall -Wextra -Werror -O2 -g
PUSH_SWAP_ARCHIVE = ../src/push_swap.a

SRCS = checker.c\
		get_next_line.c\
		get_next_line_utils.c\
OBJS = $(SRCS:.c=.o)

%.o : %.c 
	$(CC) -c $(CFLAGS) $< -o $@

all : $(NAME)

$(NAME) : $(OBJS) $(PUSH_SWAP_ARCHIVE) 
	$(CC) $^ -o $(NAME)
	cp $(NAME) ../src

$(PUSH_SWAP_ARCHIVE) :
	cd ../src && make

clean :
	rm -f $(OBJS)

fclean : clean 
	rm -f $(NAME)
	cd ../src && rm -f $(NAME)

re : fclean all

.PHONY: all clean fclean re