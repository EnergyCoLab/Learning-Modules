# Quiz

<p>Answer the following questions:</p>

<div id="quiz-container">
  <form id="quiz-form">
    <label for="q1">1. What is the capital of France?</label><br>
    <input type="radio" name="q1" value="Paris"> Paris<br>
    <input type="radio" name="q1" value="Berlin"> Berlin<br>
    <input type="radio" name="q1" value="Madrid"> Madrid<br>

    <label for="q2">2. What is the chemical symbol for water?</label><br>
    <input type="radio" name="q2" value="H2O"> H2O<br>
    <input type="radio" name="q2" value="O2"> O2<br>
    <input type="radio" name="q2" value="CO2"> CO2<br>

    <button type="button" onclick="submitQuiz()">Submit</button>
  </form>

  <div id="result"></div>
</div>

<script type="text/javascript">
  function submitQuiz() {
    let score = 0;
    const form = document.getElementById("quiz-form");

    // Question 1
    const q1 = form.querySelector('input[name="q1"]:checked');
    if (q1 && q1.value === "Paris") score++;

    // Question 2
    const q2 = form.querySelector('input[name="q2"]:checked');
    if (q2 && q2.value === "H2O") score++;

    // Display result
    const result = document.getElementById("result");
    result.innerHTML = `You scored ${score} out of 2.`;

    // Prevent form submission
    return false;
  }
</script>
