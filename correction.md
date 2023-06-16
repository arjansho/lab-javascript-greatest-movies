good work!
even if the calculate average function is missing, the rest is good:)

one possible way to solve it would be:

// Iteration 3: All scores average - Get the average of all scores with 2 decimals
function scoresAverage(moviesArray) {
  if (!moviesArray.length) return 0;

  const totalScore = moviesArray.reduce((acc, curVal) => {
    if (curVal.score) {
      return acc + curVal.score;
    } else {
      return acc;
    }
  }, 0);

  const avg = totalScore / moviesArray.length;

  return +avg.toFixed(2); //toFixed(n) return only strings, therefore we use + before the variable to convert to number
}
