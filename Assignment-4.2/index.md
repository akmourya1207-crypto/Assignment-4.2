Here is the complete code for your Job Application Form assignment (job-application.html). It includes all required fields, input types, labels, validations, a disabled field example, grouped radio buttons, checkboxes, a dropdown selection, a text area for the cover letter, and a submit button, styled cleanly and professionally.

job-application.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f7f6;
            margin: 0;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            box-sizing: border-box;
        }

        .form-container {
            background-color: #ffffff;
            padding: 30px 40px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 600px;
        }

        h2 {
            margin-top: 0;
            margin-bottom: 20px;
            color: #333333;
            text-align: center;
            border-bottom: 2px solid #0066cc;
            padding-bottom: 10px;
        }

        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            font-weight: bold;
            margin-bottom: 6px;
            color: #444444;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="url"],
        select,
        textarea {
            width: 100%;
            padding: 10px 12px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
            box-sizing: border-box;
            transition: border-color 0.2s ease-in-out;
        }

        input:focus, select:focus, textarea:focus {
            border-color: #0066cc;
            outline: none;
        }

        /* Disabled field styling example */
        input:disabled, select:disabled {
            background-color: #e9ecef;
            color: #6c757d;
            cursor: not-allowed;
        }

        .radio-group, .checkbox-group {
            display: flex;
            gap: 20px;
            margin-top: 6px;
        }

        .radio-group label, .checkbox-group label {
            font-weight: normal;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            cursor: pointer;
        }

        textarea {
            resize: vertical;
            height: 120px;
        }

        button[type="submit"] {
            width: 100%;
            background-color: #0066cc;
            color: #ffffff;
            border: none;
            padding: 12px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
            margin-top: 10px;
        }

        button[type="submit"]:hover {
            background-color: #004b99;
        }
    </style>
</head>
<body>

    <div class="form-container">
        <h2>Job Application Form</h2>

        <form action="#" method="POST">

            <!-- Disabled Field Example (e.g., Application Status) -->
            <div class="form-group">
                <label for="app-status">Application Status</label>
                <input type="text" id="app-status" name="appStatus" value="Open for Submissions" disabled>
            </div>

            <!-- Full Name -->
            <div class="form-group">
                <label for="full-name">Full Name *</label>
                <input type="text" id="full-name" name="fullName" placeholder="Enter your full name" required>
            </div>

            <!-- Email -->
            <div class="form-group">
                <label for="email">Email Address *</label>
                <input type="email" id="email" name="email" placeholder="applicant@example.com" required>
            </div>

            <!-- Phone Number -->
            <div class="form-group">
                <label for="phone">Phone Number *</label>
                <input type="tel" id="phone" name="phone" placeholder="123-456-7890" required>
            </div>

            <!-- Date of Birth -->
            <div class="form-group">
                <label for="dob">Date of Birth *</label>
                <input type="date" id="dob" name="dateOfBirth" required>
            </div>

            <!-- Portfolio URL -->
            <div class="form-group">
                <label for="portfolio">Portfolio Website URL</label>
                <input type="url" id="portfolio" name="portfolioUrl" placeholder="https://www.yourportfolio.com">
            </div>

            <!-- Job Role Dropdown -->
            <div class="form-group">
                <label for="job-role">Preferred Job Role *</label>
                <select id="job-role" name="jobRole" required>
                    <option value="" disabled selected>-- Select a Position --</option>
                    <option value="frontend">Frontend Developer</option>
                    <option value="backend">Backend Developer</option>
                    <option value="fullstack">Full Stack Engineer</option>
                    <option value="uiux">UI/UX Designer</option>
                </select>
            </div>

            <!-- Radio Buttons for Preferred Shift -->
            <div class="form-group">
                <label>Preferred Shift *</label>
                <div class="radio-group">
                    <label><input type="radio" name="shift" value="morning" required> Morning (9 AM - 5 PM)</label>
                    <label><input type="radio" name="shift" value="evening" required> Evening (2 PM - 10 PM)</label>
                    <label><input type="radio" name="shift" value="flexible" required> Flexible / Remote</label>
                </div>
            </div>

            <!-- Checkboxes for Skills -->
            <div class="form-group">
                <label>Key Technical Skills</label>
                <div class="checkbox-group">
                    <label><input type="checkbox" name="skills" value="html"> HTML5</label>
                    <label><input type="checkbox" name="skills" value="css"> CSS3</label>
                    <label><input type="checkbox" name="skills" value="js"> JavaScript</label>
                    <label><input type="checkbox" name="skills" value="react"> React</label>
                </div>
            </div>

            <!-- Textarea for Cover Letter -->
            <div class="form-group">
                <label for="cover-letter">Cover Letter</label>
                <textarea id="cover-letter" name="coverLetter" placeholder="Tell us why you are a great fit for this role..."></textarea>
            </div>

            <!-- Submit Button -->
            <button type="submit">Submit Application</button>

        </form>
    </div>

</body>
</html>
Requirements Checklist Summary
Full name, email, and phone: Included with appropriate text, email, and tel input types.

Date input for Date of Birth: Included using type="date".

URL input for Portfolio URL: Included using type="url".

Radio buttons for preferred shift: Grouped with the exact same name="shift" attribute.

Checkboxes for skills: Included using type="checkbox" with name skills.

Dropdown for job role: Included using <select> and <option> elements.

Textarea for cover letter: Included using <textarea>.

Submit button: Included using <button type="submit">.

Labels & Required Fields: Every input has a matching <label>, and mandatory fields include the required attribute.

Disabled field example: Included a disabled text input (disabled) at the top showing application status.

How to Complete Your Submission
Copy and save the code above as job-application.html.

Open job-application.html in your web browser.

Take a screenshot of the form rendered in your browser.

Submit your job-application.html file along with the screenshot to your instructor.