


  document.addEventListener("DOMContentLoaded", function() {
    // Get a reference to the form element
    const checkoutForm = document.getElementById("checkout");

    // Function to check if the input fields are filled
    function isFormValid() {
      const cardNumber = document.getElementById("cardnumber").value;
      const cardHolder = document.getElementById("cardholder").value;
      const cvc = document.getElementById("cvc").value;

      if (!cardNumber || !cardHolder || !cvc) {
        return false;
      }
      return true;
    }

    // Function to handle the form submission
    function handleFormSubmission(event) {
      event.preventDefault();

      if (isFormValid()) {
        // Perform the purchase action here (you can add your logic for what happens after a successful purchase)
        alert("Purchase successful!");
        // You can add more code here to process the purchase, for example, sending data to a server, etc.
      } else {
        alert("Please fill in all the required fields.");
      }
    }

    // Attach the form submission handler to the "Purchase" button click event
    const purchaseButton = document.querySelector(".btn");
    purchaseButton.addEventListener("click", handleFormSubmission);
  });
