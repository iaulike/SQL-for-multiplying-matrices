# SQL-for-multiplying-matrices

This SQL snippet I wrote gets the 3,5 element of the matrix multiplication of A and B:

SELECT A.row_num, B.col_num, sum(A.value * B.value)

FROM A, B

WHERE A.col_num = B.row_num AND A.row_num = 3 AND B.col_num = 5

GROUP BY A.row_num, B.col_num ;

A quote from Bill Howe, instructor of the Data Science at Scale course, regarding why someone would want to use SQL to do matrix multiplication:

"If you're wondering why this might be a good idea, consider that advanced databases execute queries in parallel automatically. So it can be quite efficient to process a very large sparse matrix --- millions of rows or columns --- in a database. But a word of warning: In a job interview, don't tell them you recommend implementing linear algebra in a database. You won't be wrong, but they won't understand databases as well as you now do, and therefore won't understand when and why this is a good idea. Just say you have done some experiments using databases for analytics, then mention the papers in the reading if they seem incredulous!"

I feel certain I'm going to want to do this one day as my statistics PhD was linear algebra. Good for multiplying X transpose by X, where X is n by p and sparse. 
