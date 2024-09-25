# code3
* {
    box-sizing: border-box;
    font-family: 'Times New Roman', Times, serif; /* Set Times New Roman globally */
}

body {
    background: linear-gradient(135deg, #2eddff, #0467fb); /* Vibrant gradient background */
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: auto; /* Allow the body to grow with content */
    padding: 20px; /* Add some padding */
}

.container {
    height: auto; /* Allow the container to grow with content */
    padding: 20px;
    max-width: 1200px; /* Set a maximum width */
    margin: 0 auto; /* Center the container */
    background-color: #dcf9ff; /* Container background */
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    overflow-x: auto;
}


header {
    text-align: center;
}

h1 {
    font-size: 24px;
    margin-bottom: 10px;
    color: #333; /* Header color */
}

p {
    font-size: 14px;
    color: #666;
    margin-bottom: 20px;
}

.form-input {
    margin-bottom: 15px;
}

.form-input label {
    display: block;
    margin-bottom: 5px;
    font-size: 14px;
    color: #333; /* Label color */
}

.form-input-size {
    width: 100%; /* Full width for inputs */
    padding: 10px; /* Increased padding */
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 4px;
    transition: border-color 0.3s; /* Smooth transition for focus */
}

.form-input-size:focus {
    border-color: #ff7e5f; /* Focus border color */
    outline: none; /* Remove default outline */
}

.error {
    font-size: 12px;
    color: red;
    margin-top: 5px;
}

button {
    width: 100%; /* Full width for buttons */
    padding: 10px;
    background-color: #28a745; /* Submit button color */
    color: #fff;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s; /* Smooth transition for hover */
}

button:disabled {
    background-color: grey; /* Grey out the button when disabled */
    cursor: not-allowed; /* Not allowed cursor */
}

button:hover:not(:disabled) {
    background-color: #218838; /* Darker green on hover */
}

button.updateDelete {
    background-color: #007bff; /* Update/Delete button color */
    margin-top: 10px;
}

button.updateDelete:hover {
    background-color: #0056b3; /* Darker blue on hover */
}

/* Responsive Styles */
@media (max-width: 414px) {
    .container {
        margin: 0 1rem; /* Smaller margin for smaller screens */
        padding: 1rem; /* Adjust padding */
        width: 100%; /* Full width for smaller screens */
    }

    form {
        width: 100%; /* Full form width */
    }

    .form-input-size {
        height: 2rem; /* Decrease height on smaller screens */
    }

    button {
        width: 100%; /* Make buttons take up full width */
    }
}
/////////////////////////////////////////////
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Form</title>
    <style>
        * {
            box-sizing: border-box;
            font-family: 'Times New Roman', Times, serif; /* Set Times New Roman globally */
        }

        body {
            background: linear-gradient(135deg, #2eddff, #0467fb); /* Vibrant gradient background */
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            max-width: 600px; /* Adjust maximum width for better readability */
            width: 100%; /* Full width for smaller screens */
            margin: 0 auto; /* Center the container */
            padding: 40px 20px; /* Padding */
            background-color: #dcf9ff; /* Container background */
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        header {
            text-align: center;
        }

        h1 {
            font-size: 24px;
            margin-bottom: 10px;
            color: #333; /* Header color */
        }

        p {
            font-size: 14px;
            color: #666;
            margin-bottom: 20px;
        }

        .form-input {
            margin-bottom: 15px;
        }

        .form-input label {
            display: block;
            margin-bottom: 5px;
            font-size: 14px;
            color: #333; /* Label color */
        }

        .form-input-size {
            width: 100%; /* Full width for inputs */
            padding: 10px; /* Increased padding */
            font-size: 14px;
            border: 1px solid #ccc;
            border-radius: 4px;
            transition: border-color 0.3s; /* Smooth transition for focus */
        }

        .form-input-size:focus {
            border-color: #ff7e5f; /* Focus border color */
            outline: none; /* Remove default outline */
        }

        .error {
            font-size: 12px;
            color: red;
            margin-top: 5px;
        }

        button {
            width: 100%; /* Full width for buttons */
            padding: 10px;
            background-color: #28a745; /* Submit button color */
            color: #fff;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s; /* Smooth transition for hover */
        }

        button:disabled {
            background-color: grey; /* Grey out the button when disabled */
            cursor: not-allowed; /* Not allowed cursor */
        }

        button:hover:not(:disabled) {
            background-color: #218838; /* Darker green on hover */
        }

        button.updateDelete {
            background-color: #007bff; /* Update/Delete button color */
            margin-top: 10px;
        }

        button.updateDelete:hover {
            background-color: #0056b3; /* Darker blue on hover */
        }

        /* Responsive Styles */
        @media (max-width: 414px) {
            .container {
                padding: 20px; /* Adjust padding */
            }

            .form-input-size {
                height: 2rem; /* Decrease height on smaller screens */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Submit Your Details</h1>
        </header>

        <form id="userForm">
            <div class="form-input">
                <label for="firstname">First Name</label>
                <input type="text" id="firstname" name="firstname" placeholder="First Name" class="form-input-size" required autocomplete="given-name">
                <div class="error" id="firstnameError"></div>
            </div>

            <div class="form-input">
                <label for="lastname">Last Name</label>
                <input type="text" id="lastname" name="lastname" placeholder="Last Name" class="form-input-size" required autocomplete="family-name">
                <div class="error" id="lastnameError"></div>
            </div>

            <div class="form-input">
                <label for="email">Email Address</label>
                <input type="email" id="email" name="email" placeholder="Email Address" class="form-input-size" required autocomplete="email">
                <div class="error" id="emailError"></div>
            </div>

            <div class="form-input">
                <label for="countrycode">Country Code</label>
                <select id="countrycode" name="countrycode" class="form-input-size" required>
                    <option value="">Select Country Code</option>
                    <option value="+1">USA (+1)</option>
                    <option value="+91">India (+91)</option>
                    <option value="+44">UK (+44)</option>
                </select>
                <div class="error" id="countrycodeError"></div>
            </div>

            <div class="form-input">
                <label for="mobileno">Mobile No.</label>
                <input type="text" id="mobileno" name="mobileno" placeholder="Mobile No." class="form-input-size" required autocomplete="tel">
                <div class="error" id="mobilenoError"></div>
            </div>

            <div class="form-input terms-container">
                <input type="checkbox" id="terms" required>
                <label for="terms" class="terms-label">I agree to the Terms & Conditions</label>
            </div>

            <div class="form-input">
                <button type="submit" class="submit" disabled id="submit">Submit Record</button>
                <button type="button" class="updateDelete">Update/Delete</button>
            </div>
        </form>

        <div id="responseMessage"></div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
    <script>
        $(document).ready(function() {
            function validateForm() {
                const firstname = $('#firstname').val();
                const lastname = $('#lastname').val();
                const email = $('#email').val();
                const countrycode = $('#countrycode').val();
                const mobileno = $('#mobileno').val();
                const isTermsChecked = $('#terms').is(':checked');
                const emailValid = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
                const mobileValid = /^\d{10}$/.test(mobileno);

                // Reset error messages
                $(".error").text("");

                let isValid = true;

                if (!firstname) {
                    $("#firstnameError").text("* This field is required.");
                    isValid = false;
                }

                if (!lastname) {
                    $("#lastnameError").text("* This field is required.");
                    isValid = false;
                }

                if (!emailValid) {
                    $("#emailError").text("* Please enter a valid email address.");
                    isValid = false;
                }

                if (!countrycode) {
                    $("#countrycodeError").text("* Please select a country code.");
                    isValid = false;
                }

                if (!mobileValid) {
                    $("#mobilenoError").text("* Mobile number must contain exactly 10 digits.");
                    isValid = false;
                }

                if (!isTermsChecked) {
                    $("#mobilenoError").append("<br>* You must agree to the terms.");
                    isValid = false;
                }

                $("#submit").prop("disabled", !isValid);
            }

            // Enable/disable submit button based on form validity
            $("input, select").on("input change", validateForm);
            $("#terms").on("change", validateForm);

            $("#userForm").on("submit", function(event) {
                event.preventDefault();

                const firstname = $('#firstname').val();
                const lastname = $('#lastname').val();
                const email = $('#email').val();
                const countrycode = $('#countrycode').val();
                const mobileno = $('#mobileno').val();

                $.ajax({
                    type: "POST",
                    url: "https://mcsz6740-shssv34d-jxn10f-nm8.pub.sfmc-content.com/jn4ta43fo1r",
                    crossDomain: true,
                    dataType: 'text',
                    data: {
                        firstname: firstname,
                        lastname: lastname,
                        email: email,
                        countrycode: countrycode,
                        mobileno: mobileno
                    },
                    success: function(data) {
                        $("#responseMessage").html("<p>Record inserted successfully!</p>");
                    },
                    error: function(jqXHR, textStatus, errorThrown) {
                        $("#responseMessage").html("<p>Error: " + jqXHR.responseText + "</p>");
                    }
                });
            });

            $(".updateDelete").on("click", function () {
                window.location.href = "newform2.html"; // Update this URL as needed
            });
        });
    </script>
</body>
</html>
////////////////////////////////////////////////////////////////////////

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
    <title>Update Your Details</title>
</head>
<body>
    <div class="container">
        <header>
            <h1>Update Your Details</h1>
        </header>
        <form id="updateForm">
            <div class="form-input">
                <label for="firstname">First Name</label>
                <input type="text" id="firstname" name="firstname" placeholder="First Name" required class="form-input-size">
            </div>

            <div class="form-input">
                <label for="lastname">Last Name</label>
                <input type="text" id="lastname" name="lastname" placeholder="Last Name" required class="form-input-size">
            </div>

            <div class="form-input">
                <label for="email">Email Address</label>
                <input type="email" id="email" name="email" placeholder="Email Address" required disabled class="form-input-size">
            </div>

            <div class="form-input">
                <label for="countrycode">Country Code</label>
                <select id="countrycode" name="countrycode" required class="form-input-size">
                    <option value="">Select Country Code</option>
                    <option value="+1">USA (+1)</option>
                    <option value="+91">India (+91)</option>
                    <option value="+44">UK (+44)</option>
                </select>
            </div>

            <div class="form-input">
                <label for="mobileno">Mobile No.</label>
                <input type="text" id="mobileno" name="mobileno" placeholder="Mobile No." required class="form-input-size">
            </div>

            <div class="form-input">
                <button type="submit" class="submit">Update Record</button>
            </div>
        </form>
        <div id="responseMessage"></div>
    </div>

    <script>
        $(document).ready(function() {
            const urlParams = new URLSearchParams(window.location.search);

            // Extract values from URL parameters
            const firstname = urlParams.get('firstname');
            const lastname = urlParams.get('lastname');
            const email = urlParams.get('email');
            const countrycode = urlParams.get('countrycode');
            const mobileno = urlParams.get('mobileno');

            // Pre-fill the form fields if values are present
            if (firstname) $('#firstname').val(firstname);
            if (lastname) $('#lastname').val(lastname);
            if (email) $('#email').val(email); // Email will be displayed but not editable
            if (countrycode) $('#countrycode').val(countrycode);
            if (mobileno) $('#mobileno').val(mobileno);

            // Handle form submission
            $("#updateForm").on("submit", function(event) {
                event.preventDefault(); // Prevent the default form submission
                
                // Gather the updated data
                const updatedData = {
                    firstname: $('#firstname').val(),
                    lastname: $('#lastname').val(),
                    email: $('#email').val(), // Email will be sent but not updated
                    countrycode: $('#countrycode').val(),
                    mobileno: $('#mobileno').val()
                };

                // AJAX call to submit the updated data
                $.ajax({
                    type: "POST",
                    url: "https://mcsz6740-shssv34d-jxn10f-nm8.pub.sfmc-content.com/sioy3rl2fa2",
                    data: updatedData,
                    crossDomain: true,
                    dataType: 'text',
                    success: function(response) {
                        $("#responseMessage").html("<p>Record updated successfully!</p>");
                        console.log(response); // Print response for debugging
                    },
                    error: function(jqXHR, textStatus, errorThrown) {
                        $("#responseMessage").html("<p>Error: " + textStatus + " - " + errorThrown + "</p>");
                    }
                });
            });
        });
    </script>
</body>
</html>

