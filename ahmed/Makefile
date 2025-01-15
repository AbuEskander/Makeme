include Includes.mk
CC = cc 
CFLAGS = -Wall -Werror -Werror -I.includes/ 
SRC_DIR = src
OBJ_DIR = build
NAME = ahmed 
SRCSDIR = $(addprefix src/,$(SRCS))
OBJS = $(patsubst $(SRC_DIR)/%.c, $(OBJ_DIR)/%.o, $(SRCSDIR)) 

all:$(NAME)

$(NAME):$(OBJS)
	$(CC) $(OBJS) $(CFLAGS) -o $(NAME)
$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(OBJ_DIR)
	$(CC) $(CFLAGS) -c $< -o $@
clean:
	rm -f $(OBJS)
fclean:clean
	rm -f $(NAME) 
re: fclean all
.PHONY: all clean fclean re
