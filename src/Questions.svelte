<script>
  let Q = [
    {
      question: "how do you stop the car",
      options: [
        "A. Press the hooter",
        "B. Use the indicator",
        "C. Use the brake"
      ],
      answer: "C"
    },
    {
      question: "how do you start the car",
      options: [
        "A. Press the hooter",
        "B. Use the indicator",
        "C. Use the key"
      ],
      answer: "C"
    }
  ];

  let QNum = 0;

  function inc() {
    QNum++;
    if (QNum == 2) {
      QNum = 0;
    }
    
  }
</script>

<div>
  <p>{Q[QNum].question}</p>
  {#each Q[QNum].options as option}
       <label>
    <input type="radio" />
    <span>{option}</span>
  </label>
  <br>
  {/each}
  

  <button on:click={inc} class="btn">Next</button>
</div>
