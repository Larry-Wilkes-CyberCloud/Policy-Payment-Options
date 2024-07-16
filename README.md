<div>
  <h2>QA Engineer Portfolio: Policy Payment Options Validation</h2>
  <p><strong>Company:</strong> General Insurance INC.</p>
  <p>
    As a QA Engineer at General Insurance INC., I conducted detailed test cases to validate the handling of different payment options during the vehicle policy creation process. The focus was on ensuring the API's adherence to specified payment option rules, such as accepting valid options and rejecting invalid ones.
  </p>

  <h3>Test Case Outline:</h3>
  <ol>
    <li>Verify that the user is able to successfully create a new vehicle with a valid payment option "Monthly". Status code 201 received.</li>
    <li>Verify that the API rejects a new vehicle creation with an invalid payment option "Yearly". Expected status code 400, but a defect was reported as status code 201 was received.</li>
    <li>Verify that the API rejects a new vehicle creation with an empty payment option. Expected status code 400, but a defect was reported as status code 201 was received.</li>
    <li>Verify that the user is able to successfully create a new vehicle with a valid payment option "Total". Status code 201 received.</li>
  </ol>

  <h3>Test Case Results:</h3>
  
  <!-- Test Case 1 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC01</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "policynumber": 62738964,
            "policteffectivedate": "2023-02-06",
            "createddate": "2022-06-10",
            "total_amount": 900,
            "paymentoption": ["monthly"]
          }
        </td>
        <td>Verify that a user can successfully create a new vehicle with a valid payment option such as 'Monthly'. Status code 201 expected.</td>
        <td>I verified the user can successfully create a new vehicle with a valid payment option such as 'Monthly'. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/user-attachments/assets/42f8c98a-c475-4fe5-afa5-70572affc433" width="1000" height="500" alt="Test Case 1"></td>
      </tr>
    </tbody>
  </table>
  <br><br><br>
  
  <!-- Test Case 2 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC02</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "policynumber": 62738962,
            "policteffectivedate": "2023-02-06",
            "createddate": "2022-06-10",
            "total_amount": 900,
            "Monthly_premium": 133,
            "paymentoption": ["yearly"]
          }
        </td>
        <td>Verify that the user cannot create a new vehicle with an invalid payment option such as 'yearly'. Status code 400 expected.</td>
        <td>Users can create a new vehicle with an invalid payment option such as "yearly". This is a defect and will be reported to the developers. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/user-attachments/assets/71886102-b1bf-4b67-a620-9403e284fcd8" width="1000" height="500" alt="Test Case 2"></td>
      </tr>
    </tbody>
  </table>
  <br><br><br>

  <!-- Test Case 3 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC03</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "policynumber": 62738960,
            "policteffectivedate": "2023-02-06",
            "createddate": "2022-06-10",
            "total_amount": 900,
            "Monthly_premium": 133,
            "paymentoption": [" "]
          }
        </td>
        <td>Verify that the user cannot create a new vehicle with an empty payment option " ". Status code 400 expected.</td>
        <td>Users can create a new vehicle with an empty payment option. This is a defect and will be reported to the developers. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/user-attachments/assets/99cc0d10-1d1b-45d5-9930-4f365f67dc3b" width="1000" height="500" alt="Test Case 3"></td>
      </tr>
    </tbody>
  </table>
  <br><br><br>

  <!-- Test Case 4 -->
  <table border="1">
    <thead>
      <tr>
        <th colspan="4">Test Case ID: TC04</th>
      </tr>
      <tr>
        <th>API Body</th>
        <th>Expected Result</th>
        <th>Actual Result</th>
        <th>Status Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          {
            "policynumber": 62738963,
            "policteffectivedate": "2023-02-06",
            "createddate": "2022-06-10",
            "total_amount": 900,
            "Monthly_premium": 133,
            "paymentoption": ["total"]
          }
        </td>
        <td>Verify that the user can successfully create a new vehicle with a valid payment option such as 'total'. Status code 201 expected.</td>
        <td>I verified the user can successfully create a new vehicle with a valid payment option such as 'total'. Status code 201 received.</td>
        <td>Status code 201 received.</td>
      </tr>
      <tr>
        <td colspan="4"><img src="https://github.com/user-attachments/assets/bd3bfd0b-4465-4afd-a094-d44a808b65af" width="1000" height="500" alt="Test Case 4"></td>
      </tr>
    </tbody>
  </table>
  <br><br><br>
</div>


