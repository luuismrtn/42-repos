
NAME = push_swap

LIBFT_DIR = ./libft

LIBFT = $(LIBFT_DIR)/libft.a

SRCS = main.c \

OBJS = $(SRCS:.c=.o)

CC = cc
CFLAGS = -Wall -Wextra #-Werror

all: $(LIBFT) $(NAME)

$(LIBFT):
	@make -C $(LIBFT_DIR)

$(NAME): $(OBJS)
	$(CC) $(CFLAGS) -o $(NAME) $(OBJS) $(LIBFT)

%.o: %.c push_swap.h
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJS)
	@make clean -C $(LIBFT_DIR)

fclean: clean
	rm -f $(NAME)
	@make fclean -C $(LIBFT_DIR)

re: fclean all

.PHONY: all clean fclean re
