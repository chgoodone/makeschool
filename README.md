# makeschool

Collaborators:  Henry

import Foundation
func length(string:String)->Int{
    var countNumber = 0
    for _ in  string.characters{
        countNumber+=1
    }
    return countNumber
}

func palindrome(input:String)->Bool{
    var result = true
    var number = length(string:input)
    number = number-1
    for i in  0...number {
        let index = input.index(input.startIndex,offsetBy:i)
        let index2 = input.index(input.startIndex,offsetBy:number-i)
        let char = input[index]
        let char2 = input[index2]
        if char != char2{
            result = false
        }
    }
    return result
}

palindrome(input: "hhhooohhh")










func tell2DArray(input:[[Int]])->Bool{
    
    func horizen(twoDarray:[[Int]])->Int{
        var horizenNumber = 0
        for _ in twoDarray[0]{
            horizenNumber = horizenNumber+1
        }
        return horizenNumber
    }
    
    
    var VerticalNumber=input.count
    VerticalNumber-=1
    horizen(twoDarray: input)
    var result = true
    var horizenNumber=horizen(twoDarray: input)
    let firstNumber = input[0][0]
    horizenNumber=horizenNumber-1
    
    for n in 0...VerticalNumber{
        
        
        for i in 0...horizenNumber{
            let element = Int(Double(firstNumber) * (pow(2.0, Double(i+n))))
            print("element :", element, " i:", i, " n:", n,"firstNumber:",firstNumber)
            if element != input[n][i]{
                result = false
                
            }
            
        }
    }
    return result
}

tell2DArray(input: [[2,4,8,16,32],[4,8,16,32,64],[8,16,32,64,128]])










