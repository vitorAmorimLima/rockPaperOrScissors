# rockPaperOrScissors
const getUserChoice = userInput => {
  userInput = userInput.toLowerCase();
  if(userInput === 'rock' || userInput === 'scissors'|| userInput === 'paper') {
    return userInput;
  } else {
    console.log('Error, pelase type: rock, paper or scissors.');
  }
}

const getComputerChoice = () => {
 const randomNumber = Math.floor(Math.random()* 3)
  switch (randomNumber) {
    case 0:
     return 'rock';
    case 1:
     return 'scissors';
    case 2:
     return 'paper';
  }
};

const determineWinner = (userChoice, computerChoice) => {
  if (userChoice === computerChoice)
  return 'Draw!';
}
if (userChoice === 'rock') {
  if(computerChoice === 'paper') {
    return "Sorry, computer won!";
  } else {
    return "Congratulations,you won!";
  }
};

if(userChoice === 'paper') {
 if(computerChoice === 'scissors') {
  return "computer won!"
  } else {
   return "Congratulations, you won!";
   }

 if (userChoice === 'scissors') {
   if (computerChoice === 'paper') {
     return 'computer won!'
   } else {
     return "Congratulations, you won!";
   }
 }
};

console.log(determineWinner('rock', "scissors"));
console.log(determineWinner('paper', 'scissors'));
console.log(determineWinner('rock', 'rock'));
