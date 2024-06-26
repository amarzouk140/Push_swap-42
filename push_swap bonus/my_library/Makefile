# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: amarzouk <amarzouk@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/01/03 22:12:55 by ayman_marzo       #+#    #+#              #
#    Updated: 2024/02/05 17:09:32 by amarzouk         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME			= libft.a

INC				= inc/
SRC_DIR			= src/
OBJ_DIR			= obj/

CC				= gcc
CFLAGS			= -Wall -Wextra -Werror -I
RM				= rm -f
AR				= ar rcs

LIBFT_DIR =		$(SRC_DIR)libft/ft_isalnum.c \
				$(SRC_DIR)libft/ft_isalpha.c \
				$(SRC_DIR)libft/ft_isascii.c \
				$(SRC_DIR)libft/ft_isdigit.c \
				$(SRC_DIR)libft/ft_isprint.c \
				$(SRC_DIR)libft/ft_bzero.c \
				$(SRC_DIR)libft/ft_calloc.c \
				$(SRC_DIR)libft/ft_memchr.c \
				$(SRC_DIR)libft/ft_memcmp.c \
				$(SRC_DIR)libft/ft_memmove.c \
				$(SRC_DIR)libft/ft_memcpy.c \
				$(SRC_DIR)libft/ft_memset.c \
				$(SRC_DIR)libft/ft_putchar_fd.c \
				$(SRC_DIR)libft/ft_putendl_fd.c \
				$(SRC_DIR)libft/ft_putnbr_fd.c \
				$(SRC_DIR)libft/ft_putstr_fd.c \
				$(SRC_DIR)libft/ft_atoi.c \
				$(SRC_DIR)libft/ft_itoa.c \
				$(SRC_DIR)libft/ft_tolower.c \
				$(SRC_DIR)libft/ft_toupper.c \
				$(SRC_DIR)libft/ft_split.c \
				$(SRC_DIR)libft/ft_strchr.c \
				$(SRC_DIR)libft/ft_strdup.c \
				$(SRC_DIR)libft/ft_striteri.c \
				$(SRC_DIR)libft/ft_strjoin.c \
				$(SRC_DIR)libft/ft_strlcat.c \
				$(SRC_DIR)libft/ft_strlcpy.c \
				$(SRC_DIR)libft/ft_strlen.c \
				$(SRC_DIR)libft/ft_strmapi.c \
				$(SRC_DIR)libft/ft_strncmp.c \
				$(SRC_DIR)libft/ft_strncpy.c \
				$(SRC_DIR)libft/ft_strnstr.c \
				$(SRC_DIR)libft/ft_strrchr.c \
				$(SRC_DIR)libft/ft_strtrim.c \
				$(SRC_DIR)libft/ft_substr.c \
				$(SRC_DIR)libft/ft_lstadd_back.c \
				$(SRC_DIR)libft/ft_lstadd_front.c \
				$(SRC_DIR)libft/ft_lstclear.c \
				$(SRC_DIR)libft/ft_lstdelone.c \
				$(SRC_DIR)libft/ft_lstiter.c \
				$(SRC_DIR)libft/ft_lstlast.c \
				$(SRC_DIR)libft/ft_lstmap.c \
				$(SRC_DIR)libft/ft_lstnew.c \
				$(SRC_DIR)libft/ft_lstsize.c \
				$(SRC_DIR)libft/ft_strcmp.c 

FTPRINTF_DIR	=	$(SRC_DIR)ft_printf/ft_printf.c \
					$(SRC_DIR)ft_printf/ft_func1.c \
					$(SRC_DIR)ft_printf/ft_func2.c \

GNL_DIR			=	$(SRC_DIR)get_next_line/get_next_line.c \
					$(SRC_DIR)get_next_line/get_next_line_utils.c \

SRC 			= $(LIBFT_DIR) $(FTPRINTF_DIR) $(GNL_DIR)

OBJ 			= $(patsubst $(SRC_DIR)%.c,$(OBJ_DIR)%.o,$(SRC))

all: 			$(NAME)

$(NAME): 		$(OBJ)
				@$(AR) $(NAME) $(OBJ)

$(OBJ_DIR)%.o:	$(SRC_DIR)%.c
				@mkdir -p $(@D)
				@$(CC) $(CFLAGS) $(INC) -c $< -o $@

clean:
				@$(RM) -r $(OBJ_DIR)
				@$(RM) .cache_exists

fclean: 		clean
				@$(RM) $(NAME)

re: 			fclean all

.PHONY: 		all clean fclean re