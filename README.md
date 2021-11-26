# ritu
<script>

// Javascript Code For A Boolean Matrix Question
	
	function modifyMatrix(mat,R,C)
	{
		let row=new Array(R);
		let col = new Array(C);
		
		/* Initialize all values of row[] as 0 */
		for (i = 0; i < R; i++)
		{
			row[i] = 0;
		}
		
		/* Initialize all values of col[] as 0 */
		for (i = 0; i < C; i++)
		{
			col[i] = 0;
			
		}
		
		/* Store the rows and columns to be marked as
		1 in row[] and col[] arrays respectively */
		for (i = 0; i < R; i++)
		{
			for (j = 0; j < C; j++)
			{
				if (mat[i][j] == 1)
				{
					row[i] = 1;
					col[j] = 1;
				}
			}
		}
		
		/* Modify the input matrix mat[] using the
		above constructed row[] and col[] arrays */
		for (i = 0; i < R; i++)
		{
			for (j = 0; j < C; j++)
			{
				if ( row[i] == 1 || col[j] == 1 )
				{
					mat[i][j] = 1;
				}
			}
		}
	}
	
	/* A utility function to print a 2D matrix */
	function printMatrix(mat,R,C)
	{
		let i, j;
		for (i = 0; i < R; i++)
		{
			for (j = 0; j < C; j++)
			{
				document.write(mat[i][j]+ " ");
			}
			document.write("<br>");
		}
	}
	
	/* Driver program to test above functions */
	
	let mat = [[1, 0, 0, 1],[0, 0, 1, 0],[0, 0, 0, 0]];
	document.write("Matrix Initially <br>")
	printMatrix(mat, 3, 4);
	modifyMatrix(mat, 3, 4);
	document.write("Matrix after modification n <br>");
	printMatrix(mat, 3, 4);
	
	// This code is contributed by avanitrachhadiya2155
	
</script>
