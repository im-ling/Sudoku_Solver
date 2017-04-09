# Sudoku_Solver

how to use:

	  	let originMap: [[Int]] = [[9,0,0, 5,0,0, 0,0,0],
                                  [0,0,0, 0,0,0, 1,0,7],
                                  [0,0,0, 2,0,0, 0,0,0],
                                  
                                  [2,9,0, 0,0,0, 3,0,0],
                                  [4,0,0, 0,0,2, 0,6,0],
                                  [0,0,5, 0,0,3, 0,7,9],
                                  
                                  [0,0,0, 7,0,0, 5,0,0],
                                  [0,3,6, 9,0,0, 0,0,0],
                                  [0,0,2, 3,0,1, 0,4,0]]
        
        let solver = DLSudokuSolver.sharedSudokuSolver
        
        solver.originMap = originMap	//1. give the map to the solver
        
        solver.solveSudoku()    //2. solving puzzle map(or you can say the originMap)
        
        if solver.isUnavailableMap {    // 3. check the map is available or not
            print("UnavilableMap")
        }else{
            for (i,map) in solver.resultMap.enumerated() { 			// 4. print
                print("Result \(i+1):")
                solver.printTwoDimensionalArray(two_DimensionalArray: map)
                print(" ")
            }
        }