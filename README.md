<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Circles</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: auto;
            width: auto;
            margin: 0;
            background-color: #f5f5f5;
        }

        .circle-container {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }

        .circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: #007bff;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-right: 20px;
            cursor: pointer;
            font-size: 1.2em;
            transition: background-color 0.3s ease-in-out;
        }

        .circle:hover {
            background-color: #0056b3;
        }

        .caption {
            text-align: center;
            color: #555;
            font-size: 0.8em;
            margin-top: 5px;
        }

        .linked-section {
            display: none;
            padding: 90px;
            border: 1px solid #ccc;
            text-align: left;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .linked-section.show {
            display: block;
            height:1700px;
            width: 700px;
        }

        .container {
            width: 100%;
            margin: 20px;
            padding: 20px;
            text-align: left;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: #333;
        }

        .form-group input[type="text"],
        .form-group select,
        .form-group input[type="date"],
        .form-group input[type="time"],
        .form-group input[type="file"],
        .form-group input[type="email"] {
            width: 100%;
            padding: 10px;
            box-sizing: border-box;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-top: 5px;
        }

        .form-group button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }

        .form-group button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <div class="circle-container">
        <div class="circle" onclick="showLinkedSection(1)">1</div>
        <div class="caption">Initial Information</div>
        <div class="circle" onclick="showLinkedSection(2)">2</div>
        <div class="caption">Party Information</div>
        <div class="circle" onclick="showLinkedSection(3)">3</div>
        <div class="caption">Logistics</div>
        <div class="circle" onclick="showLinkedSection(4)">4</div>
        <div class="caption">Additional Services</div>
    </div>

    <div id="linkedSection1" class="linked-section show">
        <div class="container">
            <h1>Initial Information</h1>
            <form id="initial-info-form">
                <!-- Your form for Initial Information goes here -->
            </form>
        </div>
    </div>

    <div id="linkedSection2" class="linked-section">
        <div class="container">
            <h1>Party Information</h1>
            <form id="party-info-form">
                <!-- Your form for Party Information goes here -->
                <!-- ... -->
                <p>Use information on account?</p>
        <label for="useInfo">Yes</label>
        <input type="radio" id="useInfo" name="useInfo" value="Yes" checked>
        <label for="dontUseInfo">No</label>
        <input type="radio" id="dontUseInfo" name="useInfo" value="No">

        <div id="firmInfo">
            <label for="firmName">Firm Name &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="bookingContactName">Booking Contact &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="phoneNumber">Phone Number (No Spaces)</label>
            <input type="text" id="firmName" name="firmName" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="bookingContactName"  name="bookingContactName" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="phoneNumber" name="phoneNumber" required>
        </div>
        <div id="billingInfo">
            <label for="Billing Address">Billing Address &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="Zip/Postalcode">Zip/Postalcode &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="Country/City">Country/City</label>
        <div id="billingInfo">
            <input type="text" id="Billing Address" name="Billing Address" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="Zip/Postalcode"  name="Zip/Postalcode" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="Country/City" name="Country/City" required>
        </div>
        </div>
        <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="role">Role</label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="clientName">Name of Represented Client</label>
        <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="role" name="role" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="clientName" name="clientName" required>
        </div>
        </div>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel">Lead counsel(s) information</label>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>
        </div>
        </div>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> + </label>
            <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>
        </div>
    <h1>Opposing Party Information</h1>
    <form id="bookingForm">
        <div id="firmInfo">
            <label for="firmName">Firm Name &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="bookingContactName">Booking Contact &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="phoneNumber">Phone Number (No Spaces)</label>
            <input type="text" id="firmName" name="firmName" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="bookingContactName"  name="bookingContactName" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="phoneNumber" name="phoneNumber" required>
        </div>
        <div id="billingInfo">
            <label for="Billing Address">Billing Address &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="Zip/Postalcode">Zip/Postalcode &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
            <label for="Country/City">Country/City</label>
        <div id="billingInfo">
            <input type="text" id="Billing Address" name="Billing Address" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="Zip/Postalcode"  name="Zip/Postalcode" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="Country/City" name="Country/City" required>
        </div>
        </div>
        <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="role">Role</label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="clientName">Name of Represented Client</label>
        <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="role" name="role" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="clientName" name="clientName" required>
        </div>
        </div>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel">Lead counsel(s) information</label>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>
        </div>
        </div>
        <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> + </label>
            <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <input type="text" id="leadCounsel" name="leadCounsel" required>
        </div>
        <div>
        <button type="Additional Parties">+ADDITIONAL PARTIES</button>
        <div id="additionalPartiesForm" style="display: none;">
            <h2>Additional Parties</h2>
            <form id="additional-parties-form">
                <div id="firmInfo">
                    <label for="firmName">Firm Name &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="bookingContactName">Booking Contact &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="phoneNumber">Phone Number (No Spaces)</label>
                    <input type="text" id="firmName" placeholder="Input" name="firmName" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="bookingContactName"  placeholder="Type here" name="bookingContactName" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="phoneNumber" placeholder="Type here" name="phoneNumber" required>
                </div>
                <div id="billingInfo">
                    <label for="Billing Address">Billing Address &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="Zip/Postalcode">Zip/Postalcode &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="Country/City">Country/City</label>
                <div id="billingInfo">
                    <input type="text" id="Billing Address" name="Billing Address" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="Zip/Postalcode"  name="Zip/Postalcode" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="Country/City" name="Country/City" required>
                </div>
                </div>
                <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="role">Role</label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="clientName">Name of Represented Client</label>
                <div id="clientInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="role" name="role" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="clientName" name="clientName" required>
                </div>
                </div>
                <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel">Lead counsel(s) information</label>
                <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                </div>
                <div id="counselInfo">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> + </label>
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                </div>
                </form>
                <!-- Your Additional Parties form content -->
            </form>
        </div>

    </form>
</div>
                

            </form>
        </div>
    </div>

    <div id="linkedSection3" class="linked-section">
        <div class="container">
            <h1>Basic Logistics</h1>
            <form id="logistics-form">
                <div class="form-group">
                    <label for="cover-page">Upload Cover Page (optional)</label>
                    <input type="file" id="cover-page" name="cover-page">
                </div>
                <div id="firmInfo">
                    <label for="firmName">Style of cause &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="bookingContactName">Court File# &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</label>
                    <label for="phoneNumber">Booking Dates</label>
                    <input type="text" id="firmName" placeholder="Input" name="firmName" required> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="bookingContactName"  placeholder="Type here" name="bookingContactName" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="date" id="phoneNumber" placeholder="Type here" name="phoneNumber" required>
                </div>
                <div class="form-group">
                    <label for="start-time">Start time</label>
                    <input type="datetime-local" id="start-time" name="start-time">
                
                    <label for="end-time">End Time</label>
                    <input type="datetime-local" id="end-time" name="end-time">
                
                </div>
                
                <div class="form-group">
                    <label for="time-zone">Time Zone</label>
                    <select id="time-zone" name="time-zone">
                        <!-- Add options for time zone here -->
                        <option value="GMT">GMT</option>
                        <option value="EST">EST</option>
                        <option value="CST">CST</option>
                        <option value="PST">PST</option>
                    </select>
                </div>
                <div>
                    <label for ="arbitrator(s)">Arbitrator(s)</label>
                </div>
                <div id="counselInfo">
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                <div id="counselInfo">
                    <label for="leadCounsel"> + </label>
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                <div class="field-group">
                    <label for="reporter">Tribunal secretary</label>
                    <input type="radio" id="yes-reporter" name="reporter" value="yes">
                    <label for="yes-reporter">Yes</label>
                    <input type="radio" id="no-reporter" name="reporter" value="no">
                    <label for="no-reporter">No</label>
                </div>
                <div>
                    <label for ="arbitrator(s)">Witness(es)</label>
                </div>
                <div id="counselInfo">
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                <div id="counselInfo">
                    <label for="leadCounsel"> + </label>
                    <input type="text" id="leadCounsel" name="leadCounsel" required>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <label for="leadCounsel"> ... </label>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
                    <input type="text" id="leadCounsel" name="leadCounsel" required>
                </div>
                <h1>Virtual Logistics</h1>
                <div class="field-group">
                    <label for="reporter">Do you require a VCM(virtual case manager)?</label>
                    <input type="radio" id="yes-reporter" name="reporter" value="yes">
                    <label for="yes-reporter">Yes</label>
                    <input type="radio" id="no-reporter" name="reporter" value="no">
                    <label for="no-reporter">No</label>
                </div>
                <div class="form-group">
                    <label for="Is there a particular VCM you want to work with">Is there a particular VCM you want to work with</label>
                    <input type="text" id="Is there a particular VCM you want to work with" name="Is there a particular VCM you want to work with">
                </div>
                <div class="form-group">
                    <label for="virtual-platform">Select a virtual platform</label>
                    <select id="virtual-platform" name="virtual-platform">
                           <option value="Zoom">Zoom</option>
                           <option value="Google Meet">Google Meet</option>
                           <option value="Microsoft Teams">Microsoft Teams</option>
                           <option value="Skype">Skype</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="Number of virtual breakout rooms">Number of virtual breakout rooms</label>
                    <input type="text" id="Number of virtual breakout rooms" name="Number of virtual breakout rooms">
                </div>
                <div class="form-group">
                    <label for="Do you need us to provide Document Managing Services?">Do you need us to provide Document Managing Services?</label>
                <label for="useInfo">Yes</label>
                    <input type="radio" id="useInfo" name="useInfo" value="Yes" checked>
                    <label for="dontUseInfo">No</label>
                    <input type="radio" id="dontUseInfo" name="useInfo" value="No">
                </div>
                <div class="form-group">
                    <label for="booking-dates">Do you have any special accommodations for your booking that our I.T. team can look into prior to the start date?</label>
                    <input type="text" id="booking-dates" name="booking-dates">
                </div>
            </form>
        </div>
    </div>

    <div id="linkedSection4" class="linked-section">
        <div class="container">
            <h1>Additional Services</h1>
            <form id="additional-services-form">
                <!-- Your form for Additional Services goes here -->
                <!-- ... -->
                <h3>Court Reporting</h3>
    <form id="reporting-form">
        <div class="field-group">
            <label for="reporter">Will this matter plan to have a Court Reporter?</label>
            <input type="radio" id="yes-reporter" name="reporter" value="yes">
            <label for="yes-reporter">Yes</label>
            <input type="radio" id="no-reporter" name="reporter" value="no">
            <label for="no-reporter">No</label>
        </div>
    <h3>Additional Features</h3>
    <form id="reporting-form">
        <div class="field-group">
            <label for="reporter">Do you require interpretation?</label>
            <input type="radio" id="yes-reporter" name="reporter" value="yes">
            <label for="yes-reporter">Yes</label>
            <input type="radio" id="no-reporter" name="reporter" value="no">
            <label for="no-reporter">No</label>
        </div>
        <div class="field-group">
            <label for="reporter">Do you require CART services?</label>
            <input type="radio" id="yes-reporter" name="reporter" value="yes">
            <label for="yes-reporter">Yes</label>
            <input type="radio" id="no-reporter" name="reporter" value="no">
            <label for="no-reporter">No</label>
        </div>
        <div class="field-group">
            <label for="reporter">Will you need a quote priop to confirmation?</label>
            <input type="radio" id="yes-reporter" name="reporter" value="yes">
            <label for="yes-reporter">Yes</label>
            <input type="radio" id="no-reporter" name="reporter" value="no">
            <label for="no-reporter">No</label>
        </div>
        <div id="clientInfo">
            <label for="role">Please list any additional requests or considerations you might have at this time</label>
            <input type="text" id="role" name="role" required>
        </div>
    </form>
            </form>
        </div>
    </div>

    <script>
        function showLinkedSection(section) {
            // Hide all linked sections
            for (let i = 1; i <= 4; i++) {
                const sectionElement = document.getElementById(`linkedSection${i}`);
                if (sectionElement) {
                    sectionElement.classList.remove('show');
                }
            }

            // Show the specific linked section based on the clicked circle
            const selectedSection = document.getElementById(`linkedSection${section}`);
            if (selectedSection) {
                selectedSection.classList.add('show');
            }
        }

        document.addEventListener('DOMContentLoaded', function() {
            const additionalPartiesBtn = document.querySelector('#linkedSection2 form #bookingForm button[type="Additional Parties"]');
            if (additionalPartiesBtn) {
                additionalPartiesBtn.addEventListener('click', function(event) {
                    event.preventDefault();
                    // Show the Opposing Party Information form (linkedSection2)
                    const opposingPartySection = document.getElementById('linkedSection2');
                    if (opposingPartySection) {
                        opposingPartySection.classList.add('show');
                    }
                });
            }
        });
    </script>
</body>
</html>
