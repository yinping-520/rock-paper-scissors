# rock-paper-scissors
const getUserChoice = userInput => {
  userInput = userInput.toLowerCase();
  if (userInput === 'rock' || userInput ==="paper" || userInput ==="scissors") {
    return userInput;
  } else{
    console.log("error");
  }
};

const getComputerChoice = () => {
let num = Math.floor(Math.random()*3);
  if (num === 0) {return "rock"}
  if (num === 1) {return "paper"}
  if (num === 2) {return "scissors"}

    /*let num = Math.floor(Math.random()*3);
  switch (num) {
  case 0:
    return "rock";
    break;
  switch num:
  case 1:
    return "paper";
    break;
  switch num:
  case 2:
    return "scissors";
    break;}*/
};

userChoice = getUserChoice;
computerChoice = getComputerChoice;
 function determineWinner(userChoice, computerChoice) {
   if (userChoice === computerChoice) {
      return 'The game is a tie!'
  }
   if (userChoice === "bomb") {
     return "user won"
   }
 
   if (userChoice === 'rock') {
      if (computerChoice === 'paper') {
        return 'The computer won!'
      } else {
        return 'You won!'
  }
}
   if (userChoice === "paper") {
     if (computerChoice === "scissors"){
       return "computer won"
     } else{
       return "user won"
   }
 }

  if (userChoice === "scissors") {
     if (computerChoice === "rock"){
       return "computer won"
     } else{
       return "user won"
     }
   }
 }

 console.log(determineWinner("rock","paper"));
 console.log(determineWinner("scissors","paper"));
 console.log(determineWinner('paper', 'scissors')); // prints something like 'The computer won!'
console.log(determineWinner('paper', 'paper')); // prints something like 'The game is a tie!'
console.log(determineWinner('paper', 'rock')); // prints something like 'The user won!'


function playGame(userChoice, computerChoice) {
  console.log(determineWinner(userChoice, computerChoice));
};
playGame("bomb", "paper")
