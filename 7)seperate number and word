%{
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_LEN 100

char words[MAX_LEN][MAX_LEN];
int words_count = 0;

char numbers[MAX_LEN][MAX_LEN];
int numbers_count = 0;

void addWord(char *word) {
    strcpy(words[words_count], word);
    words_count++;
}

void addNumber(char *number) {
    strcpy(numbers[numbers_count], number);
    numbers_count++;
}

%}

DIGIT   [0-9]
NUMBER  {DIGIT}+(\.{DIGIT}+)?
WORD    [a-zA-Z]+

%%

{NUMBER} {
    addNumber(yytext);
}

{WORD} {
    addWord(yytext);
}

. ;

%%

int yywrap() {
    return 1;
}

int main() {
    yylex();
    
    printf("Words:\n");
    for (int i = 0; i < words_count; i++) {
        printf("%s\n", words[i]);
    }

    printf("\nNumbers:\n");
    for (int i = 0; i < numbers_count; i++) {
        printf("%s\n", numbers[i]);
    }

    return 0;
}
