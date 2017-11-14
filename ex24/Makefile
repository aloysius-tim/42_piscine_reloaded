# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: tkeynes <marvin@42.fr>                     +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/11/14 17:06:17 by tkeynes           #+#    #+#              #
#    Updated: 2017/11/14 17:06:25 by tkeynes          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC				= gcc
CFLAGS			= -Wall -Werror -Wextra
NAME			= libft.a
LIST_HEADER		= libft.h
LIST_C_LIBFT	= 	ft_putchar.c \
					ft_putstr.c \
					ft_strcmp.c \
					ft_strlen.c \
					ft_swap.c

PATH_LIBFT		= $(addprefix srcs/, $(LIST_C_LIBFT))
LIST_OBJ_LIBFT	= $(subst .c,.o,$(PATH_LIBFT))

all: $(NAME)

%.o: %.c
	$(CC) $(CFLAGS) -I./includes/ -c -o $@ $<

$(NAME): $(LIST_OBJ_LIBFT)
	ar rc $(NAME) $(LIST_OBJ_LIBFT)
	ranlib $(NAME)

clean:
	rm -rf $(LIST_OBJ_LIBFT)

fclean: clean
	rm -rf $(NAME)

re: fclean all

.PHONY: clean fclean re clear all libft.a
