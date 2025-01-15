include Includes.mk
CC= cc 
CFLAG= -Wall -Werror -Werror -I.includes/ 
SRC_DIR= src 
OBJ_DIR= build
NAME= basil 
SRCSDIR= $(addperfix src/,$(SRCS))
OBJS= $(patsubst $(SRC_DIR)/%.c, $(OBJ_DIR)/%.o, $(SRCSDIR)) 

all:$(NAME)
	$(NAME):$(OBS)
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
