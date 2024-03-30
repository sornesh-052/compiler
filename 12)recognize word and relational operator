%{
#include <stdio.h>
%}

%%
[a-zA-Z]+       printf("Word: %s\n", yytext);
"<"             printf("Relational Operator: %s\n", yytext);
">"             printf("Relational Operator: %s\n", yytext);
"<="            printf("Relational Operator: %s\n", yytext);
">="            printf("Relational Operator: %s\n", yytext);
"=="            printf("Relational Operator: %s\n", yytext);
"!="            printf("Relational Operator: %s\n", yytext);
.|\n            ;
%%

int main() {
    yylex();
}

int yywrap()
{
return 1;
}
